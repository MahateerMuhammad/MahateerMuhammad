<div align="center">

# Hi 👋 I'm Mahateer Muhammad

### AI/ML Engineer | Healthcare AI Specialist | Full-Stack Developer

[![Python](https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://tensorflow.org/)
[![React](https://img.shields.io/badge/-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Flutter](https://img.shields.io/badge/-Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](#)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mahateer-muhammad-a74284356)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mahateermuhammad100@gmail.com)

![Profile Views](https://komarev.com/ghpvc/?username=MahateerMuhammad&color=blueviolet&style=flat-square)

</div>

---

## 📋 Table of Contents
- [About Me](#-about-me)
- [Featured Projects](#-featured-projects)
- [Tech Stack](#-tech-stack)
- [GitHub Stats](#-github-stats--insights)
- [Currently](#-currently)
- [Get in Touch](#-get-in-touch)

---

## 🧠 About Me

```python
class Mahateer:
    def __init__(self):
        self.role = "AI/ML Engineer"
        self.focus = ["Healthcare AI", "Preference Optimization", "LLM Systems"]
        self.background = "2+ years Flutter dev, co-founder @ UXELERATE"
        self.currently_learning = "LLM/RAG, applied AI systems"
        self.fun_fact = "trained a DPO model on a single T4 in ~2 hours"

    def say_hi(self):
        print("Let's build something that doesn't hallucinate.")
```

I build AI systems for healthcare — clinical trajectory models, hallucination-reducing LLM fine-tunes, and production-grade multi-agent orchestration. Currently pivoting from mobile development into applied AI, RAG, and preference optimization.

### 🎯 Key Specializations

| Area | Expertise | Evidence |
|---|---|---|
| 🎯 **Preference Optimization** | DPO fine-tuning for factual grounding | F1 0.535 → 0.650 on MedHallu |
| 🏥 **Clinical Data Engineering** | Large-scale EHR pipelines | 546K+ MIMIC-IV stays, 40GB+ processed |
| 🤖 **LLM Systems in Production** | Multi-agent orchestration, LLMOps | Rate limiting, prompt injection defense, hardened Docker |
| 🖼️ **Medical Imaging** | CNN classification + explainability | 90.69% accuracy, Grad-CAM |
| 📱 **Mobile Development** | Flutter cross-platform apps | Firebase, real-time features |

---

## 🔬 Featured Projects

### 1. 🩺 **MedTrust** — Faithfulness-Optimized Medical QA via DPO

> Teaching a 7B model to stop confidently making things up in clinical answers

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/MedTrust)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch)
![Unsloth](https://img.shields.io/badge/Unsloth-FF6600?style=flat)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)

Fine-tunes Qwen2.5-7B-Instruct with **Direct Preference Optimization** (not SFT) on the MedHallu benchmark — matched grounded vs. hallucinated PubMedQA answers, 4-bit QLoRA, 40.3M trainable LoRA params (0.53% of total weights), ~2 hours on one Kaggle T4.

**Benchmark results (999 held-out human-annotated pairs):**

| Tier | Base F1 | MedTrust DPO F1 | Δ |
|---|---|---|---|
| 🟢 Easy | 0.612 | **0.747** | +13.5 |
| 🟡 Medium | 0.530 | **0.648** | +11.8 |
| 🔴 Hard | 0.498 | **0.586** | +8.8 |
| **Overall** | **0.535** | **0.650** | **+11.5** |

Hard-tier score (0.586) lands close to GPT-4o's reported ~0.625 on the same split — from a model 1/20th the size, fine-tuned on a free GPU.

**Case study — the model catching a fatal contraindication:**

*Query:* Should beta-blockers be given immediately in cardiogenic shock from acute MI?

❌ Base model: "Yes, initiate immediately in all AMI patients." *(dangerous — beta-blockers are contraindicated here)*
✅ MedTrust: "No — contraindicated in cardiogenic shock due to negative inotropic effects. Stabilize hemodynamics first."

---

### 2. 🏥 **Clinical Digital Twin** — Patient Risk & Decision-Support System

> 40GB of raw hospital data in, a risk-scoring RAG agent out

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/Clinical-Digital-Twin)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas)
![XGBoost](https://img.shields.io/badge/XGBoost-blue?style=flat)
![SHAP](https://img.shields.io/badge/SHAP-red?style=flat)

Production pipeline processing 546K+ MIMIC-IV hospital stays (40GB+ raw temporal tables) into ML-ready Parquet datasets, feeding multi-task clinical prediction models.

**5-Stage Pipeline:** Load (schema inference) → Clean (validation) → EDA → Feature Engineering → Datasets

- 🎯 **0.949 AUROC** — 24-hour mortality prediction
- 🎯 **0.897 AUROC** — 6-hour ward deterioration
- 🧩 LLM/RAG decision-support agent: SHAP TreeExplainer interpretability, counterfactual "what-if" simulation, clinical guideline retrieval (KDIGO, Surviving Sepsis)
- 🔗 Patient embedding layer for similar-patient retrieval

---

### 3. ⚔️ **Multi-Agent Debate Framework** — Production LLM Orchestration

> A single API call, 25 nested LLM calls, and enough hardening to survive contact with the real world

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/multi-agent-debate)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)

FastAPI service where `/api/v1/run` spawns up to 25 nested LLM calls across Proponent/Opponent agents. Pushed through a full LLMOps + security hardening pass:

- 🛡️ Distributed rate limiting (`slowapi` + Redis, cross-worker/pod safe)
- 🛡️ Prompt injection defense — XML delimiter encapsulation, input tag-stripping, system-level security directive
- 📊 Request tracing with correlation IDs, structured JSON logs
- 🔒 Docker hardened — non-root user, `cap_drop: ALL`, correct ownership
- ⚡ Async connection pooling moved outside the retry loop, `asyncio.wait_for` timeouts

---

### 4. 🧠 **Brain Tumor Detection with Explainable AI**

> Healthcare AI that shows its work

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/Brain-Tumor-Detection-and-Classification-using-Deep-Learning)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit)
![ResNet50](https://img.shields.io/badge/ResNet50-Transfer_Learning-blue?style=flat)

- 🎯 **90.69% accuracy** on 4-class tumor classification (ResNet50 transfer learning)
- 📊 Grad-CAM explainability layered on top of every prediction
- 🎨 Interactive Streamlit dashboard
- 🧪 Five-notebook pipeline: EDA → Preprocessing → Custom CNN → Transfer Learning → Grad-CAM

---

### 5. 🎨 **DeepVision** — Interactive Neural Network Visualizer

> Neural networks, explained by the network itself

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/DeepVision)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch)
![React](https://img.shields.io/badge/React_19-61DAFB?style=flat&logo=react)

- 🖼️ Network Canvas — semantic-zoom D3 graph, VCR-style stepping
- 🧪 Activation Lab, CNN Lab (filter factory, receptive fields, saliency), Optimizer Arena, BatchNorm Tracker
- ✅ 255 tests, zero faked data — every number comes live from PyTorch hooks

---

### 6. ⚡ **Retail Data Analyzer**

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/Retail_data_analyzer)
![PySpark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=flat&logo=apachespark)

Distributed retail analytics on PySpark — revenue analysis, customer metrics, spend classification, rolling averages.

---

### 7. 📱 **Social-Swap (Konexea)** — Flutter Social App with AI

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/Social-Swap)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)

Real-time chat, AI translation, media sharing, Rive animations.

---

### 8. 🚑 **CALiNGA** — On-Demand Healthcare Platform

[![View on GitHub](https://img.shields.io/badge/View_on_GitHub-181717?style=flat-square&logo=github)](https://github.com/MahateerMuhammad/calinga)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter)
![GoogleMaps](https://img.shields.io/badge/Google_Maps-4285F4?style=flat&logo=googlemaps)

Real-time location tracking, provider matching, in-app notifications.

---

## 🛠 Tech Stack

### Languages
![Python](https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Dart](https://img.shields.io/badge/-Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![C++](https://img.shields.io/badge/-C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

### AI & Machine Learning
![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/-Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![Scikit_Learn](https://img.shields.io/badge/-Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![HuggingFace](https://img.shields.io/badge/-HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

### Data Engineering
![Apache_Spark](https://img.shields.io/badge/-Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

### Backend & APIs
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Express](https://img.shields.io/badge/-Express-000000?style=for-the-badge&logo=express&logoColor=white)
![NodeJS](https://img.shields.io/badge/-Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

### Frontend & UI
![React](https://img.shields.io/badge/-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/-Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/-Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![D3JS](https://img.shields.io/badge/-D3.js-F9A825?style=for-the-badge&logo=d3.js&logoColor=black)

### Mobile & Cloud
![Flutter](https://img.shields.io/badge/-Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Firebase](https://img.shields.io/badge/-Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![AWS](https://img.shields.io/badge/-AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

---

## 📊 GitHub Stats & Insights

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=MahateerMuhammad&show_icons=true&theme=radical&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=MahateerMuhammad&layout=compact&theme=radical&hide_border=true)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=MahateerMuhammad&theme=radical&hide_border=true)

![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=MahateerMuhammad&theme=redical&hide_border=true)

</div>

---

## 💡 Skill Levels

```
AI/ML Development     ████████████████░░ 90%
Data Engineering       ██████████████░░░░ 80%
Backend Development    █████████████░░░░░ 85%
Frontend Development   ████████████░░░░░░ 75%
DevOps & Deployment     ███████░░░░░░░░░░░ 40%
```

---

## 🎯 Currently

- 🔭 Working on preference-optimization methods (DPO) for factual grounding in clinical LLMs
- 🌱 Learning applied RAG architectures and production LLMOps
- 🤝 Open to collaborating on healthcare AI and applied LLM projects
- ⚡ Fun fact: trained MedTrust's DPO adapter (40.3M params) end-to-end on a free Kaggle T4 in under 2 hours

---

## 📫 Get in Touch

<div align="center">

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mahateermuhammad100@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mahateer-muhammad-a74284356)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MahateerMuhammad)

**Status:** ✅ Open to opportunities

</div>
