머신러닝 기반 모기 활동 지수 예측 시스템
기후 변화로 인한 모기 매개 감염병 증가 문제에 대응하기 위해,
기후 및 대기 데이터를 분석하여 모기 활동 지수(MAI)를 예측하고
기존 서울시 모기 예보 시스템의 정확도를 개선하는 머신러닝 예측 모델이다.

서울시 기후·대기 데이터는 기상청 및 서울시 대기환경정보 API를 활용하여 수집하였으며,
모기 활동 지수는 서울시 보건환경연구원의 모기 포집 데이터를 기반으로 구축하였다.

Pipeline Overview
기후·대기 데이터 (23개 변수)
→ 데이터 전처리 (결측치 대체, 단위 표준화)
→ EDA 및 상관관계 분석
→ 피처 엔지니어링 (파생 변수 생성)
→ Train/Test 분할

머신러닝 모델링
→ 다중회귀, KNN, Random Forest, LGBM, XGBoost
→ GridSearchCV/RandomizedSearchCV를 활용한 하이퍼파라미터 최적화
→ 모델 성능 비교 (R², RMSE)
→ XGBoost 최종 모델 선정 (R² 0.95, RMSE 48.4)

변수 중요도 분석
→ 0.5m 지중온도(0.5UT), 아황산가스(SDC), 이산화질소(NDC) 등
→ 기존 예보에서 고려하지 않은 새로운 영향 요인 도출

인사이트 도출
→ 서울시 모기 예보 정확도 72% → 95%로 개선 가능성 입증
→ 킬러모기 방생 최적 조건: 봄·여름(3-8월), 밤 10시-새벽 2시
→ 대기오염 농도 높은 하천·공원·인구밀집 지역 우선 방생 제안

Key Features
기상청, 서울시 대기환경정보, 보건환경연구원 데이터 통합 구축

23개 기후·대기 변수 기반 머신러닝 예측 모델링

5가지 회귀 모델 비교 분석 및 XGBoost 최적화

변수 중요도 분석을 통한 핵심 영향 요인 도출

미국 플로리다주 벤치마킹을 통한 킬러모기 방생 전략 제시

기존 서울시 모기 예보 시스템 대비 23%p 정확도 향상 검증

Tech Stack
Python 3.10

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn (GridSearchCV, Cross Validation)

XGBoost, LightGBM

Jupyter Notebook, Google Colab

Directory Structure
plaintext
mosquito-activity-prediction/
├─ data/
│  └─ mosquito_final_air_data.csv
├─ notebooks/
│  ├─ 01_EDA.ipynb
│  ├─ 02_Preprocessing.ipynb
│  └─ 03_Modeling.ipynb
├─ preprocessing/
│  └─ data_cleaning.py
├─ modeling/
│  ├─ regression_models.ipynb
│  ├─ random_forest.ipynb
│  ├─ xgboost_optimization.ipynb
│  └─ feature_importance.ipynb
├─ visualization/
│  ├─ correlation_heatmap.png
│  ├─ feature_importance.png
│  └─ killer_mosquito_map.png
├─ results/
│  ├─ model_performance.csv
│  └─ best_params.txt
└─ README.md
