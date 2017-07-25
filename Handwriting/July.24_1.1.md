필기 1주차 1회 7.24.2017
Hunger = True 나와있는 표
? 알고리즘을 표로 만든 것.
?	이 표는 불완전함. 굶는다라는 결과가 해결되지 않음. 
컴퓨터 작동 과정
사용자 ? 인풋 & 아웃풋
CPU ? 프로그램 카운터: 명령을 받아 쌓아 놓고 (ALU에게) 명령을 내리는 장치 / ALU: 기본적 연산 장치
MEMORY ? 실제 연산에 필요한 값들을 가지고 있는 곳. 연산을 해서 결과를 CPU에게 전달.
Patch: 기능을 수정, 업데이트할 때 사용하는 용어.
Debug: 오류를 수정하는 것. (실제 컴퓨터 본체 안에 벌레를 잡는 것에서 유래) 
Shell Command
Shell: OS에서 사용자의 명령을 하드웨어에 전달하는 프로그램 (시스템 소프트웨어)
?	유닉스와 리눅스에서는 배쉬(BASH) 사용
?	윈도우에서는 CMD, EXPLORER 사용. 
Shell 사용하기 위해서는 ? (윈도우 사용자의 경우 GIT BASH 다운로드 필요)
코드 설명시 앞에 $가 있다면 그것은 Shell 명령어라는 것.
?	$라는 표시는 단지 이것은 shell command라는 것이고 실제 입력시에는 사용되지 않음.
<몇가지 간단한 shell 명령어>
?	ls: 해당위치에서 들어가거나 사용할 수 있는 파일과 폴더의 종류를 나열해준다. (li == list)
?	ls -al: al이라는 옵션을 줘서 리스트를 다시 불러옴.
? a:는 숨긴 파일을 다 보여주는 옵션, l은 한줄 한줄 자세히 보여주는 옵션. 
같이 해볼 것: 특정한 폴더에 들어가 새폴더 생성하기
?	cd + 위치: 해당 위치로 들어감 (cd refers changing directory)
cd와 위치 사이에는 띄어쓰기 필수
?	mkdir + 새로운 디렉토리명 : 새로운 디렉토리 만듬

?	두가지 명령 동시에 하려면 ? && 사용
형식: 명령1 + && + 명령2
mkdir python && cd python 
(파이썬이란 디렉토리 만들고 파이썬으로 이동하라)

?	cd.. : 해당 위치에서 한단계 상위 폴더로 이동
여러 개의 폴더를 나가야 할때는, ..을 많이 붙이면 됨.
cd + ~ : 최초의 위치로 돌아옴.(최상위 폴더)

?	/ :디렉토리간 상위 하위 관계를 나타냄.
cd../..의 경우 상위로 2개를 나가게 됨. 
cd css/python ? 한번에 css안에 있는 python 디렉토리까지 이동가능

여기까지 새 폴더 만드는 것 배움
새로운 파일 만들기
?	touch + file name + extension: 해당 이름의 파일을 만듬. 
ex) touch hello.py
?	mv+ file+extension +위치: 파일 옮기기(이동)
ex) mv hello.py .. : 하나의 상위 폴더로 이동시킴
?	cp + file+extension + 위치: 파일 복사하기
ex) cp hello.py python
?	rm file+extension : 해당 파일 지우기
폴더를 삭제 할수 없음. 
?	rm -rf + 폴더명:  해당 폴더와 폴더 내용 모두 삭제
파일 수정하기
방법1
Git bash를 이용해서 원하는 디렉토리에 파일 만든다음 (hello.py) 윈도우로 나와서 메모장에서 작업하면 된다.
메모장에 print(“hello world”)와 같은 내용을 입력해서 저장ㅂ”해주고
다시 git-bash로 와서 hello.py를 실행시키면 hello world라는 값이 뜰 것. 
?	파이썬 파일 실행 명력 ? python hello.py
?	뜻: python으로 hello.py를 실행하라.
?	따라서 python이라는 프로그램이 없으면 실행할수 없는 명령이다.

방법2
Vim(빔) 이라는 프로그램을 이용하여 수정
Vim은 여러 단축기가 있기에 사용하기 위해서 이러한 단축기가 익숙해지는 것이 필요.
단축기가 익숙해지기 전까지는 그냥 text editor이용해서 파일 수정해주는 것이 편하다.
vim으로 들어가는 방법
1. (git bash에서) vi + file+extension 입력
2. 입력하면 해당하는 file의 내용이 보임.
“Vim을 이용하는 방법은 이후에 자세히 다룰 것.”

