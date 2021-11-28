# 객체지향 디자인
- 이 세상은 순차적이다. 또한 세상은 객체지향적이기도 하다.

## 1.1 디자인 예찬
- 최종적으로 만들려는 애플리케이션이 소프트웨어가 만들어지는 진짜 이유다.
- 객체지향 디자인 기법은 프로그래밍의 윤리적/기술적 이율배반을 해소해 줄 수 있다.
- 이런 디자인을 통해 비용-효율적인 소프트웨어를 만들 수 있다.

### 1.1.1 디자인이 해결해 줄 수 있는 문제들
- 코드를 한번 작성하고 애플리케이션이 절대 바뀌지 않는다면 디자인은 중요치 않다.
- 불행히도 무언가는 분명 변한다. 변화는 어디에나 있고 모든 곳에 있으며 피할 수 없다.
- 쉽게 변경할 수 있는 애플리케이션을 짜는 과정도 즐겁고 확장하는 과정도 즐겁다.
- 변화를 주기 힘든 애플리케이션은 정확히 그 반대다. 수정을 하려면 많은 시간이 필요하고 하나를 수정하면 다음번 수정이 어려워져 즐겁게 작업할 수도 없다.

### 1.1.2 왜 수정은 어려운가
- 객체지향 애플리케이션은 상호작용하는 여러 부분으로 구성되어 있고, 상호작용은 객체가 주고받는 메시지 속에 녹아 있다.
- 수신하는 객체에 대한 이 지식이 두 객체 사이의 의존성을 만들어 내고. 이런 의존성이 애플리케이션을 수정하기 어렵게 만든다.
- 객체지향 디자인은 의존성을 관리하는 것이고 의존성을 정리하는 코딩 기술의 묶음이다. 관리되지 않은 의존성은 재앙을 불러온다.
- 객체가 너무 많은 것을 알면 세상에 바라는 것도 많아진다. 까다롭게 굴고 모든 것이 그냥 그대로이길 바란다.

### 1.1.3 디자인의 실용적 정의
- 디자인의 어려움 중 하나는 모든 문제가 두 부분으로 구성되어 있다는 점이다. 오늘 완성해야 하는 기능을 구현하는 코드를 짜야하고, 동시에 내일 쉽게 바꿀 수 있는 코드를 짜야한다.
- 디자인은 나중에 디자인할 수 있는 여지를 남겨 놓기 위한 것이고, 그 최종 목표는 변화의 비용을 최소화하는 것이다.
- 디자인은 미래를 추측하지 않는다.

---

## 1.2 디자인 도구들
- 디자인은 정해진 법칙을 따르는 활동이 아니다.

### 1.2.1 디자인 원칙들
- [SOLID](https://ko.wikipedia.org/wiki/SOLID_(%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%EC%84%A4%EA%B3%84)) 객체지향 디자인의 잘 알려진 디자인 원칙 다섯가지
  - 단일 책임(Single Responsibility)
  - 개방-폐쇄(Open-Closed)
  - 리스코프 치환(Liskov Substitution)
  - 인터페이스 분리(Interface Segregation)
  - 의존성 역전(Dependency Inversion)
- [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) (Don’t Repeat Yourself)
- [LoD](https://en.wikipedia.org/wiki/Law_of_Demeter) (the Law of Demeter)

### 1.2.2 디자인 패턴
- 객체지향 디자인은 원칙뿐만 아니라 패턴을 갖고 있다.
- 디자인 패턴은 객체지향 소프트웨어 디자인에서 명확한 문제를 처리하는 간단하고도 우아한 해결책

---

## 1.3 디자인하기

### 1.3.1 디자인은 어떻게 실패하는가
- 디자인이 없는 애플리케이션은 붕괴의 씨앗을 품고 있다.
- 지나치게 디자인하는 함정에 빠질 수 있다. 이런 프로그래머들은 다음과 같이 말한다. “새로운 기능을 추가할 수 없어 처음부터 그렇게 디자인되지 않았다고”
- 애자일 소프트웨어 개발운동은 잘 디자인된 애플리케이션을 만드는데 매우 적합하다.

### 1.3.2 언제 디자인을 해야 하나
- 애자일의 경험은 고객과의 혐업 과정을 통해 만들어진 결과물이 처음 상상했던 것과 사뭇 다르다는 사실을 보여준다.
- 애자일이 올바른 방식을 취하고 있단 사실
  - BUFD(Big Up Front Design)을 취할 이유가 하나도 없다.
  - 애플리케이션이 완성되는 시점을 누구도 예상할 수 없다.
- BUFD방식은 고객과 프로그래머를 서로 대립하게 만든다.
- 애자일 작업방식은 변화를 보장한다.
- 애자일은 디자인을 필요로한다.

### 1.3.3 디자인 평가하기
- ‘코드 줄 수‘를 확인하는 방법은 쓸모가 없어졌고 그 자리를 ‘객체지향 디자인 점수’ 가 대신하는 주장을 조심스럽게 받아들여야한다.
- 디자인에 얼마나 시간과 돈을 쓸지 결정하기 위해선 두 가지를 고려해야한다.
  - 기술 수준
  - 시간

---

## 1.4 객체지향 프로그래밍에 대한 간략한 소개
객체지향 애플리케이션은 객체와 객체가 서로 주고 받는 메시지로 구성되어 있다.

### 1.4.1 절차적 언어들
- 데이터와 행동은 전혀 다른 것이다.
- 데이터는 변수 속에 갇혀 있고, 행동은 이 데이터를 들여다 볼수 있다.
- 데이터에게 무슨 일이 벌어질지 예측할 수 없고, 대부분 추적할 수도 없다.

### 1.4.2 객체지향적 언어들
- 객체는 행동을 가지고 있고, 데이터를 가지고 있을 수도 있다.
- 객체는 메시지 전송을 통해 상대의 행동을 실행시킨다.
- 모든 객체는 자신의 데이터를 외부세계로부터 캡슐화시켜 놓는다.

---

## 1.5 요약
- 애플리케이션의 가장 큰 문제는 변화를 받아들이는 것이다.
- 우리는 변화를 받아들일 수 있는 개발을 해야한다.
- 디자인은 변화를 손쉽게 받아들일 수 있도록 코드를 배치하는 일이다.