# 창원시 불법 주정차 데이터 분석 프로젝트

### Public Data–Driven Urban Parking Violation Analysis
 
창원시 불법 주정차 단속 데이터를 기반으로 **주정차 위반의 시간적·공간적 패턴을 분석하고,  
주차 인프라 및 인구 데이터와의 관계를 탐색한 데이터 분석 프로젝트**

---
 
## Tech Stack

Python · Pandas · Numpy · Matplotlib · GeoPandas · Folium · Geospatial Analysis

---

## Analysis Pipeline
Data Collection
↓
Data Preprocessing
↓
Geospatial Mapping
↓
Exploratory Data Analysis
↓
Parking vs Enforcement Analysis
↓
Visualization


---

# 1. 프로젝트 개요

<img width="453" height="200" alt="image" src="https://github.com/user-attachments/assets/473ab3a3-f743-4bb2-a17c-15dc362e188c" />


불법 주정차는 도시 교통 흐름을 방해하고 보행자 안전을 위협하는 대표적인 도시 문제 중 하나이다.  
본 프로젝트는 창원시의 불법 주정차 단속 데이터를 기반으로 불법 주정차 발생 패턴을 분석하고, 인구·차량·주차 인프라와의 관계를 탐색하는 것을 목표로 한다.

단순히 단속 건수를 분석하는 것을 넘어 다음과 같은 다양한 데이터를 결합하였다.

- 불법 주정차 단속 데이터  
- 주민등록 인구 데이터  
- 유동 인구 및 생활 인구 데이터  
- 차량 등록 데이터  
- 주차장 데이터  
- 행정동 공간 데이터 (GIS)

이를 통해 불법 주정차 발생과 도시 구조적 요인 간의 관계를 분석하고, 데이터 기반의 도시 교통 정책 인사이트를 도출하고자 하였다.

---

# 2. 프로젝트 목표

본 프로젝트는 다음과 같은 질문에 답하는 것을 목표로 한다.

- 불법 주정차는 어떤 지역에서 많이 발생하는가  
- 불법 주정차는 어떤 시간대에 많이 발생하는가  
- 불법 주정차는 주차장 수와 관련이 있는가  
- 인구 밀도나 차량 등록 수는 불법 주정차 발생에 영향을 미치는가  
- 행정동 단위에서 공간적 패턴이 존재하는가  

---

# 3. 사용 데이터

## 불법 주정차 단속 데이터

창원시에서 제공하는 불법 주정차 단속 기록 데이터

주요 변수

- 단속 일시  
- 단속 위치  
- 단속 구분  
- 단속 장소명  

---

## 인구 데이터

- 주민등록 인구  
- 생활 인구  
- 유동 인구  

---

## 차량 및 주차 데이터

- 차량 등록 수  
- 공영 및 민영 주차장 수  

---

## 공간 데이터

행정동 경계 데이터 (Shapefile)

이를 활용하여 불법 주정차 발생 위치를 행정동 단위로 매핑하였다.

---

# 4. 사용 기술

### Programming
Python

### Data Analysis
pandas  
numpy  

### Visualization
matplotlib  

### Geospatial Analysis
geopandas  
shapely  
folium  

### Data Processing
geopy  
requests  
json  

### Environment
Google Colab

---

# 5. 분석 과정

## 5.1 데이터 전처리

공공데이터 특성상 위치 정보가 불완전한 경우가 많아 다음과 같은 전처리를 수행하였다.

- 주소 데이터 정제  
- 누락된 위치 정보 보정  
- 주소 기반 위도·경도 변환 (Geocoding)

이를 통해 지도 기반 분석이 가능한 데이터셋을 구축하였다.

---

## 5.2 공간 데이터 결합

GeoPandas와 행정동 경계 데이터를 활용하여 불법 주정차 위치 데이터를 행정동 단위로 매핑하였다.

사용 기술

- GeoPandas  
- Shapely  
- Shapefile  

---

## 5.3 탐색적 데이터 분석 (EDA)

다음 기준으로 불법 주정차 패턴을 분석하였다.

### 시간 기반 분석

- 시간대별 단속 건수  
- 평일과 공휴일 비교  

### 지역 기반 분석

- 행정동별 단속 건수  
- 구청별 단속 패턴  

---

## 5.4 주차 인프라와의 관계 분석

불법 주정차 발생이 주차 인프라 부족과 관련이 있는지 분석하였다.

분석 변수

- 주차장 수  
- 차량 등록 수  
- 인구 데이터  

이를 통해 주차 공급과 불법 주정차 발생 간의 관계를 탐색하였다.

---

# 6. 데이터 시각화



## 불법 주정차 위치 지도 시각화

아래 지도는 불법 주정차 단속 위치를 기반으로 생성한 공간 분포 지도이다.
<img width="341" height="164" alt="image" src="https://github.com/user-attachments/assets/1d9cfa50-98ca-4d26-80c3-b619f54b8c73" />

---

### 불법 주정차 주변 환경 분석


<img width="457" height="178" alt="image" src="https://github.com/user-attachments/assets/ca397fe8-5d33-4c3c-9420-709b238879c1" />


---

## 시간대별 단속 건수 분석

불법 주정차 단속 건수를 시간대 기준으로 분석하였다.

<img width="399" height="271" alt="image" src="https://github.com/user-attachments/assets/4401c5da-927d-44f3-a420-87f5cb32d5c5" />


<img width="1133" height="642" alt="image" src="https://github.com/user-attachments/assets/705df174-764d-472b-bda0-2d25aeddc58a" />


---

## 행정동별 단속 건수 분석

행정동 단위로 불법 주정차 단속 건수를 비교하였다.

<img width="397" height="310" alt="image" src="https://github.com/user-attachments/assets/d095cb0f-9266-4a5f-8af0-1cc1fbf1c48e" />


---

## 주차장 수와 단속 건수 비교

주차 인프라와 단속 건수 간의 관계를 분석하였다.
<img width="431" height="259" alt="image" src="https://github.com/user-attachments/assets/36765360-4873-4793-afe3-7675aeba7c9d" />

---

# 7. 주요 분석 결과

분석 결과 다음과 같은 패턴을 확인할 수 있었다.

- 특정 시간대에 불법 주정차 단속이 집중되는 경향이 나타남  
- 일부 행정동에서 단속 건수가 높은 공간적 패턴이 존재함  
- 차량 등록 수가 많은 지역에서 단속 건수가 높은 경향이 나타남  
- 인구 밀도가 높은 지역에서 불법 주정차 발생이 상대적으로 많음  

이는 도시 구조적 요인이 불법 주정차 발생에 영향을 미칠 가능성을 보여준다.

---



---

# 8. 향후 확장 가능성

- 머신러닝 기반 불법 주정차 발생 예측 모델 구축  
- 시간 기반 예측 모델 (Time Series Forecasting)  
- 실시간 교통 데이터 연계  
- 데이터 시각화 대시보드 구축 (Streamlit / Tableau)

---

# 9. 프로젝트 수행

AI · Software Department  
Artificial Intelligence Major  

관심 분야

- Data Analysis  
- Public Data Analytics  
- Machine Learning  
- Urban Data Analysis  

---

# 10. 프로젝트 의의

본 프로젝트는 공공데이터와 공간 데이터를 결합하여 도시 문제를 분석한 데이터 분석 프로젝트이다.

- 실제 공공데이터 기반 데이터 분석 경험  
- 데이터 전처리 및 정제 능력  
- 탐색적 데이터 분석 수행  
- 공간 데이터 분석 (Geospatial Analysis)  
- 데이터 시각화 및 인사이트 도출  
