![](https://images.velog.io/images/sinichy7/post/af104cb2-2cd4-4f1b-9fc6-bb00187a9d9c/image.png)

# 1. OSI 7계층

(사용자와 가까운 위의 계층)
1. application
2. presentation
3. session
4. transport
5. network
6. datalink
7. physical

---

# 2. TCP / IP 4계층
(1~3) application
(4) transport
(5) internet
(6~7) network

- clien에서 server에 요청하면 위의 4단계를 거쳐서 서버로 이동하여 역으로 다시 가는 것.

- data를 보내면 transport, internet에서 추가 정보를 붙여서 같은 구역에서 정보가 붙은 것을 까면서 서버로 올라간다는 것.

# 3. TCP와 UDP와의 비교

- TCP/IP는 transfer 부분에서 전송계층이 일어난다.

#### 1. 순차전송
- TCP는 데이터를 자르고 추가 정보를 붙인다.
- 순차적으로 조합한다.
- 어그러질 가능성 있기에 받는 쪽도 순차적 조합하는 것 있다.-> 데이터 완전성 보장 vs UDP는 막 보낸다.
> e.g tcp는 물을 입에 넣는 것이고, udp는 물을 그냥 들이 붙는다. 그래서 속도 차이가 난다.

#### 2. Three ways handshake(오픈) : 

**데이터 보낼건데 괜찮니?(수락 과정)**

(client)  syn -> (server) : 잘 들려?
(client)  <- syn, ack (server) : 어 잘 들려, 너도 잘 들리니?
(client)  ack + 패킷-> (server) : 어 잘 들려!

#### 3. Four ways handshake(클로즈) : 

**이제 다 보냈는데 닫아줄래?(닫는 과정)**
(client) fin -> (server) : 이제 전송 다 했어!
(client) <- ack (server) : 알겠어!, 잠깐 기다릴게!
(client) <- fin (server) : 통신이 끝났구나!
(client) ack -> (server) : 끝남 메시지 확인했어! + 연결 close + 서버가 안 준 데이터 있을지 모르니 기다리자.

#### 4. Error Detection
- TCP는 흐름문제, 혼잡문제 생기면 데이터를 다시 보낸다. 처음부터 다시 보낸다.

- 근데 UDP는 그런거 없다.
- 데이터도 app계층에서 잘라야한다.(tcp는 tcp가 자른다.)
- 3ways니 뭐니 없이 바로 소켓 열린 상태로 바로 받는다.(미리 열린 소켓)

> 문제 : 순차 전송, 흐름문제, 혼잡문제 전혀.. 데이터가 완벽하지 않다. 비슷하게만 맞는 방식이라면 선호되는 방식 ; 스트리밍 서비스
