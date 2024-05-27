# 한 눈에 보는 게임 데이터
## 1. 프로젝트 주제
유관부서를 대상으로 하는 게임 유저/매출 분석 및 대시보드 구축하기
## 2. 프로젝트 목적
- 2024년 매출증대를 위한 적합한 전략을 세워 새로운 수익을 올릴 수 있는 모델 및 시장 발견
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

## 4. 대시보드
<p align='center'><img width="700" alt="image" src="https://github.com/MijeongKim0533/PJ_Game_Data_Analysis/assets/152786534/aad50fb6-f9c0-4b54-90e3-7d2a43fb81ab">

## 5. 결과
1. 최근 접속일(last_login_date)이 가까운 유저일수록 매출을 향상 시킴<br>
    -> 이탈이 예상되는 시점에 알람이나 프로모션을 통해 게임에 지속적으로 접속하도록 유도
2. 레벨별 유저의 분포가 비슷한 것으로 보아 게임 난이도가 쉽고, 컨텐츠가 단조로움<br>
    -> 컨텐츠 추가 개발 필요, 게임 성취욕을 높일 수 있는 level package 상품을 재구성
3. 상위레벨 유저가 전체 매출의 약 30% 차지<br>
    -> 상위레벨의 유저들이 흥미를 잃지 않도록 더 높은 레벨 설계 필요<br>
    -> 상위레벨만 참여할 수 있는 독점 이벤트를 열어 지속적 흥미 유도<br>
4. 현재 게임 플레이타임 TOP1은 중국 하지만 당국 게임 제한 정책으로 추가 진출 전략 부적절<br>
    -> 신규 시장 개척 : 게임시장 규모 성장세가 큰 방글라데시 진출 고려



