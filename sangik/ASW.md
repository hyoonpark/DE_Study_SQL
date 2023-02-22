# 2강 클라우드 컨셉

## 확장성 있는 설계

- 클라우드는 확장성의 개념을 가지고 디자인

- IT자원의 확장성을 바탕으로 확장성이 있는 서비스 설계가 가능

- 서비스 레벨에서 병목과 획일적인 구성 요소들을 확인하여 효율적으로 설계를 개선하여 클라우드의 이점들을 활용해야 한다

#### 확장성 있는 어플리케이션의 특징

- 리소스 증가에 비례한 성능의 증가

- 회복력

- 분산된 시스템의 관리 능력

- 효율적인 운영 방법

- 비용의 효율적 관리

### 확장성 있는 설계 형태

- Scale Up/Down(수직적)
  
  - 시스템을 업그레이드, 다운그레이드

- Scale Out/In(수평적)
  
  - 병렬젹으로 확장(서버 증가), 감축

    

    

## 탄력성에 대한 이해

- 탄력성 : 최소한의 마찰로 리소스를 스케일링 가능하게 하는 특징

- 앱 구조에 클라우드 이점을 적용할 수 있도록 탄력성의 개념을 설계

- 간소화한 시스템 설계 및 프로세스의 관점의 변화가 필요

- 리소스를 서비스 양에 맞게 즉각적으로 늘리고 줄이는 프로세스를 자동호하고 이용률을 높이는 작업을 적용한다

### 탄력성의 구조

- 전통적인 방식의 비탄력적인 구조 (서비스 용량과 실사용량의 불일치)

- 클라우드의 탄력적인 구조(트래픽변화를 확장성으로 따라감)

    

    

## 제약에 대한 극복

- 시스템의 요구사항들이 클라우드에서 충분히 제공되는지 충족되지 않는 부분은 어떻게 극복해야 하는지

- 온프라미스 환경과 동일한 하드웨어 혹은 솔루션을 활용하기는 여럽다

- 추상화된 자원들을 활용하여 서비스를 딜리버리할 수 있다

##### 데이터 읽기 성능 확보 방법 사례

- 온프라미스 : 메모리 추가 구매

- 클라우드 : 레디스(인메모리 데이터베이스, key-value 데이터 저장소)

    

    

## 가상화 시스템 관리자

##### 시스템 관리자의 역할 변화

- 가상화 시스템 관리자 역할

- 최적의 비즈니스를 이끌어 낼 수 있도록 다양한 부분에 대헤 관심과 노력

- 기술 레벨의 확장 필요, 추상화된 클라우드에 대해 제어, 관리 및 서비스 기능 제안

#### 역할 변화

- 온프라미스 : DB설치 및 운영, 규칙적인 DB관리 작업

- 클라우드 : 기존 + DB인스턴스 이미지 관리, 분산 DB환경 관리

    

# 3강 AWS 서비스의 이해

## AWS

- 높은 신뢰성, 확장성을 바탕으로 웹스케일의 솔루션을 제공하며 it자원들을 탄력젹이며 효율적으로 비용을 관리할 수있는 대표적인 클라우드 제공자이다

- 웹스케일 : 글로벌 수준의 대규모의 환경에서도 높은 품질의 서비스를 영속적으로 제공하며 비즈니스의 요구사항에 맞춰 신속하고 안정적으로 IT자원을 설계, 구축 및 관리하는 패턴

## AWS의 이점

- 민첩성과 즉각적인 탄력성

- 비용 절감 효과

- 개방성 및 유연성

- 보안

- 높은 기술 노하우

## AWS의 대표 솔루션

- 어플리케이션 호스팅

- 웹 사이트

- 백업 및 스토리지

- 데이터베이스

- 엔터프라이즈 IT

    

#### AWS 글로벌 인프라

- 총 12개 지역, 계속 확장

    

### AWS 서비스 레이어

- 빌딩블럭

![](클라우드%20컨셉_assets/2023-02-21-23-32-22-image.png)

| 구분           | 사례      | 내용                                                              |
| ------------ | ------- | --------------------------------------------------------------- |
| 백업 및 스토리지    | NASDOQ  | 기하급수적으로 늘어나는 금융 산업의 정보를 무기한으로 저장하고 보호하면서 필요한대로 용량 조절            |
| 어플리케이션 및 호스팅 | NETFLEX | 컨텐츠 서비스를 글로벌하게 제공하기 위해 테라 규모의 수천대 서버가 필요하며 즉각적이고 확장성 있게 IT자원 확보 |

- 물리적 인프라 환경, low level 빌딩 블럭, high level 빌딩 블럭, cross service 기능, 접근 관리를 위한 툴의 서비스 레이어 등

 

  

### AWS 책임 분담 모델

#### infrastructure 서비스 모델

![](클라우드%20컨셉_assets/2023-02-21-23-38-13-image.png)

- 물리적인 것들을 다 aws가 관리

