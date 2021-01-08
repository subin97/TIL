# git command

> git을 사용하기 위한 기본 명령어

---

### 설정

##### 1. init

- `git init`
- 현재 폴더를 `git` 으로 관리하겠다. => `.git` 폴더를 생성
- 최초에 한 번만 실행하는 명령어



##### 2. config

- `git config --global user.email "email@email.com"`
- `--global` 옵션과 `--local` 둘 중 하나 선택해서 사용
  - 일반적으로 global 설정을 해놓으면 내 컴퓨터에서 추가적으로 변경할 일이 없음



##### 3. status

- `git status`
- 현재 git의 상태를 출력해주는 명령어



##### 4. remote add

- `git remote add origin [url]`
- 깃아, 원격저장소 추가해줘. 별명은 origin이고 실제 주소는 [url]이야.
- 원격저장소 주소를 저장

---

### 확인

##### 1. git version 확인

- `git --version`



##### 2. 로그 확인

- `git log` : 커밋 히스토리를 출력

  - `--oneline` 옵션 : 한 줄로 표시

  - `--oneline --graph` : 분기 처리 시각화하여 보여줌

    

##### 3. 변경사항 확인

- `git diff` : 마지막 커밋과 현재 폴더 상태를 비교해서 차이점을 출력

---

### 저장

##### 1. add

- `git add [추가하려는 파일]`
  - `git add .` : 한 번에 모든 파일과 모든 폴더를 add
- working directory에서 변경점을 staging area로 이동



##### 2. commit

- `git commit -m "커밋 메시지"`



##### 3. push

- `git push origin master`
- 원격저장소에 master 브랜치의 데이터를 전송

----

### Branch

##### 1. git branch

- `git branch` : 현재 생성되어 있는 branch 확인
- `git branch [새 브랜치 이름]` : 새 브랜치 생성

- `-d` 옵션 : 브랜치 삭제

  - 활동중인 브랜치는 삭제 불가능

  

##### 2. git checkout

- `git checkout [브랜치 이름]` : 브랜치 변경
- git 2.23 버전 이상에서 `checkout` 대신 `git switch` 명령어 사용

---

### Undo

##### 1. Unstage(add 취소)

- `git reset HEAD [파일]`
  - 2.23 버전 이후 : `reset` 대신 `restore`



##### 2. Uncommit

> 방법은 알아두되, 사용하지 않는 것이 좋음
>
> 커밋은 신중히!

- `git commit --amend` : 직전 commit의 **commit message** 수정
- `git reset HEAD^` : 직전 로그 삭제
  - `^` 개수만큼의 커밋 삭제

- `git reset`
  - `--hard` 
  - `--soft` 
  - `--mixed` 