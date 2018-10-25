# Git 명령어 정리

* # 1. 설정과 초기화

* > ## 전역사용자명/이메일 구성하기
* ### git config - -global user.name “Your name”
* ### git config - -global user.email “Your email address”

* > ## 저장소별 사용자명/이메일 구성하기 (해당 저장소 디렉터리로 이동후)
* ### git config user.name “Your name”
* ### git config user.email “Your email address”


참고로 user 설정이 되어 있지 않으면 Github에 있는 repository에 변경사항을 푸시 한다고 해도 commit count 집계도 안되고 해당 커밋의 작성자 프로필 아이콘도 ? 로 표시되기 때문에 웬만하면 name과 email 주소를 설정하는 것이 좋다.
