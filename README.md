# Mahateer Muhammad

AI/ML Engineer | Full-Stack Developer | Healthcare AI Specialist

---

## About Me

I'm an AI and machine learning engineer with a strong focus on **healthcare AI** and **data engineering**. My work spans deep learning for medical imaging, clinical data preprocessing at scale, and building interactive tools for understanding neural networks. I'm proficient in both backend and frontend development, with experience building production-ready systems that process complex datasets and make machine learning interpretable.

My projects demonstrate expertise in:
- **Medical AI**: Brain tumor detection with explainability (Grad-CAM)
- **Clinical Data Engineering**: Processing MIMIC-IV datasets with Spark
- **Deep Learning Education**: Building interactive neural network visualization tools
- **Full-Stack Development**: From React/TypeScript frontends to FastAPI/Express backends
- **Mobile Development**: Flutter applications for healthcare and social platforms

---

## 🔬 Featured Projects

### 1. **DeepVision** — Interactive Neural Network Visualizer
A production-grade educational platform for understanding how neural networks actually work, layer by layer, with real PyTorch activations and gradients.

**Live Instruments:**
- Network Canvas: Semantic-zoom graph with VCR-style forward/backward stepping
- Activation Lab: Curves, derivatives, freehand drawing mode
- CNN Lab: Filter factory, convolution explorer, receptive field visualization, saliency mapping
- Optimizer Arena: Loss surfaces, optimizer racing, divergence analysis
- BatchNorm Tracker: Real-time feature normalization visualization

**Tech Stack:** PyTorch 2.2 · FastAPI · React 19 · Vite · D3.js · Three.js · Tailwind CSS

**Why it matters:** 255 tests, zero faked data. Every number on screen comes live from PyTorch via hooks. Designed for students, educators, and researchers who want to *see* what's happening inside their models.

