# Chapter 1 - Git & GitHub 요약

## Git이란?

> **Git** = 파일의 변경 사항을 추적하고 여러 사용자 간 협업을 조율하는 **분산 버전 관리 시스템**

### 핵심 기능
1. **파일 변경 사항 추적**  
   - 언제, 무엇이 변경되었는지 기록  
   - 여러 버전을 한 파일 내에서 관리 가능  
   - 이전 시점으로 되돌리기 쉬움  

2. **여러 사용자 간 협업 조율**  
   - 로컬(Local) ↔ 원격(Remote, 예: GitHub)  
   - 여러 사용자가 동일한 프로젝트를 동시에 작업 가능  

3. **분산 버전 관리 시스템**  
   - 각 사용자는 전체 저장소의 복사본을 가짐  
   - 네트워크가 없어도 독립 작업 가능  

---

## Git의 주요 구성 요소

| 구성 요소 | 설명 |
|------------|------|
| **Working Directory** | 실제 작업 중인 폴더 |
| **Staging Area** | 커밋 전 준비 공간 (`git add`) |
| **Local Repository** | 로컬에 저장되는 커밋 이력 (`git commit`) |
| **Remote Repository** | GitHub 등 원격 서버 저장소 (`git push`) |

---

## Git 기본 명령어

| 목적 | 명령어 | 설명 |
|------|---------|------|
| 파일 추적 해제 | `.gitignore` | 특정 파일/폴더를 Git에서 무시 |
| 파일 추가 | `git add .` / `git add 파일명` | 변경 파일을 스테이징 |
| 변경사항 기록 | `git commit -m "메시지"` | 커밋 생성 (버전 저장) |
| 원격 업로드 | `git push origin main` | 로컬 변경사항을 원격에 반영 |
| 상태 확인 | `git status` | 현재 추적 상태 확인 |

---

## 브랜치 (Branch)

| 명령어 | 설명 |
|---------|------|
| `git branch 브랜치명` | 브랜치 생성 |
| `git switch 브랜치명` | 브랜치 전환 (`checkout`보다 최신) |
| `git merge 브랜치명` | 다른 브랜치의 변경사항 병합 |
| `git log` | 커밋 기록 조회 |

> 협업 시에는 직접 `merge`하지 않고 **Pull Request(PR)** 를 이용해야 충돌 위험을 줄일 수 있음.

---

## HEAD란?

- **HEAD** = 현재 브랜치의 최신 커밋을 가리키는 포인터  
- `git log` 에서 `(HEAD -> main)` 형태로 표시됨  

---

## GitHub 협업 도구

### Issue
- **작업 단위 목표**를 등록하는 공간  
- 내용 구성:
  - 제목 (예: `feat: 로그인 기능 구현`)
  - 작업 내용 (To-Do)
  - 담당자(Assignee)
  - 태그(Label)
- 위치: Repository → `Issues` → `New Issue`

### Pull Request (PR)
- 기능 브랜치의 작업 내용을 **메인 브랜치에 반영 요청**
- PR 내용:
  - 작업 요약 및 변경사항
  - 리뷰어(Reviewers) 지정  
- 위치: Repository → `Pull requests` → `New pull request`