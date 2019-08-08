# 20190808<br>

**자식 commit id는 부모의 commit id를 항상 참조한다.<br>**
**commit은 commit이 동작한 시점의 stage area에 대한 스냅샷이다.**


# 20190807<br>

`Sourcetree 설치: https://www.sourcetreeapp.com/`

**하나의 단일 작업이 git의 version이다.**

**version을 만드려면 파일이 stage에 올라와야 한다.**

**git의 3가지 공간**
 * working directory: .git directory를 제외한 나머지 directory. 실제 작업 공간.
 * repository: .git directory
 * stage area: working directory에서 변경(작업)이 일어난 공간.

**commit을 하게 되면 stage area의 파일이 repository에 복사가 된다.**<br>
 -> 복사된 버전은 바로 이전 버전을 부모 key를 저장한다.<br>
 -> 부모 Key를 이용하여 해당 버전으로 되돌릴 수 있다.<br>
 -> HEAD를 기준으로 version이 생성된다.<br>
 -> check out 후 commit 하는 경우 새로운 version이 생성. <br>
 
 **MASTER는 마지막 commit(마지막 version)을 가리킨다.**
 
 **HEAD는 MASTER를 가리키고 MASTER는 마지막으로 Commit한 버전을 가리킨다.**<br>
  - HEAD는 나의 working copy가 어느 버전에서 유래했는가를 알려준다.
  - Project의 상태를 알려주는 역할. Project 시작 시 HEAD의 위치를 파악한다.
  
`check out`<br>
  - git에게 HEAD를 원하는 버전을 보게끔 하는 명령어.
  - working directory가 HEAD가 보는 버전 상태로 변경된다.
  - stage area에 올라가지 않은 파일이 있다면 check out이 되지 않는다.
  
`commit을 삭제하고 싶다면 MASTER를 원하는 버전을 바라보게끔 설정.`
  - reset은 MASTER를 움직인다.
  - $ git reset C1: Master를 C1으로 초기화한다.(옮긴다)
  - reset을 통해 원하는 버전으로 이동한다. 
  - $ git reset --hard 'commit ID' 를 하면 강력하게 돌린다.(강제 덮어쓰기)
  - $ git reset --hard 'HEAD@index'