- 소프트웨어적인 부분 우리가 관리

#### abstrracted 서비스 모델

- 물리적 영역 + 플랫폼, 네트워크 등 AWS가 관리

- 나머지는 고객이 관리

![](클라우드%20컨셉_assets/2023-02-21-23-40-08-image.png)

    

# 5강 장애에 대한 디자인

### AWS 지역, 가용영역 및 엣지

- 지역 : 다양한 클라우드 서비스들을  세계 각지에서 제공하고 있고 지리적 위치를 바탕으로 지역을 구성한다

- 가용영역 : 지역을 물리적으로 격리된 여러 데이터 센터들의 집합들로 구분

#### 가용영역

- 하나의 지역 안에서 기본적인 서비스를 구성하도록 IT자원 등을 제공

- 사용자가 직접 가용 영역을 선택 및 여러 가용영역에 복수개의 인스턴스들을 배치하여 서비스의 가용성을 높인다

- 높은 가용성을 위해 하나의 지역에는 다수개의 AZ가 존재하며 해당 AZ간은 전용 사설 네트워크를 통해 낮은 네트워크 응답시간을 보장한다

#### 엣지

- 컨텐츠 전송 네트워크이며 웨삽이드, API, 동영상 콘텐츠 또는 기타 웹 자산의 전송을 가속화

- HTTP 또는 HTTPS 프로토콜을 사용하여 콘텐츠를 다운하거나

- RTMP 프로토콜로 콘텐츠를 스트리밍하여 배포할 수 있게 지원한다.

## AWS 컴퓨트 서비스

- 가상 컴퓨팅 자원(EC2)를 할당하여 탄력적인 웹스케일의 컴퓨팅이나 병렬작업 처리를 가능하게 한다

- 시스템의 가장 기본적인 구성자원이 된다

### Elastic Compute Cloud(EC2)

- 가장 기본이 되는 Low-Level 빌딩 블럭에 속하는 컴퓨팅 서비스

- 가상 서버를 구축하고 보안 및 네트워크 구성과 스토리지 관리가 가능

- 인스턴스 : 가상 컴퓨팅 환경

- AMI :아마존 머신 이미지, 인스턴스에 필요한 OS와 소프트웨어가 구성된 템플릿

- 인스턴스 타입 : CPU, 메모리 사이즈

- EIP(elastic ip) : 가상의 컴퓨팅 서버에 할당되는 고정 공인 IP

- VPC : 가상의 컴퓨팅 서버가 속하는 독립된 네트워크 블럭

### Lambda

- 이벤트에 응답하여 코드를 실행하고 자동으로 기본 컴퓨팅 리소스를 관리하는 서버 없는 컴퓨팅 서비스이다

- AWS에서 백엔드 서버와 운영 체제 유지 관리, 용량 프로비저닝 및 자동 조정, 코드 및 보안 패치 배포, 코드 모니터링 및 로깅 등 모든 컴퓨팅 리소스 관리를 수행한다.

### 컴퓨트 서비스 장애에 대한 디자인

- 확장성 : AZ단위로 확장 가능하며 autoscailing를 통해 요구되는 트래픽들을 수용

- 모니터링 및 운영 관리 : API와 대시보드를 통해 손쉽게 관리

- 이중화 : 여러 AZ에 DB를 구성하여 단일 요소의 장애 제거

- Failover : EIP와 Disk를 별도로 관리 가능하여 정상적인 상태의 서버로 대체

    

#### AWS 데이터베이스

- 용량과 성능에 맞게 조정가능하며 시간 소모적인 관리 작업들로부터 자유롭게 해준다

- 관계형 데이터베이스 : 정형데이터, RDS

- 비관계형 데이터베이스 : 비정형, DynamoDB

#### 관계형 데이터 베이스

- 키값에 의해 서로 관련되는 테이블로 구성하는 가장 일반적인 유형

- 각 테이블/관계는 하나의 엔티티 타입을 대표

- 효율적이고 정확하게 운용되기 위해서는 ACID 트랜잭션 특징
  
  - atomicty(원자성), isolation(고립성), consistency(일관성), durability(지속성)

##### NoSQL

- 스키마가 없으며 각 테이블에는 각 데이터 항목을 고유하게 식별하는 기본 키가 있어야 하지만 키가 아닌 다른 속성인 값에 대해서는 제한이 없다

- DynamoDB는 JSON 문서를 비롯한 정형 또는 반정형 데이터를 관리할 수 있으며 NoSQL은 BASE의 특징
  
  - basically available, sogr-state, eventually consistency

    

## 데이터 베이스 장애에 대한 디자인

- 확장성 : AZ 단위로 확장 가능하며 다른 AZ 로의 두번쨰 구성가능

- 백업 및 운영 관리 : API와 대시보드를 통해 손쉽게 관리

- 이중화 : 여러 AZ에 DB를 구성하여 단일요소의 장애 제거

- Failover : 데이터가 소결합으로 저장되어 있어 대체작동 가능