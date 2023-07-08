# 📖 프로젝트명

### ✔️ 수입 중고차 가격 예측 프로젝트 (메티버스 아카데미 2기 AI반 ML 프로젝트)

# 📃 프로젝트 소개

### ✔️ 머신러닝(XGBoost/LightGBM, RandomFroest, LinearRegression, Lasso/Lidge)을 활용한 수입 (외제) 중고차 가격 예측 프로젝트입니다.  

국내 자동차 시장에서 중고차 시장은 신차 시장에 비해 2배 이상의 규모를 차지하고 있습니다. 또한 수입차(외제차)의 보편화로 인한 수입차 점유율 증가 추세로 중고 수입차 가격에 대해 신뢰할 수 있는 지표가 필요한 시점입니다.
이번 프로젝트를 통해 중고 수입차 시장의 구매자, 판매자 모두에게 합리적인 가격 선정의 근거를 제공하여 수입차 중고 거래 활성화를 도모할 수 있을 것입니다. 

# 👩‍🔧 팀원 소개 및 역할

### ✔️ 팀원
메타버스 아카데미 2기 AI반 라경훈, 김우정, 임정민, 서주완 총 4명

### ✔️ 역할 분담
모든 팀원들의 전반적인 머신러닝 프로젝트 프로세스 경험을 위해 데이터 수집/전처리, EDA , 모델링, 파라미터 튜닝, 인사이트 도출 등을 각각 수행하였습니다. 각 팀원별 이름 (lala,wj,jm,jw)으로 branch를 나누어 기록하였습니다. 단, 주요 머신러닝 모델들(XGBoost/LightGBM, RandomFroest, LinearRegression, Lasso)을 전담하여 학습하고 비교하였습니다.

LinearRegression : 라경훈

Lasso : 김우정

RandomForest : 임정민

XGBoost/LightGBM : 서주완


# 📅프로젝트 진행 기록

### ✔️ 수행 기간
2023.06.13 ~ 2023.06.21

### ✔️ 세부 진행 기록
- 23-06-12 : 회의 및 주제 정하기, 보배드림 데이터 크롤링
- 23-06-13 : Dacon 데이터 수집, EDA
- 23-06-14 : PPT 초안 작성, EDA, 워드클라우드
- 23-06-15 : 머신 러닝 회귀 모델링 (XGBoost/LightGBM, RandomForest, LinearRegression, Lasso)
- 23-06-16 : K-Fold 학습, GridSearchcv 하이퍼파라미터 튜닝 학습 후 비교
- 23-06-19 : GridSearchcv 하이퍼파라미터 튜닝, AutoML (Pycaret) 학습, PPT 수정
- 23-06-20 : AutoML(Optuna, Autogluon)학습, 각 모델별 MAE 비교, 인사이트 도출 , PPT 수정, 발표 대본 작성 
- 23-06-21 : PT 발표 및 질의응답


