# Projet-de-session

## Classification virale

Ce code permet de faire une classification viral du virus VIH-1 en utilisant deux methodes. Le but est de faire une comparaison des resultats des deux methodes sur le temps d'execution et la precision de la classification.

Apres avoir selectionner les donnees ainsi que la taille du K-mer, la selection d'attributs est faite selon les deux techniques suivantes:

### Recursive features elimination (RFE):

RFE est une méthode de sélection d'attribut qui supprime les attributs les plus faibles jusqu'à ce que le nombre spécifié d'attributs soit atteint. L'algorithme SVM est utilise par la suite pour la classification.

### Auto-encoder (AE) :

AE est utilisé pour une meilleure représentation des données. L'objectif est d'utiliser un auto-encodeur profond, de sorte que la nouvelle représentation est représentée par des attributs les plus pertinent. 

L'auto-encoder est alimenté par tout l'ensemble de données décrivant les séquences VIH (Matrice avec les fréquences k-mer pour chaque séquence). Selon un certain nombre d'itération, une nouvelle représentation des données d'origine est obtenue. Cette dernière sera utilisée par l'algorithme SVM pour la classification.

## Plan d'experimentation:

Lorsque nous utilisons des données nettoyees, la précision de la classification est proche de 100% à partir de K = 4, pour le RFE et l'AE, et il n'est pas facile de faire la comparaison. Pour cette raison, nous conservons les données telles quelles.

Puisque nous voulons faire une comparaison, et afin d'avoir une exécution rapide dans la sélection des attributs avec RFE, nous choisissons 30% pour l'entraînement et 70% pour le test. Les mêmes données d'entrainement et de test sont utilisées pour RFE et AE

L'experimentation est faite sur differentes taille du k-mer allant de 3 jusqu'a 5.
Pour chaque taille un nouveau modele d'auto-encoder est utilise, avec des archtecture differentes.

