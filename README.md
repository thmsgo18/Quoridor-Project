# Quoridor Project

[![fr](https://img.shields.io/badge/lang-fr-blue.svg)](README.fr.md)

A Python implementation of the Quoridor board game with AI opponents of varying difficulty levels.

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [AI Difficulty Levels](#ai-difficulty-levels)
- [Project Structure](#project-structure)
- [Benchmarking](#benchmarking)
- [Author](#author)
- [License](#license)

## 🎮 About

Quoridor is a strategic board game where players try to reach the opposite side of the board while using walls to block their opponent's path. This implementation features:

- A complete game engine with rule validation
- AI opponents using minimax algorithm with alpha-beta pruning
- Three difficulty levels (easy, medium, hard)
- AI vs AI benchmarking capabilities
- Transposition table for optimized gameplay

## ✨ Features

- **Human vs Human**: Two players on the same computer
- **Human vs AI**: Play against the computer with different difficulty levels
- **AI vs AI**: Watch two AI opponents battle each other
- **Intelligent AI**: Uses heuristics for movement optimization and strategic wall placement
- **Performance Benchmarking**: Test different AI configurations and analyze results
- **Path Finding**: Dijkstra's algorithm to ensure valid paths remain

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Dependencies

Install the required packages:

```bash
pip install numpy matplotlib pandas seaborn
```

### Clone the Repository

```bash
git clone https://github.com/thmsgo18/Quoridor-Project.git
cd Quoridor-Project
```

## 🎯 Usage

### Start a Game

Run the main game file:

```bash
python3 Quoridor.py
```

### Game Modes

When launching, you can configure:
- Player 1 and Player 2 as Human or AI
- AI difficulty level (easy, medium, hard)

### Controls

- Follow the on-screen prompts to make moves
- Choose between moving your pawn or placing a wall
- Enter coordinates when prompted

## 🤖 AI Difficulty Levels

The AI has three difficulty levels with different characteristics:

| Level | Depth | Epsilon | Advance Weight | Block Weight | Wall Weight |
|-------|-------|---------|----------------|--------------|-------------|
| **Easy** | 1 | 0.4 | 1.0 | 0.5 | 0.2 |
| **Medium** | 2 | 0.2 | 1.2 | 0.8 | 0.3 |
| **Hard** | 3 | 0.1 | 1.5 | 1.0 | 0.4 |

- **Depth**: Search depth in the game tree (minimax)
- **Epsilon**: Randomness factor for unpredictability
- **Weights**: Heuristic parameters for strategic decision-making

## 📁 Project Structure

```
Quoridor-Project/
├── Quoridor.py           # Main game file
├── GameState.py          # AI logic and game state management
├── benchmark_ia.py       # AI benchmarking tool
├── Object/
│   ├── Joueur.py        # Player class
│   ├── Mur.py           # Wall class
│   └── Plateau.py       # Board class
└── README.md            # This file
```

### Key Components

- **Quoridor.py**: Main game loop and user interface
- **GameState.py**: AI implementation with minimax, alpha-beta pruning, and heuristics
- **Plateau.py**: Game board management and validation
- **Joueur.py**: Player representation and movement
- **Mur.py**: Wall placement and validation

## 📊 Benchmarking

Run AI vs AI benchmarks to analyze performance:

```bash
python3 benchmark_ia.py
```

This will:
- Run 50 games for each difficulty combination
- Generate statistics on win rates and game duration
- Create visualization charts with matplotlib
- Output results to CSV and display graphs

## 👨‍💻 Author

**Thomas**
- GitHub: [@thmsgo18](https://github.com/thmsgo18)

## 📄 License

This project is an academic project for university coursework (Licence 3, Semester 2, AI Course).

---

*For the French version of this README, click [here](README.fr.md).*
