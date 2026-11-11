# 장경석 (KyongSeok Jang)

[English](https://github.com/rudjtr234/Profile/blob/main/README.md) · **한국어**

**AI Research Engineer | 디지털 병리 · 의료 AI · 멀티모달 / RAG**

서울 · wkdrudtjr95@gmail.com

[![GitHub](https://img.shields.io/badge/GitHub-rudjtr234-181717?style=flat&logo=github)](https://github.com/rudjtr234)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0002--0255--5512-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0002-0255-5512)
[![Google Scholar](https://img.shields.io/badge/Google_Scholar-4285F4?style=flat&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?hl=ko&user=AUUdyOAAAAA)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/%EA%B2%BD%EC%84%9D-%EC%9E%A5-9a8170373)
[![MTS](https://img.shields.io/badge/MTS_Company-000000?style=flat&logo=googlechrome&logoColor=white)](https://www.mtsco.co.kr/)

---

## 소개

딥러닝과 의료 영상, 특히 디지털 병리(WSI)를 다루는 AI 엔지니어입니다.
변이 예측, 해석 가능성(attention heatmap), RAG·멀티모달 파이프라인을 결합해 임상에 적용 가능한 헬스케어 AI 시스템을 만들고 있습니다.
Python / PyTorch / TensorFlow / Flask / Docker로 연구부터 서빙까지 이어지는 워크플로를 다룹니다.
병리 foundation model(UNI2-h, H-optimus-0/1, Hibou-L, Virchow/Virchow2, Midnight)과 vision-language model(LLaVA-Med, MedGemma)을 활용하고 있습니다.
재현 가능한 실험 관리(MLflow/Git)와 기술 문서화(최종보고서, 특허)에 관심이 많습니다.

---

## 경력

**AI Research Engineer**
MTS Company, R&D AI-DT팀 · 서울
2025.01 – 현재

---

## 프로젝트 및 연구

**갑상선 BRAF 변이 예측**
2025.10 – 현재 · [GitHub](https://github.com/rudjtr234/Thyroid_Mutation_Prediction_Model)

- 갑상선 H&E WSI(4,900장)에서 BRAF V600E 변이를 예측하는 AI 모델 개발
- 파이프라인: WSI 타일링 → 병리 foundation model 임베딩(UNI2-h / H-optimus-0 / H-optimus-1 / Hibou-L, Virchow2 / GenBio-PathFM으로 확장 중) → MIL 분류기
- Multi-MIL model zoo(ABMIL / CLAM-SB / DSMIL / ACMIL / TransMIL)와 5-model 확률 평균 앙상블 구축
- **내부 테스트: AUC 0.9286, Acc 0.8550** (ABMIL 앙상블, H-optimus-0 40x)
- **TCGA-THCA 외부검증(498 WSI): AUC 0.8492** — 앙상블로 단일 최고 모델 대비 일반화 성능 +0.041 AUC 향상
- 같은 타일·같은 fold로 인코더 비교: 내부 CV 차이는 0.03 AUC 이내였지만 TCGA 외부검증 AUC는 0.06~0.15 벌어짐 → bootstrap CI를 포함한 외부검증을 인코더 선택의 1차 기준으로 설정
- 타일 임베딩 1억 800만 개 이상 추출, 사전 타일링한 PNG 대신 WSI를 직접 읽어 추출 시간 약 4배 단축(NFS I/O 병목 해소)
- 혼종 GPU 서버용 장애 내성 DDP 추출 파이프라인 구축(처리량 가중 분배, GPU별 배치 크기, resume 기반 자동 재시작)
- 변이 관련 조직 영역을 강조하는 attention heatmap 시각화 설계
- MLflow와 GitLab으로 실험 재현성 관리

**갑상선 TERT promoter 변이 예측**
2026.02 – 현재 · [GitHub](https://github.com/rudjtr234/Thyroid_TERT_Mutation_Model)

- 갑상선 H&E WSI 201장(Wild 113 / C228T 69 / C250T 19)으로 TERT promoter 변이 예측 모델 개발
- 파이프라인: WSI 타일링 → UNI2-h / H-optimus-0/1 / Hibou-L foundation model 임베딩 → Gated ABMIL 분류기
- **5-Fold CV (2-class, Wild vs Mutant): 최고 AUC 0.9716** (H-optimus-0 + ABMIL) · **최고 F1 0.9312 / Acc 0.9404** (UNI2-h + ABMIL)
- MIL 아키텍처 6종(ABMIL / TransMIL / ACMIL / DTFD / MHIM / CLAM)을 인코더 4종·배율 2종에 걸쳐 벤치마크
- 모델 선택 편향 정량화: test AUC로 run을 고르면 validation 기준 선택보다 평균 +0.013 AUC 부풀려짐 — 인코더 간 차이(0.010)보다 큼 → validation 기준 선택, fold별 CI, 유의성 검정 중심으로 평가 체계 재설계 중
- 변이 아형 구분을 위해 3-class 분류(Wild / C228T / C250T)로 확장
- 하이퍼파라미터 스윕 병렬화를 위한 멀티 GPU 스윕 도구 구축(GPU별 run 큐, 덮어쓰기 방지, GPU 번호 고정)
- WSI 썸네일 위에 attention heatmap을 겹쳐 병리학적 해석 가능성 확보

**위 생검 Updated Sydney System 등급 예측**
2026.10 – 현재 · [GitHub](https://github.com/rudjtr234/sydney_public)

- 위 생검 H&E WSI(998사례 / 1,002장)에서 Updated Sydney System 5개 항목(H. pylori, 호중구, 단핵구, 위축, 장상피화생; 등급 0~3)을 동시에 예측하는 multi-task MIL 모델 개발
- 파이프라인: iSyntax → TIFF 변환 → TRIDENT 조직 분할·패치 추출 → foundation model 4종(Hibou-L / H-optimus-0 / Virchow / Midnight-12k) 임베딩, 10x / 20x / 40x → multi-task attention MIL
- SydneyMTL 재구현(shared adaptor, 항목별 attention head, logit-adjusted cross entropy) 및 생검 부위 입력 확장(logit 보정 / FiLM)
- **5-fold CV: 평균 QWK 0.602** (H-optimus-0, 20x) · 장상피화생 QWK 0.902
- 인코더 4종 × 배율 3종을 같은 fold로 비교: 평균 QWK는 0.575~0.608 안에 머문 반면 항목 간 난이도 차이가 훨씬 큼(20x 기준 위축 0.27~0.34 vs 장상피화생 0.88~0.90)
- 위축 오류의 원인을 생검 부위가 아닌 2·3등급 경계에서 찾음 — 부위 입력은 일관된 개선이 없어 다음 단계로 순서형(ordinal) 손실 설정
- 드문 등급을 fold마다 균등 배분하는 다중 라벨 iterative stratification 구현, 설정·라벨·코드 hash가 다르면 실행을 거부하는 버전 관리(MLflow 자동 기록)

**사내 LLM-RAG 파이프라인 (Redmine / CRF 데이터)**
2025.11 – 현재 · [GitHub](https://github.com/rudjtr234/redmine_RAG)

- Redmine 지식(이슈, 위키, 실험 로그, 커밋 이력)과 유방암 CRF 임상 데이터를 자연어로 검색하는 사내 RAG 챗봇 설계·구현
- 데이터 자동 수집·정제 ETL 파이프라인 구축, ChromaDB 의미 검색 인덱스 생성
- 하이브리드 라우팅: 키워드 기반 빠른 라우팅 + 임베딩 유사도 라우팅
- E2E 흐름: Flask Web UI → 검색 → 컨텍스트 구성 → Gemini / Ollama 응답 생성
- Docker Compose + Gunicorn으로 배포, Kubernetes/Airflow로 확장 가능한 구조 설계

**병리 보고서 자동화를 위한 Tile-RAG (REG_2025 Challenge)**
2025.06 – 2025.08

- Tile-RAG 워크플로 구축: WSI 타일링 → UNI2-h 임베딩 → ChromaDB 인덱싱 → k-NN 검색 → 캡션/QA 생성
- 병리 보고서 자동화를 위한 대규모 이미지–캡션 QA 모델 학습
- 전 세계 12위, 국내 3위 (1위 서울대, 2위 LG전자)

**R&D 제안 및 기술 기획**
2025.01 – 2025.05

- 국가 R&D 과제 제안서 작성 및 발표: NIPA (2025.02), 전북테크노파크 (2025.05)
- AI 병리 플랫폼 데모 개발과 기술 로드맵 수립 지원

**최종보고서 및 특허 작성**
2026.02 – 현재

- 국가 R&D 과제 최종보고서 작성: 데이터셋·모델·검증, 정량 지표(AUC/F1/Acc), 실험 설계, 한계와 보완 방안
- 산출물을 MLflow/Redmine/GitLab 기록과 연결해 추적성과 감사 대응 가능한 재현성 확보
- 디지털 병리 AI 특허 4건 출원을 대표 발명자로 주도: 선행기술 조사, 차별성 분석, 명세서 핵심부 작성 (아래 특허 참고)

---

## 특허

4건 모두 **대표 발명자**로 출원했으며, MIL 신뢰성, 불확실성 기반 의사결정 정책, 생성형 병리를 다룹니다.

**불확실성 기반 의사결정 정책을 적용한 계층적 MIL 유전자 변이 예측**
2026.09 출원 · KR 10-2026-0180304 (심사 중)

- 변이 유무를 먼저 예측하고, 보정된 확률이 기준을 넘을 때만 hotspot 아형(예: TERT C228T / C250T)으로 분기하며, 엔트로피나 마진이 불안정하면 *아형 불확실*로 판정 보류
- 아형별 adversarial 가중치를 둔 gradient-reversal layer로 동반 변이에 대한 shortcut 학습을 억제해 외부 코호트 일반화 향상

**Attention 합의 기반 동적 앙상블을 이용한 바이오마커 예측**
2026.09 출원 · KR 10-2026-0180301 (심사 중)

- 출력 확률을 단순 평균하는 대신, attention map이 얼마나 일치하는지에 따라 앙상블 모델에 가중치를 부여해 같은 조직 영역에 근거한 모델이 결정을 주도하도록 설계
- 불확실한 슬라이드에서만 모델 간 의견이 갈리는 타일을 골라 선택적으로 재추론(전체 재추론 대비 연산량 약 18% 절감)

**시계열 슬라이드와 약물 조건으로 미래 시점의 가상 병리 슬라이드 생성**
2026.05 출원 · KR 10-2026-0084848 (심사 중)

- foundation model 타일 임베딩에 시간·약물 조건 벡터(Temporal Transformer / TCN, cross-attention)를 조건으로 주는 latent diffusion model
- 약물 투여 계획을 바꿨을 때의 조직 반응을 반사실적으로 시뮬레이션하고, 변화 heatmap과 샘플링 분산 기반 불확실성 제공

**저배율 유도 패치 중요도를 이용한 다중 배율 MIL 예측**
2026.04 출원 · KR 10-2026-0066206 (심사 중)

- 저배율 구조 특징을 고배율 패치 좌표계로 매핑해 MIL attention을 동적으로 재가중하고 정보가 없는 타일을 건너뜀
- 배율 간 예측 불일치를 감지해 신뢰도 강화 정책(gating 재조정, 추가 패치 샘플링, 검토 플래그) 적용

*출원인: MTS Company. 심사 중이며 명세서는 아직 공개 전입니다.*

---

## 학력

**광운대학교 전기공학과 석사** (2022.03 – 2024.02)
학점: 4.5 / 4.5
학위논문: Deep Learning-Based Device-Free Human Activity Recognition Using Wi-Fi CSI and FMCW Radar in Indoor Environments

**원광대학교 정보통신공학과 학사** (2017.03 – 2021.02)
학점: 4.07 / 4.5
수상: Wonkwang Honors Club, 창의 캡스톤디자인 경진대회

---

## 기술 스택

**딥러닝 / ML**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)

**디지털 병리 / CV**

![OpenSlide](https://img.shields.io/badge/OpenSlide-4CAF50?style=flat)
![UNI2-h](https://img.shields.io/badge/UNI2--h-8E75B2?style=flat)
![H-optimus](https://img.shields.io/badge/H--optimus--0%2F1-6A4C93?style=flat)
![TRIDENT](https://img.shields.io/badge/TRIDENT-5C6BC0?style=flat)
![MIL](https://img.shields.io/badge/Multiple_Instance_Learning-2E7D32?style=flat)

**RAG / 검색**

![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat)
![FAISS](https://img.shields.io/badge/FAISS-0694E2?style=flat)

**MLOps / DevOps**

![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-FC6D26?style=flat&logo=gitlab&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

---

## 자격증

- 정보통신기사 (2022.05)

## 수상

- Wonkwang Honors Club
- 창의 캡스톤디자인 경진대회 수상
- REG_2025 Challenge — 전 세계 12위, 국내 3위
