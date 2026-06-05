
# Algorithme génétique — INF1008

Notebook Jupyter implémentant un algorithme génétique pour optimiser automatiquement les hyperparamètres d'un réseau de neurones MLP sur le dataset MNIST.

## Fonctionnement

Chaque chromosome représente une configuration d'hyperparamètres du MLP (taille des couches cachées, nombre d'itérations, solveur, taux d'apprentissage). L'algorithme fait évoluer la population sur plusieurs générations pour trouver la meilleure configuration.

## Fonctionnalités

- Initialisation aléatoire d'une population de chromosomes
- Évaluation (fitness) par entraînement et précision du MLPClassifier sur MNIST
- Sélection des meilleurs individus par tri décroissant de fitness
- Crossover à point unique entre deux parents
- Mutation aléatoire contrôlée par un taux configurable (défaut : 5%)
- Évolution sur N générations avec suivi de la performance moyenne
- Affichage d'un graphique de convergence par génération

## Hyperparamètres optimisés

```
hidden_layer_sizes : [(2,), (5,), (50,), (100,), (50,50), (10,10,10)]
max_iter           : [100, 500, 1000, 5000]
solver             : [adam, lbfgs, sgd]
learning_rate      : [0.01, 0.005, 0.001]
```

## Concepts démontrés

- Algorithme génétique (sélection, crossover, mutation)
- Optimisation d'hyperparamètres de réseau de neurones
- Classification sur MNIST avec MLPClassifier

## Technologies

- Python
- scikit-learn (MLPClassifier, datasets, accuracy_score)
- Matplotlib
- Google Colab

## Prérequis

```bash
pip install scikit-learn matplotlib
```

Développé sous Google Colab. Le dataset MNIST est chargé directement via `sklearn.datasets` — aucun fichier externe requis.

## Structure

```
Algorithme_Genetique.ipynb  — notebook principal
```

---

Projet universitaire solo — cours INF1008, UQTR.
