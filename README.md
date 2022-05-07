# git-command
Github를 통한 협업에 있어 실수를 줄이기 위한 git command 공부 기록 공간

## Organization repository commit 작업 git 명령어 순서

1. git checkout main -> main 브렌치로 switch
2. git pull -> main 브렌치의 변경사항 내려받음 
3. git checkout -b 본인깃허브닉네임(소문자)
4. 소스 코드 파일 구조에 맞게 생성 (ex. BOJ폴더 생성 -> 생성된 폴더 안에 Stack폴더 생성 -> 그 안에 본인 id폴더 생성
-> 그 안에 문제 이름(ex. balloons) 폴더 생성)
5. git add .
6. git commit -m "양식내용" 양식에 맞게 잘하면 됨
7. git push origin 본인깃허브닉네임(소문자)
8. Pull request 생성
->repository하려는 github 페이지 상단에 뜬 Compare& pull request 클릭 후 양식 rule에 맞춰 PR 생성
9. merge 진행하고 delete 브렌치 수행
10. git checkout main
11. git pull main
12. git branch -d 본인깃허브닉네임(소문자)

## <현재 나의 부족한 점 feedback>
1. Git 상태 명령어 숙지(작업중인 branch를 항상 인지할 것)
-> 현재 내가 어디서 뭔작업을 하고 있는지 숙지하는게 중요함.
2.  Git 명령어 수행 log들 읽을줄 알아야함!
-> 깃 명령어들의 의미를 파악하고 쓸 것
3. 깃 레포 연습(main branch, 다른 branch 생성해서 안보고 가능하도록연습해볼 것)

## <반복연습하며 숙지할 코드들>
- 현재 작업 branch 삭제할 경우 (branch main이동 -> calisyj branch 삭제 -> main 최신상태 받아오기 -> calisyj branch 생성, 이동)
git checkout main 
git branch -d calisyj 
git pull origin main
git checkout -b calisyj

git checkout main ->현재 branch main으로 
git branch -d calisyj  ->-d는 delect를 의미
git pull origin main -> 현재 시점의 변경사항을 다운로드
git checkout -b calisyj -> calisyj branch 재생성하고 다시 작업 시작. add., commit, pr생성, merge, 브렌치삭제, 등등

## <협업 시 branch가 꼬이는 것을 방지하기 위한 주요 코드들>
git status
git log
git branch
git checkout main  
git pull origin main
shift; q
