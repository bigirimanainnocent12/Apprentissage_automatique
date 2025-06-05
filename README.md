# *🎯 Objectif*
  * Aider Bob, un entrepreneur, à estimer la catégorie de prix de téléphones portables (de 0 à 3) en fonction de leurs caractéristiques techniques.

# *📊 Données*
  * Source : Kaggle - Mobile Price Classification
  * 21 variables, dont :
  * Quantitatives : RAM, mémoire interne, résolution, batterie, etc.
  * Qualitatives (binaires) : Bluetooth, 3G, 4G, écran tactile, etc.
  * Cible : price_range (0 à 3)
# *🧪 Prétraitement*
  * Séparation des variables qualitatives et quantitatives.
  * Conversion des variables binaires en booléens.
  * Séparation des données en train/test (70%/30%).
# *🤖 Modélisation*
  * Utilisation d’un pipeline avec :
    * StandardScaler pour les variables quantitatives.
    * LogisticRegression avec GridSearchCV pour l’optimisation des hyperparamètres :
    * penalty: l1, l2
    * C: 0.1, 1, 10
    * solver: liblinear, saga
# *📈 Évaluation*
  * Prédictions sur l’ensemble de test.
  * Histogramme des probabilités de prédiction.
  * Métriques :
    * Exactitude
    * Précision (pondérée)
    * Rappel (sensibilité)
    * Matrice de confusion
    * Rapport de classification
    * AUC ROC (multi-classes)
# *💾 Sauvegarde*
Le meilleur modèle est sauvegardé dans un fichier modele.pkl avec joblib.
