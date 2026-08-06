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

<img width="695" height="304" alt="image" src="https://github.com/user-attachments/assets/42921861-7993-4f98-b1ff-cd26857c5296" />

**HBA 이중화 (Host Bus Adapter)**

- 서버와 스토리지를 연결하는 어댑터를 2개 씀
- 하나가 고장나도 다른 경로로 스토리지에 계속 접근 가능
- 목적 : 저장장치 연결이 끊기지 않게!

<img width="694" height="357" alt="image" src="https://github.com/user-attachments/assets/75ea1be2-1d88-4dc0-b8db-b5a12f1a6f1d" />

**서버 이중화(Server)**

- 서버 자체를 2대 병렬로 운영
- 한 서버가 죽으면 다른 서버가 그 역할을 바로 이어받음
- 목적 : 단일 지점 장애 (SPOF, 한 곳 고장으로 전체가 멈추는 것)를 막음

⇒ 공통 원리 : NIC → HBA → 서버 순으로, 범위가 점점 커지면서 똑같이 하나가 죽어도 나머지가 살아있게 하는 식

⇒ **이중화 :** 고가용성을 만드는 방법 중 하나

고가용성 (High Availability, HA) : 시스템이 지속적으로 가용하고 신뢰성 있게 능력

- 시스템의 장애나 중단에 복구력을 갖춤
- 사용자에게 끊김 없는 서비스를 제공함

<img width="698" height="369" alt="image" src="https://github.com/user-attachments/assets/1e2aab03-090b-4224-acda-41596ad93189" />

**장애 허용 클러스터링 (Fault-Tolerant Clustering) :**

- 여러 대의 서버를 하나의 팀(클러스터)으로 묶음
- 한 서버가 죽으면 다른 서버가 그 역할을 자동으로 대신함
- 클러스터링 소프트웨어가 이 “장애감지 → 자동 이전”을 관리

**로드 밸런싱과 스케일 아웃 :**

- 로드 밸런싱 : 트래픽(요청량)을 여러 서버에 골고루 분산해서, 한 서버만 과부하 걸리지 않게 함
- 스케일 아웃 : 트래픽이 늘어나면 서버를 더 추가해서 대응함
- 로드 밸런싱은 이미 여러 개 열어놔서 분산시키는 거고, 스케일아웃은 트래픽이 늘어나면 그 때 돼서 추가하는 것

<img width="692" height="364" alt="image" src="https://github.com/user-attachments/assets/642acda2-7f48-4ed1-8c57-87aa1f9fe601" />

- 고가용성 클러스터 : DB 서버 하나 죽어도 나머지가 서비스 계속
- 부하분산 클러스터 : 웹 트래픽을 4대 서버로 분산
- 고성능 클러스터 : 여러 노드가 힘을 합쳐 연산 처리

**5. DR**

**DR (Disaster Recovery) :** 시스템이나 데이터가 재해 (자연재해, 인간 오류, 사이버 공격 등) 로 손상됐을 때, 복구해서 다시 운영 가능한 상태로 되돌리는 절차와 계획 

목표 : 비즈니스 연속성 유지 + 중단 시간 최소화

<img width="668" height="374" alt="image" src="https://github.com/user-attachments/assets/fc02534e-118b-4e63-9bcf-6b06f7a527d0" />

**DR 계획에 들어가는 요소 :**

1. 정기적인 백업과 데이터 복제로 데이터 보호
2. 비상 대응팀 구성 + 역할/책임 명확화
3. 재해 시 쓸 대체 인프라/시설 준비
4. 정기적인 DR 계획 테스트 + 직원 교육

**DR 계획 :** 

- 조직의 비즈니스 요구사항과 리스크 프로파일에 맞게 구성
- 주기적 검토 및 업데이트

**6. VDI**

<img width="699" height="382" alt="image" src="https://github.com/user-attachments/assets/c0f4109e-e81a-4318-b655-9eb2d2cf7a87" />

사용자의 데스크톱 환경을 가상화해서 중앙 서버에서 실행하고, 그 화면만 내 노트북/PC(클라이언트)로 전송해주는 기술

사용자는 로그인만 하고, 실제 연산은 서버에서 다 이뤄짐

**VDI 장점 :**

