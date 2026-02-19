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

%% TOP FLOW (Left to Right)

UI["User Interface Layer
Web / Tablet App
Public Health Dashboard"]

API["API Gateway Layer
Authentication
Rate Limiting
Logging
Secure Routing"]

APP["Application Services Layer
EHR Intake
Voice Processing
NLP Extraction
Outbreak Service
Risk Scoring
Recommendation
Explainability"]

AI["AI Model Layer"]

CLOUD["Cloud Deployment
MeghRaj (NIC)
Docker + Kubernetes"]

UI --> API --> APP --> AI --> CLOUD


%% SECOND LEVEL (Models Inside AI - Vertical)

subgraph AI_DETAILS["AI Model Layer – Internal Components"]
direction TB

INPUT["Input Intelligence Models
Whisper (Speech-to-Text)
spaCy NER (Entity Extraction)"]

OUTBREAK["Outbreak Intelligence Engine
Isolation Forest
XGBoost
SHAP Explainability"]

RECOMMEND["Recommendation Intelligence Engine
Rule-Based AYUSH Engine
KNN Matching
Confidence Estimator"]

end

AI --> INPUT
INPUT --> OUTBREAK
OUTBREAK --> RECOMMEND
