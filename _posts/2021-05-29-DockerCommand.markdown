---
layout: post
title: "Docker command"
date: 2021-05-29 17:40:00 +0300
image: docker-logo.png
tags: Docker
---

## 시작하는 말  

시간날때 진행하는 사이드 프로젝트에서 팀원이 도커를 통해 서버를 구축하였으며 이때 사용한 명령어를 정리해보고자 한다.
간단히 필요한 명령어를 정리해보고 추후에 작성한다.  

---

## Docker Command  

먼저 Docker의 라이프 사이클이다.  

![dockerLifeCycle](/images/doc1.PNG)  
 
해당 라이프 사이클을 docker의 command로 수행할 수 있으며 명령어는 다음과 같다.  

```
 - docker pull {image name}      // Docker hub에서 사용할 이미지를 받아온다.  
 - docker run -d -p 80:80 {docker hub id}/{repository name}:latest // 받아온 Docker image를 실행하여 컨테이너로 만든다. (포워딩)
   - 'Ctrl + d'                  // 쉘 종료 - 컨테이너 종료  
   - 'Ctrl + p' + 'Ctrl + q'     // 컨테이너가 살아 있는 채로 Host OS로 복귀  

 - docker ps (-a)                // 실행중인(생성된) 컨테이너 목록 확인  
 - docker start                  // docker 시작  

 - docker images                 // 현재 Host PC에 받은 image들을 보여준다. (Size가 작은 이유 : Docker 이미지에는 커널이 포함되어 있지 않고 실행하기 위한 파일만 존재)
 - docker attach "container ID"  // 컨테이너 접속
 - docker stop "container ID"    // 컨테이너 종료
 - docker rm "container ID"      // 컨테이너 삭제
```

---

#### 성장에 도움을 주신 개발자분  

[출처 : ](https://kouzie.github.io/docker/docker-command/#docker-command) https://kouzie.github.io/docker/docker-command/#docker-command  

오늘도 감사합니다.