쉬는시간
윈도우는 ssh라는 프로토콜 사용함.
Git bash를 사용하면 ssh라는 프로토콜을 자동으로 사용 가능.

git이란?
?	Version control system (VCS), 버전을 컨트롤 해주는 시스템
?	SCM: Source code management; 소스 코드를 관리하는 것 = 버전을 컨트롤 함
?	특정한 시기의 소스코드를 버전으로 부름

SCM: 형상관리? 개발을 위한 모든 자원, 일정조정, 등등 모든 일들을 관리하는 것. 
SCM 중에서도 SCM을 다룰 것.
Cf) 캔탐슨 리누스 토발즈

Git에 대해서
각각의 수정 내용 단위 commit이라 부름
전의 commit을 돌아가는 것은 checkout이라 부름. 
수정 내용을 commit을 통해 반영가능.(commit 시점에서만 인터넷 연결되면 됨)

git에는 여러 언어의 source code가 있음.
수정과 커멘트를 남기는 것은 큰 커리어.(기회만 있다면 수정하자 어짜피 컨펌받아야 저장됨)

Git의 구성요소
Blob(블롬) 파일의 최소 단위
Tree blob의 모음
Commit 파일 변경 내용 단위



<표>
파일 만드는 공간 workspace(실제 사용자의 컴퓨터)
파일을 올리는 공간 index (stage) <add명령>
index에서 파일에 tag를 붙여줌
index로 올라오는게 blob
local repo로 올라오는게 commit <commit 명령>
이것을 remote repo로 올림 <push 명령>
remote repo는 sanfrancisco에 있는 git server 



?	Git과 git hub 
Git과 github는 다른 것.
Git은 scm(source code management)
Github는 git을 이용해서 제공하는 서비스 중 하나. 
(open source 사용자가 가장 많이 쓰는 서비스가 github)
?	Git
mail 주소: 자기 호스팅이 제일 좋지만 없는 경우 gmail이용
?	Repository: github에서 저장소를 부르는 용어.

