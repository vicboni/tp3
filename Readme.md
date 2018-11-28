# TP 3 : Introduction Tensorflow
Ce tp est le premier d'une suite de 3 tp visant à entrainer et déployer des modèles prédictifs dans un environement orchestré afin de multiplier sa vitesse d'apprentissage.

## Mise à jour
Après avoir forké le repo, pour se mettre à jour avec la dernière version, exécuter les commandes suivantes:
```bash
git remote add parent https://github.com/cours-ece/tp3.git
git pull
```

## Instructions
Les réponses aux questions posées dans cet énoncé sont attendues dans un fichier **answers.md** situé dans le repo mentionné ci-dessus.
Ce TP a pour but de vous donner une vision sur les concepts ML et sur les outils utilisés dans ce domaine.

> Il est important que vous compreniez les concepts présents pour être en mesure de réaliser la suite du projet.

## Présentation des outils/concepts

* Machine Learning (Deep learning, data mining, ...)
* Deep learning 
* Neural network
* Entrainement du modèle  

![ML Training model](https://image.slidesharecdn.com/evaluatingml-150916204123-lva1-app6892/95/evaluating-machine-learning-models-a-beginners-guide-29-638.jpg?cb=1442436244 "ML Training model")
* TensorFlow
* TensorFlow serving
![Tensorflow Serving](https://cdn-images-1.medium.com/max/1600/1*mHePtJJbR2TUtM6sYZNdzA.jpeg "Tensorflow Serving")
* Appel depuis les machines client (RPC: remote procedure call)
* Jupyter notebook

## 1 : Tensorflow + Jupyter

### 1.0 : Pull request time !!
Forker et cloner [le repository du tp2](https://github.com/cours-ece/tp2).
Ajouter votre prénom, votre nom au fichier answers.md et votre numéro d'équipe (de 1 à 7), puis réaliser une pull request sur le repository du tp.

### 1.1 : Deployer Tensorflow
En cherchant sur docker hub, trouver l'image officielle tensorflow et la déployer en local sur votre machine.
> Attention à ne pas oublier l'ouverture de port

### 1.2 : Naviguer dans l'interface Tensorflow
Se connecter à l'interface web Jupyter qui a été déployée par le container tensorflow.
Ouvrir le premier notebook (1_hello_tensorflow.ipynb) et suivre les instructions du notebook pas à pas.

> Note: 
>   Les notebooks sont des interfaces de développement et d'exécution de code (en l'occurence Python dans cet exemple. Utiliser les boutons d'actions dans la bandeau du haut pour exécuter les différents blocs de code.

### 1.3 : Création d'un nouveau modèle
Retourner à la racine de l'interface Jupyter déployé en local et créer un nouveau notebook destiné à accueillir le modèle du tutoriel Tensorflow.

Puis, suivre le [tutoriel officiel du site Tensorflow](https://www.tensorflow.org/tutorials/keras/basic_classification) pour créer votre premier réseau de neurones (les blocs de code sont à coller dans le notebook que vous venez de créer).

> Bien que la difficulté soit relevée, essayez de comprendre ce que font chacune des parties du code.

Au terme de cette partie, vous êtes censés avoir une idée des concepts de base:
* graph
* tensor
* layers

Répondre aux questions présentes dans la partie 1.3 du fichier answers.md.


## 2 : Tensorflow Serving
Dans cette partie, nous allons mettre à disposition un modèle entrainé pour que les applicatifs puissent utiliser l'intelligence du modèle.

### 2.1 : Entrainer et exposer le modèle
Suivre le [tutoreil officiel de Tensorflow serving](https://www.tensorflow.org/serving/serving_basic) pour entrainer le modèle mnist et le rendre disponible à travers Tensorflow Serving.

### 2.2 : Docker time
A partir du modèle entrainé de la question précédente, créer une image Docker paramétrée pour démarrer directement sur le modèle mnist.

### 2.3 : Docker compose time
Créer le fichier docker-compose.yml vous permettant de démarrer votre serveur Tensorflo Serving via la commande `docker-compose up`

## 3 : Préparation TP suivant
Effectuer des recherches pour apréhender la complexité de mise en production de modèle.
Quelles sont ces difficultés ? Quels sont les solutions proposées sur le marché aujourd'hui ? Ecrire la commande utilisée dans le fichier answers.md

