# AYU-INTEL  
## Explainable AI for AYUSH Public Health Intelligence

---

## 📌 Overview

AYU-INTEL is an Explainable AI-based Public Health Intelligence and Personalized AYUSH Decision Support System designed to enhance the Ayush Hospital Management Information System (AHMIS).

Over 12,000+ AYUSH centers generate large-scale clinical data across India. However, this data is primarily used for record-keeping rather than predictive intelligence, outbreak detection, or personalized treatment optimization.

AYU-INTEL transforms passive clinical records into actionable public health intelligence using:

- Voice-enabled EHR capture
- Anomaly-based outbreak detection
- Probabilistic risk modeling
- SHAP-based explainability
- Prakriti-aware personalized treatment recommendation

The system is scalable, interoperable with AHMIS, and designed for MeghRaj cloud deployment.

---

## 🚩 Problem Statement

### Current Challenges

- Manual and time-consuming EHR entry
- Underutilization of AYUSH clinical data
- No district-level outbreak intelligence
- No AI-driven personalized treatment support
- Limited transparency in predictive systems

### National Importance

- 12,000+ AYUSH centers across India
- Need for preventive healthcare intelligence
- Demand for explainable and responsible AI
- Data-driven governance in public health

---

## 🎯 Proposed Solution

AYU-INTEL consists of three core components:

1. Voice-Enabled EHR Capture  
2. Explainable Outbreak Intelligence Engine  
3. Prakriti-Aware Personalized Recommendation System  

The system uses a hybrid AI + rule-based architecture to ensure:

- Domain correctness
- Transparency
- Interpretability
- Scalability

---

# 🏗 System Architecture

Below is the high-level layered architecture of AYU-INTEL.

```mermaid
flowchart LR

UI["User Interface Layer\nWeb/Tablet App\nPublic Health Dashboard"]

API["API Gateway Layer\nAuthentication\nRate Limiting\nLogging\nSecure Routing"]

subgraph APP["Application Services Layer"]
    EHR["EHR Intake Service"]
    VOICE["Voice Processing Service"]
    NLP["NLP Extraction Service"]
    OUTSVC["Outbreak Analytics Service"]
    RISK["Risk Scoring Service"]
    REC["Recommendation Service"]
    EXP["Explainability Service"]
    FEED["Feedback Learning Service"]
    DASH["Dashboard Reporting Service"]
end

subgraph DATA["Data Layer"]
    DB["PostgreSQL - Patient Records"]
    TS["Time-Series DB - Disease Trends"]
    OBJ["Object Storage - Reports"]
    REG["Model Registry"]
    LOG["Audit Logs"]
end

subgraph AI["AI Model Layer"]

    subgraph INPUT["Input Intelligence Models"]
        W["Whisper - Speech to Text"]
        NER["spaCy NER - Entity Extraction"]
    end

    subgraph OUTBREAK["Outbreak Intelligence Engine"]
        IF["Isolation Forest - Anomaly Detection"]
        XGB["XGBoost - Risk Probability"]
        SHAP["SHAP - Feature Contribution"]
    end

    subgraph RECOMMEND["Recommendation Intelligence Engine"]
        RULE["Rule-Based AYUSH Engine"]
        KNN["KNN - Similar Patient Matching"]
        CONF["Confidence Estimator"]
    end
end

CLOUD["Cloud Deployment\nMeghRaj (NIC)\nDocker + Kubernetes"]

UI --> API --> APP --> AI --> DATA --> CLOUD

UI --> API --> APP --> AI --> DATA --> CLOUD

