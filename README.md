# Curriculum Vitae — Grégoire Lorgnier

CV LaTeX basé sur le template [data-science-tech-resume-template](https://github.com/TimmyChan/data-science-tech-resume-template).

[![Build and deploy CV](https://github.com/Wuraim/curriculum_vitae/actions/workflows/build-and-deploy.yml/badge.svg)](https://github.com/Wuraim/curriculum_vitae/actions/workflows/build-and-deploy.yml)

**Hosted PDF:** [https://wuraim.github.io/curriculum_vitae/](https://wuraim.github.io/curriculum_vitae/) · [direct PDF](https://wuraim.github.io/curriculum_vitae/resume.pdf)

## Prérequis (local)

- [MiKTeX](https://miktex.org/download) (ou TeX Live)
- Extension Cursor/VS Code : **LaTeX Workshop** (recommandé)

## Compiler en local

```bash
pdflatex resume.tex
```

Le PDF généré est `resume.pdf` (ignoré par git).

## Build & host (GitHub)

Chaque push sur `master` (ou un lancement manuel via **Actions → Build and deploy CV → Run workflow**) :

1. Compile `resume.tex` avec TeX Live (GitHub Actions)
2. Publie `resume.pdf` + une page d’accueil sur **GitHub Pages**

### Activation Pages (une fois)

1. Ouvre le dépôt → **Settings** → **Pages**
2. Sous **Build and deployment** → **Source**, choisis **GitHub Actions**
3. Relance le workflow si le premier déploiement a échoué avant cette étape

Le dépôt doit être **public** pour Pages gratuit sur un compte perso (ou GitHub Pro si privé).

## Structure

```
resume.tex              # Fichier principal
_header.tex             # En-tête / contact
TLCresume.sty           # Style du template
site/index.html         # Page d’accueil GitHub Pages
sections/
  objective.tex
  skills.tex
  experience.tex
  education.tex
  project.tex
.github/workflows/
  build-and-deploy.yml  # CI compile + deploy Pages
```
