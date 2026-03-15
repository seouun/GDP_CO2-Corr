# GDP–CO₂ Analysis: Economic Growth and Carbon Emissions

📌 국가별 GDP와 CO₂ 배출량 간의 관계를 탐색한 데이터 분석 프로젝트.
시각화 중심의 탐색 분석과 시계열 확장 분석을 통해
경제 성장과 탄소 배출 간의 동조화 및 탈동조화 양상을 살펴본다.

---

## 파일 구성

| 파일 | 설명 |
|------|------|
| `analysis.ipynb` | 1차 분석: 상관관계 시각화 탐색 |
| `analysis_advanced.ipynb` | 2차 분석: 시계열 확장 분석 |
| `report.pdf` | 1차 분석 결과 보고서 |
---

## 분석 구성

### 1차 분석 (`analysis.ipynb`)

| 섹션 | 내용 |
|------|------|
| 데이터 로드 & 전처리 | 결측치 처리, 분석용 컬럼 정제 |
| 상관관계 분포 | 총량 기준 / 1인당 기준 국가별 GDP–CO₂ 상관계수 분포 |
| 성장률 산점도 | GDP 성장률 vs CO₂ 성장률 산점도 (인구 규모별 색상) |
| 대표 국가 시계열 | 동조화(India, Thailand) / 탈동조화(Germany, Sweden) 사례 비교 |
| 상·하위 국가 | 상관계수 상위·하위 5개국 바차트 |
| 카테고리별 분포 | 인구 규모 / 배출 수준 / GDP 수준에 따른 상관관계 분포 비교 |

### 2차 분석 (`analysis_advanced.ipynb`)

| 섹션 | 내용 |
|------|------|
| 전 세계 총량 추세 | 글로벌 GDP & CO₂ 장기 추세 시각화 |
| Rolling Correlation | 5년 이동 상관계수로 관계 변화 추적 |
| 기간별 상관관계 비교 | 2000–2010 vs 2011–2020 구간 비교 |
| Decoupling Index | CO₂ 성장률 / GDP 성장률 비율로 탈동조화 정도 정량화 |

---

## 데이터 준비

Kaggle에서 데이터셋을 다운로드하여 노트북과 **같은 폴더**에 저장.

🔗 [Kaggle Dataset](https://www.kaggle.com/datasets/mackness/global-gdp-and-co-emissions-dataset-19602022)
저장 파일명: `gdp_co2_by_country_v2.csv`

---

## 주요 결과

- 다수의 국가에서 GDP 총량과 CO₂ 배출량 간 강한 양(+)의 상관관계 확인
- 1인당 기준에서는 분산이 크며, 일부 국가에서 음(-)의 상관관계 관찰
- 고소득 국가(Germany, Sweden)에서 시간이 지날수록 탈동조화 강화 경향 확인
- Decoupling Index 분석에서 국가별·시기별 성장–배출 결합 강도 차이 확인
- 총량 기준과 1인당 기준 결과가 다르게 나타나는 경우 존재
  → 성장–배출 관계는 인구 규모, 경제 수준, 배출 구조에 따라 복합적으로 달라짐

---

## 한계 및 향후 연구

- 상관관계 분석으로 인과관계 확인 불가
- CBAM 등 무역 규제가 CO₂ 배출에 미치는 영향은 별도 분석 필요
- 향후 계량경제 모형(패널 회귀, 인과추론) 적용으로 확장 가능

---

## 사용 환경

- **Language**: Python 3.x
- **패키지**: pandas, numpy, matplotlib, seaborn
