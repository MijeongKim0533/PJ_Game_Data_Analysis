# 한 눈에 보는 게임 데이터
## 1. 프로젝트 주제
한 눈에 보는 게임 데이터
## 2. 프로젝트 목적
- 유관부서를 대상으로 하는 게임 유저 접속/매출 대시보드 구축
- 매출 증대를 위한 매출현황과 유저행동 분석
## 3. 분석 과정
- 데이터 :<br>
<p align='center'><img width="450" alt="image" src="https://github.com/MijeongKim0533/PJ_Game_Data_Analysis/assets/152786534/5a6c1124-aead-40d5-8d71-bcf41cd8e378">

- Data Flow<br>
  <p align='center'><img width="400" alt="image" src="https://github.com/MijeongKim0533/PJ_Game_Data_Analysis/assets/152786534/115b6e34-ca64-43a1-87c1-87cee4703aae">

- 기존 데이터셋의 'pay_user_type'은 매출 증대를 위한 고객 세그먼트로 부적절<br>
    -> 'pay_amount'컬럼을 기준으로 새로운 고객 세그먼트를 만듦
- 다중 선형회귀 분석과 후진 제거법으로 'pay_amount'에 가장 영향을 많이 주는 변수 탐색
- ANOVA 분석에서 'last_login_data'와 'level'이 'pay_amount'와 평균 간 차이가 있음을 확인
- k-elblow mothod 사용하여 군집 수 결정(n=4) -> k-means clustering
  
## 4. 결론
- 최근 접속일(last_login_date)이 가까운 유저일수록 매출을 향상 시킴<br>
    -> 이탈이 예상되는 시점에 알람이나 프로모션을 통해 게임에 지속적으로 접속하도록 유도

## 5. 대시보드
<p align='center'><img width="700" alt="image" src="https://github.com/MijeongKim0533/PJ_Game_Data_Analysis/assets/152786534/aad50fb6-f9c0-4b54-90e3-7d2a43fb81ab">