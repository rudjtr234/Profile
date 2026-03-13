# KyongSeok Jang (장경석)

**AI Research Engineer | Digital Pathology · Medical AI · Multimodal / RAG**

Seoul, Republic of Korea · wkdrudtjr95@gmail.com

[![GitHub](https://img.shields.io/badge/GitHub-rudjtr234-181717?style=flat&logo=github)](https://github.com/rudjtr234)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0002--0255--5512-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0002-0255-5512)
[![Google Scholar](https://img.shields.io/badge/Google_Scholar-4285F4?style=flat&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?hl=ko&user=AUUdyOAAAAA)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/%EA%B2%BD%EC%84%9D-%EC%9E%A5-9a8170373)
[![MTS](https://img.shields.io/badge/MTS_Company-000000?style=flat&logo=googlechrome&logoColor=white)](https://www.mtsco.co.kr/)

---

## About

AI engineer focused on deep learning and medical imaging, especially digital pathology (WSI).
Building clinically applicable healthcare AI systems that integrate mutation prediction, interpretability (attention heatmaps), and RAG/multimodal pipelines.
Experienced with Python / PyTorch / TensorFlow / Flask / Docker for research-to-serving workflows.
Actively exploring foundation models (UNI2-h) and vision-language models (LLaVA-Med, MedGemma).
Interested in reproducible experiment management (MLflow/Git) and technical documentation (final reports, patents).

---

## Experience

**AI Research Engineer**
MTS Company, R&D BIO-DT · Seoul
Jan 2025 – Present

---

## Projects & Research

**Thyroid BRAF Mutation Prediction**
Oct 2025 – Present · [GitHub](https://github.com/rudjtr234/Thyroid_Mutation_Prediction_Model)

- Developed an AI model to predict BRAF V600E mutation from thyroid H&E WSI (5,000 slides)
- Pipeline: WSI tiling → UNI2-h embeddings (1536-dim) → ABMIL classifier
- 5-Fold CV: AUC 0.89 ± 0.04, F1 0.85 ± 0.05 (Bag size: 500–5,000)
- Designed attention heatmap visualization to highlight mutation-related tissue regions
- Managed experiments with MLflow and GitLab for reproducibility

**Thyroid TERT Promoter Mutation Prediction**
Feb 2026 – Present · [GitHub](https://github.com/rudjtr234/Thyroid_TERT_Mutation_Model)

- Developed TERT promoter mutation (Wild vs Mutant) prediction model using 200 thyroid H&E WSIs
- Pipeline: WSI tiling → UNI2-h embeddings (1536-dim) → Gated ABMIL classifier
- 5-Fold CV: AUC 0.9699 ± 0.0217, F1 0.9312 ± 0.0221, Acc 0.9404 ± 0.0197
- Overlaid attention heatmaps on WSI thumbnails for pathology-aware interpretability

**Internal LLM-RAG Pipeline (Redmine / CRF Data)**
Nov 2025 – Present · [GitHub](https://github.com/rudjtr234/redmine_RAG)

- Designed and implemented an internal RAG chatbot for natural-language search across Redmine knowledge (issues, wiki, experiment logs, commit history) and breast cancer CRF clinical data
- Built ETL pipelines for automated data collection and cleaning; created ChromaDB semantic index
- Hybrid routing strategy: keyword-based fast routing + embedding similarity routing
- E2E flow: Flask Web UI → retrieval → context construction → response generation via Gemini / Ollama
- Deployed with Docker Compose + Gunicorn; designed Kubernetes/Airflow-ready extensible architecture

**Tile-RAG for Pathology Report Automation (REG_2025 Challenge)**
Jun 2025 – Aug 2025

- Built a Tile-RAG workflow: WSI tiling → UNI2-h embeddings → ChromaDB indexing → k-NN retrieval → caption/QA generation
- Trained a large-scale image–caption QA model for pathology report automation
- Ranked 12th worldwide, 3rd in Korea (1st: SNU, 2nd: LG Electronics)


**R&D Proposals and Technical Planning**
Jan 2025 – May 2025

- Wrote and presented national R&D proposals: NIPA (Feb 2025), Jeonbuk Techno Park (May 2025)
- Supported demo development and technical roadmap planning for an AI pathology platform

**Final Reports and Patent Drafting**
Feb 2026 – Present

- Authored final reports for national R&D projects: dataset/model/validation, quantitative metrics (AUC/F1/Acc), experiment design, limitations and mitigation strategies
- Linked deliverables to MLflow/Redmine/GitLab logs for traceability and audit-ready reproducibility
- Supported patent filing in digital pathology AI: prior-art review, differentiation points, and drafting key specification sections

---

## Education

**M.S. in Electrical Engineering — Kwangwoon University** (Mar 2022 – Feb 2024)
GPA: 4.5 / 4.5
Thesis: Deep Learning-Based Device-Free Human Activity Recognition Using Wi-Fi CSI and FMCW Radar in Indoor Environments

**B.S. in Information & Communication Engineering — Wonkwang University** (Mar 2017 – Feb 2021)
GPA: 4.07 / 4.5
Awards: Wonkwang Honors Club, Creative Capstone Design Competition

---

## Skills

**Deep Learning / ML**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)

**Digital Pathology / CV**

![OpenSlide](https://img.shields.io/badge/OpenSlide-4CAF50?style=flat)
![UNI2-h](https://img.shields.io/badge/UNI2--h_Embedding-8E75B2?style=flat)

**RAG / Search**

![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat)
![FAISS](https://img.shields.io/badge/FAISS-0694E2?style=flat)

**MLOps / DevOps**

![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-FC6D26?style=flat&logo=gitlab&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

---

## Certification

- Information & Communication Engineer (May 2022)

## Awards

- Wonkwang Honors Club
- Creative Capstone Design Competition Award
- REG_2025 Challenge — 12th worldwide, 3rd in Korea

---

## GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=rudjtr234&show_icons=true&theme=default&hide_border=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=rudjtr234&layout=compact&hide_border=true)