[Repository](https://github.com/MahateerMuhammad/DeepVision)

---

### 2. **Brain Tumor Detection with Explainable AI**
ResNet50 transfer learning model for 4-class MRI classification (glioma, meningioma, notumor, pituitary) with Grad-CAM explainability and interactive Streamlit dashboard.

**Key Features:**
- ~91–92% test accuracy on 4-class brain tumor classification
- Grad-CAM saliency maps for model interpretability
- Interactive web interface via Streamlit
- Comprehensive documentation on known limitations

**Tech Stack:** TensorFlow/Keras · ResNet50 · Streamlit · NumPy · Matplotlib

**Educational Value:** Demonstrates the importance of explainability in medical AI and handles the practical trade-offs between accuracy and real-world applicability.

[Repository](https://github.com/MahateerMuhammad/Brain-Tumor-Detection-and-Classification-using-Deep-Learning-with-Explainable-AI--Grad-CAM-)

---

### 3. **Clinical Digital Twin** — Production Data Engineering Pipeline
Enterprise-grade preprocessing and feature engineering pipeline for MIMIC-IV (40GB+ clinical dataset). Transforms raw hospital/ICU/clinical notes into ML-ready datasets.

**Pipeline Stages:**
1. **Load**: Schema inference for CSV/gzip files (hospitals, ICU stays, clinical notes)
2. **Clean**: Data validation, missing value handling, duplicate removal
3. **EDA**: Automated exploratory analysis with publication-quality plots
4. **Features**: Demographic, diagnostic, laboratory, vital, medication, procedure, temporal, and interaction features
5. **Datasets**: Patient/admission/ICU/time-series/clinical-notes level datasets

**Output:** Six Parquet datasets ready for mortality/readmission/LOS prediction, embedding models, or Transformer NLP

**Tech Stack:** Pandas · PyArrow · Scikit-learn · Plotly · YAML config · Jupyter

**Production Ready:** Chunked I/O for 40GB+ chartevents · Comprehensive logging · Reproducible with central config · No silent data removal

[Repository](https://github.com/MahateerMuhammad/Clinical-Digital-Twin)

---

### 4. **Retail Data Analyzer with PySpark**
Large-scale retail transaction analysis using distributed Apache Spark with PostgreSQL backend. Demonstrates data transformation, aggregations, window functions, and ML-ready feature engineering.

**Analytics Delivered:**
- Revenue analysis by country and customer
- Basket size and product diversity metrics
- Spend classification (Low/Medium/High)
- Rolling averages and purchase ranking

**Tech Stack:** PySpark · PostgreSQL · Window Functions · Spark SQL

[Repository](https://github.com/MahateerMuhammad/Retail_data_analyzer)

---

### 5. **School Management System** — Enterprise Backend
Full-featured school management backend with payment reconciliation, fee vouchers, and admin dashboards. Demonstrates professional backend architecture.

**Features:**
- Express.js + PostgreSQL
- AWS S3 file uploads
- JWT authentication
- Rate limiting and security (Helmet, CORS)
- Fee reconciliation scripts with dry-run mode

**Tech Stack:** Express.js · PostgreSQL · AWS S3 · JWT · Helmet · Morgan logging

[Repository](https://github.com/MahateerMuhammad/School-B)

---

### 6. **Velzck Shop** — Full-Stack E-Commerce Platform
Complete e-commerce system with separate frontend (React) and backend (Express + MongoDB).

**Backend:** Express.js · MongoDB · Mongoose · Cloudinary · JWT authentication · Email notifications (Nodemailer/Resend)

**Frontend:** React 18 · Vite · React Router · Axios · Cookie management

[Repository](https://github.com/MahateerMuhammad/Velzck_Shop)

---

### 7. **Social-Swap (Konexea)** — Flutter Social App with AI
Modern Flutter social media application featuring AI-powered interactions, real-time chat, and multimedia sharing.

**Tech Stack:** Flutter 3+ · Firebase (Auth, Firestore, Storage) · Supabase · Google ML Kit Translation · Rive animations

[Repository](https://github.com/MahateerMuhammad/Social-Swap)

---

### 8. **CALiNGA** — On-Demand Care Mobile App
Healthcare platform connecting patients with care providers. Built in Flutter with Firebase and Google Maps integration.

**Features:**
- Real-time location services (Google Maps, Geolocator)
- Firebase authentication and real-time database
- Provider matching and routing
- In-app notifications

**Tech Stack:** Flutter · Firebase · Google Maps · Geolocator · Geocoding

[Repository](https://github.com/MahateerMuhammad/calinga)

---

## 🛠 Tech Stack

### **Programming Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=java&logoColor=white)

### **AI & Machine Learning**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)

### **Data Engineering & Analytics**
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![PyArrow](https://img.shields.io/badge/PyArrow-FF6B6B?style=flat)

### **Backend & APIs**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)

### **Frontend & UI**
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![React Router](https://img.shields.io/badge/React%20Router-CA4245?style=flat&logo=reactrouter&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![D3.js](https://img.shields.io/badge/D3.js-F9A825?style=flat&logo=d3dotjs&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat&logo=threedotjs&logoColor=white)

### **Mobile Development**
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)

### **Cloud & Infrastructure**
![AWS S3](https://img.shields.io/badge/AWS%20S3-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Cloudinary](https://img.shields.io/badge/Cloudinary-3448C5?style=flat&logo=cloudinary&logoColor=white)

### **Developer Tools**
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37726?style=flat&logo=jupyter&logoColor=white)

---

## 🎯 Current Focus

- **Healthcare AI**: Medical imaging, clinical data pipelines, and AI explainability
- **Deep Learning Education**: Making neural networks interpretable and understandable
- **Data Engineering**: Scalable pipelines for complex clinical datasets
- **Full-Stack Development**: Building complete systems from ML backend to interactive frontend

---

## 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=MahateerMuhammad&show_icons=true&theme=dark&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=MahateerMuhammad&layout=compact&theme=dark&hide_border=true)

---

## 📫 Get in Touch

<!-- Update these with your actual contact information -->
- **Email**: mahateermuhammad100@gmail.com
- **LinkedIn**: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)
- **Twitter/X**: [@yourhandle](https://twitter.com/yourhandle)
- **Portfolio**: [Your Portfolio Website](https://yourportfolio.com)

---

*I'm always interested in healthcare AI, deep learning research, and building tools that make complex systems understandable. Feel free to reach out to discuss projects or collaborate!*