?	디렉토리를 github에 연결하기
특정 디렉토리를 설정, 그 하위에 있는 모든 폴더, 파일을 github와 연결하기
?	이 디렉토리부터 github를 쓰겠다는 명령어
형식: git init
입력시 ‘master’이 뜬다. 
# master는 현재 branch 상태를 보여줌
?	git status: 해당 git 상태를 보여줌
?	README.md 파일 ? github에서 해당 repo의 기본 정보를 담고 있는 파일.
(mb 형식은 git hub에서 바로 읽을수 있는 형식)
?	README.md 파일 수정하기 (메모장 이용해서)
#는 중요한 제목 텍스트를 표현하기 위해 사용
(#는 6개까지 붙여 단계 크기 구분 가능)
?	문단 구분을 위해서는 엔터를 두번 입력해야 함.

Git status 치면 생성한 readme.md가 뜸
?	새 파일이 생겼으며 add가 필요하다는 것을 보여줌.(add 라는 명령어를 통해서 stage로 넘겨 달라는 것)
?	git add + (탭을누르면 자동으로 tracking 되지 않은 파일을 자동완성 시켜줌) : 해당 파일을 add 해줌 
?	git add + . : 해당 디렉토리 안에 있는 모든 파일들을 add함
?	git add + 특정 디렉토리 이름 : 해당하는 디렉토리 안의 모든 내용을 add해줌

git status를 눌러주면
?	commit할 파일이 있다고 보여줌
?	(주의 git commit: 텍스트 에디터(vi나 nano)로 넘어감)
?	git commit -m: 해당 commit의 기능과 내용을 추가해서 commit 하는 것
git commit -m “Create README.md
<note> I created README.md at Sinsa.
~~~~~” (쌍따옴표를 닫기 전까지 계속해서 메시지 입력 가능)


(주의사항) 이전에 해당 컴퓨터(work place)와 git hub를 연결해줘야한다
?	git config --global user.name “username” #github에 등록된 유저 네임
?	git config --global user.email “github email address” #github에 등록된 유저 이메일
?	git config --list #위의 등록과정이 잘 이루어졌는지 확인
?	이러한 과정을 통해 workspace와 github간의 연결이 가능하다.
(연결이 안되도 add는 가능하지만 commit은 연결이 필수적)
?	git config --unset-all user.email: 해당 git bash에서 github 계정을 삭제함


git status를 눌러주면
?	nothing to commit이 뜨면 됨. (push만 남았다는 것)
?	github의 repository로 와서 주소를 복사함.(push의 위치를 가져오는 것) 
?	어디로 push하는지 명령하는 것
?	git remote add origin + repo address
리모트 레포를 추가하라라는 뜻.
# ‘origin’은 해당 레포를 앞으로 부를 별칭.
# 별명이기에 자유롭게 설정가능 
# git bash에서 붙여넣기 하기 위해서는 마우스로 우클릭 후 paste해줘야 함.
?	Push 해주기
?	명령: git push origin master
origin의 master 버전으로 보내라라는 것. 
# 아까 origin이라는 별칭을 정해준 repo의 master 버전으로 보냄. 

Github 사이트의 repository에 들어가서 새로고침을 하면 등록한 파일이 뜰 것.(완료됨)


<파이썬 Basic>

c언어의 기반으로 하는 파이썬이 기본 형태
인터프리터: complie이 필요없음. Code의 실행가능한 변환과정이 없이 바로 수행. 
memory의 과정이 필요없이 그냥 바로바로 code로 실행. 
동적타이핑: 특정 변수에 값을 정해줄 때, 해당 값의 종류를 따로 알려줄 필요가 없다. 즉 string인지 integer 인지 Boolean 인지 말할 필요 없이 그냥 값을 정해주면 변수 설정 완료. 

?	[윈도우-시작]에서 idle 를 찾아서 실행해줌. 
?	Import this 입력하면 파이썬의 철학이 뜸. 
?	파이썬이 추구하는 코딩
?	아름다운 형태
?	평면적인 구조(code들을 최대한 붙여서 짜줌)
?	간단한 형태 > 복잡한 형태 > 이해하기 어려운 형태
?	가독성이 좋아야 함.

?	Idle는 repl 구조다 (read evaluate print loop) ? 해당 코드를 바로 실행해서 출력하는 공간

주피터 노트북 설치하기
?	Git bash에서 [pip ?version]을 입력해서 버전을 확인한다. 
?	Pip는 파이썬의 패키지 인스톨러. (파이썬 설치시 보통 자동으로 같이 설치됨)
?	[pip ?version]을 입력하면 pip의 버전과 python의 버전이 출력됨. 
?	[pip install jupyter]을 입력하면 jupyter notebook이 설치됨. 

설치되면 jupyter notebook을 입력해서 실행시켜줌.
주피터 화면에서 오른쪽 위에new누르고 python3 실행 
? 새파일이 생김. 
? 제목을 누르고 수정 가능
? 주피터 노트북을 키고 print (“hello world”) 를 입력하고 shift enter 통해 실행 가능
(그냥 enter는 줄바꿈으로 됨)
주피터 노트북은 print가 필요 없음. 그냥 입력하고 shift enter 누르면 됨.
두개의 명령을 print 하기 위해서는 print를 통해 실행문으로 만들고 단순히 하나의 명령의 값을 보고 싶으면 print 필요가 없다. 

주피터 노트북 끄기 위해서는 ctrl c 하고 y 해주면 됨

파이썬 용어
피연산자: 연산의 대상이 되는 것들.
연산자: 연산 명령

/ ? 나누고 소수까지 가지고 옴
// ? 나누고 그것의 inte값만 가지고 옴.
Type(연산) ? 연산의 결과값의 종류를 보여줌(int or float etc)


(용어) 비교연산자: >, <, == 등등으로 이루어진 식을 부르는 용어.

과제-파일 참고
원의 부피: 3/4 r의 세제곱 파이.
저장을 하고 그 저장한 값을 가져오는 것.

# define r
# get r,d,c,a,v 각자 구하고 그 저장한 값을
# print r,d,c,a,v 여기서 출력하는 것

Ex) 
r = 10
radious = r
diameter = 2 * r
print (“radious =”, radious)
print (“diameter =”, diameter)
print (“circumference =”, circumference)
print (“area =”, area)
print (“volume =”, volume)


?	Github 에서 til 오늘 배운 것을 올리는 기능(
