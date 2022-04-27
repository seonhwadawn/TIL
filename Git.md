## Git ?

- : 협업도구, 코드를 카톡으로 보내거나 이메일로 보내는건 매우 비효율적이고... 대부분의 개발 작업은 공동작업 이므로
  보통 Git을 사용하여 협업을 진행한다. 회사 생활 필수 잇템이라 할 수 있겠다.

- : UI 어플리케이션등도 존재하지만 그냥 회사 들어갔을때 많이 쓰는걸 사용하는게 좋고 이걸 적고 있는 본인은 터미널을 선호한다.

## Set up

1. mkdir git => ls al 을 커맨드창에 적어 깃 확인하기, 깃관련된건 그 안에 들어가짐
2. 만들고 나면 마스터 브랜치가 생김 (가장 기본 브랜치)
3. git 초기화는 git init
4. git status 작성이 귀찮을 때 = git config --global alias.st status 하면됨

## Git Work Flow

크게는 3가지로 나눠진다
|working directory|staging area| .git directory|

working directory 에 있는 것을 => staging area로 옮기고 => commit 을 통해 git directory로 보내 히스토리에 저장된다

- checkout을 통해 깃 버젼관리 가능

하지만... 이렇게만 저장하면 내 로컬에만 저장이 되기 때문에 우리는 git 클라우드에 push 를 통해 일종의 백업을 해 준다.
