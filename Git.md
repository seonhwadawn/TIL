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
