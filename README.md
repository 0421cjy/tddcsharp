## The Art of Unit Testing

### 1장 단위테스트의 기본

- 단위테스트와 통합 테스트의 정의
- 간단한 단위 테스트 작성하기
- 테스트 주도 개발 탐구하기

Unit Test - '단위 테스트(unit test)'는 다른 코드를 호출한 후 몇가지 가정이 성립하는지 검사하는 코드 (대개 메서드)다. 가정이 성립하지 않는 것으로 판명되면 단위테스트는 실패한다. 여기서 '단위(unit)'라는 말은 메서드나 함수를 의미한다.

SUT - SUT는 테스트 대상 시스템을 의미한다. 어떤 사람들은 CUT[테스트 대상 클래스 (class under test) 테스트 대상 코드 (code under test)의 준말]라고 부르기도 한다. 무엇인가를 테스트할 때 그 대상을 SUT라고 부른다.

1. 좋은 단위 테스트의 속성

- 자동화되고 반복 실행이 가능해야한다.
- 구현하기 쉬워야 한다.
- 한번 작성하면 변경되지 않아야 한다.
- 누구나 실행이 가능해야한다.
- 버튼 하나를 실행이 가능해야 한다.
- 빨라야 한다.

통합 테스트 - '통합 테스트(intergration testing)'는 두 개 이상의 독립적인 소프트웨어 모듈을 하나의 그룹으로 테스트하는 것을 의미한다.

단위 테스트 <-> 통합 테스트

### 3장 스텁을 이용한 의존성 분리

외부 의존물 - '외부 의존물(external dependency)'이란, 시스템 상에 존재하는 객체로서, 테스트 중인 코드와 상호작용함에도 전혀 제어할 수 없는 객체를 말한다.
(일반적인 예를 들면 파일시스템, 스레드, 메모리, 시간 등이 있다.)

스텁 - '스텁(stub)'이란, 시스템 상의 외부 의존물(또는 협력자, collaborator)을 대신하기 위해 쓰이는 제어 가능한 대체물이다. 
스텁을 사용하면 의존 관계를 직접 다루지 않고서도 코드를 테스트 해볼 수 있다.

### 4장 목 객체를 이용한 상호작용 테스트

상호 작용 테스트 - '상호 작용 테스트(Inerraction test)'란, 한 객체가 어떻게 다른 객체로 입력을 전달하거나 입력을 받는지, 즉 객체가 어떻게 다른 객체와 상화작용하는 지 검사하는 테스트다.e

'동작 주도 테스트(action-driven testing)' vs '결과 주도 테스트(result-driven testing)'

목 객체 - '목 객체(mock object)'란, 시스템 내부에서 단위 테스트의 통과 또는 실패 여부를 판단하는 가짜 객체를 말한다. 목 객체는 가짜 객체를 이용해 테스트 대상 객체가 올바른 방식으로 상호작용했는지 검증한다. 대개 테스트당 하나의 목 객체만 사용한다.

### 5장 격리(목 객체) 프레임 워크

격리 프레임 워크 - '격리 프레임워크(isolation framework)'란, 목과 스텁 객체를 훨씬 쉽게 생성할 수 있게 해주는 API들의 모음이다. 격리 프레임워크를 이용하면 개발자들이 객체의 상호작용을 테스트하거나 시뮬레이션하기 위해 코드를 반복 작성하는 일을 줄일 수 있다.

#Etc

프로젝트 설치 가이드 사이트  
https://www.kdata.or.kr/info/info_04_view.html?field=&keyword=&type=techreport&page=26&dbnum=181181&mode=detail&type=techreport
