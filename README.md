# NAFDAC AI Fake Drug Text & Barcode Checker

**Fellow Name:** Abdulhameed Idris  
**Fellow ID:** FE2539271676  
**Track:** Artificial Intelligence & Machine Learning  
**ALC:** Ibadan Digital Academy (Oyo State)  
**Project Code:** AI-06  

---

## 📌 Project Overview
This project addresses the critical challenge of counterfeit pharmaceutical products in Nigeria. It implements a **Dual-Layer Machine Learning Architecture** combined with barcode/text scanning to evaluate drug registration details against NAFDAC databases.

## 🏗️ System Architecture & Features
* **Barcode & Text Processing:** Extracts registration codes and product details.
* **Supervised Classification:** Random Forest Classifier trained to classify registered vs. fake drug signatures.
* **Anomaly Detection:** Isolation Forest model to detect novel counterfeit patterns or altered NAFDAC numbers.
* **Text Vectorization:** TF-IDF feature extraction for textual comparison.

## 📁 Repository Structure
* `AI06_Fake_Drug_Checker_Idris_Abdulhamood_FE2539271676.ipynb` — Full end-to-end Google Colab notebook
* `rf_model.pkl` — Trained Random Forest model
* `isolation_forest.pkl` — Trained Isolation Forest model
* `vectorizer.pkl` — TF-IDF Vectorizer
* `nafdac_registered_drugs.csv` — Registered drugs database
* `balanced_fake_drug_dataset.csv` — Training dataset
