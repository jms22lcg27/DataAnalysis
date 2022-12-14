# DataAnalysis
데이터분석 연습

## 1. 마켓 이용자 분석🏪 (marketing_campaign) <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">
> * #### 데이터 살펴보기
>   * head(), info() 로 데이터를 살펴보고 value_counts()로 더 자세히 살펴보았다.
> * #### 고객의 연령층
>   * np.array로 데이터를 뽑아내고 lambda로 현재 나이를 계산했다. 그리고 pd.cut으로 연령대별로 나누어 고객의 연령층을 구했다. displot으로 나이대를 살펴보았다.
> * #### 웹사이트, 카탈로그, 매장방문중 고객의 이용이 많은 것
>   * set_index로 고객아이디를 인덱스로 설정하고 loc를 사용해 이용방식 데이터를 잘라내어 V_data에 설정했다. 그리고 np.sum으로 이용방식의 합을 구했다.
> * #### 연령층별 이용이 많은 쇼핑방식
>   * V_data에 연령층 데이터인 Age를 추가하고 조건으로 많이 이용한 방식에 따라 나누었다. 모든 연령층에서 스토어 이용이 가장 많다는 것을 알 수 있다.
> * #### 연령층별 소득비교
>   * describe()로 수익의 요약을 구하고 catplot으로 연령층과 수익에 대해 그려보았다.
> * #### 소득과 지출금액의 관계
>   * 수익과 총 지출금액이 들어있는 DataFrame을 만들었다.(o_data) 그리고 OLS를 이용해 둘의 관계를 보았다. y = 27.8735x + 3.533e+04로 수익이 증가함에 따라 지출금액도 증가한다는 것을 알 수 있다.
> * #### 물품별 지출금액 살펴보기
>   * matplotlib 라이브러리를 이용해 물품별 지출금액을 시각화 했다.
> * #### 자녀가 있는 가정의 결혼여부
>   * 자녀가 있는 집의 데이터를 home에 집어넣고 displot으로 그래프를 그려 한눈에 확인했다. value_counts()로 혼인여부에 대해 살펴보았다.
> * #### 결혼했고 자녀가 있는 가정의 각 분류별 지출액 평균
>   * 결혼한 데이터와 아이가 있는 데이터를 골라내었다. 그리고 둘을 pd.merge를 이용해 inner 조인해서 하나의 테이블로 만들었다. value_counts()로 373개의 데이터 모두 결혼했고 아이가 있다는 것을 알 수 있다. np.average를 이용해 평균을 내었다.
> * #### 아이가 있는 가정과 없는 가정의 와인 지출비교
>   * catplot으로 결혼상태로 데이터를 나누어 시각화했다. 그리고 자녀의 유뮤에 따라 와인 지출금액을 describe()로 요약했다.
> * #### 학력별 소득 비교
>   * catplot으로 최종학력과 수익에 대해 그래프를 그렸는데 유독 높은 데이터 때문에 대부분의 데이터를 자세히 볼수 없게되었다. 그래서 그 데이터를 제외하고 그래프를 다시 그려보았다. swarm으로 살펴보았다. np.average를 이용해 학력별로 수익 평균을 내는데 nan데이터를 제외하기위해서 dropna()를 사용하였다.
