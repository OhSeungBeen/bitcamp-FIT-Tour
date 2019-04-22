# UC000 - 현지 투어 상품예약하기  (BookLocalTourProduct)

현지 투어 상품을 예약,취소,조회 할 수 있는 유스케이스이다.
## 주 액터(Primary Actor)

- 회원
- 관리자
## 보조 액터(Secondary Actor)
는
## 사전 조건(Preconditions)

  - 회원 또는 관리자로 로그인 되어 있다.
## 종료 조건(Postconditions)

- 현지 투어 상품을 예약하였다.
- 현지 투어 상품을 예약취소하였다.
- 현지 투어 상품을 예약내역을 조회하였다.

## 시나리오(Flow of Evnets)

### 현지 투어 상품 예약 하기

1. 액터는 상품 예약날짜를 입력한다.
2. 액터는 예약 인원수를 입력한다.
3. 액터는 예약하기 버튼을 클릭한다.
   - 시스템은 회원 로그인이 되어 있지 않다면 로그인이 되어있어야 됨을 알린다.
   - 시스템은 로그인이 되어 있고 필수 입력 항목 (예약날짜, 예약 인원수)가 비어 있다면,
     시스템은 필수 입력 항목이 비어 있음을 알린다.
4. 시스템은 예약하기 폼을 출력한다.
5. 액터는 약관동의채크,여행자 연락처,여행 컨셉, 결제정보 요청사항을 입력하고 결제하기 버튼을 클릭한다.
 - 필수항목(약관동의채크,여행자 연락처,여행 컨셉, 결제정보)이 비어 있다면,
  - 시스템은 필수 입력 항목이 비어 있음을 알린다.
5.2 시스템은 '결제하기' 유스케이스로 이동한다.
5.2 액터는 취소하기 버튼을 클릭한다.
6.2 시스템은 '현지 투어 상품 상세 조회하기' 유스케이스로 간다.


### 현지 투어 상품 예약 내역 보기
1. 액터는 웹페이지 오른쪽상단에 예약내역을 클릭한다.
2. 시스템은 액터가 예약한 현지 투어 상품을 출력한다.


### 현지 투어 상품 예약 취소 하기
1. 액터는 웹페이지 오른쪽상단에 예약내역을 클릭한다.
2. 시스템은 액터가 예약한 현지 투어 상품을 출력한다.
3. 액터는 삭제할 현지 투어상품의 예약취소 버튼을 클릭한다.
4. 시스템은 예약취소 버튼을 클릭한 해당 현지 투어상품의 주문상태를 취소 요청중으로 변경한후
   '현지 투어 상품 예약 내역 보기' 유스케이스의 2번으로 간다.


## UI 프로토타입

###
![현지 투어 상품 예약](./images/uc15-BookLocalTourProduct01.png)
###
![현지 투어 상품 예약내역](./images/uc15-BookLocalTourProduct02.png)