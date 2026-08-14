# 4회차. 26.08.13(목)
### DX - Cloud
교육형 인턴십에서 제공하는 다양한 DX 개념들을 공부하고, 이에 대해 정리하는 것을 이번 4회차 모각코의 목표로 삼는다.

<img width="698" height="383" alt="image" src="https://github.com/user-attachments/assets/c1936894-9c16-4d2f-9d37-843cfbd7efd1" />

⇒ 유연성, 확장성, 비용 효율성 제공

### 클라우드 컴퓨팅 (Cloud Computing)

인터넷을 통해 컴퓨팅 자원 (서버, 스토리지, 데이터베이스, 네트워크, 소프트웨어 등)에 접근하고 사용할 수 있게 해주는 기술이다.

사용자는 물리적인 하드웨어를 직접 구매, 설치, 유지보수할 필요 없이, 필요한 만큼만 자원을 빌려서 쓰고 사용한 만큼 비용을 지불한다.

<img width="690" height="370" alt="image" src="https://github.com/user-attachments/assets/62ef4406-22e5-4c06-91b6-eb31d46d52b7" />

<img width="692" height="358" alt="image" src="https://github.com/user-attachments/assets/1d7ab615-9621-4f1e-9b0d-670537adc85d" />

**CSAP (클라우드 보안 인증제)** — Cloud Security Assurance Program

공공기관, 지자체, 금융기관 등은 국민의 민감한 데이터를 다루기 때문에, 아무 클라우드나 마음대로 쓸 수 없다.

한국 정부(과학기술정보통신부 산하 한국인터넷진흥원, KISA)가 이 클라우드는 공공기관이 써도 안전하다!!고 검증해주는 제도가 CSAP.

이름은 비슷하지만, 다른 클라우드 서비스 제공 업체 **CSP**

<img width="695" height="391" alt="image" src="https://github.com/user-attachments/assets/0641ea5a-3623-4d81-a17e-0efab40356b5" />

리전(Region) : CSP가 전세계 여러 국가/지역에 설치해둔 데이터센터 묶음!!

⇒ 사용자와 물리적으로 가까운 리전을 쓰면 응답속도가 빨라진다.

<img width="695" height="387" alt="image" src="https://github.com/user-attachments/assets/18df8263-2137-41b9-8e3a-0b38f13b0ef4" />

애플리케이션을 클라우드 환경에 최적화된 방식으로 설계, 개발, 운영하는 접근 방식 ⇒ **클라우드 네이티브**

애초에 클라우드의 특성 (확장성, 유연성, 자동화) 을 최대한 활용하도록 처음부터 설계하는 방법론

<img width="695" height="389" alt="image" src="https://github.com/user-attachments/assets/8c6b04e0-aa3b-45c5-904e-96e455343113" />

### SaaS (Software-as-a-Service)

별도의 인프라, 소프트웨어를 설치할 필요 없이 클라우드를 통해 서비스 이용 가능

ex. zoom

전부 다!!! 해주고 직접하는 건 없음 걍 날먹.

<img width="695" height="372" alt="image" src="https://github.com/user-attachments/assets/00efdef5-b05f-49df-bb7e-d2fc4fdb3fbd" />

### PaaS (Platform-as-a-Service)

서버, 운영체제, IP 설정 필요 없이 MySQL 플랫폼만 이용하여 바로 데이터베이스 활용 가능!

인프라 + OS + 개발에 필요한 런타임, DB 환경까지 미리 세팅되어 제공되고 **코드 개발에만 집중**할 수 있다!!

⇒ 인프라 관리는 귀찮고, 빠르게 앱 개발하고 배포하고 싶다면~?

<img width="695" height="367" alt="image" src="https://github.com/user-attachments/assets/c7d38f06-562b-4aa6-b56e-74f383ad7949" />

### IaaS (Infrastructure-as-a-Service)

서버, 스토리지, 네트워크와 같은 IT인프라를 필요에 따라 유연하게 확장 및 축소 가능

서버를 구매하거나 네트워크 케이블을 연결하는 등의 물리적 작업이 불필요하다!

⇒ 서버, 스토리지, 네트워크 같은 가상화된 하드웨어만 제공받음

⇒ OS 설치, 보안 패치, 웹서버 설정, DB설치, 애플리케이션 개발 **모두 사용자 몫.**

<img width="694" height="363" alt="image" src="https://github.com/user-attachments/assets/b634bfda-b287-42f2-a957-9884a7129d35" />

### FaaS (Function-as-a-Service)

IaaS보다 경량화 된 서비스
“개발 코드”만으로 모듈화 및 유연하게 구성

⇒ Serverless 방식 — 서버를 상시로 켜둘 필요가 없음

코드를 함수 단위로 올려두면, 이벤트가 발생했을 때만 실행되고 그 실행 시간만큼만 과금된다.

실행이 끝나면? ⇒ 자원이 자동으로 해제됨!

특정 이벤트에만 반응하는 짧은 작업 (예 : 이미지 업로드 시 자동 리사이징, 특정 API 호출 시 알림 발송) 과 같은 때~~! ⇒ 비용이 매우 효율적이다.

<img width="693" height="360" alt="image" src="https://github.com/user-attachments/assets/aeb0644e-eb23-4985-8037-bdaa9dd1e157" />

- 여러 사용자가 공유하는 클라우드 인프라를 서비스 제공 업체가 인터넷을 통해 제공
- 인터넷에 연결되어 있으면 누구나 접근 가능, 사용한 만큼만 비용 지불
- ex. AWS, Azure, Naver Cloud, Tencent, KT Cloud
- 장점 : 초기 비용 없음, 빠른 확장, 관리 부담 없음
- 단점 : 다른 사용자와 인프라를 공유하므로 보안, 규제 민감 데이터에는 부적합할 수 있음

<img width="698" height="386" alt="image" src="https://github.com/user-attachments/assets/f2eb23ef-c54d-4d2c-ae6c-4832b9e6d999" />
