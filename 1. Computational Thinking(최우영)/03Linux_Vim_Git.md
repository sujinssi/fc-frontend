
# 1주차-180511(목)
---
## [1] 

## 1. Linux

## Before Linux

- 1965년 데니스 리치, 켄 톰슨 외 x명이 AT&T Bell 연구소에서 PDP-7 기반 어셈블리어로 작성한 UNIX를 개발
 
- 1973년 데니스 리치와 켄 톰슨이 C를 개발한 뒤, C 기반 UNIX 재작성

- 1984년 리차드 스톨먼이 오픈 소프트웨어 자유성 확보를 위한 GNU 프로젝트 돌입 (GNU == `G`NU is `N`ot `U`nix)

- But, GNU 프로젝트에는 커널이 없었고..

---
### Kernel
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8f/Kernel_Layout.svg/380px-Kernel_Layout.svg.png)
- 하드웨어와 응용프로그램을 이어주는 운영체제의 핵심 시스템소프트웨어

---
## Linus Torvalds
<iframe width="860" height="480" src="https://www.youtube.com/embed/IVpOyKCNZYw" frameborder="0" allowfullscreen></iframe>

- 헬싱키 대학생이던 리누스 토발즈는 앤디 타넨바움의 MINIX를 개조한 Linux를 발표
- 0.1 - bash(GNU Bourne Again SHell), gcc(UNIX 기반 C 컴파일러)

---
## Linux
- 리누스 토발즈가 작성한 커널 혹은 GNU 프로젝트의 라이브러리와 도구가 포함된 운영체제
- PC와 모바일, 서버, 임베디드 시스템 등 다양한 분야에서 활용
- Redhat, Debian, Ubuntu, Android 등 다양한 배포판이 존재

---
## Shell
- 운영체제의 커널과 사용자를 이어주는 소프트웨어(대화하기 위해 만든 프로그램)

- sh(Bourne Shell): AT&T Bell 연구소의 Steve Bourne이 작성한 유닉스 쉘
- csh: 버클리의 Bill Joy가 작성한 유닉스 쉘(C언어랑 비슷한 모양)
- bash(Bourne Again Shell): Brian Fox가 작성한 유닉스 쉘
	- 다양한 운영체제에서 기본 쉘로 채택
- zsh: Paul Falstad가 작성한 유닉스 쉘(강사님 사용하심)
	- sh 확장형 쉘
	- 현재까지 가장 완벽한 쉘

- 쉘 바꾸는 것은 쉽다. 배시 위에서 루트 위에 서 chsh(changshell)하면 바꿀 수 있다.

---
## Let's learn bash
- 터미널을 사용해보자! 

```
~$ //최상위 유저 폴더
~/ //최상단폴더
```
ls 하면 하위 폴더 보기
ls -l 하면 상세정보까지 볼 수 있다
ls -al 숨김파일까지 다 폴 수 있음

touch .index.js //숨김파일 만들기
mv index.js ../ //상위폴더로 옮기기(슬래시 안붙여도 됨) 
mv index.js server.js //파일을 옮기는게 아니라 파일 이름 바꾸는 것.

cp server.js sample/ //server.js파일을 sample폴더 안으로 복사해서 안으로 넣기
현재폴더 안에 있는 sample폴더로 옮기고 싶으면 ./sample/ 을 사용할 것

rm server.js //파일 지우기
rm -rf sample //폴더(객체묶음)를 지우기
	-r 옵션은 안의 내용을 지우고 나와서 빈폴더까지 지우는 것
	-f 는 허가를 받지 않고 그냥 지우겠다는 뜻

---
## Shell Command Basic
```
$ cd documents

$ mkdir python - make directory python
$ cd python - change directory
$ cd .. - up to

$ ls
$ ls -al

$ touch hello.py - create hello.py
$ exit - terminate shell

```

---
## chmod
> 파일의 권한을 설정할 때 사용