1. **액세스 가능성 :** 인터넷이 연결됨 → 가상 데스크톱에 액세스 가능함
2. **보안 :** 중앙 집중식 데이터 저장소, 암호화된 통신
3. **자원 효율성 :** 물리적 서버 자원을 효율적으로 활용하여 여러 사용자가 하나의 서버에서 작동 가능
4. **관리 용이성 :** 중앙 집중식 관리
5. **비용 절감**

<img width="690" height="378" alt="image" src="https://github.com/user-attachments/assets/b91ba803-1021-4359-bac2-c55ef857d2b8" />

**CJ그룹 VDI 서비스 사례**

3가지 핵심 가치:

- **① 업무 연속성**: 내부망(본사, 사내) + 외부망(재택, 해외)에서 어디서든 VPN 타고 접속
- **② 보안 강화**: VDI 인프라 안에 스토리지(OS/사용자 데이터 저장 영역, 백업 영역)를 두고, DDoS·방화벽·IPS 같은 보안 장비로 계속 감시
- **③ 사용자 편의성**: 로그인만 하면 O/A 문서작업, 엑셀, 인트라넷, ERP 등 회사 업무 환경을 그대로 씀

흐름: **사용자(내부/외부) → VDI Portal(로그인) → 사용자 VD환경(Windows 운영체제 실행) → VDI인프라(관리서버, 스토리지) → 최종적으로 사용자 업무환경 화면만 전송**

### 컴퓨터 네트워크 (Computer network)
컴퓨터들 간 정보 또는 데이터를 전달하기 위해 컴퓨터들을 서로 연결한 것, 컴퓨터 연결에 대해 연구하는 분야

<img width="695" height="384" alt="image" src="https://github.com/user-attachments/assets/0e66c512-8524-4691-8596-046fc2792547" />

<img width="691" height="380" alt="image" src="https://github.com/user-attachments/assets/89f0287b-b5fd-45ab-962a-327026f29dd1" />

**범위에 따른 구분**

- **LAN (Local Area Network) :** 일정 지역 내 (건물, 사무실) 근거리 통신망, 구내정보통신
- **WAN (Wide Area Network) :** 거리 제한 없는 원거리 통신망. 광역통신망

**네트워크 장치 (라우터 vs 스위치)**

<img width="694" height="380" alt="image" src="https://github.com/user-attachments/assets/cea3da75-cfce-43a4-a47b-e3f660bd9748" />

<img width="695" height="386" alt="image" src="https://github.com/user-attachments/assets/6f577f1b-5be1-47ec-80d3-ab2b282e451c" />

역할 : 목적지로 가는 적합한 경로를 찾아주는 장치

계층 : L3(네트워크 계층) 소속, **IP 주소 기반**으로 장치 위치 파악하고 통신

핵심 기능 : 

- 서로 다른 네트워크 (LAN-LAN, LAN-WAN) 를 연결함.
- 브로드캐스트 도메인을 구분해서 나눠줌

<img width="695" height="387" alt="image" src="https://github.com/user-attachments/assets/5d1dc088-64ae-4d4f-8605-f14d080c320c" />

<img width="698" height="386" alt="image" src="https://github.com/user-attachments/assets/ea004f61-c3f8-47be-969d-6cb92cca3c59" />

역할 : 소규모 네트워크 안에서 여러 디바이스를 서로 연결해서 자원 공유하게 함

계층 : L2(데이터 링크 계층) 소속, **MAC 주소 기반**으로 디바이스 위치 파악

한계 : 브로드캐스트 도메인을 구분 못함 
(목적지 불분명하면 모든 포트로 다 뿌림 = 브로드캐스트)

**데이터 통신**

<img width="691" height="385" alt="image" src="https://github.com/user-attachments/assets/c656d4ae-5266-4a3c-9568-a89510ec71f8" />

⇒ 개방형 시스템 상호 연결 모델의 표준

컴퓨터 회사마다 통신 규격이 제각각이면 서로 연결이 안 되는 문제(호환성 문제)가 생기니까, ISO가 데이터 통신 규격과 프로토콜을 통일하기 위해 만든 참조 모델임.

<img width="694" height="350" alt="image" src="https://github.com/user-attachments/assets/cb096cea-2857-4247-a9d5-eb5dfa729d0d" />
