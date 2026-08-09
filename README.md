# 🛡️ NAFDAC AI Anti-Counterfeit Verification System

**Fellow Name:** Abdulhameed Idris  
**Fellow ID:** FE/25/3927167605  
**Track:** Artificial Intelligence & Machine Learning  
**ALC:** Ibadan Digital Academy (Oyo State)  
**Project Code:** AI-06  

---

## 📌 Project Overview
Counterfeit pharmaceuticals pose a severe public health risk in Nigeria. This project delivers a **Dual-Layer Real-Time Anti-Counterfeit Verification System** combining official registry lookups with advanced machine learning inference and computer vision barcode scanning. 

The system allows users to verify drug authenticity by either scanning product barcode/QR images or manually entering product details (Drug Name, NAFDAC Registration Number [NRN], and Manufacturer Name).

---

## 🏗️ System Architecture

The verification pipeline operates across two complementary layers:

```text
                          [ Input: Barcode Image OR Typed Data ]
                                            │
                                            ▼
                    ┌──────────────────────────────────────────────┐
                    │  LAYER 1: Official Registry Exact Matching   │
                    └──────────────────────┬───────────────────────┘
                                           │
                        ┌──────────────────┴──────────────────┐
                        │                                     │
                 [ Match Found ]                      [ No Match Found ]
                        │                                     │
                        ▼                                     ▼
            🟢 100% AUTHENTIC PRODUCT          ┌─────────────────────────────┐
             (Returns Registry Info)           │ LAYER 2: AI ML Engine       │
                                               │ • TF-IDF Vectorizer         │
                                               │ • Random Forest Classifier  │
                                               │ • Isolation Forest Anomaly  │
                                               └──────────────┬──────────────┘
                                                              │
                                            ┌─────────────────┴─────────────────┐
                                            │                                   │
                                    [ Suspicious/Fake ]                [ Critical Anomaly ]
                                            │                                   │
                                            ▼                                   ▼
                                 🟠 / 🔴 COUNTERFEIT ALERT          🚨 UNLICENSED / TAMPERED
