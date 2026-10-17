# EEG-Based BCI Classification Pipeline

A modular, leak-free Brain-Computer Interface (BCI) classification framework comparing **Motor Imagery (Mental)** versus **Motor Movement (Physical)** using EEG signals.

---

## 📂 Project Structure & Execution Flow

To ensure proper data flow and automated results aggregation, run the notebooks in sequential order:

1. **`01_motor_imagery_demo.ipynb`** — Processes mental motor imagery EEG data, evaluates performance via cross-validation, and exports fold scores.
2. **`02_motor_movement_demo.ipynb`** — Processes physical motor movement EEG data, evaluates performance via cross-validation, and exports fold scores.
3. **`03_model_comparison.ipynb`** — Dynamically reads exported scores from the `bci_scores.json` bridge, computes mean and standard deviation metrics, and outputs a comparative visualization.

---

## 🔬 Key Engineering & Scientific Highlights

* **Leak-Free Pipelines:** Built using `sklearn.Pipeline` to guarantee signal processing and spatial filtering (CSP) are strictly isolated within cross-validation folds.
* **Statistical Rigor:** Evaluates model performance using **Mean Accuracy** and **Standard Deviation Error Bars** across 5 folds.
* **Automated Data Bridge:** Notebooks write and read directly via `bci_scores.json`, eliminating hardcoded values in downstream analysis.
* **50% Chance Threshold:** Includes a visual chance-level reference line for binary classification benchmarking.

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

2. Environment Setup
Install core BCI libraries:

pip install -r requirements.txt

3. Run the Pipeline
Execute 01_motor_imagery_demo.ipynb, 02_motor_movement_demo.ipynb, and 03_model_comparison.ipynb sequentially.

---