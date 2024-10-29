# 프로그램 개요: 로또  

------

이 프로그램은 사용자가 입력한 로또 구입 금액 만큼 로또를 발행하고, 입력한 로또 번호에 따라 당첨 내역을 출력하고 총 수익률을 계산하는 프로그램 입니다.


# 기능 구현 목록

-------

### 1. 입력 기능

- 로또 구입 금액 입력받기(1장 가격 1000원)
  - 구입 금액이 1000원으로 나누어 떨어지지 않는 경우 예외 처리
  - 구입 금액이 1000원 미만일 경우 예외 처리


- 당첨 번호 입력받기: 쉼표(,)로 구분되는 6개 숫자
  - 로또 번호 범위는 1~45, 범위에서 벗어날 경우 예외처리
  - 쉼표 이외의 구분자 입력될 시 예외 처리
  - 당첨 번호중 중복되는 번호 있을 시 예외 처리
  - 6개보다 적거나 많다면 예외처리


- 보너스 번호 입력받기
    - 마찬가지로 범위 1~45
    - 보너스 번호가 당첨 번호와 중복될 경우 예외처리


- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.


### 2. 출력 기능

- 발행한 로또 수량 출력


- 발행한 로또 번호 출력(오름차순)
  - 출력 시 대괄호, 쉼표 포함


- 당첨 내역 출력
  - 당첨 통계 밑에 --- 출력


- 총 수익률 출력(소수점 둘째자리에서 반올림)


### 3. 로또 발행 기능

- 로또 구입 금액으로 가능한 만큼 로또 발행


- pickUniqueNumbersInRange() 사용하여 1~45 사이 랜덤 값 추출


### 4. 당첨 내역 계산 기능
- 발행된 로또들 중 보너스 번호를 포함한 당첨 번호와 비교하여 당첨 개수를 계산


- 총 수익도 계산


### 5. 총 수익률 계산 기능 
- 총 수익과 로또 구입 금액으로 수익률 계산
  - ((구입금액-총수익)/구입금액) * 100

