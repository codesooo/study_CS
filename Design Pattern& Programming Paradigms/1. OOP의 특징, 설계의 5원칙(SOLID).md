# OOP의 특징, 설계의 5원칙(SOLID)
## **객체 지향 프로그래밍란?**
- 객체 간의 상호작용을 통해 프로그래밍하는 방식
  
객체란?
- 상태(=변수)와 행위(=메소드)를 정의한 클래스의 인스턴스
<br/>
<img src="https://github.com/DevTechGrowth/study_CS/assets/108642272/bdcd8805-79bc-484d-8358-63f2d13785ab">

절차 지향 프로그래밍

- 실행 순서에 따라 프로그래밍하는 방식
<img src="https://github.com/DevTechGrowth/study_CS/assets/108642272/34abde7c-c636-42e2-8717-7f255e5cce1e">

## **객체지향언어의 장단점**
- 장점
    1. **재사용성** : 상속을 통해 프로그래밍시 코드의 재사용을 높일 수 있음.
    2. **생산성 향상** : 잘 설계된 클래스를 만들어서 독립적인 객체를 사용함으로써 개발의 생산성을 향상시킬 수 있음.
    3. **자연적인 모델링** : 우리 일상생활의 모습의 구조가 객체에 자연스럽게 녹아들어 있기 때문에 생각하고 있는 것을 그대로 자연스럽게 구현할 수 있다.
    4. **유지보수의 우수성** : 프로그램 수정시 추가, 수정을 하더라도 캡슐화를 통해 주변 영향이 적기때문에 유지보수가 쉬워서 매우 경제적이라할 수 있다.
- 단점    
    1) **실행 속도** : 객체지향언어는 상대적으로 실행 속도가 느림.    
    2) **프로그램 용량이 큼** : 객체 단위로 프로그램을 많이 만들다보면, 불필요한 정보들이 같이 삽입될 수 있고, 이는 프로그램의 용량 증가로 이어질 수 있음    
    3) **설계에 많은 시간 소요** : 클래스별로, 객체별로 설계하고, 상속 등의 구조 또한 설계하여야 하기 때문에, 설계단계부터 많은 시간이 소모

## **SOLID 원칙**
<img src="https://github.com/DevTechGrowth/study_CS/assets/108642272/76282c89-aa46-448f-afdc-c5e798ba73b7">

1. **Single Responsibility Principal(단일 책임 원칙)**
    - 한 클래스는 하나의 책임만 가져야한다.
    <br/>
2. **Open-Closed Principal (개방-폐쇄 원칙)**
    - 확장에는 열려 있고, 변경에든 닫혀 있어야 한다.
   <br/>
    - <img src="https://github.com/DevTechGrowth/study_CS/assets/108642272/ce44e05a-c280-428c-b345-db6b5267f9e4">
    <br/>
3. **Liskov Substitution Principal (리스코프 치환 원칙)**
    - 상위 타입으로 하위타입의 인스턴스를 제어할 수 있어야 한다.
   <br/>
4. **Interface segregation principal (인터페이스 분리 원칙)**
    - 사용하지 않는 인터페이스는 구현하지 않아야 한다.
    <br/>
    <img src="https://github.com/DevTechGrowth/study_CS/assets/108642272/900f8560-3f66-45a1-8c0b-d6b6b045a8b5">
    <br/>
5. **Dependency Inversion Principal (의존관계 역전의 원칙)**
    - 추상화에 의존해야하고, 구체적인 구현에 의존하면 안된다.
