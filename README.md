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

| Module | What you add | Lesson |
|---|---|---|
| M1 — Python for ML Engineers | A clean, importable and runnable package: typed data contracts, a `__main__` entry point, a dependency lock. | https://learn.dutchengineer.org/courses/python-for-ml-engineers/ |
| M2 — Data Wrangling & Pipelines | A deterministic feature transform, reused at train and serve time. | https://learn.dutchengineer.org/courses/data-wrangling-pipelines/ |
| M3 — Numerical & Statistical Foundations | A leakage-free train/val/test split and a documented baseline. | https://learn.dutchengineer.org/courses/numerical-statistical-foundations/ |
| M4 — Classical Machine Learning | A trained, serialized, calibrated model that beats your M3 baseline. | https://learn.dutchengineer.org/courses/classical-machine-learning/ |

By the end of Module 4 your repository is the trained product that the **Phase 2 (ship)**
starter is built from.

## Approximate structure to build out

This is the shape your repo grows into across M1–M4. The starter ships the skeleton; you
write the contents. Names are a guide, not a rule — match the layout, not the spelling.

```
phase1-starter/
├── pyproject.toml          # package metadata + pinned dependencies (M1, M4)
├── README.md
├── .gitignore
├── data/
│   └── adult.csv           # the Adult / Census Income dataset
└── src/
    └── <yourpkg>/
        ├── __init__.py     # the importable API (M1)
        ├── data.py         # load the Adult / Census data (M1)
        ├── features.py     # the deterministic feature transform (M2)
        ├── split.py        # leakage-free train/val/test split (M3)
        ├── model.py        # train + calibrate the model (M4)
        └── __main__.py     # `python -m <yourpkg>` runs a baseline score end to end (M1)
```

## Fill in

Every file in this repo is empty — you write all of it. The list below is what each empty
file becomes, in the module that fills it. Rename `census_pipeline` to your own package name
(update `pyproject.toml` and the folder together).

**Module 1 — Python for ML Engineers**
- `pyproject.toml` — package metadata and dependencies, so `pip install -e .` works.
- `.gitignore` — ignore `__pycache__/`, `.venv/`, `*.egg-info/`, and the tooling caches.
- `src/census_pipeline/__init__.py` — the importable API (re-export your public functions).
- `src/census_pipeline/data.py` — load the Adult / Census Income data, return `(df, y)`.
- `src/census_pipeline/__main__.py` — `python -m census_pipeline` runs a baseline score end to end.

**Module 2 — Data Wrangling & Pipelines**
- `src/census_pipeline/features.py` — a deterministic feature transform, fit on train, applied identically at serve.

**Module 3 — Numerical & Statistical Foundations**
- `src/census_pipeline/split.py` — a leakage-free split: split raw, fit the transform on train only, apply to both.

**Module 4 — Classical Machine Learning**
- `src/census_pipeline/model.py` — train and score on the pre-split matrix, with an imbalance-aware metric.
- `src/census_pipeline/artifact.py` — bundle the fitted transform + calibrated model + a model card into one saved, reloadable file.

Read the reference package (below) to see the finished shape of each file before you write
your own. Build each module's piece on its own branch and merge to `main` when it meets the
rubric.

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
