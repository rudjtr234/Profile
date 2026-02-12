<div align="center">

<img src="https://github.com/user-attachments/assets/4ef225e8-115c-44f9-8e01-a0d18f1f3397" alt="이력서 사진" width="200" />

## 장경석 (Jang KyongSeok)  
📍 서울, 대한민국 · 📧 wkdrudtjr95@gmail.com · 🔗 GitHub: https://github.com/rudjtr234  

**AI Research Engineer | Digital Pathology · Medical AI · Multimodal / RAG**
</div>

---

## 👋 소개
- 🧠 딥러닝 및 의료영상(특히 디지털 병리 WSI) 분석 중심의 AI 개발자  
- 🧪 실제 의료 현장 적용을 목표로 **WSI 기반 변이 예측·해석(heatmap)** 및 **RAG/멀티모달** 시스템 개발  
- 🛠️ Python / PyTorch / TensorFlow / Flask / Docker 기반 실험·서빙 환경 구축 경험  
- 🌱 Foundation Model(UNI2-h)·Vision-Language 모델(LLaVA-Med, MedGemma) 지속 연구  
- 📝 연구 결과를 **재현성(MLflow·Git)** 및 **문서화(보고서·특허)**까지 연결하는 업무를 선호

---

## 🧑‍💻 경력
### AI Research Engineer  
**MTS Company, R&D BIO-DT (Development Team) – 서울, 대한민국**  
*2025년 1월 – 현재*

---

## 🧬 프로젝트 / 연구

### 1) 갑상선 BRAF 변이 예측 모델 (연구 프로젝트)  
📅 *2025년 10월 ~ 진행 중*  
- 갑상선 H&E WSI 기반 **BRAF V600E 변이 여부 예측** 모델 개발 (총 **5,000장** WSI)  
- 파이프라인: **WSI 타일링 → UNI2-h 임베딩(1536-dim) → ABMIL(Attention MIL) 분류**  
- 5-Fold CV: **AUC 0.89 ± 0.04, F1 0.85 ± 0.05** (Bag size: 500–5000)  
- **Attention Heatmap 시각화 모듈** 설계로 변이 연관 조직 영역 해석 가능성 및 신뢰도 강화  
- **MLflow 기반 실험 관리 + GitLab 기반 재현성 운영**(버전/파라미터/성능 추적)

---

### 2) 갑상선 TERT promoter 변이 예측 모델 (연구 프로젝트)  
📅 *2026년 2월 ~ 진행 중*  
- Thyroid H&E WSI **200장** 기반 **TERT promoter mutation(Wild vs Mutant)** 예측 모델 개발  
- 파이프라인: **WSI 타일링 → UNI2-h 임베딩(1536-dim) → Gated ABMIL 분류**  
- Heatmap을 WSI 썸네일에 오버레이하여 **병리적 해석 가능성 및 신뢰도 강화**  
- 5-Fold(Test, 평균±표준편차): **AUC 0.9699 ± 0.0217, F1 0.9312 ± 0.0221, Acc 0.9404 ± 0.0197**  
- MLflow 기반 실험 관리 및 성능 시각화 파이프라인 운영

---

### 3) 사내 데이터(Redmine/CRF) 기반 LLM-RAG 파이프라인 구현  
📅 *2025년 11월 ~ 현재*  
- Redmine(이슈/위키/실험로그/커밋 기록) + CRF 유방암 임상 데이터를 **자연어로 통합 검색**하는 사내 RAG 챗봇 설계·구현  
- ETL: 비정형 데이터 자동 수집·정제 → **ChromaDB(Vector DB) 인덱싱** 구성  
- 라우팅: **키워드 기반 빠른 라우팅 + 벡터 유사도 기반 라우팅(threshold) 결합**으로 검색 정확도/일관성 향상  
- E2E: Web UI(Flask) → Retrieval → Context 구성 → **Gemini / Ollama 응답 생성**까지 연결  
- 운영 확장: Docker Compose·Gunicorn 배포, (확장 가능 형태로) Kubernetes·Airflow 기반 주기적 동기화/임베딩 자동화 구조 설계

---

### 4) LNMP KNN Retrieval (연구 프로젝트)  
📅 *2025년 8월 ~ 10월*  
- 림프절 전이 예측(LNMP) 성능 개선을 위한 **FAISS k-NN 검색 기반 Retrieval 알고리즘** 설계·구현  
- **UNI2-h 임베딩 + τ=99.99% 분위수 임계값 + 5-NN 다수결 투표** 적용  
- 재현율 유지 조건에서 **특이도 약 6% 향상**(실험 기반 검증)

