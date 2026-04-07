# Projet Fairness — Analyse et Mitigation des Biais dans les Modèles de Classification

> Projet académique d'étude de l'équité (*fairness*) appliquée à des modèles de machine learning, en utilisant la bibliothèque **AI Fairness 360** d'IBM.

---

## Table des matières

- [Contexte](#contexte)
- [Objectifs](#objectifs)
- [Structure du projet](#structure-du-projet)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Résultats](#résultats)
- [Technologies utilisées](#technologies-utilisées)
- [Auteur](#auteur)

---

## Contexte

Les modèles de machine learning peuvent reproduire, voire amplifier, des biais présents dans les données d'entraînement. Ce projet explore les méthodes de détection et de mitigation de ces biais à travers la **fairness algorithmique**, en s'appuyant sur des métriques reconnues telles que la *demographic parity*, l'*equal opportunity* et l'*equalized odds*.

---

## Objectifs

- **Détecter** les biais dans un classificateur entraîné sur des données réelles
- **Quantifier** ces biais à l'aide de métriques de fairness standards
- **Appliquer** des techniques de mitigation (pré-traitement, post-traitement)
- **Comparer** les performances et l'équité avant/après mitigation

---

## Structure du projet

```
Projet_FAIRNESS/
│
├── Projet_Fairness.ipynb            # Notebook principal — analyse complète et résultats
├── train_classifieur.py             # Script d'entraînement du classificateur (exécution locale/cluster)
├── train_classifieur_local.ipynb    # Notebook d'entraînement en local
│
├── expe_log/                        # Logs des expériences (métriques, checkpoints) *
├── data/                            # métadonnées et images utilisés dans le projet
│
├── pyproject.toml                   # Dépendances et configuration du projet (uv)
├── uv.lock                          # Lockfile des dépendances
└── .gitignore
```

*Pour avoir le expe_log au complet il faut lancer le projet depuis sa machine, certains documents ne sont pas disponibles ici dû à leur grande taille

---

## Installation

Ce projet utilise [**uv**](https://github.com/astral-sh/uv) comme gestionnaire de dépendances. Python **3.12** est requis.

### 1. Cloner le dépôt

```bash
git clone https://github.com/educob23/Projet_FAIRNESS.git
cd Projet_FAIRNESS
```

### 2. Installer les dépendances

```bash
# Avec uv
uv sync

### 3. Lancer Jupyter

```bash
jupyter notebook Projet_Fairness.ipynb
```

> **Note :** L'installation de `aif360` peut nécessiter des dépendances système supplémentaires. Consultez la [documentation officielle d'AIF360](https://github.com/Trusted-AI/AIF360).

---

## Utilisation

### Notebook principal

Ouvrir `Projet_Fairness.ipynb` pour suivre l'analyse complète :

1. Chargement et exploration du jeu de données
2. Entraînement d'un classificateur de référence (*baseline*)
3. Mesure des métriques de fairness initiales
4. Application des techniques de mitigation
5. Évaluation comparative des résultats

### Entraînement du modèle (standalone)

```bash
python train_classifieur.py
```

Les logs et métriques sont sauvegardés dans le dossier `expe_log/`.

---

## Résultats

Les expériences menées montrent l'impact des techniques de mitigation sur le compromis **performance / équité**. Les résultats détaillés (courbes, tableaux de métriques) sont disponibles dans le notebook principal `Projet_Fairness.ipynb`.

---

## Technologies utilisées

| Catégorie | Bibliothèque |
|-----------|--------------|
| Fairness  | [AI Fairness 360 (AIF360)](https://github.com/Trusted-AI/AIF360) |
| Deep Learning | PyTorch, PyTorch Lightning |
| Machine Learning | scikit-learn |
| Vision    | torchvision |
| Données   | pandas, numpy |
| Visualisation | matplotlib |
| Métriques | torchmetrics |
| Gestion des deps | uv |

---

## Auteurs

**Eduardo Cobos Fernández**  
**Jeremy Rakotonirina**  
**Sipan Bareyan**  
**Amine Berrahma**  

Projet réalisé dans le cadre de l'UE Analyse et Réduction des Biais en Machine Learning. Enseignement suivi en trosième année de Licence Double Diplôme Informatique-Mathématiques à l'Université Paris-Saclay.

---
