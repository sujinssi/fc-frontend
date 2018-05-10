
## terminal 명령어 정리


* cd(change directory): 이동하기

```
$ cd ..
# 폴더 빠져나가기
$ cd foldername
# 폴더로 들어가기
```

* pwd / cd: 현재 folder 보여주기


* ls / dir: 현재 folder list 보여주기


* mkdir: 폴더생성

```
$ mkdir foldername
```

* rm : 폴더 삭제
```
$ rm [option] filename
```
    * 옵션

    -f : 쓰기권한(수정, 추가 삭제)이 없더라도, 묻지말고 지우기
    -i : 물어보고 지우기 (-I : 여러파일을 지울땐 한번만 물어보기)
    -r : 디렉토리 및 그 안의 모든 파일 지우기(reculsive의 약자)

* touch: 파일 생성(확장자 빼먹지 말기)

```
$ touch filename.extention
```

* cp / copy: 카피

```
# mac
$ cp filename copyfilename

# window
> copy filename copyfilename
```

* mv / move: 폴더 & 파일 이동

```
# mac
$ mv folder(file)name location

# window
> move folder(file)name location
```

* 터미널에서 VScode 실행

```
$ code .
// 만약 VScode가 실행이 안되면,
// mac: command + shift + p
// window: control + shift + p
// shell command: install 'code' command in PATH 추가
```

참조:<br> 

https://www.cybrary.it/0p3n/command-line-interface-cli-vs-graphical-user-interface-gui/

https://github.com/austinpark420/fds10-Activity.git

https://macinjune.com/mac/terminal/mac-terminal-rm-command%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%98%EC%97%AC-%ED%8C%8C%EC%9D%BC-%EC%82%AD%EC%A0%9C%ED%95%98%EA%B8%B0/

