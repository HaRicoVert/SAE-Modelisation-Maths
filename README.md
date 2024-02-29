# SAE Modélisation Mathématiques

Ce projet vise à créer un système de reconnaissance de visages utilisant des techniques de traitement d'images et de classification. Le système peut être adapté pour un cas d'utilisation spécifique, notamment la reconnaissance binaire pour déterminer si un visage appartient à une personne spécifique ou non. Nous utilisons différents algorithmes de classification, y compris des réseaux de neurones, pour ce faire.

## Détails de Fonctionnement

### Analyse du Code de Génération du Dataset

Le code dans le premier notebook utilise la bibliothèque OpenCV pour capturer des images de visages en temps réel. Il détecte les visages à l'aide d'un classificateur en cascade pré-entraîné fournis pas la bibliothèques CV2 et enregistre les images dans un format adapté à l'entraînement de modèles de classification.

### Modifications

Nous avons apporté des modifications pour améliorer la quantité de données de test collectées. Au lieu de collecter seulement 10 images par personne, nous avons augmenté ce nombre à 30 pour une meilleure représentation des visages. De plus, nous avons afficher une image de chaque personne enregistrées.


## Contenu du Projet

Le projet est organisé comme suit :

## - **Notebook 1 : Création du Dataset**
  - Ce notebook présente le code utilisé pour collecter des images de visages en temps réel à partir d'une webcam. Il détecte les visages dans les images capturées et les enregistre dans un ensemble de données pour l'entraînement du modèle de reconnaissance.
  - Il utilise la bibliothèque OpenCV pour la capture d'images et la détection de visages à l'aide de classificateurs en cascade. Le code d'origine a légerement était modifié.
### Répertoire `data`

- **data/noms.pkl**
  - Fichier contenant les noms des personnes dont les visages ont été capturés.
  
- **data/admis.pkl**
  - Fichier indiquant si chaque visage capturé appartient à une personne admise ou non.

- **data/visages.pkl**
  - Ensemble de données contenant les images des visages capturés.
## - **Notebook 2 : Classification des Visages**
  - Ce notebook traite la classification des visages en utilisant différents algorithmes de machine learning. Initialement, il est configuré pour utiliser des algorithmes classiques comme la régression logistique et les arbres de décision.
  - Nous adaptions également ce notebook pour inclure des algorithmes de classification par réseaux de neurones traditionnels et convolutionnels pour améliorer la précision de la reconnaissance.

## Conclusion

Ce projet fournit une base solide pour la création d'un système de reconnaissance de visages. Il est extensible et peut être adapté à différents cas d'utilisation grâce à l'utilisation d'algorithmes de classification variés, notamment ceux basés sur les réseaux de neurones. L'utilisation de GitHub facilite la collaboration et la gestion du code source.
