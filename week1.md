# Week 1

## Git이란?
- 여러 사용자가 같은 파일의 작업을 관리할 수 있도록 돕는 **분산 버전 관리 시스템**  
- 코드를 **안전하게 기록하고 되돌릴 수 있게 하는 도구**

---

## Git의 3가지 영역
1. **Working Directory**  
   → 실제로 내가 작업하는 공간  
2. **Staging Area**  
   → 커밋하기 전에 변경 내용을 잠시 올려두는 공간  
3. **Local Repository**  
   → 최종적으로 커밋이 저장되는 나의 로컬 저장소

---

## Git 기본 흐름
1. 원격 저장소(Remote)와 로컬 연결  
2. `.gitignore`로 추적하지 않을 파일 관리  
3. `add`, `commit`, `push`로 파일 상태 관리  
4. `git status`로 현재 상태 확인

---

## 브랜치(Branch)
- 독립적인 작업 공간으로, 여러 기능을 동시에 개발할 때 사용  
- 명령어  
  - `git branch` : 브랜치 목록 보기  
  - `git checkout -b 브랜치명` : 새 브랜치 생성 + 이동  
  - `git merge` : 브랜치 병합  

---

## 커밋 기록 확인
- `git log` : 커밋 내역 조회  
- `HEAD` : 현재 브랜치의 최신 커밋을 가리킴  

---

## Issue와 PR (Pull Request)
- **Issue** : 해야 할 일이나 버그를 기록하고 관리  
- **Pull Request(PR)** : 브랜치에서 작업한 내용을 메인 브랜치에 반영할 때 사용  
