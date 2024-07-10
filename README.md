# Classification d'Images avec un Réseau de Neurones Convolutifs (CNN)

Ce projet a pour objectif de créer et d’entraîner un réseau de neurones convolutifs (CNN) pour la classification d’images en utilisant les bibliothèques TensorFlow et Keras. Le modèle sera entraîné pour différencier entre deux classes d’images : Homer et Bart Simpson. Le projet suit une série d'étapes allant de la préparation des données à l'entraînement du modèle.
Le fichier Jupyter Notebook contient du code pour la création et l'entraînement d'un réseau de neurones convolutifs (CNN) pour la classification d'images.

# 1. Importation des Bibliothèques
TensorFlow et Keras : Pour créer et entraîner des modèles de réseaux de neurones.
Matplotlib et Seaborn : Pour visualiser les données et les résultats.
Zipfile et os : Pour gérer les fichiers compressés et les chemins de fichiers.
Numpy et OpenCV : Pour la manipulation d'images et les opérations numériques.

# 2. Montage de Google Drive
Google Drive : Monté pour accéder aux fichiers de données stockés dans le Drive.

# 3. Extraction des Données
Fichier Zip : Extraction des images à partir d'un fichier zip stocké dans Google Drive, contenant les datasets d'entraînement et de test.

# 4. Préparation des Données
Chargement des Images : Vérification des images en les chargeant individuellement.
Générateur d'Images pour l'Entraînement : Utilisation de ImageDataGenerator pour augmenter les images d'entraînement (rotation, zoom, flip horizontal) afin de rendre le modèle plus robuste.

# 5. Création du Dataset d'Entraînement et de Test
Entraînement : Création d'un générateur d'images à partir des répertoires d'images d'entraînement, avec un redimensionnement à 64x64 pixels.
Test : Création d'un générateur d'images à partir des répertoires d'images de test sans augmentation.

# 6. Construction du Modèle CNN
Sequential Model : Utilisation de Keras pour construire un modèle séquentiel.
Couches Convolutives : Ajout de trois couches convolutives, chacune suivie d'une couche de pooling pour extraire les caractéristiques des images.
Flatten : Transformation des matrices en vecteurs pour les couches entièrement connectées.
Couches Entièrement Connectées : Ajout de deux couches denses (fully connected) avec la fonction d'activation ReLU.
Couche de Sortie : Une couche dense avec la fonction d'activation softmax pour la classification en deux classes.

# 7. Compilation du Modèle
Optimiseur Adam : Utilisation de l'optimiseur Adam pour l'apprentissage.
Fonction de Perte : categorical_crossentropy, adaptée aux problèmes de classification multi-classes.
Métrique : Utilisation de l'accuracy pour évaluer les performances du modèle.

# 8. Résumé du Modèle
Summary : Affichage de la structure du modèle, y compris le nombre de paramètres et les dimensions de chaque couche.


# En résumé, le code configure un environnement pour entraîner un réseau de neurones convolutifs (CNN) à l'aide de Keras et TensorFlow