`drwxr-xr-x` //d는 directory, r-x=group(유저들)권한, r-x=visitor권한
`d` or `-`: directory or file
(user)(group)(other)

`r`: read
`w`: write
`x`: execute
`-`: no permission


---
## chmod
`$ chmod [옵션] (8진수) (파일명)`

8진수
0: 000
1: 001
2: 010
3: 011
4: 100
5: 101
6: 110
7: 111

- 아마 거의 111이나 777만 사용할 것.

---
## Shell Command Basic
```
$ mv hello.py python
$ cp hello.py python

$ rm hello.py
$ rm -rf python/


$ python --version
$ python --help
```

- 참고자료 :  https://asciinema.org/a/6cciD0bDcHnH6i6G2n64PJtIa

---
##2. Vim
## Vim
![](https://www.vim.sexy/img/Vimlogo.svg)
- 윈도우의 메모장이랑 비슷한데 많은 추가기능을 붙일 수 있다. 

---
## Vim
![](http://www.vim.org/images/0xbabaf000l.png)
Copyright (c) 2007 Laurent Gregoire
- Vi improved Text Editor

---
## Vim Basic

빔을 열면 노멀모드로 열리기 때문에 코딩하기 빡세다. 
i를 누르면 편집가능한 insert 상태가 된다. 
esc를 누르면 normal mode가 종료된다. 
저장 안하고 나가기는 esc -> :qa
콜론(:)이 메뉴다. q는 quite w=write
저장하고 나가기는 :wq 저장하지 않고 나가기는 :q
터미널에서 cat index.js 하면 안의 내용을 확인할 수 있다.
git commit을 옵션없이 하면 vim으로 넘어가기 때문에 그때 대처할 수 있도록 지금 배우는 것. 
vim에서 편집할 때는 title과 내용으로 저장 됨. 제목이 깃에 저장되기 때문에 어떤 일을 언제 했는지 잘 남겨주는 것이 중요.

---

## Vim Basic

Command
```text
h,j,k,l - move cursor
i - insert mode
v - visual mode
d - delete
y - yank
p - paste
u - undo
r - replace
$ - move end of line
^ - move start of line

:q - quit
:q! - quit w/o write(no warning)
:wq - write and quit

:{number} - move to {number}th line
```

---
### write `hello.py` with Vim
`$ vim`
`$ vim hello.py`

`i`
`-- insert --`
type `print("hello python!")`
press `esc` to escape

`:wq`

`$ python hello.py`

---
### copy & paste
`$ vim hello.py`

`v`
`-- visual --`
블록지정 후 `y`
`p`

press `esc` to escape
`:wq`

`$ python hello.py`

---
### Use macro with Vim 
`$ vim hello.py`
`qa` - a라는 매크로를 생성

`--recording--`이 보이면 매크로 작성

`q` - 매크로 작성 종료

`@a` - a 매크로 실행
`10@a` - a 매크로 10회 실행


---
##3. Git
## git
![](http://ipengineer.net/wp-content/uploads/2015/04/git-logo.jpg)

---
## VCS (Version Control System) : git은 버전을 관리하기 위한 시스템
== SCM (Source Code Management)
< SCM (Software Configuration Management: 형상관리)
- 형상관리는 리소스, 연봉, 네트워크 등 개발을 하기 위한 모든 제반사항을 관리하는 것. 

---
## chronicle of git
![](https://www.blogcdn.com/www.engadget.com/media/2009/10/linus-torvalds-gives-windows-7-a-big-thumbs-up.jpg)

---
## chronicle of git
- Linux Kernal을 만들기 위해 Subversion을 쓰다 화가 난 **리누스 토발즈**는 2주만에 git이라는 버전관리 시스템을 만듦
[git official repo](https://github.com/git/git)
- 깃의 깃에 들어가면 소스코드를 볼 수 있다. 2주만에 만들었기 때문에 빠르고 간단함.

---
## Characteristics of git
- 빠른속도, 단순한 구조
- 분산형 저장소 지원
- 비선형적 개발(수천개의 브랜치) 가능

---
## Pros of git
- **중간-발표자료_최종_진짜최종_15-4(교수님이 맘에들어함)_언제까지??_이걸로갑시다.ppt**


- 소스코드 주고받기 없이 동시작업이 가능해져 생산성이 증가
- 수정내용은 **commit** 단위로 관리, 배포 뿐 아니라 원하는 시점으로 **Checkout** 가능
- 새로운 기능 추가는 **Branch**로 개발하여 편안한 실험이 가능하며, 성공적으로 개발이 완료되면 **Merge**하여 반영
- 인터넷이 연결되지 않아도 개발할 수 있음

---
## Open-source project

- 파이선, Angular의 소스코드를 확인할 수 있다. 내가 쓰는 기능이 이렇게 구현되어 있구나 볼 수 있다.

https://github.com/python/cpython
https://github.com/tensorflow/tensorflow

https://github.com/JuliaLang/julia
https://github.com/golang/go


https://github.com/jkeun

---
## git inside
- Blob: 모든 파일이 Blob이라는 단위로 구성 
- Tree: Blob(tree)들을 모은 것
- Commit: 파일에 대한 정보들을 모은 것

---
## git Process and Command
![](https://i.stack.imgur.com/MgaV9.png)

우리가 작업하는 공간이 workspace
workspace에서 index에 올려서 git이 인식하는 순간 한번 commit된 것
local repository에 올리면 또 한번 commit된 것.
(벌써 commit이 두번 이뤄진 것)
마지막으로 local repository에서 remote repository에 push!


---
## Useful manager for mac
http://brew.sh/index_ko.html


---
### install git
https://git-scm.com/

```shell
// MacOS
$ brew install git
// Linux
$ sudo apt-get install git
```

- Windows: install [git bash](https://git-scm.com/)

`$ git --version` 으로 정상적으로 설치되었는지를 확인


---
## git is not equal to github
![](http://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s1600/Github2.png)


---
### sign up github
https://github.com/


**important!!**
- 가입할 `email`과 `username`은 멋지게
- private repo를 원한다면 $7/month


---
##github 실습

github에서 repo 하나를 파주자
초기 세팅을 미리 할 수 있다. 
- 'add .gitignore'로 숨김파일만들 수 있다.
- 'add a license' 라이센스를 추가할 수도 있음
- readme.md 미리 만들 수 있다 / 우리는 만들지 않고 시작하는 방법으로 할 것.

```
$git init
```
git init을 하는 순간부터 git과 연결되는 것. 프로젝트를 시작할 때 처음부터 git init하고 시작하면 ㅈ호음
git init으로 유저의 최상단 폴더에서 깃을 설치하면 안된다. 그러면 내 컴퓨터를 공유하는 것. 
ls -al로 .git이 있냐 없냐를 통해 깃과 연결되어 있는지 확인할 수 있다.

파일을 추가하거나 수정한 뒤에

```
$git status // 상태 확인
$git add filename
#git status
$git commit //vim으로 들어와 메세지 입력. (i로 들어와서 쓰고 esc로 나가기하고 :wp로 저장해서 vim나가기)
```
받는 사람이 누군지 알기 위해 리모트저장소를 알려주자
받는 사람 주소에 대한 별명 같은 것이 origin. 다른 별명을 해도 상관 없는데 한번 하면 계속 그 별명을 사용해야함.
받는 사람 주소는 프로젝트 할 때 한번만 하면 된다.
``` 
$git remote origin https://github.com/sujinssi/deleted_soon.git
```
이제 우리 변경사항을 master차원으로 올려보자
```
$git push origin master 
```

빔으로 들어가서 직접 수정해보자
```
$vi readme.md
```
이번에는 빔에서 말고 터미널에서 바로 메세지를 달아보자
```
$git commit -m "Practicing git
```
이렇게 하면 개행이 열린다. 여기부터 내용을 적으면 됨.내용 다 적으면 
```
$"
```
마지막으로 푸시하기
```
$git push origin master
```
---
github에서 MIT license가 가장 자유로운 라이센스다. 만약 GNU open소스는 별로 오픈되어 있지 않아서
어떤 오픈소스가 저 라이센스라면 그 소스는 안쓰는게 좋다.

이미 깃이 연결되어있는 폴더와는 연결하면 안된다. 꼬임.
방금만든 깃 레포를 연결해서 와보자
깃헙 원격저장소 -> 로컬로 클론 해보자
$git clone https://github.com/sujinssi/TIL.git
ls로 찍어보면 방금 만든 TIL가 받아져내려온 것을 알 수 있다. 
$ cd TIL
$ mkdir README.md
$ vi README.md // 내용을 수정한다
$ git add .
$ git status
$ git commit - "modified content"
$ git push origin master


* 레포 지우는 법

setting-danger zone

---
## Important github User Interface

spoqa.github.io처럼 기술 뿜뿜하는 블로그를 만들 수 있다. 
유저네임.github.io로 사용할 수 있음. 
블로그 글 하나당 html파일 하나가 존재해야 하는 단점이 있다. 

* 블로그 만들어보자!
1. 새로운 레포를 먼저 판다(sujinssi.github.io)
2. 새 래포 주소를 복사해서 
```
$ git clone https://github.com/sujinssi/sujinssi.github.io.git
```
3. 클론된 레포 파일 안에 index.html파일을 만들어준다
```
$ cd sujinssi/github.io.git
$ touch index.html
```
4. ...? 졸아서 기억이 안남

* commit의 개념

 : 커밋은 기능별로 다르게 해주는 것이 좋다
 ex. 결제기능 + 유저 로그인 ==> 하나의 커밋 (x)
     결제기능 ==> 결제 커밋
     유저로그인 ==>유저로그인 커밋

로컬 파일 안에도 새로운 파일을 만들었고, git에서도 how-to-use-git.md 새로운 것을 했다(?) 

1. 새로운 폴더를 dev폴더 안에 만들어준다.
2. 안에 180510-sample.md를 만든다
3. git init
4. 180510-sample.md 파일 내용을 만든다
5. 우리가 만든 파일 먼저 푸시해보자
우리가 필요한 기능만 싸서 송장에 붙여서 택배를 붙이는 것. 일단 인덱스에 있는 것 먼저 올리자
git commit -m "Add 180510-sample.md"
git add git/180510-how-to-use-git.md
git status
git commit -m "edit 180510-how-to-use-git.md"
git status
git push origin master

---
### Star
![](../img/star.png)

### watch
![](../img/watch.png)

---
## Set configuration
terminal
```shell
$ git config --global user.name "username"
$ git config --global user.email "github email address"
$ git config --list
```

---
## My First Repo
Let's make your first repo with github

---
## My First Repo
`$ git init`
`$ git add .`
`$ git commit -m "some commit"`

After create new repo through github,

`$ git remote add origin https://github.com/username/repo.git`
`$ git push origin master`


---
## github pages

---
## My First Github Pages
github 저장소를 활용해 정적인 사이트 호스팅이 가능

`username`.github.io 
http://tech.kakao.com/
https://spoqa.github.io/

---
### sample index page
After create new repo throuch github,

`$ git clone https://github.com/username/username.github.io.git`

Create New file `index.html`

`$ git add .`
`$ git commit -m "first page"`
`$ git push origin master`

---
### sample index page
```html
<!doctype html>
<html>
 <head>
  <meta charset="utf-8">
  <title>My first gh page</title>
 </head>
 <body>
  <h1>Home</h1>
  <p>Hello, there!</p>
 </body>
</html>
```

---
### Static Site Generator
- [Jekyll](https://jekyllrb.com/): Ruby 기반 정적인 블로그 생성기
	- 설치와 사용이 쉬움
	- 사용자가 많았음 
- [Hugo](https://gohugo.io/): Golang 기반 정적인 블로그 생성기
	- 빠른 속도로 사이트를 생성
	- 사용자 증가 중
- [Hexo](https://hexo.io/): Node.js 기반 정적인 블로그 생성기
	- Node.js를 안다면 커스터마이즈가 쉬움
	- 빠른 속도로 사용자 증가 중

**Recommand**
`Jekyll` > `Hugo` > `Hexo`

---

## What is branch? 
![](https://www.sideshowtoy.com/assets/products/3005011-groot/lg/marvel-guardians-of-the-galaxy-groot-premium-format-3005011-02.jpg)


## What is branch?
분기점을 생성하고 독립적으로 코드를 변경할 수 있도록 도와주는 모델

ex)

master branch : 생성하지 않아도 만들어지는 메인 차원.
```python
print('hello world!')
```

another branch 
    -> 본 소스에 영향을 미치지 않고 코딩가능. 보통 배포용
```python
for i in range(1,10):
    print('hello world for the %s times!' % i)
```


---
## Branch

Show available local branch
`$ git branch`

Show available remote branch
`$ git branch -r`

Show available All branch
`$ git branch -a`

---
## Branch


Create branch
`$ git branch stem`

Checkout branch
`$ git checkout stem`

Create & Checkout branch
`$ git checkout -b new-stem`

make changes inside readme.md
`$ git commit -a -m 'edit readme.md'`
`$ git checkout master`

merge branch
`$ git merge stem`

---
## Branch

delete branch
`$ git branch -D stem`

push with specified remote branch
`$ git push origin stem`

see the difference between two branches
`$ git diff master stem`

---
## git flow strategy
![](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAKMAAAAJDM2NjY0OWE4LTc0NDAtNDdkMS1hMDdiLWU3MzkwM2FjYWExNw.png)



---
## use git flow easily!
[Link](https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html)

![](https://danielkummer.github.io/git-flow-cheatsheet/img/git-flow-commands.png)

---
## Collaborate with your Co-worker

---
## Method 1: Collaboration
Add Collaborator
![](../img/collaborators.png)

---
## Collaboration
Add, Commit and Push like you own it. 

---
## Method 2: Fork and Merge
![](../img/fork1.png)

---
## Fork and Merge
![](../img/fork2.png)

---
## Fork and Merge
![](../img/fork3.png)

---
## Fork and Merge
`$ git clone https://github.com/username/forked-repo.git`
`$ git remote add upstream https://github.com/anotheruser/original-repo.git`

---
## Fork and Merge

`$ git fetch upstream`
`$ git merge upstream/master`
`$ git branch -a`
`$ git checkout -b new-feature`

---
## Fork and Merge

Make some change

`$ git add file`
`$ git commit -m "commit message"`
`$ git push origin new-feature`

---
## Fork and Merge
![](../img/pr1.png)

---
## Fork and Merge
![](../img/pr2.png)

---
## Fork and Merge
![](../img/pr3.png)

---
## Fork and Merge
![](../img/pr4.png)

---
## Fork and Merge
![](../img/pr5.png)

---
## Fork and Merge
![](../img/pr6.png)

---
## Fork and Merge
![](../img/pr7.png)
---
## continuous pull

---
## continuous pull

`$ git remote add upstream https://github.com/anotheruser/original-repo.git`

`$ git fetch upstream`
`$ git merge upstream/master`

---
## Assignment

1. [Try git](https://try.github.io/levels/1/challenges/1)
마지막 결과를 Print Screen 후 'fds-random'에 제출
2. TIL에 오늘 배운 깃 정리해서 올리기


* 강의 녹화 영상

	https://asciinema.org/a/rpankaih2wQt2NfdX1hdlbzVb
	https://asciinema.org/a/6cciD0bDcHnH6i6G2n64PJtIa

	https://youtu.be/A3wb9ldtMjY
	https://youtu.be/jBywy9G0CEE
	https://youtu.be/0CR4qLBhhBA
	https://youtu.be/Zk1akSOtCP4