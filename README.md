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

> ## add 명령에서 Git 대화 모드를 사용하여 파일 추가하기
<pre>git add -i</pre> 

> ## 수정되고 추적되는 파일의 변경 사항 스테이징하기
<pre>git add -u [<경로> [<경로>]]</pre>

> ## 수정되고 추적되는 모든 파일의 변경 사항 커밋하기
<pre>git commit -m “<메시지>” -a</pre>

> ## 작업 트리의 변경 사항 돌려놓기
<pre>git checkout HEAD <파일> [<파일>]</pre>

> ## 커밋되지 않고 스테이징된 변경 사항 재설정하기
<pre>git reset HEAD <파일> [<파일>]</pre>

> ## 마지막 커밋 고치기
<pre>git commit -m “<메시지>” - -amend</pre>

> ## 이전 커밋을 수정하고 커밋 메시지를 재사용하기
<pre>git commit -C HEAD - -amend</pre>

* * *

# 3. 브랜치
> ## 지역 브랜치 목록 보기
<pre>git branch</pre>

> ## 원격 브랜치 목록 보기
<pre>git branch -r</pre>

> ## 지역과 원격을 포함한 모든 브랜치 목록 보기
<pre>git branch -a</pre>

> ## 현재 브랜치에서 새로운 브랜치 생성하기
<pre>git branch <새로운 브랜치></pre>

> ## 다른 브랜치 체크아웃하기
<pre>git checkout <브랜치></pre>

> ## 현재 브랜치에서 새로운 브랜치 생성하고 체크아웃하기
<pre>git checkout -b <새로운 브랜치></pre>

> ## 다른 시작 지점에서 브랜치 생성하기
<pre>git branch <새로운 브랜치> <브랜치를 생성할 위치></pre>

> ## 기존의 브랜치를 새로운 브랜치로 덮어쓰기
<pre>git branch -f <기존 브랜치> [<브랜치를 생성할 위치>]</pre>

>## 브랜치를 옮기거나 브랜치명 변경하기
<pre>git checkout -m <기존 브랜치> <새로운 브랜치></pre>
* ### <새로운 브랜치>가 존재하지 않을 경우
<pre>git checkout -M <기존 브랜치> <새로운 브랜치></pre>
* ### 무조건 덮어쓰기 

> ## 다른 브랜치를 현재 브랜치로 합치기
<pre>git merge <브랜치></pre>

> ## 커밋하지 않고 합치기
<pre>git merge - -no-commit <브랜치></pre>

> ## 선택하여 합치기
<pre>git cherry-pick <커밋명></pre>

> ## 커밋하지 않고 선택하여 합치기
<pre>git cherry-pick -n <커밋명></pre>

> ## 브랜치의 이력을 다른 브랜치에 합치기
<pre>git merge - -squash <브랜치></pre>

> ## 브랜치 삭제하기
<pre>git branch -d <삭제할 브랜치></pre>

* ### 삭제할 브랜치가 현재 브랜치에 합쳐졌을 경우에만
<pre>git branch -D <삭제할 브랜치></pre>

* ### 삭제할 브랜치가 현재 브랜치에 합쳐지지 않았어도
