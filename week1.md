Git과 Github란 무엇인가?
========================

- Git은 특정 파일, 폴더의 변경사항을 저장하는 시스템. 이를 분산 버전 관리 시스템이라 부른다.
- Git으로 로컬 파일의 버전을 관리할 수 있다면, 온라인 상에 있는 저장소인 Github를 이용하면 여러 사용자가 하나의 프로젝트를 동시에 접근하고 관리할 수 있다

---
    
### Git을 이용한 관리 방법

- Git은 레포지토리라는 저장소를 사용하는데, 이 저장소 안에서 여러 파일, 폴더를 관리할 수 있다.   

* 내가 현재 작업하고 있는 공간을 *working directory* 라고 부른다.
    - 기본적으로 *working directory* 내부의 파일은 추적되지만, 보안상의 이유로 원격 저장소에 올리지 못하는 경우 .gitignore이라는 파일을 이용해 추적을 못하게 할 수 있다.
* 많이 사용했듯이 Git에서 버전을 관리할 때는 add, commit, push를 사용한다
    - add : 변경사항이 있는 파일(폴더)를 commit하기 위해 stage에 올려주는 명령어
    - commit : staged상태인 파일을 로컬 레포에 기록하는 명령어
    - push : commit된 내용을 원격 레포인 Github에 올려주는 명령어

add 사용 예시: 

    $ git add .
    $ git add kano.txt

commit 사용 예시:

    $ git commit -m "my first commit"

push 사용 예시:

    $ git push origin (branch)

여기서 origin은 원격 레포지토리의 URL을 담고 있는 키워드인데, 꼭 origin을 쓰지 않아도 되지만 보통 origin을 사용함.  

기본적으로 로컬 레포를 만들 때 **git clone**으로 만들었다면 origin으로 URL이 할당된다.

내 파일의 상태를 확인하는 명령어: 

    $ git status

해당 명령어는 working directory에서 파일의 변경사항이 있는지를 보여준다.  

-----

### Branch란?
- repository에는 메인 작업 공간이 되는 main 이 있다.
- 이 main에서는 각 팀원이 작업한 내용이 합쳐지는 공간이 되고, 기능별로 branch를 만들어 그 기능을 담당하는 인원들은 해당 branch에서 작업을 진행한다.
- 모두 작업이 끝나면 합치는 작업을 하는데, 방법으로 merge와 pull request가 있다
- 하지만 보통 충돌의 위험때문에 merge는 사용하지 않고 pull request로 main과 병합한다.

branch를 만드는 명령어:

    $ git branch (branch)

해당 branch로 이동하는 명령어:

    $ git checkout (branch)
    $ git switch (branch)

여기서 **checkout**과 **switch**가 있는데, 기존 **checkout**은 브랜치를 이동, 파일의 수정 내용을 복원해주는 역할을 모두 사용했지만, 현재는 이 역할이 너무 과도하다고 판단해 브랜치를 이동시키는 **switch**와 파일의 수정 내용을 복원하는 **restore**로 명령어가 나뉘었다.  

따라서 **checkout**보다는 **switch**를 사용하는게 좋다.

-------

### Commit 기록 확인

> Git은 버전 관리 시스템이다. 커밋으로 진행사항을 저장했으니 어떤 변화가 있었는지, 언제 수정했는지, 심지어는 다시 돌아갈 수도 있다.

그러면 어떻게 커밋한 내용을 확인할 수 있을까.

    $ git log

해당 명령어는 지금까지 커밋한 로그를 보여준다.

이 로그에는 어떤 내용이 들어가있을까

> **커밋 해시** : `commit 691ceb4268ec2c5b2d1afd79dd41f5783dcfac46`
> 
> **커밋 생성자** : `youz2me <kynhun20@gachon.ac.kr>`
> 
> **커밋 일시** : `Sun Sep 22 18:34:03 2024 +0900`
> 
> **커밋 메시지:** `fix: validate 명령어 파라미터 안들어가게 수정`

근데 로그를 보면 이런 내용이 보인다

    (HEAD -> main, origin/main, origin/HEAD)

- HEAD 현재 브랜치의 가장 최신 커밋을 참조하는 값으로, 브랜치를 새로 생성할 때 이 전 브랜치의 commit 기록을 모두 그대로 가져온다.
- 그래서 main의 commit이 v1까지 있다면 main에서의 head는 v1이고, 여기서 파생된 kano 브랜치에서 새로 v2커밋을 했을 때 kano에서의 헤드는 v2이다.

-------

### Issue와 PR

- Issue는 main 브랜치에서 기능 브랜치를 나누기 전 팀원들과 프로젝트의 직업 진행 현황과 기능 구현, 버그 수정, 리팩토링 등을 공유하기 위한 페이지이다.
- 이슈에는 제목, 내용, assignees, Labels, Projects, Milestone, Develop과 같은 내용이 있다.

> `이슈 제목`: 팀 내 프로젝트 컨벤션에 따라 달라질 수 있지만 보통 작업 태그(기능 구현 시 `feature`, 버그 수정 시 `fix`, …)와 대략적인 작업 요약이 들어가게 됩니다. 
>
>`이슈 내용`: 이 부분도 컨벤션에 따라 달라지는 부분입니다. 예시 자료에서는 작업할 브랜치와 작은 단위의 `To-Do`가 들어가 있네요!
>
>`Assignees`: 이슈를 작업할 담당자가 할당되는 부분입니다. 톱니바퀴 아이콘을 누르신 후 적절하게 할당하시면 됩니다! 보통 작업자가 이슈를 작성하기 때문에 작업자가 들어갑니다.
>
>`Labels`: 작업 태그가 할당되는 부분입니다. 이 부분도 팀 내 컨벤션에 따라 달라지는 부분입니다.
>
>`Projects`, `Milestone`: 조금 더 큰 단위의 작업 내용을 적을 수 있는 부분입니다. 이 부분은 이번 워크북 내에서는 다루지 않습니다! 시간 여유가 있으시다면 찾아보고 적용해보시는 것을 추천해드립니다.
>
>`Development`: 이슈와 연결된 브랜치 또는 PR을 연결할 수 있습니다.

- 이슈를 생성, 각 브랜치에서 기능을 만들고 작업한 내용을 main으로 병합할 때 내 작업 내용의 pull을 요청(request)하는 것이 PR이다.
- 이슈와 마찬가지로 PR에도 제목, 내용, Reviewers, Assignees, Labels, Projects, Milestone, Development가 있다.
- 다른 내용은 같지만 Reviewers 라는게 추가되었다.

> `Reviewers` 는 이렇게 리뷰가 필요한 상황에서 특정 인물을 리뷰어로 추가할 수 있습니다. 리뷰어로 추가된 사람은 작업이 할당되어 리뷰를 진행하게 됩니다!