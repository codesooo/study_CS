# TCP/IP 4 계층
![Alt text](../images/tcp-ip.png)

## TCP/IP 4 계층
- 정의 : 네트워크 통신을 위한 프로토콜을 계층적으로 나눈 것

### <span style='color:#33ccff;'>1계층 (Network Access Layer)</span>
- MAC Address : 물리적인 네트워크와의 상호작용을 위함
- OSI 7계층의 데이터 링크 계층 + 물리 계층을 합친 것
- 장비 : L2 스위치

### <span style='color:#33ccff;'>2계층 (Internet Layer)</span>
- 논리적인 네트워크와의 상호작용을 위함
- IP : 통신자의 호스트를 식별하기 위함
- 장비 : L3 스위치, 라우터

### <span style='color:#33ccff;'>3계층 (Transport Layer)</span>
- 종단간 통신을 관리
- TCP/UDP : 연결지향(TCP) 및 비연결지향(UDP) 관련 통신 프로토콜

### <span style='color:#33ccff;'>4계층 (Application Layer)</span>
- 최종 사용자에게 서비스를 제공하는 계층
- HTTP, FTP, SMTP 등..
- 장비 : 앱 등

## 웹 동작 방식 (만약, www.naver.com을 검색 했다면?)
![Alt text](image-1.png)

1. 우리 브라우저는 www.naver.com의 주소(IP)를 모른다. 따라서, DNS 서버에 해당 도메인의 IP주소를  요청한다. (DNS 서버에서 요청에 도메인에 대한 캐싱이 되어있으면, 해당 아이피를 반환하고, 그렇지 않으면 DNS Query를 통한 네이버 주소를 가져온다.)
2. DNS 서버로부터 IP주소를 얻어 온다.
3. TCP 연결을 맺고, TCP Connection을 생성한다. (3-way-hand-shaking)
4. 클라이언트(=브라우저)는 HTTP 프로코톨을 통해 데이터를 요청한다.
5. 서버는 클라이언트 요청에 대한 응답을 반환한다. (ex: html, css, javascript)
6. 브라우저는 얻어온 데이터를 렌더링 한다.
7. 필요에 따라 TCP Connection을 해제한다.