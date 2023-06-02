Partie 01 :
Le projet choisi : Classification d’images avec Keras / Tensor Flow
Il s’agit de chargement et traitement d'un jeu de données non structuré de type image
Ce projet suit le workflow suivant :
1.	Exploration et compréhension des données
2.	Création d'un pipeline d'entrée
3.	Construction du modèle d’apprentissage
4.	Évaluation du modèle
5.	Amélioration du modèle et itération

Les outils utilisés :
1.	GOOGLECOLAB
2.	numpy, matplotlib, tensorflow, keras, Sequential, PIL, pathlib

les données : un jeu de données d'environ 3 700 photos de fleurs. 
Le lien vers le dataset: https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz


L’outil utilisé pour la visualisation :
Matplotlib, PIL




Partie 02 :


 
Ce projet vise à classer des images de fleurs en utilisant Keras / TensorFlow. 
Voici un résumé des étapes suivies dans ce projet :

1. Chargement et exploration du jeu de données :
- Le jeu de données contient environ 3 700 photos de fleurs réparties dans cinq sous-répertoires, chacun représentant une classe de fleurs.- L'objectif est de vérifier le nombre total d'images et d'afficher quelques exemples à l'aide de la bibliothèque PIL.
 

2. Chargement des données à l'aide de l'utilitaire Keras :
- Les images sont chargées à partir du disque en utilisant la fonction tf.keras.utils.image_dataset_from_directory.
- Un ensemble de formation et un ensemble de validation sont construits à partir des images chargées.

3. Visualisation des données :
- Les neuf premières images de l'ensemble de formation sont affichées.

4. Configuration des performances de l'ensemble de données :
- Des méthodes telles que Dataset.cache et Dataset.prefetch sont utilisées pour optimiser les performances lors du chargement des données.

5. Normalisation des données :
- Les valeurs des canaux RVB des images sont normalisées dans l'intervalle [0, 1] à l'aide de la couche tf.keras.layers.Rescaling.

6. Création du modèle :
- Un modèle séquentiel est créé en utilisant des blocs de convolution (tf.keras.layers.Conv2D) avec des couches de max pooling (tf.keras.layers.MaxPooling2D) et une couche dense (tf.keras.layers.Dense) avec activation ReLU.

7. Compilation du modèle :
- L'optimiseur tf.keras.optimizers.Adam et la fonction de perte tf.keras.losses.SparseCategoricalCrossentropy sont utilisés pour compiler le modèle.
- La métrique de précision est également spécifiée.

8. Résumé du modèle :
- Les différentes couches du modèle sont affichées à l'aide de la méthode Model.summary.

9. Entraînement du modèle :
- Le modèle est entraîné pendant 10 époques en utilisant la méthode Model.fit.

10. Visualisation des résultats de l'entraînement :
- Des graphiques de perte et de précision pour les ensembles d'entraînement et de validation sont créés pour évaluer les performances du modèle.

11. Lutte contre le sur-apprentissage :
- L'augmentation des données est utilisée pour générer des exemples supplémentaires et éviter le sur-apprentissage.
- Les couches de prétraitement telles que tf.keras.layers.RandomFlip, tf.keras.layers.RandomRotation et tf.keras.layers.RandomZoom sont utilisées pour augmenter les images.
- La régularisation par dropout est appliquée en utilisant tf.keras.layers.Dropout pour réduire le sur-apprentissage.

12. Entraînement du modèle avec augmentation des données et dropout :
- Le modèle est entraîné à nouveau en utilisant les images augmentées et le dropout.

13. Visualisation des résultats de l'entraînement avec augmentation des données et dropout :
- Les graphiques de perte et de précision sont générés pour évaluer les performances améliorées du modèle.

14. Prédiction sur de nouvelles données :
- Une image de tournesol est téléchargée à partir d'une URL et transformée en un tenseur.
- Le modèle est utilisé pour prédire la classe de l'image.


