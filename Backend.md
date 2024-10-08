# 백엔드에서 데이터베이스는 대체 왜 쓰일까?

백엔드에서 도대체 왜 데이터베이스가 필요한 것일까?

우리는 사이트들을 들어갈 때, 로그인을 하고 들어간다.
로그인 정보들은 매우 귀중하고 안전하게 보관해야 하는데 이를 보관하기 위해 쓰이는 것이 데이터베이스이다.

그렇다면 데이터베이스는 무엇이고 백엔드에서 많이 사용되는 MySQL에 대해 알아보자.

## 데이터베이스와 SQL이란 뭘까?

### 데이터베이스

- 단어, 숫자, 이미지, 비디오, 파일들을 포함한 모든 유형의 데이터들을 전자적으로 저장되며 관리하는 체계적인 데이터 모음을 뜻한다.
- 하지만 데이터베이스는 시스템 내에서만 데이터들을 관리하며 데이터들이 사용자와 추가, 수정, 삭제, 조회와 같은 직접적인 상호작용 기능들을 할 수 없다는 한계가 존재한다.

### SQL

- SQL은 이러한 데이터베이스의 한계를 보완하기 위해 사용되는 **쿼리 언어**이다.
- SQL은 데이터베이스와 사용자의 상호작용을 돕는 인터페이스를 제공한다. 
덕분에 사용자는 데이터베이스로부터 데이터를 새로 추가하거나 데이터를 수정하고, 데이터를 삭제할 수 있으며 데이터를 조회하는 것 또한 가능하다.
- 하지만 어디까지나 "**쿼리 언어**"로서 사용자가 원하는 특정 데이터를 관리하는 점에서는 매우 좋을 수 있으나 데이터베이스 전체를 관리하기는 쉽지 않다는 한계점이 존재한다.

데이터베이스의 물리적 구조와 성능 최적화, 보안관리 등의 고급 기능은 SQL만으로 수행하기 어렵기 때문이다.

> 우선 **쿼리**란?
> 
> 
> > 쿼리는 데이터베이스에서 특정 작업을 수행하기 위해 작성된 명령이다.
> >주로 특정 데이터를 관리할 때 사용된다.
> > 
> 
> 그렇다면 **쿼리 언어**란?
> 
> > 프로그램 작성을 작성을 목표로 하는 언어들과 달리
> >사용자와 데이터베이스 간의 상호작용을 도우며 데이터들을 관리하는 특수한 목적을 가진 언어이다.
> >
> > 타 언어와 달리 데이터들을 효율적으로 다루는 것에 초점을 맞추고 있다.
> > 
> 
> 그렇다면 SQL은 많은 쿼리 언어들 중 하나일텐데 왜 SQL을 사용하는 것 일까?
> 
> > 데이터들을 열과 행으로 구성하는 테이블 형태로 조직화하는 관계형 데이터베이스에서 데이터를 정의하고 조작하는 기능을 통합한 최초의 성공적인 언어이다.
> >
> >또한 간결하고 직관적인 문법 덕분에 개발자뿐만 아니라 비전문가들 쉽게 배울 수 있다.
> > 
> 
> 이러한 장점 덕분에 국제 표준화 기구(ISO)에서 표준 쿼리 언어로 채택되었다.
> 

## MySQL이란 무엇인가?

- 이러한 SQL의 한계점를 보완하기 위해 SQL을 활용하여 데이터을 관리하는 오픈 소스 관계형 데이터베이스 관리 시스템을 말한다.
- SQL 명령문을 통해 특정 데이터 및 데이터베이스 전체를 운영하고 관리한다. 그 덕분에 기존 SQL의 기능인 데이터베이스와 상호작용하는 것은 물론이거 더불어 SQL이 수행하기 어려운 고급 기능들을 수행한다.

## MySQL가 왜 자주 쓰이는가?

### 높은 성능

- 빠른 데이터 처리와 효율적인 쿼리 실행을 통해 높은 성능을 제공한다.
- 다양한 스토리지 엔진을 지원하여 애플리케이션의 요구 사항에 맞도록 최적화가 가능하다.
- 인덱스 기능을 활용하여 데이터 검색 속도를 높인다.

### 안정성과 신뢰성

- 트랜잭션 관리와 데이터 복제 기능을 통해 데이터의 무결성과 일관성을 유지한다.
- 스토리지 엔진의 ACID 특성을 준수하여 신뢰성 높은 트랜잭션 처리를 보장한다. 덕분에 백업이나 복구 기능을 통해 데이터 손실을 방지가 가능하다.
- 사용자 권한 관리와 데이터 암호화와 같은 보안 기능들을 활용하여 보다 더욱 데이터베이스의 안정성을 높일 수 있다.

### 다양한 플랫폼 지원

- Windows, MacOS, Linux 등 다양한 운영체제에서도 운영이 가능하다.
- 또한 PHP, Java, Python 등과 같은 프로그래밍 언어들과의 호환성도 높다.

## MySQL의 한계점은 존재하는가?

그렇다. <br> MySQL도 명확한 한계점이 존재한다.

### NoSQL 지원의 부족

- 관계형 데이터베이스로 설계되어 있다.
이러한 점은 문서, 사진, 동영상과 같이 정형화된 구조를 갖지 않는 데이터들을 처리하지 못한다.
    - 비정형 데이터들은 크기가 크며, 구조가 정형화되어 있지 않아
    테이블에 직접 저장 시 성능 저하를 초래할 수 있다.
- NoSQL은 비정형 데이터를 처리하는데 최적화되어 있어서 이 점은 매우 크다.

### 대규모 데이터 처리의 제한

- MySQL은 단일 서버를 기반으로 설계되었다.
이러한 점은 매우 대규모 시스템이나 고성능 요구사항이 있는 시스템에서 성능상 한계를 가진다.
- 데이터를 여러 서버에 걸쳐 분산 저장하고 처리하는 기능이 부족하다.

## 그렇다면 해결책은 존재하는가?

### NoSQL 지원 부족의 경우

- NoSQL 데이터베이스와 병행하여 사용
    - 대표적인 MongoDB, Cassandra와 같은 NoSQL 데이터베이스와 병행하여 비정형 데이터들을 따로 관리할 수 있도록 해야한다.

### 대규모 데이터 처리의 제한의 경우

- 데이터베이스 샤딩을 사용한다.
    - 데이터베이스 샤딩이란 데이터를 여러 서버에 분산하여 저장하고 처리하는 방법을 뜻한다.
    - MySQL Cluster와 같은 외부 툴을 사용하여 샤딩이 가능하다.