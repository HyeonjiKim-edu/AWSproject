
# 📃 데이터 분석 프로젝트 : 서울시민 대상 소비 예측하기
<br>
✔ 분석 기간 : 2024년 12월 18일 ~ 12월 20일<br>
✔ 분석 목표 : 분석 도구를 활용하여 예측 또는 분류 모델 생성
<br>
<br>

## ✏ 분석 개요

서울특별시 빅데이터 캠퍼스에서 제공하는 '서울시민의 소비품목별 상품판매 데이터'를 활용하여 <br>
Linear Regression 모델을 만들어 서울시민의 소비 패턴을 학습시키고, <br>
해당 모델을 통해 소비 경향성을 파악 및 추후 소비에 대해 예측하고자 함. 

<br>

## ✏ 분석 목적

서울 시민의 구매 내역 분석을 통해 소비 패턴을 파악하여 소비와 관련된 경향성을 확인하고, <br>
추후 구매에 영향을 줄 수 있는 요인을 찾아내는 것을 목적으로 함. 

<br>

## ✏ 분석 주제

1. **행정동별 구매 경향성 파악 및 예측** <br>
 : 구매 지역에 따른 구매 경향성을 파악하고, 이에 근거하여 추후 구매 패턴을 예측하고자 함.
2. **시간대별 구매 경향성 파악 및 예측** <br>
 : 구매 시간에 따른 구매 경향성을 파악하고, 이에 근거하여 추후 구매 패턴을 예측하고자 함.
3. **다중 피처 설정 후 구매 예측** <br>
 : 다양한 요인의 상호작용이 작용할 때 소비자들의 추후 구매 여부를 예측하고자 함. 
<br>

## ✏ 이용 데이터
- **서울시민의 소비품목(통계청)별 상품판매 데이터** <br>
: “서울시 블록별 롯데멤버스 상품판매데이터”의 롯데멤버스 상품분류를 통계청 상품분류로 변환하여 <br>
  소비자의 거주지와 판매지를 기준으로 블록/행정동별로 집계한 데이터 500건

- **변수**

| 변수명         | 데이터 설명              |
|----------------|--------------------------|
| 기준년월(STD_YM) | 결제일                  |
| 행정동코드(ADSTRD_CD) | 결제가 이루어진 장소 |
| 통계청상품코드(STAT_CD) | 구매한 상품의 상품코드 |
| 성별코드(SEX_CD) | 구매자의 성별           |
| 연령대코드(AGE_CD) | 구매자의 연령대        |
| 시간대코드(TIME_CD) | 물품을 구매한 시각    |
| 구매_고객수(ACC_CNT) | 해당 물품을 구매한 고객 수 |
| 구매건수(PURH_CNT) | 해당 물품의 구매 수   |
| 구매금액(PURH_AMT) | 해당 물품의 구매 가격 |


- 데이터 출처 <br>
: https://bigdata.seoul.go.kr/data/selectSampleData.do?r_id=P213&sample_data_seq=324&tab_type=&file_id=&sch_text=&sch_order=U&currentPage=3

<br>

## ✏ 분석 방법

1. 데이터 확인 : 분석 대상 데이터 확인 
2. 기초 통계분석 실시 : 분석 데이터의 분포 및 특성 파악을 위한 기초 통계분석 실시
3. 주제별 분석 실시 : 주제별 Linear Regression 모델 생성 및 예측값 확인 

<br>

## ✏ 분석 결과

기초 통계분석 실시 결과, 요인별 상관이 매우 낮은 것으로 나타남. <br>
특히, 데이터 분포를 확인한 결과 결제 금액 및 결제 횟수 등이 좌편향된 것으로 확인됨. <br>
데이터 분석 결과, 생성된 모델들이 예측에 적합하지 않은 것으로 나타남. <br>
이는 요인들 간 상관이 낮고, 데이터가 정규분포를 이루지 않은 것이 영향을 주었을 것으로 생각됨. <br>
추후 분석 시 데이터의 정규성을 위해 이상치 제거 등의 과정을 추가하고, <br>
데이터 특성에 적합한 방식의 모델 생성 방법을 채택하는 것이 도움이 될 것으로 보임. 
<br>
