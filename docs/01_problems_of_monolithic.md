# 전통적인 계층형 아키텍처의 문제점

전통적인 계층형 아키텍처는 코드에 나쁜 습관들이 스며들기 쉽게 만들고 시간이 지날수록 소프트웨어를 점점 더 변경하기 어렵게 만드는 수많은 허점들을 노출한다.

1. 계층형 아키텍처는 데이터베이스 주도설계를 유도한다.
2. 지름길을 택하기 쉬워진다.
3. 테스트하기 어려워진다.
4. 유스케이스를 숨긴다.
5. 동시 작업이 어려워진다.

## 1. 계층형 아키텍처는 데이터베이스 주도설계를 유도한다. 

데이터베이스 주도설계? 당연한 말이지 않은가? 결국에 어떠한 문제 영역을 해결하기 위해 개발을 한다면 데이터베이스를 중심으로 개발을 할 수 밖에 없지 않은가 싶었다. 왜냐하면 도메인 로직이나 비지니스 로직에서 핸들링하는 것도 결국 데이터베이스에서 원하는 데이터를 조회하여야 한다. 그러므로 데이터베이스의 테이블 설계가 중요하고 테이블 구조만 보아도 어떤 문제 영역을 해결하고자 하는지 알 수 있도록 설계하는 것이 중요하고 결국 첫 시작은 데이터베이스이기 때문에 데이터베이스 주도설계가 당연하다고 생각했다. 

그러나 책에서 바라보는 관점은 완전 달랐다. 책에서 바라보는 비즈니스 관점에서는 데이터베이스 주도설계인 계층형 아키텍처는 합리적이지 않았다. 도메인 중심으로 설계된 애플리케이션은 도메인 로직을 먼저 만들어야하고 그래야만 우리가 로직을 제대로 이해했는지 확인할 수 있으며 이를 기반으로 영속성 계층과 웹 계층을 만들어야 한다는 것이다. 어느정도 이해가 되었지만 완벽하게 공감되는 것은 이니다. 아마 내가 아직 도메인 설계에 경험이 없고 서비스 중심적인 개발을 경험해보지 않았기 때문에 아직 어색하다고 느껴지는것 같다.

## 2. 지름길을 택하기 쉬워진다.

전통적인 계층형 아키텍처에서 전체적으로 유일한 규칙은, 특정한 계층에서는 같은 계층에 있는 컴포넌트나 아래에 있는 계층에서만 접근 가능하다는 것이다. 따라서 만약 상위 계층에 위치한 컴포넌트에 접근해야 한다면 간단하게 컴포넌트를 계층 아래로 내려버리면 된다. 그러면 접근 가능하게 되고, 깔끔하게 해결된다.

이렇게 책에서 말하는 지름길을 택하는 상황은 매우 공감이 된다. 실제로 그렇게 코딩된 레거시 코드도 보았다. 그리고 거기에 신규 기능을 넣는 나도 이미 택한 지름길을 똑같이 따라가게 되었다. 이유는 딱히 없었다. 그저 그렇게 해서 나도 똑같이 했을뿐... 책에서 말하는 '깨진 창문 이론'이 내 이야기를 하는 것 같았다.

### 3. 테스트하기 어려워진다.



### 4. 유스케이스를 숨긴다.



### 5. 동시 작업이 어려워진다.
