# 📄 README – Power BI Project: *Sales Dashboard – GreenMarket*

## 🧾 Description

Ce projet Power BI vise à créer un **tableau de bord interactif** pour une entreprise fictive, *GreenMarket*, à partir de ventes journalières simulées.  
Il permet de **suivre les performances commerciales** et d’identifier les **produits et segments les plus performants**.

> 🔁 **Automatisation** : Le rapport est connecté à une table Google BigQuery qui s’alimente automatiquement chaque jour. Cela permet un **rafraîchissement continu** des données et un suivi en temps réel.

---

## 🎯 Objectifs

- Suivre les ventes quotidiennes
- Analyser les KPI clés : chiffre d’affaires, quantité vendue, panier moyen
- Identifier les produits top et les leviers d’amélioration
- Offrir une navigation fluide et intuitive à travers les données

---

## 📁 Contenu du projet

| Fichier                            | Description                                   |
|-----------------------------------|-----------------------------------------------|
| `Rapport_GreenMarket.pbix`        | Rapport Power BI interactif                   |
| `README_GreenMarket.pdf`          | Fiche descriptive du projet                   |

---

## 📊 Structure du rapport

### Page 1 – Vue d’ensemble
- KPI globaux : revenu, quantité, panier moyen, commandes
- Graphiques : évolution des ventes, répartitions par pays, produit, mode de paiement

### Page 2 – Analyse par produit
- Filtres dynamiques par catégorie et produit
- KPI spécifiques au produit sélectionné
- Graphiques d’évolution & Top produits

---

## 🧮 Mesures DAX utilisées

```dax
Revenue = SUMX('Ventes', 'Ventes'[Quantité] * 'Ventes'[Prix Unitaire])
Panier moyen = [Revenue] / DISTINCTCOUNT('Ventes'[ID Commande])
Nombre de commandes = DISTINCTCOUNT('Ventes'[ID Commande])
```

---

## 🔍 Insights clés

- Hausse de chiffre d’affaires en fin de période
- 85 % des ventes proviennent des catégories *Alimentation* et *Maison & Entretien*
- Produit P002 = plus vendu ; P017 = plus rentable
- Apple Pay = moyen de paiement dominant

---

## 💡 Recommandations

- Valoriser les produits à **fort revenu mais peu vendus**
- Cibler les pays sous-performants (ex. Belgique, Espagne)
- Suivre les tendances sur une **période plus longue** pour anticiper la saisonnalité

---

## ☁️ Architecture de données

- Données stockées dans **Google BigQuery**
- Mise à jour automatique via un script Python et Airflow
- Connexion Power BI en direct via le connecteur BigQuery
- Modèle Power BI mis à jour quotidiennement

---

## 📌 Auteur

- **Antoine Brousse**  
- [LinkedIn](https://www.linkedin.com/in/brousseantoine/)  
- [Portfolio](https://antoinebrousse.github.io/Portofolio/)
