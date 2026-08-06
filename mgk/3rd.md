# 3회차. 26.08.05(수)
### DX - Infra, Network
인턴십 시험 준비를 위해 Infra, Network 분야의 개념 정리를 하기로 했다.

### 서버
<img width="704" height="381" alt="image" src="https://github.com/user-attachments/assets/187c2e5f-13b4-4e71-a134-7eddbb111b7b" />

**1. 하드웨어**

서버 vs 일반 PC 

서버 : 더 강력한 하드웨어를 지님, 보다 신뢰성 높은 하드웨어를 사용하여 지속적인 운영 보장

일반 PC : 주로 개인용으로 사용되며 서버보단 하드웨어 스펙이 낮음, 작업에 필요한 용량 및 성능 제공

<img width="693" height="386" alt="image" src="https://github.com/user-attachments/assets/f0a46f9e-d0ae-435d-a262-f31d142d17e6" />

=> 서버 : 네트워크 상 다른 시스템에 서비스 제공 및 데이터 관리

=> 일반 PC : 개인 사용자의 일상적인 컴퓨팅 작업

**2. 스토리지**

<img width="697" height="389" alt="image" src="https://github.com/user-attachments/assets/20a5baec-d458-480a-b518-cd17561a73d9" />

스토리지의 종류 : HDD, SSD, 테이프, 네트워크 저장소

=> 이런 매체들이 컴퓨터 시스템에서 데이터를 저장하고, 나중에 다시 꺼내 쓰고(액세스), 지키고(보호), 복사해두는(백업) 역할을 함

저장공간을 어떻게 연결하나? => DAS, NAS, SAN

**DAS (Direct Attached Storage)** - 직접 연결

- 외장하드를 USB로 내 컴퓨터에 딱 꽂는 것처럼, 케이블로 직접 연결
- 딱 그 컴퓨터 1대만 이 저장장치를 씀

**NAS (Network Attached Storage)** - 네트워크 연결

- 저장장치가 네트워크(인터넷/와이파이)에 연결되어 있어서, 여러 사람이 동시에 접속해서 파일 공유
- 회사에서 “공유폴더” 쓰는 거 생각하면 됨

**SAN (Storage Area Network)** - 전용 초고속 네트워크

- 저장장치 여러 개를 전용 초고속 네트워크로 묶어서, 여러 서버가 마치 자기 하드디스크처럼 빠르게 씀
- Fibre Channel, iSCSI 같은 전용 기술 사용 → NAS보다 훨씬 빠르고 대규모 (기업/데이터센터급)

**3. 운영체제 (Operating System, OS)**

컴퓨터 시스템에서 하드웨어와 응용시스템간 상호 작용 관리 및 제어하는 핵심 소프트웨어

<img width="690" height="384" alt="image" src="https://github.com/user-attachments/assets/458e98e8-e620-4aea-a244-97676a5bda78" />

**운영체제 :** 

1. 하드웨어 자원을 효율적 활용 및 응용 프로그램이 정상적으로 작동할 수 있도록 보장
2. 다양한 유형과 버전의 운영체제가 있으며 특정 용도나 환경에 맞게 설계

<img width="700" height="391" alt="image" src="https://github.com/user-attachments/assets/618fbdea-6c66-46d0-8f8d-c382292f80c8" />

<img width="688" height="388" alt="image" src="https://github.com/user-attachments/assets/6be3ef09-7157-44dc-a629-dbff1e295c7b" />

<img width="693" height="379" alt="image" src="https://github.com/user-attachments/assets/f39934ae-b868-4d8d-8e7e-3b097fea91cd" />

=> Windows, Linux, Unix 세 개 각각의 장단점과 특징을 통해 사용환경 및 요구사항에 따라 선택된다.

**운영체제와 H/W의 관계**

**Application :** 사용자가 직접 쓰는 프로그램들

**User Interface/Shell :** 사용자가 OS한테 명령 내리는 창구. 마우스 클릭이면 GUI, 명령어 치면 CLI, 자동화 스크립트면 Batch

**운영체제(OS) :** 프로그램이 “저장 좀 해줘”, “메모리 좀 줘” 하고 요청하면 이걸 System Call이라는 방식으로 받아서 하드웨어에 전달함

⇒ OS가 실제로 하는 일 :

- 프로세스 관리 (어떤 프로그램을 언제 실행할지)
- 메모리 공간 관리 (RAM 어떻게 나눠줄지)
- 디스크 자원 관리
- 파일시스템 관리
- 입·출력 관리
- 네트워크 보호/보안

**Hardware :** 실제 물리 부품 (CPU, Memory, Disk 등)

**4. 이중화와 고가용성**

이중화 : 똑같은 걸 2개 이상 준비해서, 하나 고장나도 나머지가 대신 일하게 하는 것

<img width="696" height="379" alt="image" src="https://github.com/user-attachments/assets/db763624-c099-42df-b7f9-914a071060bf" />

**NIC 이중화 (Network Interface Card)**

- 독립적인 두 개의 네트워크 경로 (네트워크 연결하는 카드가 두 개)
- 하나가 고장나도 다른 하나가 네트워크 연결을 계속 유지
- 목적 : 인터넷/네트워크 연결이 끊기지 않게!
