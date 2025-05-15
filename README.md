# 📊 SMS Fraud Detection and Reporting using LLM 

## 🧠 Project Overview
This project implements an end-to-end pipeline for detecting SMS spam using LLM-based embeddings (Mistral), interpretable machine learning, and risk-aware reporting.

It includes:
- Exploratory Data Analysis (EDA)
- Embedding generation using `ollama` Mistral model
- Random Forest classifier with performance evaluation
- LIME explanations for interpretability
- Executive-level HTML/PDF reporting using LLM-generated narrative

---

## 🗂️ Repository Structure

```
├── data/
│   ├── spam.csv                 # Raw dataset (Kaggle UCI SMS Spam)
│   ├── model_metrics.csv        # Saved model evaluation metrics
├── plots/
│   ├── *.png                    # Visuals from EDA, LIME, Confusion Matrix
├── reports/
│   ├── fraud_detection_report.html
│   ├── fraud_detection_report.pdf
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_llm_finetuning_prediction.ipynb
│   ├── 03_llm_executive_report.ipynb
├── README.md                   
```

---

## 📥 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sumitdeole/LLM_text_data.git
   cd LLM_text_data
   ```

2. Create environment and install dependencies:
   ```bash
   conda create -n sms-fraud python=3.10 -y
   conda activate sms-fraud
   pip install -r requirements.txt
   ```

3. Install additional system dependencies:
   - **WeasyPrint** requires [GTK3 runtime for Windows](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases)
   - Add `C:\Program Files\GTK3-Runtime Win64\bin` to your system PATH

---

## ⚙️ Notebooks

### 1. EDA + Feature Engineering
- Loads and visualizes data
- Generates word clouds and top spam unigrams

### 2. Model Training with Mistral
- Generates 4096-D embeddings using `ollama`'s Mistral
- Trains a balanced Random Forest
- Saves metrics and plots

### 3. Executive Reporting
- Feeds metrics and text features to LLM for narrative
- Renders HTML/PDF executive report with visuals

---

## 📈 Example Outputs

- Confusion Matrix
  ![Confusion Matrix](plots/confusion_matrix.png)
- LIME Explanation
  ![LIME](plots/lime_visualization.png)

---

## 📄 License
MIT License

---

## ⭐ Star this repo
If you find this project helpful, feel free to give it a ⭐ on [GitHub](https://github.com/sumitdeole/LLM_text_data)!