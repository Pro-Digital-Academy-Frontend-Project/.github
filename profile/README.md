## 키워드 기반의 주식 인사이트 제공 플랫폼: Stockey
![introPage](../asset/1-인트로페이지.png)

## ⁉️기획 배경
테마주와 같은 특정 키워드 기반의 투자 성향에서 아이디어를 시작했습니다.
#### 투자자의 니즈
- 헤비 트레이더: 자신만의 투자 전략과 특정 키워드를 바탕으로 주식 변동성을 분석하는 투자 패턴
- 라이트 트레이더: 숙련된 트레이더의 분석 키워드와 투자 전략에 관심이 높음
#### 기존 서비스의 한계
- 한정된 키워드에 대해 한정된 주식 종목 인사이트만 제공
- 종목 토론방과 달리 키워드 기반의 커뮤니케이션 공간의 부재
#### [Stockey]의 목표
- 사용자의 키워드 자율성 보장
- 키워드와 종목 간의 관계를 시각화 및 랭킹화하여 인사이트 제공
- 키워드 기반의 헤비 트레이더-라이트 유저 연결

<br>

## 🗝️주요 기능 및 UI
- 키워드 기반의 주식 랭킹 및 차트
- 종목 기반의 키워드 랭킹 및 차트
- 키워드 별 채팅방
- 즐겨찾기 키워드/종목 알림 서비스
![image](https://github.com/user-attachments/assets/43bd4a12-c210-4c0d-9745-bb79c952ad9c)
🎥[시연 영상 보러 가기](https://www.youtube.com/watch?v=MWXZM-6tnXA)

<br>

## 🤔구현 방식
1. 스케줄링을 통해 매일 Naver Open API로 종목 별 뉴스 데이터를 가져왔습니다.
2. 뉴스 데이터에서 Kiwi로 토큰화 후, kr-wordrank로 키워드와 키워드-종목 별 가중치를 추출했습니다.
3. 추출한 데이터를 DB에 저장 후 [키워드 별 종목 랭킹], [종목 별 키워드 랭킹], [키워드 별 채팅방] 등을 제공하였습니다.

<br>

## 🤔아키텍처 및 사용 기술
### 🔹 **프론트엔드**
- React, JavaScript, Tailwind CSS
- **react-financial-charts** 라이브러리를 이용한 차트 구현 

### 🔹 **백엔드**
- ExpressJS, MySQL 사용
- 네이버 뉴스 크롤링 및 KR-wordrank를 통한 키워드 추출
- 한국투자증권 API, Slack 봇 연동

<br>
  
![image](https://github.com/user-attachments/assets/1efe2035-907b-44ac-825a-4102c439357a)

<br>

## ERD
![image](https://github.com/user-attachments/assets/d9987eb7-b08f-4b19-bedc-0af17614cdda)


## 👍회고
![image](https://github.com/user-attachments/assets/e91226fc-330e-48e9-b785-dc4e7779c8ee)

