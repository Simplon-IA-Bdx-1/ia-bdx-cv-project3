# Brief du lundi 2 décembre 2019

## Régression de House Price

	* Le dataset contient de nombreuses variables catégorielles, comment pourrait-on les intégrer à la régression linéaire ? Quelle(s) fonction(s) de Pandas utiliser ?
    * Choisissez-en une variable catégorielle dans la liste qui vous paraît la plus importante a priori, en plus de la surface déjà utilisée précédemment (nettoyez les valeurs invalides de cette variable avant)
    * En suivant le formalisme de Keras, ajoutez cette variable à la régression linéaire et comparez le résultat avec la régression à une variable
    

    * Petit détour par XGBoost :
        * Séparez les variables entre numériques et catégorielles avec Pandas
        * Eliminez les valeurs invalides du dataset
        * Transformez les variables catégorielles en numériques
        * Faut-il normaliser les variables numériques pour XGBoost ?
        * Entraînez XGBoost dans sa version "régression" sur le dataset de training
        * Evaluez la performance d'XGBoost sur le dataset de test (quelle métrique ?)
        * Comment pourrait-on améliorer la performance ?
        * Utilisez XGBoost pour classer les variables par ordre d'importance

    * Appliquez la régression linéaire avec Keras aux 5 variables les plus importantes identifiées par XGBOOST
    * Evaluez la performance

## Computer Vision avec OpenCV

Object detection : trouver plusieurs objets dans une scène
Object tracking : suivre des objets dans une vidéo
Semantic segmentation : attribuer chaque pixel à un objet identifié
Instance segmentation : différencier tous les objets dans la scène

* Installez la bibliothèque opencv sous Python
* Quelques pistes
    - Faire charger des images et explorer les espaces de couleurs
    - Choisir des images de feu
    - Utiliser les espaces de couleur pour segmenter des images de feu
    - Faire calculer des gradients
    - Revoir les scripts de test de Petronor Fournos
    - Revoir le test de GoTurn
    - Proposez la détection avec labels https://towardsdatascience.com/object-detection-with-less-than-10-lines-of-code-using-python-2d28eebc5b11


