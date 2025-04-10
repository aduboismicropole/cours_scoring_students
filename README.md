# Credit Scoring

## 📌 Description du projet
Ce projet vise à développer un modèle de scoring d'octroi de crédit afin d'identifier les clients présentant un risque de défaut de paiement. L'objectif est de minimiser les risques pour l'institution financière en classifiant les demandeurs en fonction de leur probabilité de rembourser leur crédit.

## 📁 Arborescence du projet
```
📂 credit_scoring  
│── 📂 data                  # 📊 Données brutes, intermédiaires et traitées  
│   ├── raw                  # 📥 Données brutes (non modifiées)  
│   └── processed            # 🔄 Données pré-traitées  
│  
│── 📂 notebooks             # 📒 Jupyter Notebooks pour exploration et prototypage
│   └── 📂 student_version 
│       ├── 01_Data_exploration.ipynb  
│       ├── 02_Preprocessing.ipynb  
│       └── 03_Modeling.ipynb  
│  
│── 📂 src                   # 💻 Code source du projet  
│   └── 📂 utils   # 🛠️ Fonctions utilisées dans les Notebooks  
│       ├── tools.py
│       └── class_modeling.py
│  
│── .gitignore               # 🚫 Fichiers à exclure du contrôle de version  
│── requirements.txt         # 📦 Dépendances du projet  
│── README.md                # 📝 Présentation du projet  
```

## 📊 Jeu de données
Le jeu de données utilisé comprend différentes variables socio-économiques et financières pour évaluer la probabilité de défaut de paiement.

### 📌 Description des variables

| 🏷️ Nom | 📂 Type | 📝 Description |
|------|------|-------------|
| **Comptes** | Qualitative | 🏦 Détail du compte courant (1 : < 0€, 2 : 0-200€, 3 : >= 200€, 4 : Pas de compte) |
| **Duree_credit** | Quantitative | ⏳ Durée du crédit en mois |
| **Historique_credit** | Qualitative | 📜 Historique du crédit (0 : Impayés passés, 1 : Impayé en cours ailleurs, etc.) |
| **Objet_credit** | Qualitative | 🚗 Objet du crédit (0 : Voiture neuve, 1 : Voiture d'occasion, etc.) |
| **Montant_credit** | Quantitative | 💰 Montant du crédit |
| **Epargne** | Qualitative | 🏦 Compte d'épargne (1 : < 100€, 2 : 100-500€, etc.) |
| **Anciennete_emploi** | Qualitative | 👨‍💼 Années d'emploi (1 : sans emploi, 2 : <1 an, etc.) |
| **Taux_effort** | Quantitative | 📉 Part max des revenus consacrée au prêt |
| **Situation_familiale** | Qualitative | 👨‍👩‍👧‍👦 Situation matrimoniale / Sexe |
| **Garanties** | Qualitative | 🔒 Type de garanties (1 : Aucune, 2 : Co-emprunteur, 3 : Garant) |
| **Anciennete_domicile** | Quantitative | 🏡 Années passées dans la résidence actuelle |
| **Biens** | Qualitative | 💎 Biens personnels possédés (1 : Immobilier, 2 : Assurance-vie, etc.) |
| **Age** | Quantitative | 🎂 Âge du client |
| **Autres_credits** | Qualitative | 🏦 Autres crédits en cours (1 : Banque, 2 : Établissement de crédit, 3 : Aucun) |
| **Statut_domicile** | Qualitative | 🏠 Type de logement (1 : Locataire, 2 : Propriétaire, etc.) |
| **Nb_credits** | Quantitative | 🔢 Nombre de crédits existants |
| **Type_emploi** | Qualitative | 💼 Catégorie professionnelle |
| **Nb_pers_charge** | Quantitative | 👶 Nombre de personnes à charge |
| **Telephone** | Qualitative | 📞 Présence d’un téléphone (1 : Non, 2 : Oui) |
| **Etranger** | Qualitative | 🌍 Statut de résident (1 : Oui, 2 : Non) |
| **Cible** | Qualitative | 🎯 Variable cible (0 : Non défaut, 1 : Défaut) |

## 🎯 Objectifs du projet
- 🔍 Analyser les données et identifier les variables les plus influentes
- 🔄 Appliquer des techniques de prétraitement des données
- 🤖 Entraîner et comparer plusieurs modèles de Machine Learning
- 📊 Évaluer les performances des modèles avec des métriques adaptées (AUC, précision, rappel, etc.)
- 📈 Interpréter les résultats pour une prise de décision optimisée

## 🛠️ Technologies utilisées
- **🐍 Python** (pandas, numpy, scikit-learn, matplotlib, seaborn)
- **📒 Jupyter Notebook** pour l'exploration et la visualisation des données
- **🔀 Git** pour le versionning du code

## 🚀 Installation
### 🔧 Prérequis
Avant de commencer, assurez-vous d'avoir installé :
- **Git** : [Télécharger ici](https://git-scm.com/downloads)
- **Python** (version 3.10) : [Télécharger ici](https://www.python.org/downloads/release/python-31016/)
- **VSCode** : [Télécharger ici](https://code.visualstudio.com/)

### 📥 Étapes d'installation
1. Se placer dans le répertoire où vous souhaitez cloner le projet, puis exécuter :
   ```bash
   git clone https://github.com/aduboismicropole/cours_scoring_students.git
   cd mon_projet_credit_scoring
   ```
2. Créer et activer un environnement virtuel avec `venv` :
   ```bash
   python3.10 -m venv .venv_cours_scoring # créer un environnement Python3.10 nommé .venv_cours_scoring
   source venv/bin/activate  # Sur macOS/Linux
   .venv_cours_scoring\Scripts\activate # Sur Windows
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process # si erreur quand vous lancez la ligne précédente (puis relancez la)
   ```
3. Installer les dépendances :
   ```bash
   pip install -r requirements.txt
   ```
4. Associer l'environnement `.venv_cours_scoring` à un `kernel Jupyter`
   ```bash
   python -m ipykernel install --user --name=.venv_cours_scoring --display-name "kernel_cours_scoring"
   ```
5. Créer et lancer un `Jupyter Notebook`
   ```bash
   jupyter notebook notebooks/TD.ipynb
   ```

## 👨‍💻 Auteurs
- **Alexis Dubois** - *Data Scientist*

## 📜 Licence
Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.