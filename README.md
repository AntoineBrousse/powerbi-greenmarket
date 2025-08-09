# Étude de cas – Automatisation de l’actualisation d’un rapport Power BI à partir de fichiers Excel OneDrive

## 📌 Contexte
Une PME fictive du secteur **Green Market** gère ses ventes mensuelles dans des fichiers Excel stockés sur OneDrive.  
Chaque mois, un nouveau fichier est ajouté, nécessitant :
- Une **importation manuelle** dans Power BI.
- Un **rafraîchissement manuel** du rapport.
- L’envoi des mises à jour aux équipes commerciales.

Ce processus était **chronophage**, répétitif et sujet à des oublis.

---

## 🎯 Objectif
Mettre en place une **solution automatisée** permettant :
- L’**import automatique** des nouveaux fichiers Excel depuis OneDrive dans Power BI.
- L’**actualisation du rapport** sans intervention humaine.
- L’**envoi d’une notification par email** avec un lien vers le rapport à jour.

---

## 💡 Solution mise en place

### 1. **Connexion Power BI ↔ OneDrive**
- Lien direct entre Power BI et le dossier OneDrive contenant les fichiers Excel.
- Dans **Power Query** :
  - Sélection et formatage des colonnes nécessaires (dates, produits, montants…).
  - Normalisation des formats (dates, décimales…).
  - Transformation des données pour garantir une cohérence d’analyse.

### 2. **Automatisation avec Power Automate**
- **Déclencheur** : détection d’un nouveau fichier dans le dossier OneDrive.
- **Actions** :
  1. Actualisation du dataset Power BI sur le Service.
  2. Envoi d’un email automatique aux équipes avec :
     - Un **lien direct** vers le rapport Power BI actualisé.
     - *(Option Premium)* le rapport exporté en PDF ou PowerPoint en pièce jointe.

![Performance commerciale](/images/Page-1.png)

---

## 📊 Résultats obtenus
- **Gain de temps** : plus besoin de manipulations manuelles chaque mois.
- **Réduction des erreurs** : suppression des oublis et des incohérences dans les données.
- **Accès instantané** : le rapport est disponible en temps réel après l’ajout d’un fichier.
- **Meilleure communication** : tous les destinataires sont informés automatiquement.

---

## 🛠️ Stack technique
- **Power BI Service** (connexion directe à OneDrive + Power Query pour la transformation des données)
- **Power Automate** (déclenchement et envoi des notifications)
- **OneDrive** (stockage centralisé des fichiers Excel)
- **Microsoft Outlook** (diffusion par email)

---

## 📬 Exemple d’email envoyé


---

## 🚀 Améliorations possibles
- Ajout d’un **résumé automatique des indicateurs clés** dans l’email.
- Archivage automatique des anciens rapports sur SharePoint.
- Mise en place d’un tableau de bord consolidé multi-années.

---

## 👤 Auteur
**Antoine Brousse**  
Data Analyst | Étudiant en Master Économétrie & Data Science

---

## 📌 Note
Ce projet est basé sur un scénario fictif mais reproduit fidèlement un **cas d’usage réel en entreprise**.
Il démontre ma capacité à :
- **Connecter Power BI à des sources cloud** (OneDrive)
- **Transformer et préparer les données** avec Power Query
- **Automatiser un processus de reporting complet** avec Power Automate
- **Améliorer la productivité et la qualité des données**

