# 🧠 ABSA-DANA-Security-IndoBERT
![Python](https://img.shields.io/badge/Python-3.10-blue)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Published-brightgreen)

## 📄 Overview
This repository contains the implementation of the paper:  
**“A Hybrid Approach of Aspect-Based Sentiment Analysis and Knowledge Extraction for Evaluating Security Perceptions in Digital Payment Applications.”**

The study applies **Aspect Sentiment Classification (ASC)** within an **Aspect-Based Sentiment Analysis (ABSA)** framework to evaluate user sentiment toward the *security aspect* of the **DANA** digital wallet application in Indonesia.  
Five classification models are compared — **SVM, Random Forest, CNN, BiLSTM, and IndoBERT** — and the final sentiment outputs are structured in **XML format** for knowledge extraction and system integration.

---

## 📁 Repository Structure
| Folder | Description |
|--------|--------------|
| `Dataset/` | Filtered, non-filtered (temporal), and cross-domain (GoPay) datasets |
| `Notebook/` | Jupyter/Colab notebooks for preprocessing, training, evaluation, and XML generation |
| `ABSA_KE_Final/` | Final XML outputs and schema (XSD) for knowledge extraction |
| `saved_models/` | Trained model checkpoints (tracked via Git LFS or hosted externally) |
| `.gitattributes` / `.gitignore` | Configuration for large file tracking |

---

## ⚙️ Usage via Google Colab
You can directly open and execute the project using Google Colab:  
🔗 [**Open in Google Colab**](https://colab.research.google.com/drive/1mNoFlMU-wMO2dQx8PAHsqIPg9Aeiizxd?usp=sharing)

### Setup
Before running, ensure the following Python libraries are installed:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn tensorflow torch transformers tqdm google-play-scraper joblib lxml



📦 Model Download
Due to GitHub file size limitations, the fine-tuned model files are hosted externally:

IndoBERT fine-tuned model: [Google Drive Link](https://drive.google.com/drive/folders/1-R8GM2v4kk7NHKqNNwFbG30hZpxN71so?usp=drive_link)k

Random Forest pipeline: [Google Drive Link](https://drive.google.com/file/d/1tEr-6MMyQprxGiAIii8qhQoKcDfgc8-P/view?usp=drive_link)

🔁 Reproducibility
Main experiment notebook:
Notebook/fixed_revisi version_absa_svm_random_forest_cnn_bilstm_indobert_KE_xmly.ipynb

5-Fold Cross-Validation Script:
Available inside the notebook or as Notebook/run_5fold.sh

Configuration files:
Random seeds, hyperparameters, and library versions are listed in config/ and requirements.txt.

Knowledge Extraction XML Schema:
Located in ABSA_KE_Final/knowledge_extraction_schema.xsd

📊 Evaluation Summary
The best-performing model (IndoBERT) achieved:

Accuracy: 98.0%

Precision: 97.5%

Recall: 97.4%

F1-score: 0.974

AUC-ROC: 0.996

The XML output encodes each review’s aspect, sentiment polarity, opinion words, and model confidence — enabling easy integration into sentiment dashboards or monitoring systems.

🧾 Citation
If you use this repository or its findings, please cite:
A. F. Fatihaturrahmah, “A Hybrid Approach of Aspect-Based Sentiment Analysis and Knowledge Extraction for Evaluating Security Perceptions in Digital Payment Applications,” 2025.

📩 Contact
Author: Aisyah Fatihaturrahmah
Institution: Faculty of Computer Science, Universitas Sriwijaya
📧 Email: aisyahfatiha22@gmail.com
🔗 GitHub: @aisyahfrahmaah
