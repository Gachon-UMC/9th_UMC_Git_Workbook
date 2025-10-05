## Week1 정리 시작
Git 한눈 요약
1) Git이란?

분산 버전 관리 시스템(DVCS)
→ 파일 변경 이력 추적 + 여러 사람이 동시에 협업 가능한 시스템

2) 왜 써야 해?

“최종/진짜최종” 파일 복제 대신 이력(로그)로 과거 상태 복원

여러 명이 같은 프로젝트를 작업해도 충돌 최소화 & 기록 공유

오프라인에서도 내 컴퓨터에 전체 이력 보유(분산)

3) 핵심 개념 지도

- Repository(Repo): 프로젝트 저장소 (여러 파일의 이력 보관)

- Local Repo(내 PC) ↔ Remote Repo(GitHub 등)

- Working Directory: 내가 파일을 수정하는 공간

- Staging Area: 커밋 “대기열” (선택한 변경만 커밋 가능)

- Commit: 특정 시점의 스냅샷(체크포인트)

- Branch: 독립 작업선 (기능/이슈 단위로 분기)

- Merge / Pull Request(PR): 브랜치 변경을 메인에 합치기(협업은 보통 PR로)

- gitignore: 추적 제외 목록 (비밀키/빌드 산출물 등)

4) 자주 쓰는 명령어 (기본 흐름)

# 최초만: 원격을 복제
git clone <repo-url>
cd <repo-name>

# 브랜치 생성/이동
git switch -c week1-myname   # = git checkout -b week1-myname

# 작업 후 변경 확인
git status

# 스테이징 -> 커밋
git add .                 # 전체 변경 추가(또는 특정 파일만: git add README.md)
git commit -m "feat: week1 정리 추가"

# 원격으로 푸시
git push -u origin week1-myname

# 로그 확인
git log --oneline --graph --decorate --all

5) .gitignore 빠르게

-특정 파일: ignore.md

-확장자 전체: *.log

-폴더 전체: dist/

-윈도우에서 파일 생성:

-PowerShell: New-Item .gitignore -ItemType File

-또는 Git Bash: touch .gitignore

-이미 추적된 파일을 무시하려면:
git rm --cached ignore.md && git commit -m "chore: stop tracking ignore.md"

6) 브랜치 & PR 협업 요령

-기능 단위로 새 브랜치에서 작업 → 작은 커밋으로 자주 저장

-작업 끝나면 원격 푸시 후 PR 생성

-base: main, compare: 내 브랜치

-변경 요약/의도/테스트 방법 기재 → 코드리뷰 → Merge

7) 최소 워크플로우(요약 6줄)

git switch -c week1-myname

파일 수정 → git add .

git commit -m "week1 정리"

git push -u origin week1-myname

GitHub에서 PR 생성

리뷰/승인 후 Merge
