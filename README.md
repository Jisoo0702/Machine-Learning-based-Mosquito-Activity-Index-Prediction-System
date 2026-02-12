# 모기활동지수 예측 고도화를 위한 머신러닝 기반 예측 시스템

기존의 단순 기상 변수 기반 모기활동지수 예측 방식의 한계를 개선하고,  
보다 정밀하고 일반화 성능이 높은 예측 모델을 개발하기 위한  
머신러닝 기반 모기활동지수 예측 시스템이다.

기상 데이터 및 환경 데이터를 활용하여  
모기 활동에 영향을 미치는 주요 요인을 분석하고,  
Random Forest, XGBoost, LightGBM 등 앙상블 모델을 통해  
기존 예측 시스템 대비 성능을 향상시키는 것을 목표로 한다.

본 연구는 단순 통계 기반 예측을 넘어  
비선형 관계와 변수 간 상호작용을 반영한 모델을 구축함으로써  
기존 예측 체계를 개선하기 위한 모델 개발에 초점을 둔다.

---

## Pipeline Overview

README 작성  
→ 데이터 수집 및 정리  
→ EDA (탐색적 데이터 분석)  
→ Feature Engineering  
→ 머신러닝 모델링  
→ 성능 비교 및 개선  
→ 결론 도출

---

## Key Features
- 기상 및 환경 데이터 기반 모기활동지수 예측
- 탐색적 데이터 분석(EDA)을 통한 변수 영향도 분석
- Random Forest, XGBoost, LightGBM 모델 비교
- RMSE, R² 기반 모델 성능 평가
- 기존 예측 방식 대비 성능 개선 모델 제안

---

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- LightGBM

---

## Directory Structure

```plaintext
project/
├─ README/
│  └─ README.md
├─ data/
│  └─ mosquito_activity_data.csv
├─ EDA/
│  └─ exploratory_analysis.ipynb
├─ modeling/
│  ├─ random_forest_model.ipynb
│  ├─ xgboost_model.ipynb
│  └─ lightgbm_model.ipynb
└─ conclusion/
   └─ model_comparison_and_result.ipynb
