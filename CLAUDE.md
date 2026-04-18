# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A-Level Mathematics tutoring materials built with [Quarto](https://quarto.org/). Content covers topics from A-Level Pure Mathematics (P1–P4), organized by topic unit. Each unit contains concept notes, practice problems with mark schemes, and exam-style questions.

## Build Commands

```bash
# Render the entire project (all .qmd files → _output/)
quarto render

# Render a single file
quarto render 2_transformation/basic_forms.qmd

# Live preview with hot reload
quarto preview
```

Output goes to `_output/` (configured in `_quarto.yml`).

## Project Structure

- **`_quarto.yml`** — global project config: output dir (`_output`), HTML theme (`cosmo`), MathJax, `echo: false`, `warning: false`
- **Numbered topic directories** (`2_transformation/`, `4_further_tria/`, `5_differentiation_part1/`, `6_review_exercise/`) — each is a self-contained unit
- **`.qmd` files** — Quarto documents combining LaTeX math, Python (matplotlib) plots, and explanatory text; rendered to standalone HTML (`embed-resources: true`)
- **`.md` files** — plain Markdown for concept notes and mark schemes (no code execution); used where no plots are needed

## Content Conventions

- Topic language is bilingual: English explanations with Korean annotations for the student audience (A-Level, Korean student)
- Mark scheme files follow the pattern `<topic>_practice_basic.md` and use `(M1)`, `(A1)` marks
- Python cells in `.qmd` files use a consistent plotting style: `ROOT_CLR` (blue), `YINT_CLR` (green), `ASYM_CLR` (red) for graph annotations
- Math is rendered via MathJax; use `$$...$$` for display math and `$...$` for inline

## Dependencies

```bash
pip install jupyter matplotlib numpy scipy
quarto install
```

Python kernel (`jupyter: python3`) is required for `.qmd` files that contain code cells.
