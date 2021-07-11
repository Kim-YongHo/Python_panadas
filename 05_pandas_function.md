## count() 함수

- 가장 간단한 분석은 개수를 세는 것임
- NaN 값은 세지 않음 (유효한 값만 처리한다는 의미)

![image-20210711222126090](picture\image-20210711222126090.png)



![image-20210711222507890](C:\Users\USER-PC\Desktop\Study\Python_panadas\picture\image-20210711222507890.png)

---



## import 한 값 유효성 확인

![image-20210711222654863](picture\image-20210711222654863.png)

---



## value_counts() - 카테고리 값 세기

- 시리즈의 값이 정수,문자열 등 카테고리 값인 경우에
- 시리즈.value_counts() 메서드를 사용해 각각의 값이 나온 횟수를 셀 수 있음
- 파라미터 normalize=True 를 사용하면 각 값 및 범주형 데이터의 비율을 계산
  - 시리즈.value_counts(normalize=True)

![image-20210711222954455](picture\image-20210711222954455.png)

---



## value_counts() 함수 - 범주형 데이터에 적용

- 범주형 데이터 : 관측 별과가 몇개의 범위 또는 항목의 형태로 나타나는 자료
  - ex. 성별(남,여), 선호도(좋다, 보통, 싫다), 혈액형(A,B,O,AB) 등

![image-20210711223051235](picture\image-20210711223051235.png)

----



## value_counts() 함수- 데이터 프레임 사용

- 행을 하나의 value로 정의 동일한 행이 몇 번 나타났는지를 반환
- 행 데이터의 경우가 인덱스 설정 개수된 값이 value로 표시되는 Series 반환

![image-20210711223328388](picture\image-20210711223328388.png)



![image-20210711223406258](picture\image-20210711223406258.png)

---



## 데이터 정렬 - 정렬 함수 사용

- 데이터 정렬은 Series와 DataFrame 둘다 사용 가능

- sort_index() : 인덱스를 기준으로 정렬
- sort_value() : 데이터 값을 기준으로 정렬
  - DataFrame에서 사용 시 기준 열이 필요함

---



## Series 정렬 ascending=True/False

- sort_index() / sort_value() 조합해서 사용
- ascending=True/False : 오름차순/내림차순
- 생략하면 오름차순



- 인덱스 기준

![image-20210711224047344](picture\image-20210711224047344.png)



- value 기준

![image-20210711224226047](picture\image-20210711224226047.png)

---



## DataFrame 정렬

- df.sort_values() : 특정열 값 기준 정렬
    - DataFrame은 2차원 배열과 동일하기 때문에
        - 정렬시 기준열이 필요함  (by 인수 사용 : 생략 불가)
        - by = 기준열, by=[기준열1,기준열2]
    - 오름차순/내림차순 : ascending = True/False (생략하면 오름차순)
- df.sort_index() : DataFrame의 index 기준 정렬
    - 오름차순/내림차순 : ascending = True/False (생략하면 오름차순)



- value 값 기준

![image-20210711224809982](picture\image-20210711224809982.png)



- index 기준

![image-20210711224908722](picture\image-20210711224908722.png)

---



## DataFrame 조작 함수

- 행/열 합계, 평균, 최대, 최소 등이 존재

- 사용 시 주의할 점

  - 행과 열의 합계를 구할때는 sum(axis=0/1) - axis는 0이 기본

  - 각 열의 합계를 구할때는 sum(axis=0)
  - 각 행의 합계를 구할때는 sum(axis=1)

![image-20210711225112165](picture\image-20210711225112165.png)





![image-20210711225305262](picture\image-20210711225305262.png)

---



## DataFrame 행과 열 추가

- 열 추가 : 기본 인덱싱
  - df['새로운 열 이름'] = 값
- 행 추가 : loc 인덱서
  - df.loc['새로운 행 익뎃스'] = 값



![image-20210711225416338](picture\image-20210711225416338.png)



![image-20210711225911276](picture/image-20210711225911276.png)





