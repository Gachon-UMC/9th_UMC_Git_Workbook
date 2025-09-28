# Git 1주차

## Git이란?
개발 환경에서 파일에서 변경되는 사항을 저장하고 쳬계적으로 관리하는 분산 버전 관리 시스템

## Repository란?
작업하는 파일들이 저장되는 폴더

### Working directory란?
내가 로컬에서 현재 작업하고 있는 공간

### Staging Area란?
추적되는 파일들의 상태는 총 3가지
unmodified : 변경 없음
modified : 변경된 파일
staged : 스테이지됨 (?)

#### staged 상태는 무엇일까?
commit을 위한 준비 단계

로컬에서 작업한 파일의 변경사항을 원격에서도 저장하고 싶으면,
git add -> commit -> push -> 저장완료!

### .gitignore란?
개인정보나 보안이 필요한 API key, node_module 같은 큰 용량의 파일들을 원격 저장소에 저장하지 않기 위함



