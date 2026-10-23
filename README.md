# Projet MIDL 2 — Analyse et Génération de la Danse de l'Égyptien

Projet réalisé dans le cadre de la Double Licence Mathématiques et Informatique de l'Université de Toulouse (Janvier 2026).

## Auteurs
* **Héléna CROS**
* **Sylvie HO**
* **Solène LORY**
* **Éloïse SALLET**

---

## Présentation du Projet

L'analyse automatisée du mouvement humain repose sur la vision par ordinateur et le traitement de séquences temporelles. Ce projet étudie la capacité de modèles d'intelligence artificielle à extraire, comparer et prédire des séquences chorégraphiques complexes.

Notre étude se concentre sur la **« Danse de l'Égyptien »** (issue du jeu *Just Dance*), choisie pour sa nature hautement géométrique (postures angulaires, segments corporels parallèles ou perpendiculaires).

### Objectifs principaux :
1. **Extraction de squelettes 2D** : Capturer les points clés articulaires à partir de vidéos brutes avec **MMPose**.
2. **Normalisation anatomique** : Assurer l'invariance d'échelle et de position par rapport à la caméra.
3. **Analyse comparative** : Évaluer la fidélité de reproduction de la danse par un groupe de 4 personnes par rapport à une vidéo de référence (calcul d'erreur MSE sur la trajectoire des poignets).
4. **Génération prédictive de mouvement** : Entraîner un réseau récurrent **LSTM** pour prédire la suite de la chorégraphie.

---

## Stack Technique & Dépendances

Le projet est développé en **Python 3.8+** et s'appuie sur la suite OpenMMLab ainsi que sur PyTorch.

* **Vision & Extraction de pose** : `mmpose`, `mmdet`, `mmcv`, `mmengine`
* **Deep Learning** : `torch` (PyTorch)
* **Calcul scientifique & Data** : `numpy`, `scikit-learn`
* **Visualisation & Animation** : `matplotlib`

### Installation

```bash
# Activation de l'environnement virtuel recommandation (Conda)
conda create -n openmmlab python=3.8 -y
conda activate openmmlab

# Installation de PyTorch et des librairies OpenMMLab
pip install torch torchvision
pip install mmengine mmcv mmdet mmpose
pip install numpy matplotlib scikit-learn
