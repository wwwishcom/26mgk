# 5회차. 26.08.14(금)
### DX - Database
교육형 인턴십에서 제공하는 다양한 DX 개념들을 공부하고, 이 중 Database를 정리하는 것을 이번 5회차 모각코의 목표로 삼는다.

<img width="692" height="388" alt="image" src="https://github.com/user-attachments/assets/cbe7c647-dd6c-418b-9c91-4c155ee28dc0" />

**데이터베이스란?**
- 구조화된 데이터 저장 및 관리 시스템
- 여러 테이블로 구성되며, 각 테이블은 행과 열로 이루어진 데이터의 집합 저장
- 데이터 구조화 및 효율적으로 검색, 삽입, 수정, 삭제 가능한 다양한 기능 제공

**데이터의 특징**
- 공용 데이터 : 여러 응용 시스템들이 공동으로 생성, 유지, 이용하는 데이터
- 저장된 데이터 : 컴퓨터가 접근할 수 있는 저장 매체에 저장된 데이터
- 통합된 데이터 : 검색의 효율성을 위해 중복이 최소화된 데이터의 모임
- 운영 데이터 : 조직 목적을 위해 존재 가치가 확실하고 반드시 필요한 데이터

**데이터 베이스의 기능 특징**
- 실시간 접근성 : 사용자의 요구(Query)를 실시간으로 처리하고 신속하고 정확하게 응답
- 지속적인 변화 : 새로운 데이터 삽입, 삭제, 갱신을 통해 최신 데이터 유지가 필요
- 동시 공용 : 다수의 사용자가 동시에 같은 내용의 데이터를 이용
- 내용에 따른 참조 : 데이터베이스 내의 데이터 참조 시 위치나 주소가 아닌, 데이터 내용에 따라 참조

### DBMS의 종류
<img width="694" height="369" alt="image" src="https://github.com/user-attachments/assets/a83b398f-bff0-4b77-a1d1-ab6bc17c9420" />

1.  계층형 데이터베이스 관리 시스템 (Hierarchical DBMS)
2.  망형 데이터베이스 관리 시스템 (Network DBMS)
3.  관계형 데이터베이스 관리 시스템 (Relational DBMS)
4.  No SQL (Not Only SQL)

### 계층형 데이터베이스 관리 시스템 (HDBMS)

1. 데이터가 계층적이며 상하 종속적인 관계로 구성
2. 트리 형태의 계층적 구조를 가진 데이터베이스 최상위 계층의 데이터부터 검색하는 구조
3. 장점 : 빠른 데이터 액세스 속도와 쉽게 예측 가능한 데이터 사용량
4. 단점 : 상하 종속적 관계로 구성되어 초기 셋팅 후 변화하는 프로세스 수용의 어려움

⇒ 현재는 사용하지 않음!

### 망형 데이터베이스 관리 시스템 (NDBMS)

1. 데이터 구조를 네트워크상의 노드 형태로 논리적이게 표현한 데이터 모델
2. 각각의 노드를 서로 대등한 관계로 구성한 시스템
3. 장점 : HDBMS의 문제점인 상하 종속적 관계 해결
4. 단점 : 복잡한 구성과 설계 및 데이터 종속성을 해결하지 못함

⇒ 이것도 현재는 사용하지 않음!

### 관계형 데이터베이스 관리 시스템 (RDBMS)

1. 데이터를 테이블 형태로 구성한 구조
2. 테이블 내의 컬럼 중 일부를 다른 테이블과 중복해 각 테이블 간의 상관관계 정의
3. 장점 : 업무 변화에 대한 적응력이 높아 변화하는 업무에 쉽게 활용 가능, 편리한 유지보수
4. 단점 : 다른 DBMS보다 더 많은 자원이 필요해 시스템 부하가 높음

### NoSQL

1. RDBMS와 달리 고정된 스키마가 없거나 유연한 스키마를 가짐
2. 수평적 확장을 용이하게 지원
3. 다양한 데이터 모델 지원 및 대규모 데이터 처리와 분산 환경에 최적화
4. 장점 : 수평적 확장과 스키마 변경 용이, 다양한 데이터 형식 저장 가능
5. 단점 : 데이터의 일관성과 무결성 보장 어려움, 복잡한 쿼리 지원 부족

### 상용 RDBMS 비교 : Oracle vs SQL Server
<img width="691" height="373" alt="image" src="https://github.com/user-attachments/assets/b5c019b3-cfce-4e55-a020-b66c8d750b6a" />

⇒ Oracle과 SQL Server 모두 대규모 DB·높은 트랜잭션 처리량 효율적

But, Oracle은 수평·수직 확장 모두 가능하지만, SQL Server는 수평 확장은 제한적이다.

### 오픈소스 RDBMS : MySQL vs PostgreSQL
#### 1. MySQL
- 분류 : 관계형 데이터베이스 관리 시스템
- 특징 : View, Trigger, Procedure와 같은 기능을 제한적으로 지원
- 데이터 유형 : Numeric, character, date and time, spatial, JSON 데이터 유형을 지원
- ACID 규정 준수 : InnoDB 및 NDB 클러스터 엔진만 ACID 준수
- 인덱스  : B-tree, R-tree, index 지원
- 성능 : 빈도가 높은 읽기 작업에 유리

#### 2. PostgreSQL
- 분류 : 객체 관계형 데이터베이스 관리 시스템
- 특징 : Materialized view, INSTEAD OF trigger, Stored procedure와 같은 고급 기능을 여러 언어로 지원
- 데이터 유형 : Geometric, enumerated, network address, arrays, ranges, XML, hstore, and composite 및 모든 MySQL 데이터 유형을 지원
- ACID 규정 준수 : ACID 준수
- 인덱스 : Tree index 외에 Expression index, partial index, hash index 지원
- 성능 : 빈도가 높은 쓰기 작업에 유리

### 데이터 모델링
<img width="698" height="385" alt="image" src="https://github.com/user-attachments/assets/10075f4c-696f-4dbe-a2cc-fc80724591c6" />

수집하는 데이터 => 서로 다른 데이터 세트 사이의 관계 => 데이터 저장 및 분석

**데이터 모델링 장점**
- 데이터 베이스 소프트웨어 개발 오류 감소
- 데이터베이스 설계 및 생성 속도와 효율성 추진
- 조직 전체에서 데이터 문서화 및 시스템 설계의 일관성 조성
- 데이터 엔지니어와 비즈니스 인텔리전스 팀 간의 커뮤니케이션 촉진

**데이터 모델의 유형**

<img width="558" height="347" alt="image" src="https://github.com/user-attachments/assets/6673664f-fafe-4262-b319-6952e37f3975" />

개념적 데이터 모델 : 비즈니스 요구사항 기반으로 데이터의 주요 개념과 관계를 나타내는 모델

<img width="615" height="352" alt="image" src="https://github.com/user-attachments/assets/517f12ea-b3a6-4f79-8f20-b988e888a314" />

논리적 데이터 모델 : 개념적 데이터 모델을 기반으로 데이터베이스 시스템이 실제로 구현될 때 사용되는 구체적인 데이터 구조를 정의하는 모델

<img width="524" height="353" alt="image" src="https://github.com/user-attachments/assets/74be4511-b35e-417a-ad2c-500a6ecd904f" />

물리적 데이터 모델 : 논리적 데이터 모델을 구체적인 DBMS의 스키마로 변환한 모델
