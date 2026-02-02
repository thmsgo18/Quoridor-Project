# Projet Quoridor

[![en](https://img.shields.io/badge/lang-en-red.svg)](README.md)

Une implémentation Python du jeu de plateau Quoridor avec des adversaires IA de différents niveaux de difficulté.

## 📋 Table des matières

- [Projet Quoridor](#projet-quoridor)
  - [📋 Table des matières](#-table-des-matières)
  - [🎮 À propos](#-à-propos)
  - [✨ Fonctionnalités](#-fonctionnalités)
  - [🚀 Installation](#-installation)
    - [Prérequis](#prérequis)
    - [Dépendances](#dépendances)
    - [Cloner le dépôt](#cloner-le-dépôt)
  - [🎯 Utilisation](#-utilisation)
    - [Lancer une partie](#lancer-une-partie)
    - [Modes de jeu](#modes-de-jeu)
    - [Contrôles](#contrôles)
  - [🤖 Niveaux de difficulté de l'IA](#-niveaux-de-difficulté-de-lia)
  - [📁 Structure du projet](#-structure-du-projet)
    - [Composants clés](#composants-clés)
  - [📊 Benchmarking](#-benchmarking)
  - [👨‍💻 Auteur](#-auteur)
  - [📄 Licence](#-licence)

## 🎮 À propos

Quoridor est un jeu de plateau stratégique où les joueurs tentent d'atteindre le côté opposé du plateau tout en utilisant des murs pour bloquer le chemin de leur adversaire. Cette implémentation propose :

- Un moteur de jeu complet avec validation des règles
- Des adversaires IA utilisant l'algorithme minimax avec élagage alpha-bêta
- Trois niveaux de difficulté (facile, moyen, difficile)
- Des capacités de benchmarking IA vs IA
- Une table de transposition pour un gameplay optimisé

## ✨ Fonctionnalités

- **Humain vs Humain** : Deux joueurs sur le même ordinateur
- **Humain vs IA** : Jouez contre l'ordinateur avec différents niveaux de difficulté
- **IA vs IA** : Regardez deux adversaires IA s'affronter
- **IA intelligente** : Utilise des heuristiques pour l'optimisation des mouvements et le placement stratégique des murs
- **Benchmarking de performance** : Testez différentes configurations d'IA et analysez les résultats
- **Recherche de chemin** : Algorithme de Dijkstra pour garantir que des chemins valides subsistent

## 🚀 Installation

### Prérequis

- Python 3.8 ou supérieur
- pip (gestionnaire de paquets Python)

### Dépendances

Installez les paquets requis :

```bash
pip install numpy matplotlib pandas seaborn
```

### Cloner le dépôt

```bash
git clone https://github.com/thmsgo18/Quoridor-Project.git
cd Quoridor-Project
```

## 🎯 Utilisation

### Lancer une partie

Exécutez le fichier principal du jeu :

```bash
python3 Quoridor.py
```

### Modes de jeu

Au lancement, vous pouvez configurer :
- Joueur 1 et Joueur 2 comme Humain ou IA
- Niveau de difficulté de l'IA (facile, moyen, difficile)

### Contrôles

- Suivez les instructions à l'écran pour effectuer vos mouvements
- Choisissez entre déplacer votre pion ou placer un mur
- Entrez les coordonnées lorsque demandé

## 🤖 Niveaux de difficulté de l'IA

L'IA dispose de trois niveaux de difficulté avec différentes caractéristiques :

| Niveau | Profondeur | Epsilon | Poids avancer | Poids bloquer | Poids murs |
|--------|------------|---------|---------------|---------------|------------|
| **Facile** | 1 | 0.4 | 1.0 | 0.5 | 0.2 |
| **Moyen** | 2 | 0.2 | 1.2 | 0.8 | 0.3 |
| **Difficile** | 3 | 0.1 | 1.5 | 1.0 | 0.4 |

- **Profondeur** : Profondeur de recherche dans l'arbre de jeu (minimax)
- **Epsilon** : Facteur d'aléatoire pour l'imprévisibilité
- **Poids** : Paramètres heuristiques pour la prise de décision stratégique

## 📁 Structure du projet

```
Quoridor-Project/
├── Quoridor.py           # Fichier principal du jeu
├── GameState.py          # Logique de l'IA et gestion de l'état du jeu
├── benchmark_ia.py       # Outil de benchmarking de l'IA
├── Object/
│   ├── Joueur.py        # Classe Joueur
│   ├── Mur.py           # Classe Mur
│   └── Plateau.py       # Classe Plateau
└── README.md            # Fichier README (EN)
```

### Composants clés

- **Quoridor.py** : Boucle de jeu principale et interface utilisateur
- **GameState.py** : Implémentation de l'IA avec minimax, élagage alpha-bêta et heuristiques
- **Plateau.py** : Gestion du plateau de jeu et validation
- **Joueur.py** : Représentation du joueur et déplacements
- **Mur.py** : Placement et validation des murs

## 📊 Benchmarking

Exécutez des benchmarks IA vs IA pour analyser les performances :

```bash
python3 benchmark_ia.py
```

Cela permettra de :
- Lancer 50 parties pour chaque combinaison de difficulté
- Générer des statistiques sur les taux de victoire et la durée des parties
- Créer des graphiques de visualisation avec matplotlib
- Exporter les résultats en CSV et afficher des graphiques

## 👨‍💻 Auteur

**Thomas**
- GitHub : [@thmsgo18](https://github.com/thmsgo18)

## 📄 Licence

Ce projet est un projet académique réalisé dans le cadre du cursus universitaire (Licence 3, Semestre 2, cours d'IA).

---

*Pour la version anglaise de ce README, cliquez [ici](README.md).*
