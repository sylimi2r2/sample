A.	프로젝트 명 : CI/CD 자동화 파이프라인 구축 

B.	프로젝트 멤버 이름 및 멤버 별 담당한 파트 소개

임석윤 : CI/CD 자동화 파이프라인 구축 및 AWS ECS 배포 테스트 , ECS 배포 구현 , Java 사용  : https://github.com/sylimi2r2/sample : 최종 구현 repo 

김현태 : CI/CD 자동화 파이프라인 구축 및 AWS ECS 배포 테스트 , ECS 배포 구현 JavaScript 사용 : https://github.com/Kimhyuntae9665/CI-CD_pipeline_proj , 구현 repo readme 참고 

최광진 : 자동화 파이프라인 테스트 및 배포 테스트

C.	프로젝트 소개 : 이 프로젝트는 GitHub Actions를 활용하여 Java 기반 애플리케이션의 CI/CD 파이프라인을 구축하는 것을 목표로 합니다. 코드 변경 후 Github에 commit push  시 자동으로 빌드, 테스트(GitHubAction 이용), Docker 이미지 생성 및 배포(AWS-ECS 이용)가 이루어지도록 설정하였습니다.

D.	프로젝트 필요성 소개 : 소프트웨어 개발 과정에서 반복적인 빌드 및 배포 작업은 많은 시간과 노력을 요구합니다. CI/CD 파이프라인을 도입함으로써 이러한 작업을 자동화하여 개발 효율성을 높이고, 빠른 피드백을 통해 품질 향상을 도모할 수 있습니다.

E.	관련 기술/논문/특허 조사 내용 소개 : 

GitHub Actions: GitHub에서 제공하는 CI/CD 자동화 도구로, 다양한 이벤트에 대응하여 워크플로우를 실행할 수 있습니다.

Docker: 애플리케이션을 컨테이너화하여 일관된 실행 환경을 제공하며, 배포 자동화에 유용합니다.

Gradle: Java 프로젝트의 빌드 자동화를 위한 도구로, 의존성 관리와 빌드 스크립트 작성에 사용됩니다.



F.	프로젝트 개발 결과물 소개 (+ 다이어그램)


![image](https://github.com/user-attachments/assets/b6d594ad-46d1-43b4-b6b3-2f80b03596e6)


G.	개발 결과물을 사용하는 방법 소개 (설치 방법, 동작 방법 등) : 
1. 코드를 수정한다
2. git commit m git push를 한다 ==> GitHubAction이 push 를 감지하여 동작을 시작한다 
3. Gradle 을 이용하여 Java 코드를 자동으로 빌드 , 테스트, 패키징을 한다 
4. repo와 연동되어있는, repo에서 GithubAction을 이용해서 기존에 설정해 놓았던 규정대로 빌드, 테스트를한다
5. 기존에 설정해 놓았던 규정에 맞게 빌드,테스트를 통과하면
6. Docker 이미지 생성한다 
7. AWS Elastic Container Registry로 빌드된 이미지가 올라간다
8. 이 이미지를 이용해서 AWS ECS에서 Task Definition을 진행한다
9. Task Definition 후에 클러스터 안에서 Task Definition을 이용해서 서비스를 만든다
10. 배포를 진행한다
11. 공용 IP로 접속하면 업데이트한 웹 페이지가 보인다   

H.	개발 결과물의 활용방안 소개

교육용 자료: CI/CD 파이프라인 구축에 대한 실습 예제로 활용 가능

프로젝트 템플릿: 유사한 구조의 프로젝트에서 초기 설정 템플릿으로 활용

DevOps 연습: 개발자들이 DevOps 문화를 이해하고 실습하는 데 도움