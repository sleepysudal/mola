# Git 명령어 정리

 # 1. 설정과 초기화

 > ## 전역사용자명/이메일 구성하기
 <pre> git config - -global user.name “Your name” 
 git config - -global user.email “Your email address” </pre>

 > ## 저장소별 사용자명/이메일 구성하기 (해당 저장소 디렉터리로 이동후)
<pre> git config user.name “Your name”
 git config user.email “Your email address” </pre>


* 참고로 user 설정이 되어 있지 않으면 Github에 있는 repository에 변경사항을 푸시 한다고 해도 commit count 집계도 안되고 해당 커밋의 작성자 프로필 아이콘도 ? 로 표시되기 때문에 웬만하면 name과 email 주소를 설정하는 것이 좋다.

 > ## 전역 설정 정보 조회
<pre> git config - -global - -list </pre>

 > ## 저장소별 설정 정보 조회
<pre> git config - -list </pre>

 > ## Git의 출력결과 색상 활성화하기
<pre> git config - -global color.ui “auto” </pre>

 > ## 새로운 저장소 초기화하기
<pre> mkdir /path/newDir
 cd /path/newDir 
 git init </pre>

 > ## 저장소 복제하기
<pre> git clone <저장소 url> </pre>

 > ## 새로운 원격 저장소 추가하기
<pre> git remote add <원격 저장소> <저장소 url> </pre>

* * *

# 2. 기본적인 사용법

* ### 아래 명령어에서 [ ]는 선택적인 매개변수를 의미한다.

> ## 새로운 파일을 추가하거나 존재하는 파일 스테이징하고 커밋하기
<pre>git add <파일>
git commit -m “<메시지>” </pre>

> ## 파일의 일부를 스테이징하기
<pre>git add -p [<파일> [<파일> [기타 파일들…]]]</pre>
