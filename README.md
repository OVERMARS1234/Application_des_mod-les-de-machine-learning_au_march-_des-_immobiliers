
# Analyse et Modélisation : Annonces immobilières

## Description du projet

Ce projet vise à analyser les données provenant d'une base de données PostgreSQL pour prédire :
1. Le prix des annonces à l'aide d'un modèle de régression linéaire.
2. La présence d'un équipement spécifique (par exemple, un ascenseur) via des modèles de classification.

Toutes les étapes du projet (connexion à la base de données, exploration, prétraitement, modélisation et visualisation) sont contenues dans un seul fichier Jupyter Notebook.

---

## Prérequis

- **Python 3.8+**
- **Jupyter Notebook**
- **Bibliothèques Python** :
  - `pandas`
  - `numpy`
  - `sqlalchemy`
  - `psycopg2`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`

---

## Installation

### 1. Cloner le projet

Téléchargez le fichier Notebook principal ou clonez ce projet si disponible sur un dépôt.

### 2. Configuration de la base de données

- Assurez-vous que PostgreSQL est installé et en fonctionnement.
- Créez une base de données et importez les tables nécessaires (`Annonce`, `Ville`, `Équipement`, `AnnonceEquipement`) avec vos données.

Ajoutez vos informations de connexion PostgreSQL dans le Notebook dans cette section :

```python
from sqlalchemy import create_engine

db_connection = "postgresql+psycopg2://<username>:<password>@<host>:<port>/<database_name>"
engine = create_engine(db_connection)
```

### 3. Installation des bibliothèques

Installez les bibliothèques nécessaires :

```bash
pip install pandas numpy sqlalchemy psycopg2 matplotlib seaborn scikit-learn
```

---

## Instructions

1. Ouvrez le fichier Notebook avec Jupyter :

```bash
jupyter notebook projet_annonces_immobilieres.ipynb
```

2. Suivez les étapes dans le Notebook :
   - **Connexion à la base de données** : Importation des données.
   - **Exploration et prétraitement des données** :
     - Gestion des valeurs manquantes.
     - Encodage des variables catégorielles.
     - Normalisation des variables numériques.
   - **Modélisation** :
     - Modèle de régression linéaire pour prédire les prix.
     - Modèles de classification (régression logistique, forêts aléatoires, etc.).
   - **Évaluation des modèles** :
     - Pour la régression : MSE, R².
     - Pour la classification : précision, rappel, score F1, AUC-ROC.
   - **Visualisation des résultats** : Courbes ROC, graphiques des résidus.

3. Consultez les graphiques et interprétez les résultats directement dans le Notebook.

---

## Méthodologie

- **Exploration des données** : Analyse des relations entre variables.
- **Prétraitement** :
  - Encodage des catégories et gestion des valeurs manquantes.
  - Création de nouvelles variables pour enrichir les modèles.
- **Modélisation** :
  - Régression pour les prix.
  - Classification pour la présence d'équipements.
- **Visualisation** : Graphiques explicatifs pour comprendre les résultats.

---

## Résultats attendus

1. **Régression linéaire multiple** :
   - Prédiction des prix avec des métriques comme MSE et R².
2. **Classification** :
   - Identification des facteurs influençant la présence d'équipements avec des métriques comme le score F1.

---

## Auteurs

- **Imad Elmanser**  
  Étudiant spécialisé en data science et apprentissage automatique.

---

## Licence

Ce projet est sous licence MIT. Vous êtes libre de l'utiliser et de le modifier avec attribution appropriée.

---
