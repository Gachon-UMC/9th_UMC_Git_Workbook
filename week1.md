#1주차 Git 정리
Git은 분산 버전 관리 시스템으로 
-버전 기록 및 관리
-협업
-로컬 저장소
와 같은 도구 기능을 한다.

Github는 Git을 사용하는 프로젝트를 위한 원격저장소 역할을 한다.

Working Directory: 내 로컬 프로젝트 폴더
Staging Area: git add 명령어 입력 시 파일들이 해당 영역으로 올라감
Local Repository:  git commit 명령어 입력 시 스테이징 영역에 있던 파일들이 여기에 기록됨-> 버전으로 저장된 상태가 됨

-gitignore을 통해 특정 파일이 추적되지 않도록 설정할 수 있다.

Git add: 변경된 파일들을 스테이징 영역에 올림
Git commit: 스테이징된 파일들을 로컬 저장소에 기록함
Git push origin (브랜치 이름): 로컬 저장소에 기록된 커밋을 원격 저장소로 올림
Git status: 현재 작업 상태 확인
Git merge: 다른 브랜치의 내용을 현재 브랜치로 합친다.
Git log: 커밋 내역 확인

Issue 작성:브랜치에서 기능 브랜치를 나누기 전 팀원들과 프로젝트의 작업 진행 현황과 기능 구현, 버그 수정, 리팩토링 등을 공유하기 위해 사용한다.
Pull Request: 작업한 내용을 main브랜치에 반영해줄 것을 요청