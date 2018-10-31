# README.mds
git clone : origin에 있는 repository를 로컬로 가져오는 명령어, 이렇게 해서 가져온 git이 master임
git init : git 초기화인데 git clone을 하게 되면 자동 수행됨
git add : 작업내용을 반영하는 작업
git status : 변경되고 commit되지 않은 파일 목록을 보여줌
git commit : 변경 내용 또는 신규 추가 파일이 master에 추가됨
 --amend 옵션 : 직전에 commit 메시지를 수정
 -am 옵션 : add와 commit을 동시 진행
git log : master에 변경된 내용이 log됨
 --graph 옵션 : 시각적으로 확인
git push : master의 수정 사항이 GitHub의 origin repository에 등록
git branch : 로컬의 branch 목록을 표시
 $ git branch -a라고 하면 origin의 목록까지 표시됨
git checkout -b "브렌치 명" : branch 생성
git checkout "브렌치 명" : 해당 branch를 활성화
git merge : 다시 master로 가서, git merge --no-ff "브렌치 명"
 merge 시에 충돌이 발생하면 : "fix conflicts and then commit the result"라는 문구가 나옴, 해당 파일을 열면 >>>>>>이나 ======또는 
 <<<<<< 등으로 문제 부분이 나옴, 적절히 수정 후 다시 add와 commit을 진행
git reset : 이전 단계로 되돌리는 방법, 로그를 확인해서 commit된 상태의 키 값을 확인한다.
 $ git reset --hard "commit된 키값"
git 불필요한 revision을 뭉개 없애기
 : git revase -i HEAD~2 : 현재 branch의 2개의 변경내용이 Editor에 표시됨
   pick 7a34523xxx "commit 메시지"
   pick ba98523xxx "commit 메시지" 없애고 싶은 rev을 pick 대신 fixup으로 수정 후 저장, log를 확인해보면 hash 값이 변경되어 있음 
