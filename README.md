# Curriculum Vitae — Grégoire Lorgnier

CV LaTeX bilingue (EN / FR) basé sur le template [data-science-tech-resume-template](https://github.com/TimmyChan/data-science-tech-resume-template).

[![Build and deploy CV](https://github.com/Wuraim/curriculum_vitae/actions/workflows/build-and-deploy.yml/badge.svg)](https://github.com/Wuraim/curriculum_vitae/actions/workflows/build-and-deploy.yml)

**Hosted:** [https://wuraim.github.io/curriculum_vitae/](https://wuraim.github.io/curriculum_vitae/)  
- EN: [resume.en.pdf](https://wuraim.github.io/curriculum_vitae/resume.en.pdf)  
- FR: [resume.fr.pdf](https://wuraim.github.io/curriculum_vitae/resume.fr.pdf)

## Prérequis (local)

- [MiKTeX](https://miktex.org/download) (ou TeX Live)
- Extension Cursor/VS Code : **LaTeX Workshop** (recommandé)

## Compiler en local

```bash
pdflatex resume.en.tex
pdflatex resume.fr.tex
```

Les PDF générés (`resume.en.pdf`, `resume.fr.pdf`) sont ignorés par git.

## Build & host (GitHub)

Chaque push sur `master` (ou un lancement manuel via **Actions → Build and deploy CV → Run workflow**) :

1. Compile `resume.en.tex` et `resume.fr.tex`
2. Publie `resume.en.pdf`, `resume.fr.pdf` + page d’accueil sur **GitHub Pages**

### Activation Pages (obligatoire avant le 1er déploiement)

Sans cette étape, le workflow échoue avec `Get Pages site failed` / `Not Found`.

1. Ouvre https://github.com/Wuraim/curriculum_vitae/settings/pages
2. Sous **Build and deployment** → **Source**, choisis **GitHub Actions**
3. Relance le workflow : **Actions** → **Build and deploy CV** → **Run workflow**

Le dépôt doit être **public** pour Pages gratuit sur un compte perso (ou GitHub Pro si privé).

## Structure

```
resume.en.tex           # Racine anglaise
resume.fr.tex           # Racine française
_header.tex             # En-tête / contact
TLCresume.sty           # Style du template
site/index.html         # Page d’accueil GitHub Pages
sections/               # Contenu EN
sections/fr/            # Contenu FR
.github/workflows/
  build-and-deploy.yml  # CI compile + deploy Pages
```

Quand tu modifies le contenu EN, porte le même changement dans `sections/fr/` dans le même commit.
