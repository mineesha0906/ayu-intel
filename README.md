# AYU-INTEL: Explainable AI for AYUSH Public Health Intelligence

[cite_start]**AYU-INTEL** is an Explainable AI-based Public Health Intelligence and Personalized AYUSH Decision Support System[cite: 4]. [cite_start]Designed to enhance the **Ayush Hospital Management Information System (AHMIS)**, it transforms clinical data from over 12,000 centers into predictive intelligence for outbreak detection and personalized treatment optimization[cite: 4, 5].

---

## 📌 Problem Overview
[cite_start]Currently, clinical data in AYUSH centers is primarily used for record-keeping rather than predictive intelligence or outbreak detection[cite: 5].

### [cite_start]Key Challenges [cite: 10, 21]
* [cite_start]**Manual Entry:** EHR data entry is manual and time-consuming[cite: 11].
* [cite_start]**Data Underutilization:** Clinical data is not effectively used for district-level outbreak intelligence[cite: 12, 13].
* [cite_start]**Lack of Personalization:** Absence of AI-driven treatment assistance that incorporates *Prakriti*[cite: 14].
* [cite_start]**Transparency Gap:** Existing systems lack explainability in predictive healthcare[cite: 15, 25].

---

## 💡 Proposed Solution
[cite_start]AYU-INTEL introduces a hybrid AI + rule-based architecture focusing on three integrated components[cite: 27, 31]:
1. [cite_start]**Voice-Enabled EHR Capture:** Using Whisper for speech-to-text transcription of patient data[cite: 28, 77].
2. [cite_start]**Explainable Outbreak Intelligence Engine:** Anomaly-based detection with SHAP-based feature contribution analysis[cite: 29, 107].
3. [cite_start]**Prakriti-Aware Personalized Recommendation System:** Treatment plans based on AYUSH guidelines and patient similarity[cite: 30, 116].

---

## 🏗️ System Architecture
[cite_start]The system follows a multi-layered cloud-native architecture deployable on **MeghRaj (NIC) Cloud**[cite: 7, 167].

```mermaid
graph LR
    subgraph UI["User Interface Layer"]
        A[Web/Tablet App - Doctor Interface]
        B[Public Health Dashboard - Admin View]
    end

    subgraph Gateway["API Gateway Layer"]
        C[Auth, Rate Limiting, & Secure Routing]
    end

    subgraph Services["Application Services Layer"]
        D[EHR Intake & Voice Processing]
        E[Outbreak Analytics & Risk Scoring]
        F[Recommendation & Explainability]
    end

    subgraph Data["Data Layer"]
        G[(PostgreSQL - Patient Records)]
        H[(Time-Series DB - Disease Trends)]
        I[Object Storage & Feature Store]
    end

    subgraph AI["AI Model Layer"]
        J[Input Intelligence: Whisper & spaCy]
        K[Outbreak Engine: Isolation Forest & XGBoost]
        L[Recommendation: KNN & Rule Engine]
    end

    UI --> Gateway
    Gateway --> Services
    Services --> Data
    Services --> AI
    AI --> M[Cloud Deployment]
This repository is part of an academic/government innovation proposal and is under active development.
