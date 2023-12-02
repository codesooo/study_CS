||TCP|UDP|
|--|---|---|
||Transmission Control Protocol|User Datagram Protocol|
||TCP(패킷을 추적, 관리) </br>IP(데이터의 배달)|데이터를 데이터 그램 단위로 처리하는 프로토콜|
|연결 방식|연결 지향형 프로토콜|비연결 프로토콜|
|패킷 교환|가상 회선 방식|데이터그램 방식|
|전송 순서|보장O|보장X|
|신뢰성|높음|낮음|
|전송속도|느림|빠름|
|특징|- 연결: 3-way handshake</br>- 해제: 4-way handshake||
|장점|신뢰성 보장(흐름제어, 혼잡제어, 오류제어)|네트워크 부하가 적음|
|단점|- 데이터 보내기 전에 반드시 연결 필요</br>- 1:1통신반 가능</br>- 고정된 통신 선로가 최단선이 아닐 경우 상대적으로 UDP보다 전송속도가 느림|- 신뢰성 보장X</br>- 의미있는 서버를 구축하기 위해 일일이 패킷 관리 필요|


### [TCP와 UDP의 차이에 대해 설명해 주세요.](https://github.com/VSFe/Tech-Interview/blob/main/03-NETWORK.md#7-tcp%EC%99%80-udp%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%97%90-%EB%8C%80%ED%95%B4-%EC%84%A4%EB%AA%85%ED%95%B4-%EC%A3%BC%EC%84%B8%EC%9A%94)
- 왜 HTTP는 TCP를 사용하나요?
  - [HTTP란? HTTP와 TCP의 연관성은 무엇일까?](https://stitchcoding.tistory.com/24)
  - HTTP : TCP를 기반의 어플리케이션 레이어에 속하는 프로토콜. 
    - 데이터의 형식과 절차에 관련된 프로토콜(규약)
      - <규약 특징>
      - Request(요청) & Response(응답)의 형태
      - TCP 위에서 동작
      - stateless : 상태를 기록하지 않음
      - 
- 그렇다면, 왜 HTTP/3 에서는 UDP(QUIC) 를 사용하나요? 위에서 언급한 UDP의 문제가 해결되었나요?
  - [HTTP/3는 왜 UDP를 선택한 것일까?](https://evan-moon.github.io/2019/10/08/what-is-http3/)
  - 
- 본인이 새로운 통신 프로토콜을 TCP나 UDP를 사용해서 구현한다고 하면, 어떤 기준으로 프로토콜을 선택하시겠어요?
- Checksum이 무엇인가요?
  - 체크섬 = 중복 검사의 한 형태. 오류 정정으로 송신된 자료의 무결성 보장
  - [TCP - Checksum](https://nogan.tistory.com/21)
- TCP와 UDP 중 어느 프로토콜이 Checksum(중복검사)을 수행할까요?
  - TCP. 
  - [TCP - Checksum](https://nogan.tistory.com/21)
- 그렇다면, Checksum을 통해 오류를 정정할 수 있나요?
- TCP가 신뢰성을 보장하는 방법에 대해 설명해 주세요.
- TCP의 혼잡 제어 처리 방법에 대해 설명해 주세요.


---
## 참고자료

[Ready-For-Tech-Interview-TCP](https://github.com/WooVictory/Ready-For-Tech-Interview/blob/master/Network/TCP.md)

[Ready-For-Tech-Interview-UDP](https://github.com/WooVictory/Ready-For-Tech-Interview/blob/master/Network/UDP.md)

[Tech-Interview](https://github.com/VSFe/Tech-Interview/blob/main/03-NETWORK.md)

[@jmxx219 CS-Study](https://github.com/jmxx219/CS-Study/blob/main/Network/TCP%EC%99%80%20UDP.md)

[@workhardslave CS-Study](https://github.com/workhardslave/cs-study/blob/main/Network/TCP%20vs%20UDP.md)

[[TCP/UDP] TCP와 UDP의 특징과 차이](https://velog.io/@devharrypmw/TCPUDP-TCP%EC%99%80-UDP%EC%9D%98-%ED%8A%B9%EC%A7%95%EA%B3%BC-%EC%B0%A8%EC%9D%B4)
