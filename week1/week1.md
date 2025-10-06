# 1주차 Git 학습 내용 정리

## Git이란?
Git은 분산 버전 관리 시스템으로, 소스 코드의 변경사항을 추적하고 관리하는 도구입니다.

## 주요 Git 명령어

### 1. 저장소 초기화
```bash
git init
```
- 현재 디렉토리를 Git 저장소로 초기화합니다.

### 2. 파일 상태 확인
```bash
git status
```
- 현재 작업 디렉토리의 상태를 확인합니다.
- 추적되지 않은 파일, 수정된 파일, 스테이징된 파일을 보여줍니다.

### 3. 파일 추가
```bash
git add <파일명>
git add .  # 모든 파일 추가
```
- 파일을 스테이징 영역에 추가합니다.

### 4. 커밋
```bash
git commit -m "커밋 메시지"
```
- 스테이징된 변경사항을 저장소에 저장합니다.

### 5. 브랜치 관리
```bash
git branch                    # 브랜치 목록 확인
git branch <브랜치명>         # 새 브랜치 생성
git checkout <브랜치명>       # 브랜치 이동
git checkout -b <브랜치명>    # 브랜치 생성 및 이동
```

### 6. 원격 저장소 연결
```bash
git remote add origin <저장소URL>
git push -u origin main
```

## .gitignore 파일
- Git이 추적하지 않을 파일이나 디렉토리를 지정하는 파일입니다.
- 예시:
  ```
  *.log
  node_modules/
  .env
  ```

## Git의 3가지 영역
1. **Working Directory**: 작업 중인 파일들이 있는 곳
2. **Staging Area**: 커밋할 준비가 된 파일들이 있는 곳
3. **Repository**: 커밋된 파일들이 저장되는 곳

## 학습 소감
Git을 통해 코드의 버전을 체계적으로 관리할 수 있다는 것을 배웠습니다. 특히 브랜치를 통해 여러 기능을 동시에 개발할 수 있다는 점이 인상적이었습니다.