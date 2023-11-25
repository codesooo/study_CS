## JCF (Java Collection Framework)
JAVA는 널리 알려져 있는 `자료구조`를 바탕으로 객체들을 효율적으로 관리할 수 있도록 
관련된 interface와 class들을 `java.util` 패키지에 모아놓았다.

<br>

**JCF**는 몇 가지 interface를 통해서 다양한 collection class를 이용할 수 있도록 설계되어 있다.

<br>

주요 interface로는 **`List`**, **`Set`**, **`Map`** 이 있다. 
이 interface로 사용 가능한 Collection 객체의 종류는 다음과 같다.

<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/4d4c31fc-4b7b-4260-b878-0e6602c27e2b" width="50%" height="50%">


`List`와 `Set`은 객체를 추가, 삭제, 검색하는 방법에 있어서 공통점이 있다. <br>
-> **공통된 메소드**를 따로 모아 **`Collection interface`** 로 정의해두고, 이것을 상속하고 있다.  <br>
`Map`은 `키`와 `값`을 하나의 쌍으로 묶어서 관리하는 구조로, List와 Set과는 사용 방법이 다르다. 

<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/a6aa8a2c-8e61-40d3-90f5-2e037769a070" width="70%" height="70%">


## List Collection
- 객체를 `index`로 관리
  - index를 통해 객체를 검색·삭제
    
### ArrayList
- List 컬렉션 중에서 가장 많이 사용됨
- `ArrayList`에 객체를 추가하면 **내부 배열**에 객체가 저장됨
- 일반 배열과 다르게 **제한 없이** 객체를 추가 자능
- List 컬렉션은 객체 자체를 저장하는 것이 아니라 **객체의 번지**를 저장


### Vector
- `ArrayList`와 동일한 내부 구조
    - **`차이점`** : Vector는 동기화된 메소드로 구성되어 있어 멀티 스레드가 동시에 Vector() 메소드를 실행할 수 없다.
      → 멀티 스레드 환경에서는 안전하게 객체를 추가 or 삭제할 수 있다.
      
<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/404c8875-f791-4f06-a49f-27bfb1813047" width="40%" height="40%">

### LinkedList
- **`ArrayList`** : **내부 배열**에 **객체**를 저장
- **`LinkedList`** : **인접 객체**를 체인처럼 **연결**하여 관리

<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/b0b13c00-bcb1-44c6-9c73-028d916c9318" width="40%" height="40%">
<br>
<br>

특정 위치에서 객체 삽입,삭제할 때 바로 앞뒤 링크만 변경하면 됨.
-> 빈번한 객체 삭제,삽입이 일어나는 곳에서 **ArrayList 보다 더 좋은 성능을 발휘**함
<br>

<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/b6077dc4-a8db-47d8-8ca2-9c47f4f5d2a7" width="40%" height="40%">

## Set Collection
- Set 컬렉션은 저장 순서가 유지되지 않음
- 객체 중복 저장 불가능
- 하나의 null만 저장 가능

### Hashset
- Set 컬렉션 중 가장 많이 사용됨
- 다른 객체라도 동일한 객체라고 판단하고 중복 저장하지 않는 경우
  - hashCode() 메소드의 리턴값이 같고, equals() 메소드가 true를 리턴할 때

<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/1a3df694-77fd-4def-9f86-f2a4482d061f" width="40%" >

### SortedSet
### TreeSet
- binary tree를 기반으로 한 Set 컬렉션
- TreeSet에 객체를 저장하면 다음과 같이 자동으로 정렬됨
- 부모 노드의 객체와 비교
  - 왼쪽 자식 노드 : 낮은 것
  - 오른쪽 자식 노드 : 높은 것
<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/d9d65bb0-e00a-433b-a865-e0607dc68a53" width="40%" >


## Map Collection
- `key`와 `value`으로 구성된 entry 객체를 저장한다.
  - key, value는 객체
  - key : 중복 저장 불가능
  - value : 중복 저장 가능
- 기존에 저장된 key와 동일한 key로 value를 저장하면 기존의 value는 없어지고 새로운 value로 대치된다.

<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/bf285f11-f0c6-4e31-90ee-871f9dfdac34" width="40%" height="70%">

### HashMap
- 동일 key로 보고 중복 저장을 허용하지 않는 경우
  - `key`로 사용할 `객체`가 hashCode() 메소드의 리턴값이 같고 equals() 메소드가 true를 리턴할 때
<img src="https://github.com/DevTechGrowth/study_CS/assets/88030238/1d1162d0-eedc-42dc-abb0-79b5acb37199" width="40%" height="70%">

### Hashtable
- HashMap과 동일한 내부구조


### Properties
- Hashtable의 자식 클래스
  - Hashtable의 특징을 그대로 가짐
- key와 value를 String 타입으로 제한한 컬렉션
- 확장자가 `.properties`인 프로퍼티 파일을 읽을 때 사용
  - 프로퍼티 파일 : `=`기호로 연결되어있는 텍스트 파일
  
### TreeMap
- binary tree 기반 Map 컬렉션
- TreeSet과의 차이점 : key와 value가 저장된 Entry를 저장
- Entry를 저장하면 key를 기준으로 자동 정렬
  - 왼쪽 자식 노드 : 낮은 것
  - 오른쪽 자식 노드 : 높은 것
