20190807<br>

`Sourcetree 설치: https://www.sourcetreeapp.com/`

하나의 단일 작업이 git의 version이다.

version을 만드려면 파일이 stage에 올라와야 한다.

git의 3가지 공간
 * working directory: .git directory를 제외한 나머지 directory. 실제 작업 공간.
 * repository: .git directory
 * stage area: working directory에서 변경(작업)이 일어난 공간.

commit을 하게 되면 stage area의 파일이 repository에 복사가 된다.<br>
 -> 복사된 버전은 바로 이전 버전을 부모 key를 저장한다.<br>
 -> 부모 Key를 이용하여 해당 버전으로 되돌릴 수 있다.<br>
 -> HEAD를 기준으로 version이 생성된다.<br>
 -> check out 후 commit 하는 경우 새로운 version이 생성. <br>
 
 MASTER는 마지막 commit을 가리킨다.
 
 HEAD는 MASTER를 가리키고 MASTER는 마지막으로 Commit한 버전을 가리킨다.<br>
  - HEAD는 나의 working copy가 어느 버전에서 유래했는가를 알려준다.
  - Project의 상태를 알려주는 역할. Project 시작 시 HEAD의 위치를 파악한다.
  
check out
  - git에게 HEAD를 원하는 버전을 보게끔 하는 명령어.
  - working directory가 HEAD가 보는 버전 상태로 변경된다.