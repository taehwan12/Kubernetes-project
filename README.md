# 🛡️ Team 4RSENAL: Enterprise Infrastructure & Cloud Architecture Master Portfolio

> **"오픈소스 기반의 온프레미스 인프라 엔지니어링부터 최신 클라우드 네이티브 아키텍처, 그리고 멀티 클라우드 DR(재해 복구) 체계까지."**
>
> **엔터프라이즈 서버 인프라의 모든 계층(Full-Stack Infrastructure)을 설계, 구축, 자동화하고 검증하는 최정예 인프라 엔지니어링 팀 '4RSENAL'의 종합 기술 여정입니다.**

---

## 👥 Team Members
- **전병욱** (인프라 총괄 / 아키텍트)
- **신재성** (시스템 엔지니어 / 자동화)
- **정태환** (클라우드 엔지니어 / SecOps)
- **이은석** (시스템 엔지니어 / 컴플라이언스)
- **권승빈** (네트워크 엔지니어 / QA)

<br>

## 🛠️ Core Tech Stack Vector
┌────────────────────────────────────────────────────────────────────────┐
│  OS & Core       │ Rocky Linux 9.x, Ubuntu Server 24.04 LTS            │
├──────────────────┼─────────────────────────────────────────────────────┤
│  Containerization│ Docker, Dockerfile, Containerizing                  │
├──────────────────┼─────────────────────────────────────────────────────┤
│  Cloud (AWS)     │ VPC, EC2, ALB, ECR, ECS (Fargate), Route 53         │
├──────────────────┼─────────────────────────────────────────────────────┤
│  Cloud (NCP)     │ VPC, Server, NLB, Global DNS, IPsec VPN             │
├──────────────────┼─────────────────────────────────────────────────────┤
│  Services        │ Nginx, Apache Tomcat, MariaDB/MySQL, Bind9, Samba   │
└────────────────────────────────────────────────────────────────────────┘
---

## 🚀 Core Roadmap & Portfolio Links (주요 프로젝트 요약)

### 1️⃣ [On-Premise] Rocky Linux 기반 엔터프라이즈 서버 인프라 구축
* **스토리지 및 자원 통제:** LVM(Logical Volume Manager)을 활용한 가상 볼륨 마이그레이션 및 사용자별 디스크 쿼터(Quota) 제한 정책 수립
* **6대 엔터프라이즈 필수 서버 인프라:** 인바운드 방화벽 제어 및 시스템 격리를 적용한 DNS(Bind9), Web(Apache), FTP(vsftpd), DB(MariaDB), NFS, SAMBA 서버 올인원 구축 및 이기종 간 망 연동 완료
* **인프라 네트워킹 자동화:** DHCP 주소 설계 및 `sendmail`/`dovecot` 기반의 사설 메일 통신 인프라 검증

### 2️⃣ [Cloud Native] AWS ECS Fargate 기반 컨테이너 아키텍처 프로젝트
* **컨테이너 파이프라인:** 호스트 OS 디펜던시를 제거한 Nginx 커스텀 멀티 버전 Docker 빌드 및 AWS ECR 프라이빗 레지스트리 형상 관리
* **서버리스 오케스트레이션:** AWS Fargate 아키텍처를 도입하여 자원 예측 기반의 ECS 클러스터 및 태스크 정의(Task Definition) 수립
* **고가용성 부하분산:** 다중 가용 영역(AZ 2A, 2C) 서브넷 매핑, ALB 리스너 규칙 바인딩 및 Route 53 도메인 별칭 레코드 매핑을 통한 무장애 웹 서비스 배포

### 3️⃣ [Architecture] AWS 3-Tier 엔터프라이즈 가상 아키텍처 프로젝트
* **완벽한 계층 분리:** Presentation(Nginx 퍼블릭), Application(Tomcat 프라이빗), Data(RDS MySQL 격리) 계층을 수동 네트워크 테이블로 철저히 물리 분할
* **Bastion 터널링 보안:** 사설망 인프라 보호를 위한 단일 진입점(Bastion Host)을 개설하고 SFTP 기반 .pem 키 페어 암호화 터널링 제어 가동
* **트랜잭션 파이프라인 검증:** 리버스 프록시 연동 및 웹 애플리케이션-관계형 데이터베이스 간 DB 커넥션 풀을 연동하여 종단 간(End-to-End) 게시글 적재 트랜잭션 완벽 검증

### 4️⃣ [Hybrid & Global] AWS x NCP 멀티 클라우드 글로벌 인프라 아키텍처
* **이기종 클라우드 가상망 결합:** AWS VPC 대역과 NCP(네이버 클라우드 플랫폼) VPC 대역 간의 사설 통신을 위한 IPsec VPN 터널링 구성 및 커스텀 라우팅 테이블 수동 제어
* **글로벌 로드 밸런싱 & Failover:** AWS ALB와 NCP NLB를 글로벌 DNS 체계(Route 53 x Global DNS)로 묶어 상호 헬스체크 및 특정 벤더 다운 시 트래픽을 즉시 우회시키는 무중단 재해 복구(DR) 시나리오 구현

---

## 📈 성과 및 핵심 역량 (Core Competencies)

* **종합적 인프라 수명 주기(Lifecycle) 전담:** 온프레미스 가상화 서버 인프라 단계부터 모던 클라우드 아키텍처 및 복합 멀티 클라우드 환경까지 인프라 전반의 마이그레이션 아키텍처 체계를 리딩했습니다.
* **SecOps 및 고가용성(High Availability) 내재화:** 배스천 호스트, 내부 사설망 격리, IAM 최소 권한 부여, 그리고 다중 클라우드 벤더 가용성 헬스체크 설계를 통해 엔터프라이즈 서비스가 갖추어야 할 강력한 컴플라이언스와 무중단 가용성을 실현했습니다.
* **컨테이너 및 클라우드 네이티브 숙련도:** Docker 인프라 가상화, ECR/ECS 오케스트레이션 기법을 통달하여 급격한 트래픽 변화와 스케일 아웃에 유연하게 대응할 수 있는 클라우드 네이티브 역량을 확보했습니다.
