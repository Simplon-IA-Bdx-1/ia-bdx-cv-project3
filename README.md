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
__ATTENTION__ : passez par pip et installez opencv-python

__Alternative__ : installez avec conda install -c anaconda py-opencv

__Autre alternative__ : installez avec pip install pyopencv

* Quelques thèmes à explorer dans l'ordre avec les fonctions OpenCV :

    __IMAGES__
    - charger des images en couleurs sous forme d'images en niveaux de gris ou sous forme d'images en couleur
    __NOTE IMPORTANTE__: si votre notebook tourne sans fin, insérer au tout début du notebook la ligne :

%matplotlib auto

    - Pour les images chargées en couleurs BGR, les convertir en HSV et en YUV
    - Chercher la différence entre ses 3 représentations
    - Choisir 5 images contenant des flammes (exemples : bougie, feu de cheminée, incendie, etc.) et 5 images sans flammes, les sauver dans un sous-répertoire *images*
    - En utilisant la bibliothèque python *glob*, appliquer une fonction de changement de taille d'image d'opencv à toutes les images précédentes et sauvegarder les images avec leur nouvelle taille dans le répertoire images avec un suffixe "_resized" et dans un encodage de votre choix (exemples : jpg, png, etc.). La fonction pourra soit réduire la taille en pourcentage, soit réduire indépendamment hauteur et largeur de l'image
    - Réfléchir à comment utiliser les espaces de couleur pour segmenter les images contenant des flammes pour isoler les zones contenant les flammes
    - Fabriquer des images binaires à partir de la segmentation précédente
    
    __VIDEOS__

    - Récupérer une vidéo contenant des flammes
    - Charger la vidéo dans opencv et la faire jouer dans une fenêtre
    - Appliquer la segmentation binaire précédente à chaque frame et afficher la vidéo correspondante

    __OBJECT TRACKING__
    - Par groupes de 4
    - 4 méthodes à choisir entre :
        + CSRT
        + KCF
        + MOSSE
        + GoTurn
    - Partir d'une courte viédo contenant des personnages se déplaçant (si pas d'idées, cherchez chaplin.mp4 ou filmez-vous entre vous)
    - Appliquez une des 4 méthodes de tracking


    __SEMANTIC SEGMENTATION__
    - Testez la détection avec labels sur une image de votre choix [(ici le code)](https://towardsdatascience.com/object-detection-with-less-than-10-lines-of-code-using-python-2d28eebc5b11)


