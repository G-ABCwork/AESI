# 코로나19 백신 예방접종 후 이상반응 추적 감시 연구
- 발주기관: 질병관리청
- 수행기관: 고려대학교 산학협력단
- 코로나19 예방접중 후, 의심되는 여러 이상반응(AESI: Adverse Events of Special Interest)에 관한 추적 감시를 수행합니다.
- 스핀오프 분석: 접종군(Case), 미접종군(Control) 간 각 이상반응의 10만명 당 발생율을 비교합니다.

## 분석 방법론
- 이상반응 추적감시: ARIMA 모형
  - [스터디 노트](https://be-favorite.tistory.com/63?category=928223)
  - AICc(corrected AIC)를 기반으로 최적의 ARIMA 모형을 구축하여 각 이상반응의 Baseline incidence를 구축합니다.
  - 월별 발생건수가 0에 가까운 이상반응의 경우, (log+1) 변환을 수행합니다.
- 스핀오프 분석: 이 표본 포아송 비율 검정(two-sample poisson rates test)

## 분석 툴
- R

## 데이터
- 건강보험공단 빅데이터 맞춤형 연구DB

- Example of the spin-off analysis: EDA for testing the ratio of two poisson rates

<p align="center">
<img src = "./Plot_example/Example_spinoff.png">
</p>
