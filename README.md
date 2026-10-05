# Curriculum Vitae — Grégoire Lorgnier

CV LaTeX basé sur le template [data-science-tech-resume-template](https://github.com/TimmyChan/data-science-tech-resume-template).

## Prérequis

- [MiKTeX](https://miktex.org/download) (ou TeX Live)
- Extension Cursor/VS Code : **LaTeX Workshop** (recommandé)

## Compiler

```bash
pdflatex resume.tex
```

Le PDF généré est `resume.pdf`.

## Structure

```
resume.tex              # Fichier principal
_header.tex             # En-tête / contact
TLCresume.sty           # Style du template
sections/
  objective.tex
  skills.tex
  experience.tex
  education.tex
  project.tex
```