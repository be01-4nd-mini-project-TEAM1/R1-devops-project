# devops-mini-project
![devops6](https://github.com/be01-4nd-mini-project-TEAM1/R1-devops-project/assets/148875683/6cf88504-1818-445f-9744-309eb3061bad)


[🔗 배포 URL]
## 개요
- 📝 ++
## 팀원 구성


|                                                             **🐻‍❄️ 최원규**                                                              |                                                             **🐻 전승민**                                                              |                                                             **🐰 윤채영**                                                              |                                                             **🐨 우지영**                                                              |                                                             **🐯 박재린**                                                              |
| :-------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: |
|                             nGrinder Controller                             |                                                  Nginx proxy                                                  |                                                nGrinder Agent                                               |                            nGrinder Agent                         |                             App Server & DB server                             | 



***

## <span id="goal">1. 프로젝트 목표</span>
- 

<p align="right"><a href="#top">(Top)</a></p>

## <span id="dev">2. 개발 환경 및 배포 URL</span>
### 개발 환경
- Front : 
- Back : 
- 버전 관리 및 이슈 : 🔗
- 서비스 배포 환경 : [🔗 ]
### 배포 URL
URL : 🔗 


## <span id="task">3. 개발 기간 및 작업 관리</span>
- 전체 개발 기간 : 2024-02-28 ~ 2024-02-29
### 작업 관리
- 🔗[GitHub Projects](https://github.com/orgs/be01-4nd-mini-project-TEAM1/projects/1)와 🔗[Issues](https://github.com/be01-4nd-mini-project-TEAM1/R1-devops-project/issues/1)

## <span id="pages">4. </span>

## <span id="issues">5. 개발하며 겪은 이슈</span>
### 1) WSL 환경에서 nGrinder Controller에 외부 PC에서 agent 접속 이슈
   - https://github.com/be01-4nd-mini-project-TEAM1/R3-nGrinder/issues/1
   <br>

#### 내용
- 포트포워딩한 nGrinder Controller에 외부 PC의 agent가 접속되지 않았다.
#### 결론
- nGrinder agent는 기본적으로 16001 포트의 Controller에 접속한다.
- 외부 PC에서 Controller 페이지에 접속하기 위한 8080 포트와 agent가 접속하기 위한 16001 포트 2개를 포트포워딩 해준다.
- 외부 PC가 포트에 접속할 수 있도록 방화벽 설정이 추가적으로 필요하다.
<br>

### 2) nginx test 오류
   - https://github.com/beyond-sw-camp/beyond-sw-camp-be01_4nd_mini-project/issues/14
   <br>

#### 내용
- JAVA 17 버전으로 nGrinder 를 시도했을 때 Agent 실행과정에서 아래와 같은 에러가 발생
```
Caused by: java.lang.IllegalArgumentException: Unsupported class file major version 61
```
#### 결론
- JAVA 17 버전이 호환되지 않아 발생하는 에러

- 해결 방법 (택일)
   - JAVA 11로 버전 바꾸기
   - nGrinder-3.5.6으로 재설치 후 실행

- 11로 버전 바꾼 뒤 재부팅
<br>

### 3) nginx-proxy cache 적용 시 에러 발생
   - https://github.com/be01-4nd-mini-project-TEAM1/R4-nginx-proxy/issues/4
   <br>

#### 내용
- nginx-proxy nGrinder cache 설정 적용 후 테스트에서 에러 발생
#### 결론
- proxy server 오류 발생 시 agent server 포트가 변경되어 controller의 포트와 일치하지 않는 이슈 지속적으로 발견
- nGrinder(agent, controller server) 및 proxy server 모두 재부팅 후 해결됨

<br>
