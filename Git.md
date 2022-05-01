## Git ?

- : 협업도구, 코드를 카톡으로 보내거나 이메일로 보내는건 매우 비효율적이고... 대부분의 개발 작업은 공동작업 이므로
  보통 Git을 사용하여 협업을 진행한다. 회사 생활 필수 잇템이라 할 수 있겠다.

- : UI 어플리케이션등도 존재! 선택지는 여러가지이다.

## Set up

\*터미널에서

- git cofig
  깃에 대한 모든 설정을 확인해 보고싶을때
- git config --list
  파일로 열어보고싶을때
- git config --global e
  => 에디터로 열림, 운영체제 따라 달라지지만 그건 구글링!
  code .

1. 에디터연동해서 쓰기

- git config --global core.editor "code"
  열려진 파일이 종료되기 이전에도 다른 명령어 사용가능
  git config --global -e

  2. 에디터 연동해서 쓰기
     git config --global core.editor "code --wait
     열려진 파일이 종료되기 이전에는 다른 명령어 X
     git config --global -e

  3. 사용자 관련 정보 입력

  git config --global user.name "Seonhwa"
  git config user.name // 확인 -> Seonhwa
  git config --global user.email "seonhwa.oh1@gmail.com"
  git config user.email // 확인

4. 맥/윈도우 줄바꿈 관련으로 추가로 넣어야 하는거
   git config --global core.autocrlf true (?mac == "input" : true(window))

## Start

깃 만들기

1. mkdir git
2. cd git
3. ls - al

깃 초기화 : git init => master branch 생성
숨겨진 폴더 열기 : open .git
깃 삭제 : rm -tf git
깃 상태체크 : git status

-[명령어관련자료](https://git-scm.com/docs)

## Git Work Flow

크게는 3가지로 나눠진다
|working directory|staging area| .git directory|

working directory 에 있는 것을 => staging area로 옮기고 => commit 을 통해 git directory로 보내 히스토리에 저장된다

- checkout을 통해 깃 버젼관리 가능

하지만... 이렇게만 저장하면 내 로컬에만 저장이 되기 때문에 우리는 git 클라우드에 push 를 통해 일종의 백업을 해 준다.

### Working directory

: 플젝 파일 수정, 작업하는 공간

1. 각각의 커밋에는 고유의 해시코드가 부가됨, 아이디뿐만 아니라 버젼관련, 작성자, 시간같은 정보도 포함되어 있음.

2. untracked과 tracked 로 git이 나뉨

- untracked: 새로 만든 파일이나 기존 프로젝트에서 git초기화 했을 때
- tracked Git이 tracking하고 있는 파일들
  : 지금 시점에서 파일 수정 유무에 따라 Unmodified, Modified로 구분

  - Unmodified = 이전과 비교했을 때 달라진게 없다는 의미, staging area 이동불가
  - add 명령어 사용하여 staging area로 옮긴다.

- git add : staging area추가

- git add \*.css : 특정 파일만 staging area추가

- echo \*.log > .gitignore : 트래킹 하고싶지 않은 파일

- git status :작업 내용확인

- git diff : working directory 작업 비교

* 변경된 내용, 삭제된 내용 확인 가능

.gitignore : 깃에 올리고 싶지 않은 파일들을 지정

### Commit

- 커밋 명령어를 이용하여 git directory로 옮길 수 있다.

- 보통은 Title, Description으로 나누어서 설명을 적음 저장 후 확인 해 보면
  해시코드 + 타이틀 + 변경내용 확인 가능

- git log로 보면 히스토리 확인 가능

- 커밋단위는 기능별로, 의미있게 추가해 주는 것이 좋다.(중요!) 커밋메세지에 맞게 해당하는 내용만!!

## 순서

git add . (전체파일 추가)
git commit -m "커밋메시지", or
git commit -m "Title:타이틀, Desc: 상세설명"
git pull origin main
git push origin main
