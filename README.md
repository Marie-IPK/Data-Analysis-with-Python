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
participants/marie-victoire/ventes-supermarche/
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

Exemples valides : `marie-victoire/ventes-supermarche`, `jean-paul/covid-cameroun`

❌ Pas d'espaces, d'accents, ni de majuscules dans le nom de branche.

---

## 🚀 Comment contribuer — étape par étape

### 1. Cloner le dépôt (une seule fois)
```bash
git clone [LIEN DU DÉPÔT]
cd [nom-du-dépôt]
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

## ❓ Besoin d'aide ?

Pose ta question sur le groupe Telegram de la formation, ou ouvre une **Issue** sur ce dépôt en décrivant ton problème.

Bonne formation à tous ! 🔥
