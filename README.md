# django-youtube-restapi

## (1) Project Settings

- GitHub

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