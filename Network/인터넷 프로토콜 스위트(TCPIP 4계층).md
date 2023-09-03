# 인터넷 프로토콜 스위트(TCP/IP)
## TCP/IP 4계층 모델
- **인터넷 프로토콜 스위트(Internet Protocol Suite)는 인터넷에서 컴퓨터들이 서로 정보를 주고받는 데 쓰이는 프로토콜의 집합이며, 이를 TCP/IP 4계층 모델 혹은 OSI 7계층 모델로 설명함**
- TCP/IP는 TCP(Transmission Control Protocol)과 IP(Internet Protocol)를 묶어서 부르는 명칭
- TCP/IP 4계층 모델은 프로토콜의 네트워킹 범위에 따라 네 개의 추상화 계층으로 구성됨

## 계층 구조
- TCP/IP 계층은 OSI 7계층과 많이 비교됨
- ![image](https://github.com/BBOMS9105/CS/assets/124663932/388cf3cb-71d8-46c2-b279-d195e721b067)
  - TCP/IP 계층과 달리 OSI 계층은 애플리케이션 계층을 세 개로 쪼개고 링크 계층을 데이터 링크 계층, 물리 계층으로 나눠서 표현하는 것이 다르며, 인터넷 계층을 네트워크 계층으로 부른다는 차이점이 있음
  - 이 계층들은 특정 계층이 변경되었을 때 다른 계층이 영향을 받지 않도록 설계되어있음
    - TCP를 UDP로 변경했다고 해서 인터넷 웹 브라우저를 다시 설치해야 하는 것은 아니듯 유연하계 설계됨
    - ![image](https://github.com/BBOMS9105/CS/assets/124663932/91666276-56d4-4c6a-871f-3e45141553b0)
      - ▲ 각 계층을 대표하는 스택
- **애플리케이션 계층**
  - 애플리케이션(Application) 계층은 FTP, HTTP, SSH, SMTP, DNS 등 응용 프로그램이 사용되는 계층이며 웹 서비스, 이메일 등 서비스를 실질적으로 사람들에게 제공하는 층
  - FTP : File Transfer Protocol. 장치와 장치 간의 파일을 전송하는 데 사용되는 표준 통신 프로토콜
  - SSH : Secure Shell. 보안되지 않은 네트워크에서 네트워크 서비스를 안전하게 운영하기 위한 암호화 네트워크 프로토콜
  - HTTP : HyperText Transfer Protocol. World Wide Web을 위한 데이터 통신의 기초이자 웹 사이트를 이용하는데 쓰는 프로토콜
  - SMTP : Simple Mail Transfer Protocol. 전자 메일 전송을 위한 인터넷 통신 프로토콜
  - DNS : Domain Name Server. 도메인 이름과 IP 주소를 매핑해주는 서버
    - www.google.com에 DNS 쿼리가 오면 [Root DNS] -> [.com DNS] -> [.naver DNS] -> [.www DNS] 과정을 거쳐 완벽한 주소를 찾아 IP 주소를 매핑한다
    - 이를 통해 서비스의 IP주소가 바뀌어도 사용자들은 똑같은 도메인 주소로 접속할 수 있다.
- **전송 계층**
  - 전송(transfer) 계층은 송신자와 수신자를 연결하는 통신 서비스를 제공하며 연결 지향 데이터 스트림 지원, 신뢰성, 흐름 제어를 제공할 수 있으며 애플리케이션과 인터넷 계층 사이의 데이터가 전달될 때 중계 역할을 함
  - 대표적으로 TCP와 UDP가 있다
  - TCP(Transmission Control Protocol)
    - TCP는 패킷 사이의 순서를 보장하고 연결지향 프로토콜을 사용해서 연결을 해 신뢰성을 구축해서 수신 여부를 확인함
    - 가상회선 패킷 교환 방식 사용
      - 각 패킷에는 가상회선 식별자가 포함되며 모든 패킷을 전송하면 가상회선이 해제되고 패킷들은 전송된 순서대로 도착하는 방식
  - UDP(User Datagram Protocol)
    - UDP는 순서를 보장하지 않고 수신 여부를 확인하지 않으며 단순히 데이터만 전달
    - 데이터그램 패킷 교환 방식 사용
      -패킷이 독립적으로 이동하며 최적의 경로를 선택하여 가는데, 하나의 메시지에서 분할된 여러 패킷은 서로 다른 경로로 전송될 수 있으며 도착한 순서가 다를 수 있는 방식
    
      
