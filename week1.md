# Week 1 – Git 기초 정리

## Git이란?

- 파일의 **변경 이력**을 저장하고
- 여러 사람이 함께 코드를 **공유·협업**할 수 있게 해 주는
- **분산 버전 관리 시스템(Distributed VCS)**

## Git이 필요한 이유

- `최종.hwp`, `진짜최종.hwp` 같은 **파일 복사 지옥 방지**
- 언제, 무엇이, 어떻게 바뀌었는지 **커밋 단위로 기록**
- 특정 시점으로 **되돌리기 / 비교** 가능
- GitHub(원격 레포)와 연동해서 **팀 프로젝트 협업**에 필수

---

## Git의 기본 구조

- **Repository(레포)**: 프로젝트 폴더 전체를 관리하는 저장소
  - **Local Repo**: 내 컴퓨터에 있는 레포
  - **Remote Repo**: GitHub 같은 서버에 있는 레포

- **Working Directory**  
  실제로 파일을 수정하는 작업 폴더

- **Staging Area**  
  커밋에 포함할 변경만 골라 올려두는 곳  
  → `git add` 로 **Modified → Staged** 상태로 변경

- **Local Repository**  
  `git commit`으로 Staged 된 변경을 **버전(커밋)** 으로 기록하는 곳

---

## 자주 쓰는 Git 명령어

```bash
git status                # 현재 상태 확인
git add .                 # 모든 변경 파일 staging
git add 파일이름          # 특정 파일만 staging
git commit -m "메시지"    # 커밋 생성
git push origin 브랜치이름  # 원격 레포로 올리기
