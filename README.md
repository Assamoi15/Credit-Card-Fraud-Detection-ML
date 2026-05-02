📌 Détection de fraude bancaire par Machine Learning
🧠 Présentation du projet

Ce projet vise à développer un système de détection de fraude bancaire à l’aide du Machine Learning.

Dans le secteur financier, la détection de fraude est un problème critique : il s’agit d’identifier des transactions frauduleuses rares tout en limitant les erreurs de détection.

🎯 Problématique
Type de problème : Classification binaire
Objectif :
0 → Transaction normale
1 → Transaction frauduleuse

Le dataset est fortement déséquilibré, ce qui reflète la réalité des systèmes bancaires où les fraudes sont rares mais très coûteuses.

📊 Jeu de données
Source : Kaggle – Credit Card Fraud Detection
Variables :
Time
Amount
V1 à V28 (variables anonymisées issues de PCA)
Variable cible :
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
Séparation en données d’entraînement et de test (stratifiée)
⚖️ Gestion du déséquilibre des classes

Le dataset étant très déséquilibré, la technique SMOTE (Synthetic Minority Over-sampling Technique) a été utilisée afin de générer des exemples synthétiques de la classe minoritaire (fraude).

Cela permet d’améliorer la capacité du modèle à détecter les fraudes.

🤖 Modèle de Machine Learning
Modèle utilisé :
Random Forest Classifier
Pourquoi ce modèle ?
Performant sur données tabulaires
Robuste face aux relations non linéaires
Réduit le risque de surapprentissage
Très utilisé en finance et en scoring de risque
📈 Évaluation du modèle

Les performances ont été évaluées à l’aide de :

Accuracy
Precision
Recall (très important en fraude)
F1-score
Matrice de confusion
Courbe ROC
📊 Résultats
Sans SMOTE :
Precision fraude : ~94%
Recall fraude : ~82%
Avec SMOTE :
Recall fraude amélioré (~83%)
Meilleure sensibilité aux fraudes
Légère baisse de précision

👉 Le modèle avec SMOTE est plus adapté à un contexte bancaire car il réduit les fraudes non détectées.

🧾 Matrice de confusion

La matrice de confusion permet d’analyser :

Faux négatifs (fraudes non détectées ❌)
Faux positifs (fausses alertes ⚠️)

En détection de fraude, la priorité est de réduire les faux négatifs.

📉 Analyse métier
Le dataset est fortement déséquilibré (cas réel en finance)
Les variables V1 à V28 sont anonymisées (PCA)
Le problème principal est la détection des fraudes rares
Le rappel (recall) est plus important que l’accuracy
🚀 Impact métier

Ce modèle peut être utilisé pour :

Détecter les transactions frauduleuses en temps réel
Réduire les pertes financières
Améliorer la sécurité bancaire
Aider les équipes de gestion des risques
🔮 Améliorations possibles
Optimisation des hyperparamètres
Utilisation de modèles avancés (XGBoost, LightGBM)
Ajustement du seuil de décision
Déploiement via API (Flask / FastAPI)
Mise en production en temps réel
👨‍💻 Auteur

Kouassi Assamoi Chris Emmanuel
Étudiant en Data Science | Machine Learning | Finance & Intelligence Artificielle

📌 Conclusion

Ce projet présente un pipeline complet de Machine Learning appliqué à la détection de fraude bancaire :

Analyse des données
Prétraitement
Gestion du déséquilibre
Modélisation
Évaluation
