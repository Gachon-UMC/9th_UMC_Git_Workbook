깃 사용해야 하는 이유
버전 관리\_변경 사항 저장

깃 기능
변경 사항 추적 - 수정한 시점, 어떻게 수정했는지 확인 가능
공동 작업, 협업 - 여러 유저가 원격 저장소(깃허브)에 있는 작업물 동시접근 가능
분산 버전 관리 시스템 - 여러명이 한 파일에 접근해 개별적 작업, 그걸 버전으로 반영

깃의 저장소\_Repository - 작업하는 파일이 저장되는 폴더
레포 → 로컬 저장소(내 컴) + 원격 저장소(깃허브)
1 ) working 디렉토리 : 내가 작업하고 있는 공간 - 비번같은거 .gitingnore로 빼서 여기에
2 ) staging area : staged 된 상태의 파일들
변경 후 진행상황 세이브, 체크포인트 만들기 = commit
modified된 일부 파일을 선택적으로 stage( 커밋 준비 단계 ) = add
3 ) local repository
변경 사항 반영 과정 : add → [ staged ] → commit → [ local 레포에 반영 ]

깃 클론해서 가져오고,,
gitignore 생성 - touch .gitignore << git bash 에서 해야 가능(윈도우에서는 touch X )

git add [파일명] : 파일 { staged } 상태로 변경
→ git commit -m “[커밋msg]” : staged된 파일 commit 해서 local 레포에 반영

git push origin [branch명]
→ origin : 원격 레포(in Github) 의 URL 담은 키워드 \_ 대명사
→ push : 로컬 레포 반영 내용을 원격 레포에 보내기

add*파일 staged(커밋준비)
→ commit*파일 로컬레포 반영 → push\_로컬레포 반영 내용을 원격레포에 보내기

branch 변경
git checkout / switch [브랜치명] << checkout보다 switch 권장

branch 머지
git merge [브랜치명]

커밋 기록 확인
git log

git flow 방식 : 기능 별로 브랜치 나누고 관리하는 방식
Issue : 기능 브랜치 나누기 전 작업 현황, 기능 구현, 리팩토링 등 공유하기 위해 생성

내 작업 메인 브랜치에 반영할 때 : PR
메인 브랜치에게 pull 받아줄 것을 Request 하는 것
