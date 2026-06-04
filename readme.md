# Approches Neuronales - TP

Bienvenue dans le dépôt des Travaux Pratiques (TP) sur les **Approches Neuronales** ! Ce projet couvre les fondamentaux des réseaux de neurones et du deep learning en utilisant PyTorch.

## Table des Matières

- [À propos](#à-propos)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Structure du Projet](#structure-du-projet)
- [Utilisation](#utilisation)
- [Contenu des TP](#contenu-des-tp)
- [Ressources](#ressources)

## À propos

Ce dépôt contient une série de travaux pratiques pour découvrir et maîtriser les concepts fondamentaux des réseaux de neurones artificiels. Les TP sont conçus pour les étudiants en Master 1 à l'Université d'Avignon.

**Technologies utilisées :**
- Python 3.10
- PyTorch
- Jupyter Notebook
- Linux (recommandé)

## Prérequis

Avant de commencer, assurez-vous d'avoir :

- Python 3.10 ou supérieur
- pip (gestionnaire de paquets Python)
- Un environnement virtuel (recommandé)
- Jupyter Notebook ou JupyterLab

## Installation

### 1. Cloner le dépôt

```bash
git clone <url-du-depot>
cd "approches neuronales/TP"
```

### 2. Créer et activer l'environnement virtuel

```bash
# Créer l'environnement
python3 -m venv env

# Activer l'environnement
source env/bin/activate  # Sur Linux/Mac
# ou
env\Scripts\activate     # Sur Windows
```

### 3. Installer les dépendances

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install jupyter matplotlib numpy
```

### 4. Lancer Jupyter

```bash
jupyter notebook
```

Ouvrez ensuite le fichier `TP1/tp1.ipynb` dans votre navigateur.

## Structure du Projet

```
approches neuronales/
├── TP/
│   ├── env/                    # Environnement virtuel
│   ├── TP1/
│   │   └── tp1.ipynb          # Premier TP - Introduction aux tenseurs
│   └── readme.md              # Ce fichier
```

## Utilisation

1. Activez votre environnement virtuel
2. Lancez Jupyter Notebook
3. Ouvrez le notebook souhaité
4. Exécutez les cellules dans l'ordre
5. Complétez les exercices demandés

## Contenu des TP

### TP1 : Introduction aux Tenseurs PyTorch

- Création et manipulation de tenseurs
- Opérations arithmétiques
- Broadcasting
- Indexation et slicing
- Concaténation et stacking
- Types de données (float32, float64)
- Calcul automatique de gradients (autograd)

**Objectifs d'apprentissage :**
- Maîtriser les opérations de base sur les tenseurs
- Comprendre le système de calcul de gradients automatique
- Préparer le terrain pour les réseaux de neurones

## Ressources

- [Documentation officielle PyTorch](https://pytorch.org/docs/)
- [Tutoriels PyTorch](https://pytorch.org/tutorials/)
- [Cours sur les réseaux de neurones](https://www.coursera.org/learn/neural-networks-deep-learning)

## Contribution

Les TP sont fournis tels quels pour les besoins pédagogiques. Pour toute question ou suggestion d'amélioration, contactez votre enseignant.

## Licence

Ce projet est destiné à un usage éducatif dans le cadre des cours de l'Université d'Avignon.

---

*Créé pour les étudiants en Approches Neuronales*
