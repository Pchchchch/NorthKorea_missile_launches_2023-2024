### 📖 Project Overview / 프로젝트 개요

EN
This repository presents an event-level analysis of North Korea’s missile-related launch activities during 2023–2024, based entirely on open-source information (OSINT).
The project integrates an author-collected dataset with the CSIS Missile Threat database to examine patterns, classification challenges, and uncertainty in reporting.

KR
본 프로젝트는 2023–2024년 북한 미사일 발사 활동을 대상으로 한 사건(event) 단위 OSINT 분석입니다.
직접 수집한 공개자료 기반 데이터와 CSIS Missile Threat 데이터베이스를 참고하여,
미사일 발사 활동의 시계열적·유형적·지리적 특성을 분석합니다.

---

### 🎯 Why This Project Matters / 분석 의의

EN
Missile launch reporting often contains:
ambiguous missile names,
inconsistent type classifications,
uncertain launch locations,
and speculative language such as “estimated” or “suspected”.

Rather than eliminating these ambiguities, this project explicitly preserves and analyzes them, treating uncertainty itself as an analytical object.

KR
북한 미사일 관련 보도에는 다음과 같은 불확실성이 빈번하게 존재합니다.
미사일 명칭의 불일치
유형 분류의 혼선
발사 지점의 모호성
“추정”, “추정 발사체” 등의 표현
본 프로젝트는 이러한 불확실성을 제거하기보다,
불확실성 자체를 분석의 대상으로 삼는 것을 목표로 합니다.

---

### 🗂 Data Sources / 데이터 구성

1️⃣ Author-Collected Dataset

EN
Period: January 2023 – December 2024
Sources: South Korean defense briefings & major Korean media
Unit of analysis: launch event

KR
기간: 2023년 1월 – 2024년 12월
출처: 합참 발표, 국내 주요 언론
분석 단위: 발사 사건(event)

2️⃣ CSIS Missile Threat Database

EN
Used as a reference taxonomy, not ground truth
Applied conservatively for missile name and type reconciliation

KR
절대적 정답이 아닌 참고용 분류 체계로 활용
미사일 명칭 및 유형 정합성 검토에 제한적으로 사용

---

# 🧠 Methodology / 분석 방법

EN
Korean missile name normalization & romanization
Rule-based missile name matching with CSIS
Conservative type reconciliation (no forced overrides under uncertainty)
Region extraction from textual launch-site descriptions
Visualization using pandas & matplotlib

KR
한글 미사일 명칭 정규화 및 로마자 표기
CSIS 데이터와 규칙 기반 명칭 매칭
불확실성 존재 시 유형 강제 수정 배제
발사 지점 텍스트 기반 지역 추출
pandas, matplotlib 기반 시각화

---

### 📊 Figures / 시각화 결과

📁 All figures are stored in outputs/figures/

Figure 3. Event Timeline by Missile Type
![Figure 3](/outputs/figures/fig3_timeline_by_type_and_hgv.png)

Figure 4. Missile Type Distribution
![Figure 3](/outputs/figures/fig4_type_distribution_counts.png)

Figure 5. Type Composition (Counts)
![Figure 3](/outputs/figures/fig5_type_composition_stacked_counts.png)

Figure 9. Top Launch Sites
![Figure 3](/outputs/figures/fig9_top_launch_sites.png)

Figure 12. Regional Activity (Map Overview)
![Figure 3](/outputs/figures/fig12_map_region_bubble_overview.png)

---

### ⚠️ Limitations / 한계

EN

OSINT-based reporting only
No classified or satellite-derived confirmation
Launch locations are text-derived, not geocoded
Missile classifications remain probabilistic

KR

공개자료(OSINT)에만 의존
위성·군사 기밀 정보 미사용
발사 위치는 텍스트 기반 추정
미사일 유형 분류는 확률적 판단

---

### 🔁 Reproducibility / 재현 방법

```
pip install -r requirements.txt
```

Run notebooks in order:
01_preprocess.ipynb
02_eda_and_visualization.ipynb

---

### 📎 Final Note

This repository is intended for academic and analytical learning purposes only.
It does not aim to provide operational or intelligence-level assessments.

---

### 📌 AI Usage Disclosure / AI 활용 고지

EN
This project was developed with the assistance of AI tools (including ChatGPT) for:
code structuring,
visualization design,
and documentation drafting.
However, all data collection, preprocessing rules, analytical decisions, and interpretations were designed and validated by the author.
AI tools were used strictly as a supporting instrument, not as an analytical authority.

KR
본 프로젝트는 코드 구조화, 시각화 설계, 문서 초안 작성 과정에서 AI 도구(ChatGPT)의 도움을 받았습니다.
다만 데이터 수집, 전처리 기준, 분석 로직, 해석 및 판단은 전적으로 작성자가 직접 설계·검증하였습니다.
AI는 분석 주체가 아닌 보조 도구로만 사용되었습니다.

