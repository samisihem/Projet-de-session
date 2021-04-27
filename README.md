# Projet-de-session

## Classification virale

Ce code permet de faire une classification virale du virus VIH-1 en utilisant deux méthodes. Le but est de faire une comparaison des résultats des deux méthodes sur le temps d'execution et la précision de la classification.

Après avoir selectionner les données ainsi que la taille du K-mer, la sélection d'attributs est faite selon les deux techniques suivantes:

### Recursive features elimination (RFE):

RFE est une méthode de sélection d'attribut qui supprime les attributs les plus faibles jusqu'à ce que le nombre spécifié d'attributs soit atteint. L'algorithme SVM est utilisé par la suite pour la classification.

### Auto-encoder (AE) :

AE est utilisé pour une meilleure représentation des données. L'objectif est d'utiliser un auto-encodeur profond, de sorte que la nouvelle représentation est représentée par des attributs les plus pertinent. 

L'auto-encoder est alimenté par l'ensemble de données décrivant les séquences VIH (Matrice avec les fréquences k-mer pour chaque séquence). Selon un certain nombre d'itération, une nouvelle représentation des données d'origine est obtenue. Cette dernière sera utilisée par l'algorithme SVM pour la classification.

## Plan d'expérimentation:

Lorsque nous utilisons des données nettoyées, la précision de la classification est proche de 100% à partir de K = 4, pour le RFE et l'AE, et il n'est pas facile de faire la comparaison. Pour cette raison, nous conservons les données telles quelles.

Puisque nous voulons faire une comparaison, et afin d'avoir une exécution rapide dans la sélection des attributs avec RFE, nous choisissons 30% pour l'entraînement et 70% pour le test. Les mêmes données d'entrainement et de test sont utilisées pour RFE et AE

L'expérimentation est faite sur differentes taille du k-mer allant de 3 jusqu'a 5.
Pour chaque taille un nouveau modele d'auto-encoder est utilisé, avec des archtecture différentes.

