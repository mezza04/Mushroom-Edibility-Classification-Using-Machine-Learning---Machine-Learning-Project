# 🍄 Mushroom Edibility Classification

A machine learning project that classifies mushrooms as **edible** or **poisonous** from categorical morphological features. Built in **KNIME**, it compares Decision Tree, Naive Bayes and Random Forest classifiers, tunes the decision threshold to eliminate false negatives, and uses SHAP to explain the model's predictions.

**Authors:** Ilaria Cesaratto, Chiara Mezzanzanica, Andrea Porro
**University of Milano-Bicocca – Data Science**

## Highlights

- **Dataset:** [Mushroom Classification](https://www.kaggle.com/datasets/uciml/mushroom-classification) (8,124 mushrooms, 22 categorical features + target).
- **Best model:** Random Forest, with ~0.999 accuracy and recall (5-fold cross-validation) and AUC ≈ 0.999.
- **Safety-first threshold:** lowered from 0.5 to 0.15, removing all false negatives (poisonous mushrooms classified as edible).
- **Key features (SHAP):** `odor` and `spore-print-color`.

## Repository Contents

| File | Description |
|------|-------------|
| `ML_progetto_finale.knwf` | KNIME workflow (preprocessing, modeling, evaluation, tuning) |
| `mushrooms_decoded.csv` | Dataset with readable category labels |
| `ML_project___mushrooms.pdf` | Full project report |

## How to Run

1. Open [KNIME Analytics Platform](https://www.knime.com/downloads).
2. Import the workflow: **File → Import KNIME Workflow…** → select `ML_progetto_finale.knwf`.
3. Point the CSV Reader node to your local `mushrooms_decoded.csv` and execute the workflow.

> Python is used only for a brief preprocessing step (replacing `"?"` with `NaN`); everything else is done in KNIME.

## Disclaimer

Developed for academic purposes on 1981 North American data. Do **not** use this model to decide whether a wild mushroom is safe to eat.
