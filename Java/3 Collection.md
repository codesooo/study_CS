## JCF (Java Collection Framework)
자바는 널리 알려져 있는 `자료구조`를 바탕으로 객체들을 효율적으로 관리할 수 있도록 
관련된 interface와 class들을 `java.util` 패키지에 모아놓았다.

<br>

JCF는 몇 가지 interface를 통해서 다양한 collection class를 이용할 수 있도록 설계되어 있다.

<br>
주요 interface로는 List, Set, Map이 있다. 
이 interface로 사용 가능한 Collection 객체의 종류는 다음과 같다.


![image](https://github.com/DevTechGrowth/study_CS/assets/88030238/4d4c31fc-4b7b-4260-b878-0e6602c27e2b)

List와 Set은 객체를 추가, 삭제, 검색하는 방법에 있어서 공통점이 있다. <br>
-> 공통된 메소드를 따로 모아 Collection interface로 정의해두고, 이것을 상속하고 있다.  <br>
Map은 키와 값을 하나의 쌍으로 묶어서 관리하는 구조로, List와 Set과는 사용 방법이 다르다. 

![image](https://github.com/DevTechGrowth/study_CS/assets/88030238/a6aa8a2c-8e61-40d3-90f5-2e037769a070)


## List Collection
- 객체를 index로 관리
  - index를 통해 객체를 검색·삭제
    
### ArrayList
- List 컬렉션에서 가장 많이 사용됨
- ArrayList에 객체를 추가하면 내부 배열에 객체가 저장됨
- 일반 배열과 다르게 제한 없이 객체를 추가 자능
- List 컬렉션은 객체 자체를 저장하는 것이 아니라 객체의 번지를 저장


### Vector
- ArrayList와 동일한 내부 구조
    - 차이점 : Vector는 동기화된 메소드로 구성되어 있어 멀티 스레드가 동시에 Vector() 메소드를 실행할 수 없다.
      → 멀티 스레드 환경에서는 안전하게 객체를 추가 or 삭제할 수 있다.
![image](https://github.com/DevTechGrowth/study_CS/assets/88030238/404c8875-f791-4f06-a49f-27bfb1813047)

### LinkedList
- ArrayList는 내부 배열에 객체를 저장
- LinkedList는 인접 객체를 체인처럼 연결하여 관리
![image](https://github.com/DevTechGrowth/study_CS/assets/88030238/b0b13c00-bcb1-44c6-9c73-028d916c9318)

![image](https://github.com/DevTechGrowth/study_CS/assets/88030238/b6077dc4-a8db-47d8-8ca2-9c47f4f5d2a7)

특정 위치에서 객체 삽입,삭제할 때 바로 앞뒤 링크만 변경하면 됨.
-> 빈번한 객체 삭제,삽입이 일어나는 곳에서 ArrayList 보다 더 좋은 성능을 발휘함

## Set Collection
### Hashset
### SortedSet
### TreeSet


## Map Collection
### HashMap
### Hashtable
### Properties
### TreeMap
