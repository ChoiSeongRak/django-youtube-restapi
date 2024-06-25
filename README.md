# django-youtube-restapi

## (1) Project Settings

- GitHub

## Model 구조 => ORM

(1) User => users
- email
- password
- nickname
- is_business

(2) Video => videos
- title
- description
- link
- views_count
- thumbnail
- video_file: link
- User: FK

ex) 파일(이미지, 동영상 )
=> 장고에 부하가 걸림
=> S3 Bucket(저렴, 속도가 빠름) -> 결과물: 링크

(3) Reaction => reactions
- User: FK
- Video: FK
- reaction (like, dislike, cancle) => 실제 youtube rest api 

(4) Comment => comments
- User: FK
- Video: FK
- content
- like
- dislike

(5) Subscription => subscriptions
- User: FK => subscriber (내가 구독한 사람)
- User: FK => subscriber_to (나를 구독한 사람)

(6) Common => common
- created_at
- updated_at





## 참고
- Docker란?
    애플리케이션을 컨테이너라는 격리된 환경에서 실행할 수 있도록 도와주는 오픈 소스 플랫폼이다. 컨테이너는 애플리케이션과 그 종속성을 하나의 패키지로 묶어, 다양한 환경에서 일관되게 실행할 수 있도록 한다.
- Docker 구성요소
    1. Docker Engine
        컨테이너를 생성, 실행, 배포, 관리하기 위한 기본 애플리케이션
    2. Docker Image
        모든 파일과 설정(애플리케이션, 라이브러리, 설정 파일 등)을 포함하는 불변의 템플릿
    3. Docker Container
        이미지를 실행한 상태로, 실제 애플리케이션이 동작하는 격리된 환경
    4. Dockerfile
        이미지를 생성하기 위한 설정 파일
    5. Docker Hub
        이미지의 중앙 저장소
- Docker Image와 Docker Container
    둘 다 핵심 구성요소이며, 배포와 실행을 위한 중요한 역할을 한다.
    Image = 불변, Container = 변경 가능
    Docker 이미지는 애플리케이션의 배포 기본 단위이고, 컨테이너는 그 이미지를 실행하여 실제로 애플리케이션을 구동하는 환경 제공

- CI/CD와 Github Actions
    1. CI/CD(Continuous Integration/Continuous Deployment)는 소프트웨어 개발에서 지속적 통합과 지속적 배포를 의미한다. 소프트웨어의 품질을 유지하고 소프트웨어 배포 과정을 자동화하여 개발자들이 소프트웨어를 더 빠르고 안정적으로 개발하고 배포할수 있게 한다.

    2. Github Actions는 Github에서 제공하는 CI/CD 서비스이다. 저장소에서 이벤트(push, pull,request 등) 가 발생할 때 실행되는 워크플로우를 정의할 수 있다.
    Github Actions를 사용하면 코드 품질검사, 자동화된 테스트 수행, 빌드 및 배포 자동화 등 다양한 작업을 설정할 수 있다.

-  PostgreSQL의 장점
    1. PostgreSQL?
        관계형 데이터베이스 관리 시스템(RDBMS)이다.

    2. 장점
        1. 신뢰성 및 내구성:
            PostgreSQL은 ACID(원자성, 일관성, 고립성, 지속성)를 준수하여 데이터의 신뢰성과 내구성을 보장한다.
        2. 확장성: 
            대규모 데이터베이스 환경에서도 잘 동작하며, 수평 및 수직 확장이 가능합니다.
        3. 기능의 다양성: 
            기능의 다양성: JSON 데이터 형식 지원, 공간 데이터 지원, 외부 데이터 소스 연동, Full Text 검색 등 다양한 고급 기능을 제공합니다.
        4. 높은 성능으로 최적화된 쿼리 및 병렬 처리 기능으로 높은 성능을 제공한다.






