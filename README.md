<div align="center">

# Mahateer Muhammad

**AI/ML Engineer · Healthcare AI · Applied LLM Systems**

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](#)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mahateer-muhammad-a74284356)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mahateermuhammad100@gmail.com)

</div>

---

## About

AI/ML engineer with a focus on healthcare AI, clinical data systems, and applied LLM work. Background in Flutter and full-stack development (2+ years, co-founder of UXELERATE), currently shifting focus toward LLM/RAG and applied AI systems.

Recent work: DPO fine-tuning for medical hallucination reduction, large-scale clinical trajectory modeling on MIMIC-IV, and production-hardened multi-agent LLM orchestration.

| Area | Focus | Evidence |
|---|---|---|
| Preference optimization | DPO fine-tuning for factual grounding | MedTrust — F1 0.535 → 0.650 on MedHallu |
| Clinical data engineering | Large-scale EHR pipelines | 546K+ MIMIC-IV stays, 40GB+ processed |
| LLM systems in production | Multi-agent orchestration, LLMOps | Rate limiting, prompt injection defense, Docker hardening |
| Medical imaging | CNN classification with explainability | 90.69% accuracy, Grad-CAM |
| Mobile development | Flutter cross-platform apps | Firebase, real-time features |

---

## Projects

### MedTrust — Faithfulness-Optimized Medical QA via DPO

Reduces hallucination in a 7B clinical LLM using Direct Preference Optimization rather than standard SFT. Ground-truth PubMedQA answers are the chosen response, matched hallucinated answers are the rejected response, for the same clinical query.

- Base model: Qwen2.5-7B-Instruct, 4-bit QLoRA via Unsloth
- Trained with TRL's `DPOTrainer`, LoRA rank 16, β = 0.1
- 40.3M trainable LoRA parameters (0.53% of total weights)
- ~2 hours on a single Kaggle T4/P100 (16GB VRAM)
- Evaluated on 999 held-out, human-annotated MedHallu pairs

**Results**

| Tier | Base Model F1 | MedTrust DPO F1 | Gain |
|---|---|---|---|
| Easy | 0.612 | 0.747 | +13.5 |
| Medium | 0.530 | 0.648 | +11.8 |
| Hard | 0.498 | 0.586 | +8.8 |
| **Overall** | **0.535** | **0.650** | **+11.5** |

Hard-tier performance (0.586 F1) approaches GPT-4o's reported ~0.625 on the same split.

`Python` `PyTorch` `Unsloth` `TRL` `QLoRA` `Kaggle`

---

### Clinical Digital Twin — Patient Risk & Decision-Support System

Production-grade pipeline turning 40GB+ of raw MIMIC-IV tables (546K+ hospital stays, 500K+ patients) into ML-ready datasets, with a downstream multi-task prediction and LLM decision-support layer.

- 5-stage pipeline: load (schema inference) → clean (validation) → EDA → feature engineering → dataset output
- Multi-task models across 5 clinical prediction tasks
- 0.949 AUROC for 24-hour mortality, 0.897 AUROC for 6-hour ward deterioration
- LLM/RAG decision-support agent with SHAP TreeExplainer interpretability, counterfactual "what-if" simulation, and clinical guideline retrieval (KDIGO, Surviving Sepsis)
- Patient embedding layer for similar-patient retrieval

`Python` `XGBoost` `LightGBM` `PyArrow` `SHAP` `RAG`

---

### Multi-Agent Debate Framework — Production LLM Orchestration

A FastAPI service where a single request to `/api/v1/run` can spawn up to 25 nested LLM API calls across Proponent/Opponent agents. Built past the prototype stage with a full LLMOps and security hardening pass.

- Distributed rate limiting via `slowapi` with Redis-backed storage (cross-worker/pod safe)
- Prompt injection defense: XML delimiter encapsulation of untrusted input, tag-stripping on user input, system-level security directive
- Request tracing with correlation IDs, structured JSON logging
- Docker hardened: non-root user, `cap_drop: ALL`, correct ownership
- Async connection pooling moved outside the retry loop, request timeouts via `asyncio.wait_for`

`Python` `FastAPI` `Docker` `Redis`

---

### Brain Tumor Detection with Explainable AI

Four-class brain tumor classification from MRI scans (Kaggle dataset), built as a five-notebook pipeline: EDA, preprocessing, custom CNN, transfer learning, Grad-CAM.

- 90.69% accuracy with ResNet50 transfer learning
- Grad-CAM visual explanations for model predictions
- Interactive Streamlit dashboard

`TensorFlow` `ResNet50` `Streamlit` `Grad-CAM`

---

### DeepVision — Interactive Neural Network Visualizer

Educational platform for understanding neural networks from first principles, built on live PyTorch hooks rather than simulated data.

- Network Canvas: semantic-zoom D3 graph with step-through execution
- Activation Lab, CNN Lab (filter factory, receptive fields, saliency maps), Optimizer Arena, BatchNorm Tracker
- 255 tests, all values sourced live from PyTorch

`PyTorch` `FastAPI` `React 19` `D3.js`

---

### Retail Data Analyzer

Distributed analytics pipeline for large-scale retail data using PySpark.

- Revenue analysis, customer metrics, spend classification, rolling averages

`PySpark` `PostgreSQL`

---

### Social-Swap (Konexea) — Flutter Social App with AI

Cross-platform social app with real-time chat and AI-assisted translation.

`Flutter` `Firebase` `Supabase`

---

### CALiNGA — On-Demand Healthcare Platform

Mobile platform connecting patients with healthcare providers.

- Real-time location tracking, provider matching, in-app notifications

`Flutter` `Firebase` `Google Maps`

---

## Tech Stack

**Languages:** Python · JavaScript/TypeScript · Dart · C++

**AI/ML:** PyTorch · TensorFlow · Keras · scikit-learn · Unsloth · TRL · Hugging Face Transformers

**Data Engineering:** Apache Spark · Pandas · PyArrow · PostgreSQL · MongoDB

**Backend:** FastAPI · Express · Node.js

**Frontend:** React · Vite · Tailwind CSS · D3.js

**Mobile & Cloud:** Flutter · Firebase · AWS · Docker

---

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=MahateerMuhammad&show_icons=true&theme=dark&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=MahateerMuhammad&layout=compact&theme=dark&hide_border=true)

</div>

---

## Currently

Working on LLM/RAG systems and preference-optimization methods for factual grounding in clinical applications, alongside production hardening of multi-agent LLM services.

Open to collaboration on healthcare AI and applied LLM projects.

<div align="center">

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mahateermuhammad100@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mahateer-muhammad-a74284356)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MahateerMuhammad)

</div>
