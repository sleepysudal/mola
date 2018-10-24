# Git 명령어
br전역 설정 정보 조회
br git config - -global - -list
br 전역 설정 정보 삭제시키기
br git config --global --unset-all user.email
br git config --global --unset-all user.name
br 새로운 저장소 초기화하기
br git init
br 저장소 복제하기
br git clone <저장소 url>
br 새로운 원격 저장소 추가하기
br git remote add <원격 저장소> <저장소 url>
br 새로운 파일 git에 등록시키기(staging)
br git add <파일>
br 현재까지 작업한 내용 저장하기
br git commit -m “<메시지>”
br 원격 저장소에서 합치지 않고 지역 브랜치로 변경 사항 가져오기
br git fetch <원격 저장소>
br 원격 저장소에서 변경 사항을 가져와 현재 브랜치에 합치기
br git pull <원격 저장소>
br 새로운 로컬 브랜치를 원격 저장소에 푸싱하기
br git push <원격 저장소> <지역 브랜치>
