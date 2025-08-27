# Energy-Consumption-Prediction-2023

![Illustration](PhotosReadme/LogoP3.png)

Projet réalisé en 2023 dans le cadre de ma formation en Data Science.  
Objectif : prédire la consommation d’énergie et les émissions de CO2 des bâtiments non résidentiels de Seattle, à partir de leurs caractéristiques structurelles, pour aider à mieux cibler les efforts de réduction d’émissions.

## Objectifs

- Anticiper la consommation énergétique des bâtiments pour lesquels aucune donnée n’est disponible
- Prédire les émissions de CO2
- Tester la pertinence du **ENERGY STAR Score** dans les prédictions
- Identifier les variables structurelles influentes

## Données

- **Source** : Ville de Seattle  
- **Lien** : [Télécharger le dataset](https://s3.eu-west-1.amazonaws.com/course.oc-static.com/projects/Data_Scientist_P4/2016_Building_Energy_Benchmarking.csv)

## Méthodologie

### 1. Exploration et préparation

- Analyse des données, valeurs manquantes, doublons, typage
- Cartographie des bâtiments (via latitude/longitude)  
  ![Seattle](PhotosReadme/Seattle.png)

- Analyse des variables de consommation et outliers  
  ![Consommation](PhotosReadme/Consomations.png)

- Création de variables : type de bâtiment, décennie de construction  
  ![Décennies](PhotosReadme/Decenies.png)

- Normalisation et correction des distributions (skew)  
  ![Skew](PhotosReadme/Skew.png)

### 2. Modélisation

#### Modèles testés :

- Régressions : Ridge, Lasso, ElasticNet
- Arbres de décision
- KNN
- Random Forest
- XGBoost
- SVM
- Modèles de base (Dummy, Random)

#### Évaluation :

- **RMSE**  
- **R²**  
- **Temps de calcul**

### 3. Interprétation des résultats

- Analyse des variables importantes  
  ![Features](PhotosReadme/variablespertinantes.png)

- Explication locale via **SHAP** et **LIME**  
  ![SHAP](PhotosReadme/SHAP.png)

## Résultats

- Les modèles permettent de prédire la consommation avec une précision correcte
- Le **ENERGY STAR Score** améliore significativement les résultats
- Les variables structurelles (surface, année de construction…) jouent un rôle clé
- Recommandation : utiliser le ENERGY STAR Score pour cibler les bâtiments prioritaires dans les politiques énergétiques

## Technologies utilisées

- **Langage** : Python  
- **Librairies** : pandas, numpy, seaborn, matplotlib, scikit-learn, XGBoost, SHAP, LIME, folium  
- **Environnement** : Jupyter Notebook  
- **Méthodes** : Data cleaning, ML supervisé, Feature engineering, Interprétabilité

## Contact

Projet réalisé en 2023 dans le cadre d’une formation en Data Science.  
Pour toute question ou retour :

- **Email** : [johan.rocheteau@hotmail.fr](mailto:johan.rocheteau@hotmail.fr)  
- **LinkedIn** : [linkedin.com/in/johan-rocheteau](https://www.linkedin.com/in/johan-rocheteau)
