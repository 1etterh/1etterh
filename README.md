## Introduction
> 안녕하세요, 웹 개발자 김서현입니다.
- 업무 프로세스의 다양한 변수를 고려하여 자동화 프로젝트를 진행한 경험이 있습니다.
- 프로젝트를 개선하기 위하여 꾸준히 Refactoring을 진행하고 있습니다.
- 기술 블로그에 공부한 것들을 정리하고 주기적으로 복습 및 보완하여 새로운 기술을 효율적으로 습득하고 있습니다.


## Projects
### SYNCDAY
> 효율적인 개발 업무를 위한 워크 스페이스
#### 기술 스택
> Spring Boot, Spring Data JPA, MyBatis, Spring Security, OAuth2 GitHub API, Vue.js
#### 담당 기능
1. 업무 진척도 공유 기능
2. GitHub API 연동 기능
#### Trouble Shooting
##### 1. GitHub API For Java
1. 상황: 보안을 위해 백엔드(Java)에서 Github의 데이터를 수신 후 프론트엔드에 전송하고자 하였으나, 일부 메소드가 deprecated 되어 동작하지 않는 상황 발생
2. 목표: Secret Key와 Installation 정보는 백엔드에서 관리하며 기획된 기능을 정상적으로 구현하는 것
4. 해결 방안: 인증에 관련된 정보만 GitHub API For Java를 통해 관리하고, Frontend에서 GitHub 공식 API인 Oktokit을 활용
5. 결과: Secret Key와 InstallationId를 백엔드에만 저장하여 보안성을 확보함과 동시에 공식 GitHub API인 Oktokit과 GraphQL을 통해 필요한 정보만을 요청할 수 있었다.
##### 2. User - Project M:N 문제
1. 상황: M:N 관계에 있는 User-Project 해결을 위해 중간 테이블(ProjMember) 생성
2. 목표: 순환 참조가 일어나지 않도록 한 방향에서만 다른 도메인을 참조해야 한다.
3. 해결 방안: 프로젝트 관리 권한 등의 유효성 검증을 위해 프로젝트에 관련된 내용 수정 시 ProjMemberService 호출 후 ProjService 호출
4. 결과: 순환 참조 없이 유효성 검사 구현
#### 관련 링크
1. [Repository](https://github.com/beyond-sw-camp/be09_fin_SyncDay)
2. [Refactoring 계획](https://1etterhdev.atlassian.net/wiki/spaces/S/overview)
3. [회고](https://1etterh.github.io/devlog/Projects/syncday/SyncDay-%ED%9A%8C%EA%B3%A0)



## Contact
Email: 1etterh.dev@gmail.com <br>
Github: https://github.com/1etterh <br>
Blog: https://1etterh.github.io/devlog/