---

### 5) Tile-RAG 병리 리포트 자동화 (REG_2025 챌린지)  
📅 *2025년 6월 ~ 8월*  
- 워크플로우: **WSI 타일링 → UNI2-h 임베딩 → ChromaDB 인덱싱 → k-NN 검색 → 캡션/QA 생성**  
- 대규모 이미지–캡션 QA 모델 구축 및 학습  
- **REG_2025 국제 대회 세계 12위, 국내 3위(1위 서울대, 2위 LG전자)** 달성

---

### 6) 멀티모달 AI 개발 (LLaVA-Med, MedGemma)  
📅 *2025년 1월 ~ 5월*  
- 병리 이미지 + 전문가 리포트를 결합한 **Vision-Language 파이프라인 연구**  
- 내부 데이터셋 기반 **LLaVA-Med / MedGemma 파인튜닝** 및 보고서 자동 생성 프로토타입 구현

---

### 7) 연구개발 제안서 및 기술 기획  
📅 *2025년 1월 ~ 5월*  
- 국가 연구개발 제안서 작성 및 발표  
  - NIPA (2025년 2월)  
  - 전북테크노파크 (2025년 5월)  
- AI 병리 플랫폼 데모 시스템 제작 및 기술 로드맵 수립 지원

---

### 8) 과제 최종 보고서 작성 및 특허 작성  
📅 *2026년 2월 ~*  
- 국가 R&D 과제 **최종보고서 문서화**: 데이터/모델/검증, 정량 지표(AUC/F1/Acc), 실험설계, 한계·리스크 및 대응전략 정리  
- MLflow/Redmine/GitLab 기록과 연계하여 **근거 추적(Traceability) 및 재현성 중심** 보고서 구성  
- 디지털 병리 AI **특허 출원 지원**: 선행기술 조사(논문/특허), 차별점 정의, 명세서 핵심 섹션(기술분야/배경기술/해결과제/해결수단/효과/도면설명) 초안 작성

---

## 🎓 학력
**전자공학 석사 (M.S.) – 광운대학교 대학원** (*2022.03 – 2024.02*)  
- GPA: 4.5 / 4.5  
- 학위논문: *Wi-Fi CSI 및 FMCW 레이더 기반 딥러닝 실내 인간 활동 인식*  

**정보통신공학 학사 (B.S.) – 원광대학교** (*2017.03 – 2021.02*)  
- GPA: 4.07 / 4.5  
- 수상: Wonkwang Honors Club, 창의 캡스톤 디자인 경진대회 수상

---

## 🛠️ 기술 및 도구
- **DL/ML:** PyTorch, TensorFlow, Scikit-learn  
- **Digital Pathology / CV:** WSI tiling, Feature Embedding(UNI2-h), Heatmap/Attribution, OpenSlide, Pillow  
- **RAG / Search:** ChromaDB, FAISS(k-NN), Retrieval 파이프라인 설계  
- **DevOps:** Linux, Conda, Docker, Flask, Git/GitLab, MLflow

---

## 📜 자격증
- 정보통신기사 (2022.05)

---

## 🏆 수상
- Wonkwang Honors Club  
- 창의 캡스톤 디자인 경진대회 수상

---

## 📝 논문 및 학술 활동
<details>
<summary><b>펼쳐보기 (SCI/SCIE · KCI · 학술대회)</b></summary>

### 국제 학술지 (SCI / SCIE)
- *A Study on the Lightweight and Fast Response GRU Techniques for Indoor Continuous Motion Recognition Based on Wi-Fi CSI*, **IEEE Access** (2025)  
- *Human Activity Recognition Based on Continuous-Wave Radar and Bi-directional Gated Recurrent Units*, **Electronics** (2023)  
- *Intelligent Mesh Cluster Algorithm for Device-Free Localization in Wireless Sensor Networks*, **Electronics** (2023)  
- *Indoor Localization Based on Wi-Fi, Geomagnetic, and Light Sensors on Android Device Using DFF*, **Electronics** (2023)

### 국내 학술지 (KCI)
- *Posture Estimation for Untrained Persons Using a 24GHz FMCW Radar and 2D CNN*, **한국재난정보학회지** (2023)  
- *Indoor Fall Detection Using Wi-Fi CSI and LSTM-Attention*, **한국재난정보학회지** (2024)

### 학술대회 발표
- **한국재난정보학회**, **한국통신학회** 다수 발표

</details>

---

## 🔗 링크
- GitHub Repos: https://github.com/rudjtr234?tab=repositories
