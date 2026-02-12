<div align="center">

<img src="https://github.com/user-attachments/assets/4ef225e8-115c-44f9-8e01-a0d18f1f3397" alt="Resume photo" width="200" />

## KyongSeok Jang (장경석)  
📍 Seoul, Republic of Korea · 📧 wkdrudtjr95@gmail.com · 🔗 GitHub: https://github.com/rudjtr234  

**AI Research Engineer | Digital Pathology · Medical AI · Multimodal / RAG**
</div>

---

## 👋 About
- 🧠 AI engineer focused on deep learning and medical imaging, especially **digital pathology (WSI)**  
- 🧪 Passionate about building **clinically applicable** healthcare AI systems: mutation prediction + interpretability (heatmaps) + RAG/multimodal  
- 🛠️ Experienced with **Python / PyTorch / TensorFlow / Flask / Docker** for research-to-serving workflows  
- 🌱 Actively exploring **foundation models (UNI2-h)** and **vision-language models (LLaVA-Med, MedGemma)**  
- 📝 Interested in connecting research outcomes to **reproducible experiments (MLflow/Git)** and **technical documentation (final reports/patents)**

---

## 🧑‍💻 Experience
### AI Research Engineer  
**MTS Company, R&D BIO-DT (Development Team) – Seoul, Republic of Korea**  
*Jan 2025 – Present*

---

## 🧬 Projects / Research

### 1) Thyroid BRAF Mutation Prediction (Research Project)  
📅 *Oct 2025 – Present*  
- Developed an AI model to predict **BRAF V600E mutation** from thyroid H&E **WSI** (total **5,000 WSIs**)  
- Built an end-to-end pipeline: **WSI tiling → UNI2-h embeddings (1536-dim) → ABMIL (Attention-based MIL) classifier**  
- 5-Fold CV: **AUC 0.89 ± 0.04, F1 0.85 ± 0.05** (Bag size: 500–5000)  
- Designed an **attention heatmap visualization module** to highlight mutation-related tissue regions, improving interpretability and pathology-level trust  
- Operated experiments with **MLflow** and ensured reproducibility via **GitLab-based** workflows (versioning/params/metrics tracking)

---

### 2) Thyroid TERT Promoter Mutation Prediction (Research Project)  
📅 *Feb 2026 – Present*  
- Developed a **TERT promoter mutation** (Wild vs Mutant) prediction model using **200 thyroid H&E WSIs**  
- Pipeline: **WSI tiling → UNI2-h embeddings (1536-dim) → Gated ABMIL classifier**  
- Overlaid attention heatmaps on WSI thumbnails for **pathology-aware interpretability and reliability**  
- 5-Fold (Test, mean±std): **AUC 0.9699 ± 0.0217, F1 0.9312 ± 0.0221, Acc 0.9404 ± 0.0197**  
- Managed experiments and performance visualization with **MLflow** and GitLab

---

### 3) Internal LLM-RAG Pipeline Using Redmine/CRF Data  
📅 *Nov 2025 – Present*  
- Designed and implemented an internal RAG chatbot that enables **natural-language search** across Redmine knowledge (issues/wiki/experiment logs/commit history) and breast cancer CRF clinical data  
- Built ETL pipelines for automated collection/cleaning of unstructured data and created a **ChromaDB (Vector DB)** semantic index  
- Implemented hybrid routing to improve retrieval quality: **keyword-based fast routing + embedding similarity routing (threshold-based)**  
- Delivered an E2E flow: Web UI (Flask) → retrieval → context construction → response generation with **Gemini / Ollama**  
- Deployed with **Docker Compose + Gunicorn**, and designed an extensible ops structure for periodic sync/embedding (Kubernetes/Airflow-ready)

---

### 4) LNMP k-NN Retrieval (Research Project)  
📅 *Aug 2025 – Oct 2025*  
- Designed and implemented a retrieval algorithm to improve **lymph node metastasis prediction (LNMP)**  
- Applied **UNI2-h embeddings + FAISS k-NN**, using **τ=99.99% quantile threshold + 5-NN majority voting**  
- Achieved ~**6% specificity improvement** while maintaining recall (validated via experiments)

---

