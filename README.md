# NLP-Derived Protein-Protein Interaction Validation

This repository contains a reproducible pipeline for validating protein-protein interactions (PPIs) automatically extracted from biomedical literature using natural language processing (NLP) tools and cross-referencing with curated biological databases.

## Project Summary

- **Objective:** Predict whether NLP-extracted protein-protein interactions are biologically valid, using high-confidence STING interactions as the gold standard.
- **Data sources:** INDRA NLP (TRIPS, Sparser), SIGNOR, PubMed, STING, Reactome, BioGRID.
- **Key methods:** Feature engineering (linguistic and biological features), class imbalance correction (SMOTE), model selection (Logistic Regression, Random Forest, SVM, XGBoost), cross-validation, bootstrap evaluation, SHAP interpretation, robustness testing, and simulation.

## File Structure

- `notebook.ipynb` – Main Jupyter notebook (complete workflow).
- `requirements.txt` – List of all required Python packages.
- `README.md` – This file.
- `/data/` – Directory for input/output datasets.

## Usage

1. **Clone the repository:**
    ```bash
    git clone https://github.com/YOURUSERNAME/YOURREPO.git
    cd YOURREPO
    ```

2. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the notebook:**
    Open `notebook.ipynb` in Jupyter Notebook or JupyterLab and execute the code cells step by step.

## Main Steps

- Data extraction from literature (INDRA: TRIPS, Sparser) and curated resources (SIGNOR, STING, Reactome, BioGRID).
- Protein-protein interaction filtering and normalization.
- Biological reference annotation (STING, Reactome, BioGRID).
- Feature engineering of linguistic and biological cues.
- Stratified train/test split and SMOTE oversampling for class balance.
- Hyperparameter-tuned model selection with cross-validation:
    - Logistic Regression (LASSO)
    - Random Forest
    - Support Vector Machine (SVM)
    - XGBoost
- Evaluation (test set metrics, cross-validation, bootstrap).
- Feature importance (model-based and SHAP).
- Simulation of synthetic interactions and robustness testing.

## Notes

- Adjust file paths as needed for your local environment.
- For API querying (STING, PubMed), ensure you have internet access.
- For large-scale runs, consider working with filtered or chunked datasets.

---

**Contact:** [Your Name or Email]  
**License:** MIT (or specify here)