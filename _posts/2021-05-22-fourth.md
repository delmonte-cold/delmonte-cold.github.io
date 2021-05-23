---
layout: single_v2
title:  "Docker 시작하기"
tags : [R,Rstudio,Server]
---

### Docker 명령어
```bash
docker run -it {image name} # 이미지 다운(없을시) 바로 컨테이너 생성하고 진입
docker images # 이미지 조회
docker ps # 컨테이너 조회
docker exec -it {container name} bash # bash shell 컨테이너실행
docker build -t {image name} . # Dockerfile로 이미지 생성
docker run --name {container name} -v $(pwd):{container dir} -p {local port}:{container port} -d {image name} # --name 컨테이너 이름설정, -v DIR 연결, -p PORT 연결, -d 백그라운드에서 실행
docker stop $(docker ps -aq) # 모든 컨테이너 정지
docker-compose up -d # docker-compose 실행
```

### Dockerfile 문법 
```bash
FROM # 참조 이미지
RUN # 이미지 생성시 실행 명령어
ENV # 이미지 생성시 환경변수 설정
COPY # 이미지 생성시 파일복사
WORKDIR # 명령어를 실행할 위치
CMD # 컨테이너 생성시 실행 명령어
```

### Docker-compose
```bash
version # docker-compose 버전
build # Dockerfile 위치
prots # 로컬 포트 : 컨테이너 포트
volumns: # 로컬 디렉토리 : 컨테이너 디렉토리
environment # 환경변수 설정
```


### 실습용 프로젝트
```bash
git clone https://gitlab.com/yalco/practice-docker.git 
```

[https://www.yalco.kr/36_docker/](https://www.yalco.kr/36_docker/)

### Reference 
- [https://www.yalco.kr/36_docker/](https://www.yalco.kr/36_docker/) # 실습예제
- [https://hub.docker.com/](https://hub.docker.com/) # docker image 검색
- [https://docs.docker.com/](https://docs.docker.com/) # docker docs
- [https://m.blog.naver.com/PostView.naver?blogId=ilikebigmac&logNo=221673193987&proxyReferer=https:%2F%2Fwww.google.com%2F](https://m.blog.naver.com/PostView.naver?blogId=ilikebigmac&logNo=221673193987&proxyReferer=https:%2F%2Fwww.google.com%2F) # Dockerfile 명령어