### 5) Tile-RAG for Pathology Report Automation (REG_2025 Challenge)  
📅 *Jun 2025 – Aug 2025*  
- Built a Tile-RAG workflow: **WSI tiling → UNI2-h embeddings → ChromaDB indexing → k-NN retrieval → caption/QA generation**  
- Trained a large-scale image–caption QA model for pathology report automation  
- Ranked **12th worldwide**, **3rd in Korea** (1st: SNU, 2nd: LG Electronics) in **REG_2025**

---

### 6) Multimodal AI Development (LLaVA-Med, MedGemma)  
📅 *Jan 2025 – May 2025*  
- Researched a vision-language pipeline combining pathology images and expert reports  
- Fine-tuned **LLaVA-Med / MedGemma** using internal pathology datasets  
- Implemented a prototype for **automated pathology report generation**

---

### 7) R&D Proposals and Technical Planning  
📅 *Jan 2025 – May 2025*  
- Wrote and presented **national R&D proposals**  
  - NIPA (Feb 2025)  
  - Jeonbuk Techno Park (May 2025)  
- Supported demo development and technical roadmap planning for an AI pathology platform

---

### 8) Final Reports and Patent Drafting  
📅 *Feb 2026 – Present*  
- Authored **final reports for national R&D projects**: dataset/model/validation, quantitative metrics (AUC/F1/Acc), experiment design, limitations/risks, and mitigation strategies  
- Linked deliverables to **MLflow/Redmine/GitLab** logs for traceability and audit-ready reproducibility  
- Supported **patent filing** in digital pathology AI: prior-art review (papers/patents), differentiation points, and drafting key specification sections (field, background, problems, solutions, effects, figures)

---

## 🎓 Education
**M.S. in Electrical Engineering – Kwangwoon University** (*Mar 2022 – Feb 2024*)  
- GPA: 4.5 / 4.5  
- Thesis: *Deep Learning-Based Device-Free Human Activity Recognition Using Wi-Fi CSI and FMCW Radar in Indoor Environments*  

**B.S. in Information & Communication Engineering – Wonkwang University** (*Mar 2017 – Feb 2021*)  
- GPA: 4.07 / 4.5  
- Awards: Wonkwang Honors Club, Creative Capstone Design Competition

---

## 🛠️ Skills & Tools
- **DL/ML:** PyTorch, TensorFlow, Scikit-learn  
- **Digital Pathology / CV:** WSI tiling, Feature Embedding (UNI2-h), Heatmap/Attribution, OpenSlide, Pillow  
- **RAG / Search:** ChromaDB, FAISS (k-NN), Retrieval pipeline design  
- **DevOps:** Linux, Conda, Docker, Flask, Git/GitLab, MLflow

---

## 📜 Certification
- Information & Communication Engineer (May 2022)

---

## 🏆 Awards
- Wonkwang Honors Club  
- Creative Capstone Design Competition Award

---

## 📝 Publications & Academic Activities
<details>
<summary><b>Show (SCI/SCIE · KCI · Conferences)</b></summary>

### International Journals (SCI / SCIE)
- *A Study on the Lightweight and Fast Response GRU Techniques for Indoor Continuous Motion Recognition Based on Wi-Fi CSI*, **IEEE Access** (2025)  
- *Human Activity Recognition Based on Continuous-Wave Radar and Bi-directional Gated Recurrent Units*, **Electronics** (2023)  
- *Intelligent Mesh Cluster Algorithm for Device-Free Localization in Wireless Sensor Networks*, **Electronics** (2023)  
- *Indoor Localization Based on Wi-Fi, Geomagnetic, and Light Sensors on Android Device Using DFF*, **Electronics** (2023)

### Domestic Journals (KCI)
- *Posture Estimation for Untrained Persons Using a 24GHz FMCW Radar and 2D CNN*, **Journal of the Korean Society of Disaster Information** (2023)  
- *Indoor Fall Detection Using Wi-Fi CSI and LSTM-Attention*, **Journal of the Korean Society of Disaster Information** (2024)

### Conference Papers
- Multiple presentations at the **Korean Society of Disaster Information** and **KICS**

</details>

---

## 🔗 Links
- GitHub Repos: https://github.com/rudjtr234?tab=repositories
