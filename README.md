20190807
`git offline`

- Sourcetree 설치: https://www.sourcetreeapp.com/

하나의 단일 작업이 git의 version이다.

version을 만드려면 파일이 stage에 올라와야 한다.

git의 3가지 공간
 * working directory: .git directory를 제외한 나머지 directory. 실제 작업 공간.
 * repository: .git directory
 * stage area: working directory에서 변경(작업)이 일어난 공간.

commit을 하게 되면 stage area의 파일이 repository에 복사가 된다.
 -> 복사된 버전은 바로 위버전을 부모 key를 저장한다.
 -> 부모 Key를 이용하여 해당 버전으로 되돌릴 수 있다.
 
 
 HEAD는 MASTER를 가리키고 MASTER는 마지막으로 Commit한 버전을 가리킨다.