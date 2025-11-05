# OSI 7계층

OSI 7계층 모델(OSI 7Layer)은 국제 표준화 기구(ISO)에서 네트워크 통신을 7개의 논리적인 계층으로 나눈 네트워크 참조 모델

7계층으로 나누면 통신이 일어나는 과정을 단계별로 알 수 있고, 문제가 발생했을 때 특정 계층으로 문제를 좁힐 수 있어 그 부분만 수정할 수 있음.

## OSI 7 계층 구조

<img width="713" height="768" alt="image" src="https://github.com/user-attachments/assets/a997bf1b-e025-4ccf-88c5-34d12a7e7c90" />

###### 이미지 출처: Bluecat Networks

OSI 7계층은 다시 두 가지 계층으로 나눌 수 있음.

- 1~4 계층 : 데이터 플로 계층(Data Flow Layer) / 하위 계층(Lower Layer)
- 5~7 계층 : 애플리케이션 계층(Application Layer) / 상위 계층(Upper Layer)

<mark style="background: #FFF3A3A6;">프로토콜(Protocol)</mark>이란 통신을 하기 위한 규정이나 규약을 의미함.

<br>

### 1. 물리 계층

1계층은 물리 계층(Physical Layer)으로 물리적 연결과 관련된 정보를 정의한다.

- 들어온 전기 신호를 그대로 잘 전달하는 것이 목적으로 **비트(Bit)를 전기 신호로 변환하여 물리적 매체를 통해 전달하는 역할**을 한다.

> 주요 장비 : 허브(Hub), 리피터(Repeater), 케이블(Cable), 커넥터(Connecter) 등

<br>

### 2. 데이터 링크 계층

2계층은 데이터 링크 계층(Data Link Layer)으로 전기 신호를 우리가 알아볼 수 있는 데이터 형태로 처리한다.

- 1계층과 다르게 주소 정보를 정의하고 정확한 주소로 통신이 되도록 하는 데 초점이 맞춰져있음.
- **MAC 주소**를 사용하여 프레임(frame) 단위로 데이터를 전송하며, 오류 검출, 재전송을 수행한다.
- 이더넷, Wi-Fi 프로토콜이 대표적이다.

> 주요 장비 : 스위치(Switch), 브릿지(Bridge) 등

<br>

### 3. 네트워크 계층

3계층은 네트워크 계층(Network)으로 서로 다른 네트워크 간 통신을 위해 IP 주소로 경로를 설정(라우팅)하고 패킷(Packet)을 전달하는 계층이다.

- IP 주소와 같은 논리적인 주소가 정의됨.
- IP가 대표적인 프로토콜

> 주요 장비 : 라우터

<br>

### 4. 전송 계층

4계층은 전송 계층(Transport Layer)으로 종단 간(end-to-end) 통신을 담당하며 실제로 데이터들이 정상적으로 잘 보내지도록 확인하는 계층이다.

- 데이터가 유실되거나 순서가 바뀌었을 때 바로 잡아주는 역할을 4계층에서 하기 때문에 데이터 전송의 신뢰성을 담당한다.
- 포트 번호를 사용해 애플리케이션을 구분하고, 세그먼트(Segment) 또는 데이터그램(Datagram) 단위로 데이터를 전송한다.
- 대표적인 프로토콜로는 TCP, UDP가 있다.
  - TCP : 신뢰성, 연결 지향, 순차 전송
  - UDP : 비신뢰성, 비연결형, 빠른 전송

> 주요 프로토콜 : TCP, UDP, SCTP

<br>

### 5. 세션 계층

5계층은 세션 계층(Session Layer)으로 응용 시스템 간의 통신 세션을 수립, 유지, 종료하는 계층이다.

- 세션을 관리하는 것(연결 유지, 복구, 체크포인트)이 주요 역할로, TCP/IP 세션을 만들고 없애는 책임을 진다.

> 주요 프로토콜 : NetBIOS, RPC

<br>

### 6. 표현 계층

6계층은 표현 계층(Presentation Layer)으로 다른 애플리케이션이나 시스템 간의 통신을 돕기 위해 하나의 통일된 구문 형식으로 변환시키는 계층이다.

- 일종의 변환기나 번역기 역할로 데이터 인코딩/디코딩, 암호화/복호화, 압축/압축 해제를 수행한다.
- SSL/TLS, JPEG, Base64 등이 대표적이다.

> 주요 프로토콜 : SSL/TLS, JPEG, MPEG, Base64, UTF-8

<br>

### 7. 응용 계층

7계층은 응용 계층(Application Layer)으로 애플리케이션 프로세스를 정의하고 애플리케이션 서비스를 수행하는 최상위 계층이다.

- 사용자와 가장 가까우며, 파일 전송, 이메일, 웹 브라우저 등을 통해 상호작용한다.
- HTTP/HTTPS, FTP, SMTP, DNS 등이 대표적인 프로토콜이다.

> 주요 프로토콜 : HTTP/HTTPS, FTP, SMTP, DNS

<br>

## TCP/IP 4계층 (5계층)

현재의 인터넷은 OSI 7계층보다는 TCP/IP 4계층을 기반으로 동작한다.
요새는 네트워크 인터페이스 계층을 다시 데이터 링크 계층과 물리 계층으로 나누어 TCP/IP 5계층이라고도 한다.

---

#### 면접 예상 질문

<details>
<summary>Q1. OSI 7계층에 대해서 간략히 설명하세요.</summary>
<div markdown="1">
A1. 
</div>
</details>
<br>
<details>
<summary>Q2. 7계층으로 나누는 이유에 대해서 설명하세요.</summary>
<div markdown="1">
A2. 
</div>
</details>
<br>
<details>
<summary>Q3. OSI 7계층과 TCP/IP 4계층의 차이점을 설명하세요.</summary>
<div markdown="1">
A3. 
</div>
</details>
