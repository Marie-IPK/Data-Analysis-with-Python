# 📊 Formation Pratique Data — Session de Septembre

Bienvenue dans le dépôt collaboratif de la formation ! 🚀
Ce dépôt est notre espace de travail commun pendant tout le mois : c'est ici que chacun dépose ses jeux de données, ses notebooks et ses projets, exactement comme dans un vrai projet Data en entreprise.

---

## 🎯 Objectif

À la fin du mois, chaque participant doit avoir mené **un projet complet de Data Analysis de A à Z**, publié sur ce dépôt via le workflow décrit ci-dessous — avec une vraie expérience de collaboration Git.

---

## 🔒 Règles importantes

- **La branche `main` est protégée.** Personne ne peut y pousser directement, pas même par erreur.
- Tout travail passe **obligatoirement par une Pull Request (PR)**, relue et validée avant d'être fusionnée.
- Les fichiers volumineux (> 50 Mo) ne doivent **pas** être commités directement — voir la section [Jeux de données volumineux](#-jeux-de-données-volumineux).

---

## 🌳 Structure du dépôt

Chaque participant travaille dans **son propre dossier, sur sa propre branche** (voir la convention de nommage ci-dessous), à l'intérieur du dossier `participants/` :

```
participants/
└── prenom-nom/
    └── nom-dataset/
        ├── data/              → le(s) jeu(x) de données
        ├── notebook.ipynb     → ton analyse (Python)
        ├── dashboard/         → si tu utilises Power BI (optionnel)
        └── README.md          → description de ton dataset et de ton projet
```

**Exemple concret :**
```
participants/mary/ventes-supermarche/
├── data/ventes.csv
├── notebook.ipynb
└── README.md
```

---

## 🌿 Convention de nommage des branches

Format obligatoire :
```
prenom-nom/nom-dataset
```

Exemples valides : `mary/ventes-supermarche`, `jean-paul/covid-cameroun`

❌ Pas d'espaces, d'accents, ni de majuscules dans le nom de branche.

---

## 🚀 Comment contribuer — étape par étape

### 1. Cloner le dépôt (une seule fois)
```bash
git clone git@github.com:Marie-IPK/Data-Analysis-with-Python.git
cd Data-Analysis-with-Python
```

### 2. Se mettre à jour avant de commencer
```bash
git checkout main
git pull origin main
```

### 3. Créer sa branche
```bash
git checkout -b prenom-nom/nom-dataset
```

### 4. Créer son dossier de travail
Crée ton dossier dans `participants/prenom-nom/nom-dataset/` en suivant la structure ci-dessus.

### 5. Ajouter et commiter tes fichiers
```bash
git add participants/prenom-nom/nom-dataset/
git commit -m "Ajout du projet : nom-dataset"
```

### 6. Pousser ta branche
```bash
git push origin prenom-nom/nom-dataset
```

### 7. Ouvrir une Pull Request
Sur GitHub, clique sur **"Compare & pull request"**, vérifie que ta PR cible bien `main`, décris brièvement ton projet, puis clique sur **"Create pull request"**.

### 8. Attendre la validation
Un formateur relit ta PR et peut laisser des commentaires. Corrige si besoin (nouveau commit sur la même branche → la PR se met à jour automatiquement), puis attends l'approbation.

### 9. Fusion
Une fois approuvée, la PR est fusionnée dans `main` (en squash — tes commits sont regroupés en un seul, propre et lisible).

---

## 📝 Modèle de README pour ton dataset

Chaque projet doit contenir son propre `README.md` avec cette structure minimale :

```markdown
# Nom du projet

**Participant :** Ton prénom et nom
**Source des données :** D'où viennent les données (Kaggle, INS, etc.)

## Description
Que contiennent les données ? Combien de lignes/colonnes ?

## Objectif du projet
Quelle question cherches-tu à répondre avec ces données ?

## Colonnes principales
- colonne_1 : description
- colonne_2 : description

## Outils utilisés
Python, Pandas, Power BI, etc.
```

---

## 🐍 Environnement virtuel & dépendances

Le dépôt utilise **un seul environnement Python partagé**, géré avec **[uv](https://docs.astral.sh/uv/)**. Il contient déjà tout ce qu'il faut : le fichier `pyproject.toml` (les dépendances) et le fichier `.python-version` (la version de Python à utiliser). Tu n'as rien à initialiser toi-même.

### Étape 1 : Installer uv (une seule fois)

**Linux / macOS / WSL :**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell) :**
```powershell
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### Étape 2 : Créer l'environnement

Ouvre un terminal à la racine du dépôt (dans VS Code : clic droit sur le dossier → "Open in Integrated Terminal") et tape :

```bash
uv sync
```

`uv` télécharge la bonne version de Python si elle n'est pas déjà sur ta machine, puis crée un dossier `.venv/` — c'est ton environnement, prêt à l'emploi. Il n'est jamais commité (déjà exclu par le `.gitignore`).

Active-le si besoin :
```bash
source .venv/bin/activate      # sous Windows : .venv\Scripts\activate
```

### Étape 3 : Ajouter une bibliothèque (seulement si demandé)

La plupart du temps tu n'as rien à ajouter. Si un projet a besoin d'une bibliothèque supplémentaire, ce sera précisé explicitement dans les instructions ou le notebook. Dans ce cas :

```bash
uv add nom-du-package
```

Committe ensuite `pyproject.toml` et `uv.lock` avec ton travail :
```bash
git add pyproject.toml uv.lock
git commit -m "Ajout de nom-du-package"
```

---

## 📦 Jeux de données volumineux

GitHub refuse les fichiers de plus de 100 Mo. Si ton dataset est lourd :
- Privilégie un **lien externe** (Google Drive, Kaggle) mentionné dans ton `README.md`, plutôt que de committer le fichier brut
- Ou demande au formateur comment configurer **Git LFS**

---

## ✅ Checklist avant d'ouvrir ta Pull Request

- [ ] Mon dossier respecte la structure `participants/prenom-nom/nom-dataset/`
- [ ] Mon `README.md` de projet est complet
- [ ] Aucun fichier de plus de 50 Mo n'est commité directement
- [ ] Le nom de ma branche suit le format `prenom-nom/nom-dataset`
- [ ] J'ai vérifié que ma PR cible bien `main`

---

## 🙈 Fichier `.gitignore`

Le dépôt contient un `.gitignore` à la racine qui exclut automatiquement les environnements virtuels, fichiers temporaires et checkpoints Jupyter. Tu n'as rien à faire, mais évite de forcer l'ajout de ces fichiers avec `git add -f`.

---

## ❓ Besoin d'aide ?

Pose ta question sur le groupe Telegram de la formation, ou ouvre une **Issue** sur ce dépôt en décrivant ton problème.

Bonne formation à tous ! 🔥
