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

- **data/prenoms.pkl**
  - Fichier contenant les noms des personnes dont les visages ont été capturés.
  
- **data/admis.pkl**
  - Fichier indiquant si chaque visage capturé appartient à une personne admise ou non.

- **data/visages.pkl**
  - Ensemble de données contenant les images des visages capturés.
 
## - **Les différents Notebooks : Plusieurs méthodes**
  - Les Notebooks que nous allons montrer ci-dessous traitent la classification des visages en utilisant différents algorithmes de machine learning. On retrouve différents algorithmes traditionnels comme "k-nearest neighbors", "Logistic Regression", "Random Forest, "Multi-layer Perceptron" et un algorithme convolutionnel : "Convolutional Neural Network" afin d'améliorer la précision.
  
## - **Notebook 1 : KNN**
  - Ce notebook traite la classification des visages en utilisant l'algorithme KNN. Ce notebook traite la classification des visages en utilisant l'algorithme KNN. L'algorithme des k plus proches voisins (KNN) est une méthode de classification simple mais efficace. Il fonctionne en trouvant les k échantillons d'entraînement les plus proches dans l'espace des caractéristiques et en prédisant l'étiquette de classe majoritaire parmi ces voisins. KNN est souvent utilisé pour des tâches de classification avec des données de faible dimensionnalité comme les textes et les caractères mais n'est pas le plus efficace pour une reconnaissance faciale.
## - **Notebook 2 : Logistic Regression**
  - Ce notebook traite la classification des visages en utilisant l'algorithme Logistic Regression. La régression logistique est un modèle linéaire utilisé pour la classification binaire. La régression logistique modélise la probabilité qu'une variable dépendante binaire prenne une certaine valeur en fonction des variables indépendantes. Elle utilise une fonction sigmoïde pour produire des valeurs comprises entre 0 et 1, qui peuvent être interprétées comme des probabilités. Cet algorithme est le moins efficace que nous avons pu essayer, il se trompe régulièrement sur les personnes qu'il reconnait.
## - **Notebook 3 : Random Forest**
  - Ce notebook traite la classification des visages en utilisant l'algorithme Random Forest. Random Forest est un algorithme d'apprentissage supervisé qui fonctionne en construisant un grand nombre d'arbres de décision pendant l'entraînement et en les combinant pour obtenir une prédiction plus robuste et précise. Chaque arbre dans la forêt est formé sur un échantillon de données aléatoire avec remplacement et une sélection aléatoire de caractéristiques à chaque division de nœud. En combinant les prédictions de multiples arbres, Random Forest peut réduire le surajustement et produire des résultats de prédiction plus fiables. Il est souvent utilisé pour les tâches de classification et de régression. Cet algorithme peut être utiliser bien qu'il ne soit pas le meilleur. Il reste tout de même plus efficace que celui utilisant la Regression logistique selon nos tests.
## - **Notebook 4 : MLP**
  - Ce notebook traite la classification des visages en utilisant l'algorithme MLP. Le perceptron multicouche (MLP) est un type de réseau de neurones artificiels composé d'au moins trois couches de nœuds : une couche d'entrée, une ou plusieurs couches cachées et une couche de sortie. Chaque nœud dans les couches cachées utilise une fonction d'activation pour transformer les entrées pondérées et produire une sortie. Les MLP sont capables d'apprendre des fonctions complexes et non linéaires à partir de données en effectuant une rétropropagation du gradient pour ajuster les poids du réseau pendant l'entraînement. Ils sont utilisés dans une grande variété de tâches d'apprentissage automatique, y compris la classification, la régression et le traitement du langage naturel. Cet algorithme est assez efficace sans qu'il soit le meilleur qu'on ai pu essayer
## - **Notebook 5 : CNN**
  - Ce notebook traite la classification des visages en utilisant l'algorithme CNN. Les réseaux de neurones convolutionnels (CNN) sont une classe de réseaux de neurones profonds particulièrement adaptés à l'analyse de données structurées en grille, telles que les images. Ils fonctionnent en utilisant des couches de convolution pour extraire automatiquement des caractéristiques à différentes échelles spatiales à partir des données d'entrée. Les CNN sont capables d'apprendre des hiérarchies de motifs visuels à partir de données non structurées, ce qui les rend extrêmement efficaces pour des tâches telles que la classification d'images. Ils ont révolutionné de nombreux domaines, y compris la vision par ordinateur, la reconnaissance vocale et la traduction automatique. Cet algorithme est le plus efficace que nous avons pu essayer. Sa reconnaissance faciale est rapide, efficace et sans erreurs.

Nous avons compris que lorsque qu'un visage est détecté même s'il n'a pas été enregistré, les modèles vont quand même essayé de reconnaitre une personne et l'associer à un label du dataset.

## - Conclusion
 - Ce projet fournit une base solide pour la création d'un système de reconnaissance de visages. Il est extensible et peut être adapté à différents cas d'utilisation grâce à l'utilisation d'algorithmes de classification variés, notamment ceux     basés sur les réseaux de neurones. L'utilisation de GitHub facilite la collaboration et la gestion du code source.
