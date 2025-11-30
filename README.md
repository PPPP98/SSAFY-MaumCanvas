# Maum Canvas

## 1. 서비스 소개

<div align="center">

![Maum Canvas](./docs/image/maum.png)

</div>

## 그림을 통해 당신의 마음을 표현하세요

> ## 마음 캔버스 프로젝트는
>
> 청소년이 스스로를 돌보고 이해하는 것을 돕기 위해 만들었습니다. 현재 우리나라 소아 및 청소년의 정신 장애 유병률은 16.1%로 높은 수치이며, 꾸준히 증가하고 있는 추세입니다. 하지만 부정적 인식, 이용 비용 및 치료 기관을 찾는데에 어려움이 있어 치료로 이어지기는 어려운 현실입니다. 이러한 점을 해소하기 위해 온라인 서비스로 화상 상담과 자가 그림진단을 진행할 수 있는 서비스를 만들었습니다.

- **개발 기간** : 2025.07.02 ~ 2025.08.14 **(6주)**
- **플랫폼** : Web & App(PWA)
- **개발 인원** : 5명 <br>

## 2. 핵심 차별점

### 🎨 AI 기반 HTP 그림 검사 자동화

기존 HTP 검사는 상담사의 경험에 의존하여 시간이 오래 걸리고 주관적 해석 가능성이 있었습니다.  
**Maum Canvas는 AI 기술로 이 문제를 해결했습니다.**

#### 기술적 성과
- **검색 정확도 Recall 0.9** - 정보 누락 최소화  
- **논문 기반 객관성** - Buck(1948), Hammer(1968) 등 검증된 임상 자료 활용  
- **비용 효율성 90% 개선** - Advanced RAG로 잘못된 입력 처리 최적화  
- **상담사 시간 단축** - 자동 검색으로 해석 시간 대폭 감소

#### 작동 원리
1️⃣ 그림 입력<br>
2️⃣ YOLO 객체 탐지<br>
3️⃣ 상담사 관찰 입력<br>
4️⃣ RAG 검색 (FAISS + Ensemble)<br>
5️⃣ LLM 해석 생성<br>
6️⃣ 논문 기반 결과 제공<br>

### 📄 **상세 기술 문서**  
<div style="font-size:24px;">

[AI RAG Pipeline 구축](./docs/HTP%20검사%20해석%20RAG%20pipeline구축.pdf)  
[AI RAG 최종 평가](./docs/HTP%20검사%20해석%20RAG%20최종%20평가.pdf)

</div>

## 3. 기술 스택