# 📊 데이터 소개
### ✔️ Dacon '데이콘 Basic 자동차 가격 예측 AI 경진대회' 데이터셋을 활용하였습니다.
[데이콘 Basic 자동차 가격 예측 AI 경진대회](https://dacon.io/competitions/official/236114/overview/description) <br><br>

![image](https://github.com/woojooc/ML_Car/assets/115389344/66e2a813-ab89-4802-92a7-8d49f6fe1173)


### ✔️ 데이터 세부 사항
데이터 갯수 : 57920개<br>
ID : 샘플 별 고유 id<br>
생산년도 : 차량이 생산된 연도<br>
모델출시년도 : 차량의 모델이 처음으로 출시된 연도<br>
브랜드<br>
차량모델명<br>
판매도시 : 3글자로 인코딩된 도시 이름<br>
판매구역 : 3글자로 인코딩된 구역 이름<br>
주행거리 : 총 주행 거리(km)<br>
배기량 : 내연기관에서 피스톤이 최대로 밀어내거나 빨아들이는 부피 (cc)<br>
압축천연가스(CNG) : 압축천연가스(CNG) 자동차 여부<br>
경유 : 경유 자동차 여부<br>
가솔린 : 가솔린 자동차 여부<br>
하이브리드 : 하이브리드 자동차 여부<br>
액화석유가스(LPG) : 액화석유가스(LPG) 자동차 여부<br>
가격 : 자동차 가격(백만원)<br>

# 💡 주요 내용

### ✔️ 사전 학습

주제 선정 배경
1. 국내 자동차 시장 중 신차 시장 대비 2배 이상의 규모에 해당하는 중고차 시장
2. 수입차(외제차)의 보편화로 인한 국내 수입차 점유율 증가 추이

도메인 학습
1. 국내/해외별 중고차 시장 가격 영향 요인이 다를 것이라 예상
2. 국내 중고 자동차 시장 가격 영향 요인 : 연식, 주행거리(km), 배기량(CC), 마력 순
3. 해외(튀르키예) 중고 자동차 시장 가격 영향 요인 : 브랜드, 주행거리(km), 연식, 변속기 순

### ✔️ 개요

1. 차량 번호를 조회하여 중고차 시세를 예측하는 서비스의 머신러닝 모델 기획
2. 소셜 데이터에 기반한 중고차 매매 관련 외부요인 탐색<br>
   (1) 크롤링/워드 클라우드 활용 네이버 블로그 '중고차,'중고차 하락' 검색 시 '수출','시세','사고','폐차','업체','국내' 등 키워드 도출
   (2) 해외 기준 국내 중고차 품질의 우수함을 인정받고 있지만 시스템의 부재로 걸맞는 가격을 받지 못하는 상황

### ✔️ 머신 러닝

1. 데이터 전처리<br>
   (1) 신차 / 중고차 분리 : 주행거리 < 200km 의 신차 데이터 drop<br>
   (2) 이상치 데이터 제거 : 주행거리 >= 250만km (최댓값) 데이터 1개 관측/제거<br>
   (3) 중복 Feature 통합 : get_dummies화된 연료 유형 통합<br>
   (4) 불필요한 컬럼 제거 : 'ID'(데이터 고유 키값) , 'City','Area' : 모두 폴란드 지역/도시<br>
   (5) 문자형 데이터 변환 : '브랜드','차량모델명','판매도시','판매구역' Label Encoding<br>
   (6) (선택사항) MinMaxScaling : '연도','차량모델출시년도' MinMaxScaler 적용<br>
2. 학습 결과 (MAE) <br>
   (1) LightGBM : 6.8398<br>
   (2) RandomForest : 6.3714 (K-fold,cv=5,avg값 기준)<br>
   (3) XGBoost : 6.4092<br>
   (4) LinearRegression : 11.95<br>
   (5) Lasso/LassoCV : 13.44 (alpha=1)<br>

    💡MAE 기준 가장 낮은 RandomForest 의 Feature_importances : '생상년도','CC','주행거리','차량출시년도'

3. AutoML <br>

   (1) 앞서 구현한 모델들의 MAE값을 줄이기 위해 Optuna, Auto Gluon, Pycaret 총 3가지의 AutoML을 사용<br>
   (2) Optuna : xgb의 경우 best Trial의 값이 5.885, lgbm의 경우 best trial의 값이 5.9726으로 기존의 MAE값 보다 더 나은 결과를 도출<br>
   (3) Auto Gluon :  L2 모델이 6.051919, xgb는 6.245744, lgbm은 6.165254로 기존의 MAE값 보다 더 나은 결과를 도출<br>
   (4) Pycaret : Blending을 통해 여러 모델들을 혼합하여 새로운 모델 생성 -> MAE가 가장 낮게 나온 모델인 CatBoost, XGBoost 모델 Blending : 5.8961, 렌덤으로 Blending
       한 모델 :  5.9002, 기존의 MAE 값 보다 더 나은 결과 도출<br>
   (5) 결론적으로 AutoML을 사용한 결과 모든 프레임 워크들이 기존의 K-Fold된된 모델의 MAE값보다 확연히 낮아진것을 확인하였으며, 그 중에서도 Optuna를 통해 생성한              XGBoost 모델의 MAE값이 가장 좋게 나온 것을 확인<br>

4. Auto ML 학습 결과 (MAE) <br>
   (1) Optuna (XGBoost) : 5.885<br>
   (2) Auto Gluon (L2) : 6.051919<br>
   (3) Pycaret (CatBoost, XGBoost Blend 모델) : 5.8961<br>
   

### ✔️ 결과

1. 이번 수입 중고차 가격 예측 프로젝트에서 MAE 기준 가장 최적화된 모델은 Optuna(AutoML)의 XGBoost 모델이고 '생산년도','주행거리','배기량','차량모델' 순으로 가격에 영향을 미쳤습니다.
2. 금리,나라별 가격,업체(딜러) 등을 독립변수로 추가할 수 있다면 더욱 정확한 예측 가능합니다.
3. 해당 모델/서비스를 통해 중고차 구매차 및 판매자들에게 여 중고치 시장의 활성화를 도모할 수 있습니다.

# 🛠 기술 스택

### ▪ 언어
<img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">

### ▪ 주요 라이브러리
<img src="https://img.shields.io/badge/scikit learn-F7931E?style=for-the-badge&logo=scikit learn&logoColor=white"> <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
<img src="https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white"> <img src="https://img.shields.io/badge/seaborn-99CC00?style=for-the-badge&logo=seaborn&logoColor=white"> <img src="https://img.shields.io/badge/matplotlib-0058CC?style=for-the-badge&logo=matplotlib&logoColor=white"> <img src="https://img.shields.io/badge/wordcloud-FF4F8B?style=for-the-badge&logo=wordcloud&logoColor=white">
<img src="https://img.shields.io/badge/konlpy-FF0000?style=for-the-badge&logo=konlpy&logoColor=white"> <img src="https://img.shields.io/badge/collections-7FADF2?style=for-the-badge&logo=collections&logoColor=white">

### ▪ 개발 툴
<img src="https://img.shields.io/badge/VS code-2F80ED?style=for-the-badge&logo=VS code&logoColor=white"> <img src="https://img.shields.io/badge/Google Colab-F9AB00?style=for-the-badge&logo=Google Colab&logoColor=white">

### ▪ 협업 툴
<img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=Github&logoColor=white"> <img src="https://img.shields.io/badge/Google Slides-FFBB00?style=for-the-badge&logo=Google Slides&logoColor=white">

# 🔍 참고 자료
### ✔️ 데이터
  
[데이콘 Basic 자동차 가격 예측 AI 경진대회](https://dacon.io/competitions/official/236114/overview/description)

### ✔️ 논문
1) 고찬영, 2021, 다중선형회귀분석을 이용한 중고차 가격 예측 연구 : A사의 사례를 중심으로』, 인하대학교 물류전문대학원 석사학위 논문
2) Sümeyra MUTİ1, Kazım YILDIZ2, 2023, Using Linear Regression For Used Car Price Prediction
,International Journal of Computational and
Experimental Science and ENgineering
,Vol. 9-No.1 (2023) pp. 11-16




