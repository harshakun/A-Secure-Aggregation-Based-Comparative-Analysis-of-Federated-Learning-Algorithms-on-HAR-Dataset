# A Secure Aggregation-Based Comparative Analysis of Federated Learning Algorithms on Human Activity Recognition Data

This repository contains the implementation of a **privacy-preserving Federated Learning (FL)** framework for Human Activity Recognition (HAR). The model is trained locally on edge devices using **Self-Supervised Learning (SSL)** and fine-tuned collaboratively using Federated Learning. To ensure strong privacy guarantees, the system integrates **Secure Aggregation** and **Differential Privacy (DP)** to prevent gradient leakage and data reconstruction attacks.

---

## 🔐 Key Features
- Local SSL training — no need for large labeled datasets.
- Federated training — raw data never leaves client devices.
- Secure Aggregation — encrypted model updates only.
- Differential Privacy — privacy against gradient inversion attacks.
- Comparison of three FL paradigms:
  - **Horizontal FL**
  - **Cross-Device FL**
  - **Cross-Silo FL**

---

## 🧪 Dataset
- **UCI-HAR Dataset**
- Accelerometer & gyroscope sensor data from 30 users performing 6 activities.
- Partitioned into clients to simulate real-world distributed, non-IID data.

---

## 📊 Results Summary

| FL Paradigm      | Accuracy | Privacy Protection | Communication Cost |
|------------------|----------|-------------------|-------------------|
| Horizontal FL    | ✅ Highest | Medium            | ❌ High           |
| Cross-Device FL  | Moderate | ✅ Highest         | ✅ Lowest         |
| Cross-Silo FL    | Balanced | ✅ High            | ✅ Medium         |

📌 Gradient leakage attack loss > **350**, indicating strong resilience against reconstruction attacks.

---

## 🧠 Methodology Workflow

1. **Local SSL (encoder training)** on unlabeled sensor data.
2. **Federated fine-tuning** on labeled data.
3. **Secure Aggregation + DP** to protect gradients.

```
Client Device → SSL Training → Local Fine-Tuning → Encrypted Model Update → Secure Aggregation → Global Model
```

---

## 📂 Project Structure
```
├── data/                     # UCI-HAR dataset (not included)
├── src/
│   ├── Horizontal_Federated_Learning.py    
│   ├── federated_train.py    
│   ├── secure_aggregation.py 
├── results/
│   ├── Horizontal_Federated_Learning.py    
│   ├── federated_train.py    
│   ├── secure_aggregation.py
└── README.md
```

---

## ▶️ Usage

### Install dependencies
```sh
pip install -r requirements.txt
```

---

## 🛠 Tech Stack

| Component | Tools |
|----------|-------|
| Language | Python |
| FL Framework | TensorFlow Federated / Flower |
| Data Processing | NumPy, Pandas |
| Model | 1D-CNN + SSL (Contrastive Learning) |
| Privacy | Secure Aggregation + Differential Privacy |

---

## 📄 Citation

```
Bandari, H., Gude, D., Raavi, V.K., Challa, A.K.R., & Kumar, S.
"A Secure Aggregation-Based Comparative Analysis of Federated Learning Algorithms on Human Activity Recognition Data."
```

---

## 👥 Authors

| Name | Role |
|------|------|
| Harshavardan Bandari | Research & Implementation |
| Dhanvanth Kumar Gude | Research & Dataset Processing |
| Vamshi Krishna Raavi | Model Architecture |
| Anjani Kumar Reddy Challa | Code & Experiments |
| Siddharth Kumar | Supervisor / Guide |

---

## 📬 Contact
For queries: **harshavardanbandari@gmail.com**

