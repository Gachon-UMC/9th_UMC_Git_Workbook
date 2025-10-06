# git 이란? 
분산 버전 관리 시스템 = 여러 버전을 관리하고 개발자들의 협력을 돕는 시스템

##가벼운 용어 정리 
working directory - 내가 현재 작업을 하고 있는 공간
staging area - commit 전에 변경 내용을 임시로 모아두는 공간
repository - 파일의 변경 사항들이 추적되고 관리 되는 저장소 
local repository - 내 컴퓨터 안에 있는 로컬 git 저장소 (내가 commit 시 여기에 저장된다)
remote repository - 원격저장소 내 컴퓨터에 저장하는게 아닌 원격저장소 
.gitignore - 보안등을 이유로 올라가면 안되는 파일을 설정해주는 파일!



git 흐름 
 working directory - (git add) -> Staging area - ( git commit ) -> local repository - (git push ) -> remote repository
흐름에 따른 명령어
git clone (레포지토리 주소)   -> git add . / git add (파일 이름)  -> git commit -m "(커밋 메시지)" -> git push origin (브랜치 이름)

그외 명령어
git status - 파일 상태확인 
touch (파일이름) - 파일 추가 
git log  - 니가 commit 같은거 한 기록 보기

###브랜치란?
메인 프로젝트에서 독립적으로 작업할 수 있는 분기 = 독립적인 작업과 협업 실험 등을 가능하게 함

관련 명령어
git branch - 브랜치 목록 확인
git branch (브랜치 이름)  - branch 생성
git switch (브랜치 이름) - 브랜치 이동
git branch -d (브랜치 이름) - 브랜치 삭제 

브랜치는 결국 merge 를 해야함 (메인 브랜치에 자기가 한 결과물을 합침) 근데 병합하기 전에 막 병합하면 안되니까 허락 맡아야지?
허락해줘 하는 요청 pull request  그 다음에 merge 
