# machine_learning
## 1day
- 훈련데이터 / 테스트 데이터 나누기

## 2day
- 최근접이웃(KNN)
-  K-최근접 이웃 회귀모델
    - 분류 : 범주형 데이터를 기준으로 분류하는 방식
    - 회귀 : 연속형 데이터(숫자)를 예측하는 방식
    - 회귀는 정해진 범주가 없으며, 임의의 수치값을 출력합니다.

- 과대적합 / 과소적합
    - 훈련데이터와 테스트데이터를 각각 평가하여 비교했을 때
    - 과대적합 : 훈련데이터의 평가결과가 너무 높고, 테스트데이터의 평가가 너무 낮을 경수
    - 과소적합 : 훈련데이터의 평가결과가 낮고, 테스트데이터의 평가가 높은 경수 
 

## 3day
- 선형회귀
    - 하나의 특성을 가장 잘 나타내는 직성을 찾아내는 것이 주역할
- 다항회귀
    - 다항식을 사용한 선형회귀를 "다항회귀"라고도 합니다.
- 다중회귀
    - 여러 개의 특성(독립변수 = 항목 = 컬럼 = 변수 = 퓨처)을 사용한 선형회귀
- 특성공학
    - 기존의 특성을 이용해서, "새로운 특성(항목)"을 만들어 내는 작업
- 규제 : 정규화 > ridge, lasso
    - 규제 :  과대적합 발생하지 않도록 제어
    - 릿지(ridge) : 계수 제곱한 값 기준으로 규제 적용
    - 라쏘(lasso) : 계수의 절댓값 기준으로 규제 적용

## 4day
- 로지스틱 회귀분류
- iris 데이터 활용 실습

## 5day
- 점진적 학습
    - 확률적 경사 하강법(SGD; Stochastic Gradient Descent)
        - 원하는 지점에 도착하기 위해 가장 가파른 경사를 따라 내려가는 방법 찾음
        - 훈련데이터의 전체 특성들 중 하나씩 랜덤하게 선택하여 가장 가파른 길 찾음
- 결정트리(Decision Tree)
    - 질문(조건)통해 트리(True, False) 2개씩 가지 치며 분류
    - 질문 스스로 찾아 계속해서 질문 만들어 나가며 분류(트리)
    - 더 이상 질문이 없을 시 결정
    - plot_tree
    - 특성중요도 : 트리 훈련에 사용된 독립변수(특성=퓨처) 정확도 확인
- wine 데이터 활용 실습

## 6day
- 5day 이어서
- 교차검증
- 하이퍼파라미터 튜닝(AutoML)
    - sklearn.model_selection
    - GridSearchCV
- 결정트리의 트리의 깊이 값 찾기
    - 그리드서치(GridSearch)객체 사용
- 랜덤서치
    - uniform, randint

- 트리의 앙상블
    - 정형데이터에서 가장 뛰어난 성능
    - 결정트리 기반으로 만듦
    - 랜덤포레스트
        - 앙상블 모델 중 가장 대표적
        - 훈련데이터에서 과대적합되는 것 방지
        - 결정트리 하나하나 랜덤하게 만들어 숲 만듦
        - 훈련데이터에서 랜덤하게 샘플 추출해 훈련 완료한 후 다시 원본 훈련데이터에 반환
        - 랜덤 추출 시 이전 사용 샘플 사용 가능
            - 부트스트램 샘플(Bootstrap.sample) : 중복허용 데이터 샘플링
        - 교차검증 허용
    - 엑스트라 트리(Extra Tree)
        - 기본 100개의 결정트리 훈련
        - 부트스트램 샘플링 지원 x
        - 무작위로 트리 분리
        - 과대적합 막고 검증데이터 평가 값 높일 수 있음
    - 그레디언트 부스팅(Gradient Boosting)
        - 깊이 얉은 결정트리 사용
        - 기존 훈련모델 오차 보완
        - 과대적합에 강하고 일반화에 강함
        - 훈련속도 느림
    - 히스토그램기반 그레디언트 부스팅(Histogram_base Gradient Boosting)
        - 그레디언트 부스팅 느린 속도 개선
        - XGboost
        - LightGBM
       
## 7day
