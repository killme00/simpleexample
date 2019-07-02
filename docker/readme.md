# Docker

## Docker 팁

### docker-machine 으로 virtualbox 게스트 OS 시작
Docker Quickstart Terminal 을 띄우고
```
docker-machine start
```
를 실행

### docker 에 ssh 로 접근

실행 중인 virtualbox 게스트 OS 확인
```
docker-machine ls
```

virtualbox 게스트 OS (ex: default) 에 ssh 접근
```
docker-machine ssh default
```

### virtual 게스트 OS 셧다운
```
sudo shutdown -h now
```

### sudo 로 root 로그인
```
sudo -i
```

## Docker Articles
[Docker Toolbox Setup — Windows](https://rominirani.com/docker-toolbox-setup-windows-4d65c3f691eb)

[DOCKER-MACHINE 소개, 설치 및 기본 사용법](https://seulcode.tistory.com/241)

[도커 컴포즈를 활용하여 완벽한 개발 환경 구성하기](https://www.44bits.io/ko/post/almost-perfect-development-environment-with-docker-and-docker-compose)

[Ubuntu18.04 Install](https://dico.me/server/articles/235)

[Ubuntu 18.04 / 저장소 변경하여 apt-get 패키지 다운로드 속도 높이는 방법](https://www.manualfactory.net/10525)

[VirtualBox host-only network - ssh to remote machine](https://code-maven.com/virtualbox-host-only-network-ssh-to-remote-machine)

[우분투 18.04 도커(Docker) 설치 방법](https://blog.cosmosfarm.com/archives/248/%EC%9A%B0%EB%B6%84%ED%88%AC-18-04-%EB%8F%84%EC%BB%A4-docker-%EC%84%A4%EC%B9%98-%EB%B0%A9%EB%B2%95/)

## Window Image

### Nano Server

[Development workflow for Docker apps](https://github.com/dotnet/docs/blob/master/docs/standard/microservices-architecture/docker-application-development-process/docker-app-development-workflow.md)
