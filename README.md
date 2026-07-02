
# Bangla Complaint Multilabel Classification

A multilabel text classification system for detecting multiple issues 
from Bangla customer complaints using transformer-based deep learning models.

## Project Info
- **University:** University of Asia Pacific (UAP)
- **Degree:** BSc in Computer Science and Engineering (CSE 400)
- **Team:**
  - Kazi Saria Rahman (22101046)
  - Ishtiak Ahmed Sabbir (22101044)
  - Mohiuddin Ahmed (22101011)
- **Supervisor:** Molla Rashied Hussein
- **Co-supervisor:** Dr. Subhra Prousun Paul

## Problem Statement
Bangla customer complaints often contain multiple issues at once 
(e.g., delivery delay + refund problem). This project builds an 
automated system to detect all issues simultaneously.

## Labels (8 Categories)
| Label | Description |
|---|---|
| Billing | Incorrect charges, billing errors |
| Refund | Refund not received or delayed |
| Delivery | Delayed or missing deliveries |
| Customer_Service | Poor customer support |
| Product_Quality | Defective or low-quality products |
| Account | Login or account access issues |
| Technical | App errors, technical faults |
| Network | Network failures, connectivity issues |

## Dataset
- Total: 4,082 Bangla complaint samples
- Train: 3,286 samples (90%)
- Test: 796 samples (10%)
- Collected from: Facebook, e-commerce platforms

## Models
| Model | F1 Micro | F1 Macro | Hamming Loss | ROC-AUC |
|---|---|---|---|---|
| BanglaBERT | **0.7735** | **0.7703** | **0.0656** | **0.8691** |
| XLM-RoBERTa | 0.6986 | 0.6780 | 0.0768 | — |

**Winner: BanglaBERT**

## Repository Structure
├── BanglaBERT_Final.ipynb     # BanglaBERT training & evaluation
├── XLMR_FINAL.ipynb           # XLM-RoBERTa training & evaluation
├── Preprocessing.ipynb        # Data preprocessing pipeline
├── Result_Analysis.ipynb      # Result analysis & comparison
└── README.md

## Training Config
- MAX_LEN: 128
- BATCH_SIZE: 16
- EPOCHS: 5
- Learning Rate: 2e-5
- Loss Function: BCEWithLogitsLoss
- Optimizer: AdamW

## Requirements
transformers
torch
scikit-learn
pandas
numpy
openpyxl

## How to Run
1. Open any notebook in Google Colab
2. Enable GPU runtime (T4)
3. Upload train and test Excel files
4. Run all cells sequentially
