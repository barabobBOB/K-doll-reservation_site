# K돌 공연 예매 사이트

### 개요

K돌 멤버인 레나는 개발자로 일하다 아이돌로 데뷔하게 되었다. 처음 단독 콘서트를 진행하면서 온라인으로 티켓을 판매하고자 했다. 하지만, 수수료가 생각보다 비용이 많이 들었고 레나는 개발자였기 때문에 직접 티켓 판매 서버를 만들고자 한다. 

### 요구사항

티켓 예매 서버를 구현해주세요.

1. 공연장을 등록합니다.
2. 공연을 등록합니다.
3. 예매 시간이 되었을때 공연 예매를 시작합니다.
4. 좌석을 선택합니다. 대신 다른 사람이 선택한 좌석은 고를 수 없습니다.
5. 선택한 좌석을 구매합니다.

1. 공연
    - 공연장 정보
2. 공연장
    - 좌석 정보
    - 공연장 위치
3. 공연 예매
    - 좌석 선택
    - 좌석 구매

**1. 공연장 등록 시 필요한 정보:**

- 공연장 이름
- 공연장 위치
- 총 좌석 수
- 좌석 배치도 (선택 사항)

**2. 공연 등록 시 필요한 정보:**

- 공연 이름
- 공연 일자 및 시간
- 공연 소개
- 해당 공연을 진행할 공연장 선택

**3. 예매 시작 시 필요한 조건:**

- 현재 시간이 예매 시작 시간과 일치해야 함

**4. 좌석 선택 시 필요한 정보:**

- 선택 가능한 좌석 목록 (예약되지 않은 좌석만 선택 가능)
- 사용자가 선택한 좌석 번호

**5. 좌석 구매 시 필요한 정보:**

- 선택한 좌석 정보 (좌석 번호, 가격 등)
- 결제 수단

**1. 공연장:**

- 공연장 정보 관리 (추가, 조회, 수정, 삭제)
- 공연장의 좌석 정보 관리
- 좌석 예약 여부 확인 및 업데이트

**2. 공연:**

- 공연 정보 관리 (추가, 조회, 수정, 삭제)
- 특정 공연의 예매 시작 시간 관리

**3. 공연 예매:**

- 사용자에게 좌석 선택 및 구매 기능 제공
- 사용자가 선택한 좌석이 예약되지 않았는지 확인
- 좌석 예약 및 결제 처리

**부하 테스트**

- Apache JMeter, Locust 등의 도구를 사용하여 시스템의 성능과 확장성을 테스트합니다.
- 예상되는 부하(동시 접속자 수, 트래픽 등)를 시뮬레이션하고, 서버 응답 시간 및 에러 처리 등을 확인하여 시스템의 안정성을 검증합니다.

### 제약사항

- 기술스택
    - Spring Boot(JAVA)
    - MySQL
    - h2
    - Redis
    - Docker
- 테스트코드도 작성해주세요.
    - Testcontainers를 통해 통합테스트까지 진행해주세요.
- Flyway를 활용해 DB 형상관리를 진행해주세요.