- **Backend** :  
  ![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white)
  ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
  ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
  ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
  ![YOLOv5](https://img.shields.io/badge/YOLOv5-00FFFF?style=for-the-badge&logo=opencv&logoColor=black)
  ![LangGraph](https://img.shields.io/badge/LangGraph-1D3D3C?style=for-the-badge&logo=langgraph&logoColor=white)
  ![LangChain](https://img.shields.io/badge/LangChain-1D3D3C?style=for-the-badge&logo=langchain&logoColor=white)

- **FrontEnd** :  
  ![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
  ![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
  ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)

- **DB** :  
  ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
  ![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
  ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
  
- **INFRA** :  
  ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
  ![AWS EC2](https://img.shields.io/badge/AWS%20EC2-FF9900?style=for-the-badge&logo=amazon-ec2&logoColor=white)
  ![Gerrit](https://img.shields.io/badge/Gerrit-EEEEEE?style=for-the-badge&logo=gerrit&logoColor=black)
  ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
  ![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white)
  ![Certbot](https://img.shields.io/badge/Certbot-003A70?style=for-the-badge&logo=letsencrypt&logoColor=white)

## 4. 주요 기능

1. **그림 검사**
   - **YOLOv5 객체 탐지** + **RAG Pipeline**으로 해석 자동화
   - 상담사 관찰 보조 + 논문 기반 객관적 해석 제공
   - **검색 정확도 Recall 0.9** 달성
2. **WebRTC 통한 온라인 상담**
   - 이전 검사 및 상담 내역을 상담사가 확인할 수 있도록 하여 피상담자의 특징을 활용하 상담 가능
3. **예약 및 상담 내역**
   - 이전 검사 및 상담 내역, 예약 상담 내역 모두 제공하여 지속적인 상담 및 심리 건강 관리에 도움
4. **커뮤니티**
   - 권한 구분하여 또래들부터 상담사와의 커뮤니티까지 다양한 분류의 커뮤니티 제공

## 5. 배포

### porting manual

[실행 및 배포하러가기!](./exec/porting_manual.md)

## 6. 시스템 아키텍처

![아키텍쳐 구조](./docs/image/Maum%20Canvas.png)

![ERD](./docs/E108_마음캔버스ERD.png)

<div style="font-size:24px">

[CI/CD 구성](./docs/CICD_산출물.pdf)  
[API 및 기능 명세](./docs/E108_마음%20캔버스%20API%20명세서.pdf)

</div>

## 7. 팀 소개

|팀원|담당|주요 업무|
|---|---|---|
|유정석|INFRA|CI/CD|
|전재욱|BE|API 개발|
|김현서|BE,AI|API 개발, PPT, AI 모델|
|노혜성|FE|FE 개발|
|박진호|BE, AI|BE 개발, AI 모델, 디자인|


## 8. 미리보기

![온보딩페이지](./docs/image/onboarding.png)  
![메인페이지](./docs/image/counselor.png)  
![그림진단1](./docs/image/art.png)  
![그림진단2](./docs/image/art_2.png)  
![상담예약](./docs/image/reserve.png)  
![온라인상담](./docs/image/webrtc.png)  
![커뮤니티](./docs/image/community.png)  

## 9. 프로젝트 회고

### 역할 : 그림 해석 pipeline 설계 및 구현 


<details>
<summary style="font-size:24px;">프로젝트 진행 개인 회고</summary>
<div>

### 그림 해석 자동화

HTP(House-Tree-Person) 심리 검사는 1948년 J.N. Buck에 의해 개발된 투사적 심리검사로, 그림을 통해 내담자의 내적 심리를 분석합니다. 특히 새로운 환경에 대한 불안으로 위축된 내담자들이 언어보다 그림을 통해 더 솔직하게 자신의 감정을 표현할 수 있다는 장점이 있습니다.

그러나 전문 상담사의 경험과 관찰에 크게 의존하는 해석 과정은 시간이 많이 소요되고, 상담사의 주관이 개입될 수 있다는 한계가 있습니다. 이에 AI 기술을 활용하여 접근성을 높이고 해석의 객관성을 확보하는 자동화 파이프라인을 고안하게 되었습니다.

## 프로젝트 회고

### 1. 그림 해석 자동화 파이프라인 설계

**초기 목표**: 객체 탐지만으로 그림 완전 자동 해석  
**전환 결정**: 상담사 보조 도구로 방향 재설정

#### 문제 인식
- HTP 검사는 선의 굵기, 강조 지점 등 미묘한 특징의 정량화가 어려움
- 검사 대상자의 배경, 태도 등 맥락 정보가 필수적
- 임상 실험 기반 검사로 상담사의 경험과 주관이 필수 개입

#### 최종 설계
**YOLO 객체 탐지 → 상담사 관찰 입력 → RAG 검색 → LLM 해석 생성**

객체 탐지로 관찰 포인트를 제시하고, 상담사가 검증 및 추가 정보를 입력하면 논문 기반 해석을 제공하는 구조로 **접근성과 신뢰성을 동시에 확보**했습니다.

***

### 2. 데이터 구축: 의미론적 청킹 실험

**가설**: 단순 사이즈 청킹은 질문-답변 간 의미적 연결이 약해져 검색 성능 저하

#### 실험 방법
- Buck(1948), Hammer(1968) 등 검증된 논문에서 임상 해석 정보만 발췌
- 의미가 변화하는 지점(집/나무/사람, 문/창문 등)을 수작업으로 구분
- 메타데이터 부여: `main_component`, `sub_component` 등

#### 결과
✅ **노이즈 최소화**: 해석 정보만 압축하여 문서량 대폭 감소  
✅ **정확한 매칭**: 메타데이터 활용으로 검색 정확도 향상  
⚠️ **시간 소모**: 수작업으로 인한 후속 작업(평가, 프롬프트) 압박

***

### 3. 검색 성능 최적화 실험

**목표**: 재현율(Recall) 0.9 이상 달성 (정보 누락 최소화)  
**평가 도구**: RAGAs 프레임워크 (Context Precision, Recall)

#### 실험 1: VectorDB 비교 (FAISS vs ChromaDB)

| VectorDB | Retriever | K | Precision | Recall |
|----------|-----------|---|-----------|--------|
| FAISS | Similarity | 3 | 0.9680 | 0.8097 |
| ChromaDB | Similarity | 3 | 0.9845 | 0.8440 |
| FAISS | Ensemble | 3 | 0.9503 | 0.8614 |
| ChromaDB | Ensemble | 3 | 0.9613 | 0.8585 |
| **FAISS** | **Ensemble** | **5** | **0.9424** | **0.8959** |

**결론**: FAISS + Ensemble (K=5)에서 Recall 0.9에 가장 근접

#### 실험 2: Retriever 알고리즘 비교

Dense 검색 (Similarity, MMR), Sparse 검색 (BM25), Hybrid (Ensemble) 비교

**결과**: Ensemble이 단일 알고리즘 대비 Recall 최고 성능

#### 실험 3: Ensemble 가중치 최적화

| BM25 가중치 | Similarity 가중치 | Precision | Recall |
|-------------|-------------------|-----------|--------|
| **0.3** | **0.7** | **0.9672** | **0.8653** |
| 0.5 | 0.5 | 0.9535 | 0.8601 |
| 0.7 | 0.3 | 0.9542 | 0.8459 |

**결론**: BM25:0.3, Similarity:0.7 조합이 최적 (K=3)

#### 실험 4: Rerank 전략 (CrossEncoder)

**가설**: 많은 후보(K=10)에서 Reranking하면 Recall 향상

| 방법 | K/top_n | Precision | Recall | 시간 |
|------|---------|-----------|--------|------|
| Ensemble | 3/- | 0.9680 | 0.8446 | 150s |
| Rerank | 10/3 | 0.9855 | 0.8295 | 525s |

**결론**: CPU 환경에서 시간 3.5배 증가, Recall 오히려 하락 → **미적용**  
**원인**: top_n=3으로 축소하며 좋은 후보 일부 누락

#### 최종 선택
**FAISS + Ensemble (BM25:0.3, Similarity:0.7, K=3)**  
메타데이터 활용 및 임베딩 모델 업그레이드로 **Recall 0.9 달성**

***

### 4. Naive RAG vs Advanced RAG 비교 실험

**문제**: Langchain 기반 Naive RAG는 잘못된 질문에도 항상 검색-생성 수행

#### 실험 설정
- **공통**: GPT-4o-mini, 동일 프롬프트, Ensemble Retriever
- **정상 질문**: "집에 창문은 2개 존재하고 크기는 적절함. 문은 집의 크기에 비해 작으며..."
- **잘못된 질문**: "오늘의 날씨는? 대한민국의 수도는? 최근 야구 경기 결과는?"

#### 실험 1: 지연시간 (Latency) 비교

|  | Naive RAG | Advanced RAG |
|---|-----------|--------------|
| **정상 질문** | 22초 | 23초 |
| **잘못된 질문** | 22초 | 0.7초 |

**결론**: 정상 질문은 유사, 잘못된 질문 처리 시간 **97% 단축**

#### 실험 2: 비용 (Cost) 비교

|  | Naive RAG | Advanced RAG |
|---|-----------|--------------|
| **정상 질문** | 10 credit | 16 credit |
| **잘못된 질문** | 10 credit | 1 credit |

**결론**: 
- 정상 질문 시 분기마다 2~3 credit 선형 증가
- 잘못된 질문 시 Relevance Check만 수행하여 **90% 비용 절감**

#### 최적화: 그래프 가지치기

Hallucination/Relevance 검사 중복 제거 → **비용 10% 추가 절감**

#### 최종 결론
Advanced RAG는 정상 질문 시 비용 60% 증가하나, 잘못된 입력 필터링으로 **전체 비용 효율성 및 사용자 경험 대폭 향상**

***

### 5. 최종 평가 결과

**평가 방법**: RAGAs 프레임워크 + Ground Truth 20개 Q&A set  
**사용 LLM**: Gemini-2.5-pro

#### 최종 성능
- **Context Precision**: 0.97+
- **Context Recall**: **0.9** ✅ (목표 달성)

***

### 6. API 비용 관리 교훈

**실패 사례**: 불완전한 평가 코드로 재실행 → 크레딧 3,000 → 33,000 급증

#### 실험을 통한 학습
- RAGAs 평가는 LLM 호출이 빈번하여 gpt-4o-mini 사용에도 고비용
- 테스트 코드 없이 본 평가 진행 시 회복 불가능한 비용 손실

#### 개선 조치
✅ 평가 전 테스트 코드 필수 작성  
✅ 로그 출력으로 함수 단위 검증  
✅ API 호출 전 비용 모니터링 체계 구축

***

### 핵심 성과

✅ **Recall 0.9 달성** (재현율 우선 목표)  
✅ **Advanced RAG 파이프라인** 구축 (정확도 + UX 개선)  
✅ **FAISS + Ensemble Retriever** 최적 조합 발견  
✅ **상담사 시간 단축** 및 논문 기반 객관성 확보

***

### 한계 및 향후 개선 방향

#### 프로젝트 한계
1. **최종 응답 평가 부재**: 전문가 검증 없이 Retriever 평가에만 의존
2. **프롬프트 편향**: Few-shot 예시가 오히려 편향 유발 (예시 특징 반복 생성)
3. **수작업 청킹 부담**: RAG 문서화에 과도한 시간 소모

#### 향후 개선 방향
1. **RAG 문서 자동화 파이프라인** 도입 (생산성 향상)
2. **전문가 평가 체계** 구축 (최종 응답 품질 검증)
3. **프롬프트 최적화** (Few-shot 편향 제거, 비용 절감)
4. **상용 툴 활용** (정확도 유지하며 효율성 극대화)

***

### 배운 점

**설계**: 완벽한 자동화보다 실용적 보조 도구가 더 큰 가치 창출  
**실험**: 체계적 비교 실험으로 FAISS, Ensemble, 가중치 최적 조합 발견  
**평가**: 테스트 코드 없는 LLM 평가는 비용 폭탄, 사전 검증 필수  
**파이프라인**: Advanced RAG는 비용 효율적 분기 설계가 성공의 핵심

***



</div>
</details>