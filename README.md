# Vue-project

## 목차
- 프로젝트 개요
- 프로젝트 계획
- 설명

## 프로젝트 개요
**진행 기간** : 2020.04.01 ~ 2020.05.18  
**만든 이유** : 내가 인터넷을 켯을때 자주가는 기능들을 한눈에 보기 쉽게 만들기 위해서  
**설명** : 날씨, 단어장, 비트코인 가격, to-do  
**역할** : 모두  

## 개발환경
- HTML, CSS, JavaScript
- Vue
  - vuex
  - vue-router
  - axios
  
- chart
  - vue-chartjs
  - vue-apexcharts

- tool
  - Atom
  
## 프로젝트 계획
- 보고싶은 유형 단어장 만들기
- 크롤링을 통해 날씨 정보 얻어오기
- upbit API 연동 하여 원하는 데이터 화면에 보여주기
- 날씨 데이터 vue-chartjs 이용하여 Line차트 만들기
- 비트코인 데이터 vue-apexcharts 이용하여 candle차트 만들기
- to-do

## 설명

## 1.메인화면
![메인화면](https://user-images.githubusercontent.com/52224543/82192181-983e8180-992e-11ea-8e45-40e7418c4a69.png)

## 2.단어장
- vuex store 속성을 모듈화 하여 vue 파일에서 해당 helper를 가져왔습니다.
- 원하는 날짜의 단어장을 선택하여 추가 할수 있습니다.
- 단어장을 다 선택한 후에는 전체, 한국어, 스페인어, 랜던, 보기를 선택할 수 있습니다.
![전체보기](https://user-images.githubusercontent.com/52224543/82192403-ebb0cf80-992e-11ea-9c8f-d62afc07a3c5.png)
![랜덤보기](https://user-images.githubusercontent.com/52224543/82192422-f10e1a00-992e-11ea-9315-f09875344767.png)


### vuex

1. store.js  
![store](https://user-images.githubusercontent.com/52224543/82194703-2e27db80-9932-11ea-8f70-ffe66b38a8d5.png)
2. module.js  
![module](https://user-images.githubusercontent.com/52224543/82194724-37b14380-9932-11ea-9ecf-5ee93226d28f.png)
3. word.vue  
![vue](https://user-images.githubusercontent.com/52224543/82194740-3da72480-9932-11ea-93cc-93731f9b951c.png)


## 3.날씨
- 네이버 날씨를 axios.get을 사용하여 데이터 수집하였습니다.
- 가져온 데이터를 vue-chartjs를 사용하여 line 차트로 만들었습니다
![날씨](https://user-images.githubusercontent.com/52224543/82194992-a2fb1580-9932-11ea-8785-0081aaf55517.png)

## 4. 비트코인
- 데이터를 가져오는 시간 동안 로딩 화면이 보입니다.
- 업비트 API를 통해 모든 암호화폐를 가공하여 가장 많이 (상승,하락) 7개 코인을 화면에 표시합니다.
- 시세가 상승한 정보는 빨간색 시세가 하락한 정보는 파란색으로 표시합니다.
- 가져온 데이터를 vue-apexcharts를 사용하여 candle 차트로 만들었습니다.
- 코인 이름을 클릭하면 해당 candle차트를 화면에 표시합니다.

### 로딩 화면
![로딩](https://user-images.githubusercontent.com/52224543/82195750-b22e9300-9933-11ea-906f-c2a121f712dc.png)

### 코인 클릭 전
![클릭전](https://user-images.githubusercontent.com/52224543/82195782-bf4b8200-9933-11ea-868d-ed9643a20bf8.png)

### 코인 클릭 후 상승
![가장 많이 상승한  코인](https://user-images.githubusercontent.com/52224543/82195811-cd010780-9933-11ea-9788-8e2695fa41c8.png)

### 코인 클릭 후 상승
![가장 많이 떨어진 코인](https://user-images.githubusercontent.com/52224543/82195830-d38f7f00-9933-11ea-83ef-da749248f1f7.png)

