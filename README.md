# Phase 1 Starter — Build

This is the starting point for the **Phase 1 (build)** projects of the DutchEngineer
*Ship an End-to-End ML Product* path. You fork it once, in **Module 1 (Python for ML
Engineers)**, and then carry the same repository forward through Modules 2–4, growing it
one module at a time.

## What this repo gives you

- The **Adult / Census Income** dataset (predict whether a person earns more than $50K),
  the assigned project dataset you carry through every module project.
- An **empty package shell** — the standard layout you fill in, so you do not start from a
  blank directory.

You build the package yourself. This starter exists so a rough start never blocks you, not
so you copy an answer.

## What you build on it

| Module | What you add |
|---|---|
| M1 — Python for ML Engineers | A clean, importable and runnable package: typed data contracts, a `__main__` entry point, a dependency lock. |
| M2 — Data Wrangling & Pipelines | A deterministic feature transform, reused at train and serve time. |
| M3 — Numerical & Statistical Foundations | A leakage-free train/val/test split and a documented baseline. |
| M4 — Classical Machine Learning | A trained, serialized, calibrated model that beats your M3 baseline. |

By the end of Module 4 your repository is the trained product that the **Phase 2 (ship)**
starter is built from.

## How to use it

1. **Fork** this repo to your own account (see the *Git Basics* lesson if "fork" is new).
2. Clone your fork locally and build to each module's spec and rubric.
3. Work on a **branch** per module (`git checkout -b m1-package`), open a pull request, and
   merge to `main` once it meets the rubric — `main` stays the last-good version of your
   product.

## The reference

The finished shape to aim for is the reference package
[`adutchengineer/ml-pipeline-starter`](https://github.com/adutchengineer/ml-pipeline-starter),
built on the Lending Club data the lessons use. Read it to see what good looks like — do not
fork it as your project. Yours is the same structure on Adult / Census.
