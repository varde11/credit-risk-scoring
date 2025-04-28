# 🏦 Scoring de Crédit – Détection des Clients à Risque dans le Secteur Bancaire

## Description

Ce projet a pour but de prédire le risque de défaut d’un client à partir de ses données financières. Basé sur le dataset **Give Me Some Credit** de Kaggle (10 colonnes, 150 000 lignes), il met en place un pipeline complet : exploration des données, traitement des valeurs aberrantes, imputation, modélisation et optimisation de la performance sur les cas à risque.

## Contexte

Chaque année, les retards de paiement coûtent environ **12 milliards d’euros** aux entreprises françaises, impactant directement leur trésorerie et leur stabilité financière. Dans le secteur bancaire, ces défauts de paiement représentent un risque majeur, pouvant entraîner des pertes significatives et affecter la rentabilité des établissements.

**Source :** [Comparateur Banque](https://www.comparateurbanque.com/banque/banques-pro/retard-de-paiement-recours-chiffres-cles/)

## Problème

**Comment détecter efficacement les clients susceptibles de faire défaut dans les deux prochaines années, tout en maintenant un bon équilibre entre détection (recall) et précision ?**

## Solution Apportée

Le projet propose un modèle de scoring de crédit basé sur le Machine Learning, en s’appuyant sur le dataset **Give Me Some Credit**. L'approche intègre un pipeline de bout en bout allant de l’analyse exploratoire à la modélisation via un **Random Forest Classifier**, optimisé pour maximiser la détection des clients à risque.

## Étapes Clés du Projet

- **Exploration et compréhension des données**  
  Analyse des corrélations et détection de patterns visuels (heatmaps, scatterplots, boxplots, kdeplots…).

- **Nettoyage et traitement avancé**  
  - Imputation raisonnée des valeurs manquantes (NaN)  
  - Identification d’outliers spécifiques grâce à l’analyse des quantiles extrêmes

- **Modélisation avec Random Forest Classifier**  
  Deux modèles ont été développés :  
  - **Modèle "Recall"** : Maximisation du rappel pour détecter un maximum de clients à risque (classe 1)  
  - **Modèle "Précision"** : Équilibre global optimal sur l’ensemble des clients

- **Recherche d’hyperparamètres**  
  Optimisation via **RandomizedSearchCV** et **GridSearchCV** pour améliorer les performances sans surapprentissage.

## Résultats

### Modèle 1 – Détection des Clients à Risque

| Objectif principal         | Recall (classe 1) | Accuracy |
|----------------------------|-------------------|----------|
| Détection client à risque  | 76%               | 79%      |

### Modèle 2 – Bonne Performance Globale

| Objectif principal         | Precision (classe 1) | Accuracy |
|----------------------------|----------------------|----------|
| Bonne performance globale  | 74%                  | 93%      |

## Technologies Utilisées

- **Python** (pandas, scikit-learn, matplotlib, seaborn, numpy)
- **Jupyter Lab**
- **GitHub**

## Conclusion

Dans un secteur où la gestion du risque est capitale, ce projet met en lumière la puissance des modèles prédictifs pour détecter les profils à risque de défaut. Le modèle **Random Forest**, optimisé selon différents objectifs métier (rappel ou précision), offre une base fiable pour orienter les décisions de crédit et réduire les pertes financières liées aux impayés.

## Perspectives d'Amélioration

- **Modèles plus avancés :** Tester des algorithmes comme **XGBoost**, **LightGBM** ou des réseaux de neurones.
- **Analyse de stabilité :** Vérifier la constance des performances dans le temps ou selon les segments de clientèle.
- **Détection des biais :** Évaluer l’équité du modèle vis-à-vis de catégories spécifiques (âge, genre, etc.).
- **Déploiement :** Créer une interface ou une API pour permettre aux analystes crédit d'exploiter le modèle en conditions réelles.
