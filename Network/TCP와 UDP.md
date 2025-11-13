# TCP와 UDP

TCP와 UDP는 전송 계층(4계층)에서 사용되는 프로토콜로, TCP는 신뢰성을 보장하는 연결 지향형이고, UDP는 빠른 전송을 위한 비연결형 프로토콜이다.

<br>

## TCP/IP 전송계층

전송 계층(Transport Layer)은 종단 간(end-to-end) 통신을 제공한다.
대표적인 프로토콜로 [TCP](#tcp)와 [UDP](#udp)가 있다.
TCP/IP 전송계층은 포트 번호를 사용하여 각 애플리케이션을 구분한다.

<br>

## TCP

TCP(Transmission Control Protocol)은 연결 지향형 프로토콜이다.

[TCP 3 Way Handshake](TCP%203%20Way%20Handshake%20&%204%20Way%20Handshake.md)를 통해 연결을 수립하고, TCP 헤더에 번호(Sequence Number)를 부여하여 잘 전송되었는지 신뢰성을 보장하도록(오류제어, 흐름제어, 혼잡제어 등) 하여 속도가 느리다.

세그먼트(Segment)를 전송 단위로 사용하며, 세그먼트는 **TCP 헤더와 데이터의 결합**을 의미한다.

<mark style="background: #FFF3A3A6;">파일 전송</mark>과 같은 신뢰성이 중요한 서비스에 사용됨.

<img width="2970" height="2112" alt="image" src="https://github.com/user-attachments/assets/30369d51-f833-44d3-a60d-120ebb31d166" />


여담 : 카서스 궁과 같음. 느리지만 확실하게 보내줌.

> 신뢰성, 연결지향, 순차 전송, 느림

<br>

## UDP

UDP(User Datagram Protocol)는 비연결형 전송 프로토콜이다.

TCP와 다르게 신뢰성을 보장하지 않으며, 속도가 빠르다. (오류제어, 흐름제어, 혼잡제어를 제공하지 않으며 간단함.)

데이터그램(Datagram)을 전송 단위로 사용하고, 데이터그램은 **UDP 헤더와 데이터의 결합**을 의미한다.

속도가 빠르기 때문에 <mark style="background: #FFF3A3A6;">실시간 스트리밍, RTP</mark>와 같이 연속성이 중요한 서비스에 사용됨.

<img width="2970" height="1136" alt="image" src="https://github.com/user-attachments/assets/ecd75400-f971-42c4-82d0-5125d3e49a14" />


여담 : 럭스 궁이라고 생각. 빠르지만 빗나갈 수 있음.

> 비신뢰성, 비연결형, 빠름

<br>

## TCP vs UDP 비교

| 구분          | TCP                             | UDP                     |
| ------------- | ------------------------------- | ----------------------- |
| 연결 방식     | 연결 지향 (Connection-oriented) | 비연결 (Connectionless) |
| 신뢰성        | 보장 (재전송, 순서 보장)        | 미보장                  |
| 전송 단위     | 세그먼트 (Segment)              | 데이터그램 (Datagram)   |
| 속도          | 느림                            | 빠름                    |
| 헤더 크기     | 20~60바이트                     | 8바이트                 |
| 흐름/혼잡제어 | O                               | X                       |
| 사용 예시     | HTTP, 파일 전송                 | 스트리밍, 게임          |
