                                   📌 Détection de fraude bancaire par Machine Learning

  Présentation du projet

Ce projet vise à développer un système de détection de fraude bancaire basé sur le Machine Learning.

Dans le secteur financier, la détection de fraude est un problème critique : les fraudes sont rares mais peuvent entraîner de fortes pertes financières. L’objectif est donc de construire un modèle capable de détecter efficacement les transactions frauduleuses tout en minimisant les erreurs critiques.

🎯 Problématique

Type de problème : Classification binaire

Objectif :

0 → Transaction normale

1 → Transaction frauduleuse

Le dataset est fortement déséquilibré, ce qui reflète la réalité des systèmes bancaires.

📊 Jeu de données

Source : Kaggle – Credit Card Fraud Detection

Variables :

Time

Amount

V1 à V28 (variables anonymisées via PCA)

Cible :

Class (0 = normal, 1 = fraude)

⚙️ Technologies utilisées

Python 🐍

Pandas

NumPy

Scikit-learn

Matplotlib / Seaborn

Imbalanced-learn (SMOTE)

🧹 Prétraitement des données

Vérification des valeurs manquantes

Suppression des doublons

Normalisation des variables (Time, Amount)

Split stratifié train/test

⚖️ Gestion du déséquilibre des classes

La technique SMOTE (Synthetic Minority Over-sampling Technique) a été utilisée pour générer des exemples synthétiques de la classe minoritaire (fraude).

👉 Objectif : améliorer la capacité du modèle à détecter les fraudes.

🤖 Modèle de Machine Learning

Modèle utilisé :

Random Forest Classifier

Pourquoi ce modèle ?

Très performant sur données tabulaires

Robuste aux relations non linéaires

Réduit le surapprentissage

Largement utilisé en finance et risk scoring

📈 Évaluation du modèle

Les performances sont évaluées à l’aide de :

Accuracy

Precision

Recall (métrique critique en fraude)

F1-score

Matrice de confusion

Courbe ROC

📊 Résultats

🔹 Sans SMOTE :

Precision fraude : ~94%

Recall fraude : ~82%

🔹 Avec SMOTE :

Recall fraude : ~83%

Meilleure détection des fraudes

Légère baisse de précision

👉 Le modèle avec SMOTE est plus adapté aux systèmes de détection de fraude car il réduit les fraudes non détectées.

📉 Visualisations


📌 Matrice de confusion
<img width="640" height="480" alt="confusion_matrix" src="https://github.com/user-attachments/assets/1065f4b8-4ccf-44c7-89f6-b4e96eb1a27a" />


📌 Courbe ROC
<img width="640" height="480" alt="roc_curve" src="https://github.com/user-attachments/assets/13caf9de-f367-458e-8797-5a7b7954e669" />


🧾 Analyse métier

Dataset fortement déséquilibré (cas réel en finance)

Variables V1 à V28 anonymisées (PCA)

Problème critique : détection de cas rares


Le recall est plus important que l’accuracy

🚀 Impact métier

Ce modèle peut être utilisé pour :

Détecter les transactions frauduleuses en temps réel

Réduire les pertes financières

Améliorer la sécurité bancaire

Aider les équipes de risk management

🔮 Améliorations futures

Optimisation des hyperparamètres (GridSearch / RandomSearch)

Modèles avancés : XGBoost / LightGBM

Ajustement du seuil de décision

Déploiement via API (Flask / FastAPI)

Système de détection en temps réel


👨‍💻 Auteur

Kouassi Assamoi Chris Emmanuel
Data Science | Machine Learning | Finance & IA

📌 Conclusion

Ce projet implémente un pipeline complet de Machine Learning pour la détection de fraude bancaire, incluant :

Analyse des données
Prétraitement
Gestion du déséquilibre
Modélisation
Évaluation
Visualisation
