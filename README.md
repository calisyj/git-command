# git-command
Github를 통한 협업에 있어 실수를 줄이기 위한 git command 공부 기록 공간

## Organization repository commit 작업 git 명령어 순서 
reference: https://github.com/inseonyun
1. git checkout main -> main 브렌치로 switch
2. git pull origin main  -> main 브렌치의 변경사항 내려받음 
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
11. git pull origin main
12. git branch -d 본인깃허브닉네임(소문자)

## <나의 부족한 점 feedback>
22-05-07 
1. Git 상태 명령어 숙지(작업중인 branch를 항상 인지할 것)
-> 현재 내가 어디서 무슨 작업을 하고 있는지 숙지하는게 중요함.
2.  Git 명령어 수행 log들 읽을줄 알아야함!
-> 깃 명령어들의 의미를 파악하고 쓸 것
3. 깃 레포 연습(main branch, 다른 branch 생성해서 명령어들 안보고 commit 가능하도록 연습해볼 것)

## <반복연습하며 숙지할 코드들>
현재 작업 branch가 과거 작업과 꼬여 삭제해야 할 경우  
명령어 흐름: branch main이동 -> calisyj branch 삭제 -> main 최신상태 받아오기 -> calisyj branch 생성, 이동  

git checkout main ->현재 branch main으로  
git branch -d calisyj  ->-d는 delect를 의미  
git pull origin main -> 현재 시점의 변경사항을 다운로드  
git checkout -b calisyj -> calisyj branch 재생성하고 다시 작업 시작. add., commit, pr생성, merge, 브렌치삭제, 등등  

## <협업 시 branch가 꼬이는 것을 방지하기 위한 주요 코드들>
git status -> 현재 Branch와 Stage 정보를 보여준다.  
git show -> 가장 최근 commit의 log와 변경사항을 보여준다.
git log  -> 가장 최근 commit의 log를 볼 수 있다. commi log란 다양한 commit 내역을 시간 순서대로 확인하는 것을 의미한다.   
git branch  -> 현재 branch 확인
git checkout main  ->  branch를 main으로 이동  
git pull origin main  
shift; q  -> 입력 안될 시.


## <웹 코드 깃허브 업로드 순서(협업모드)(midbar capstone용)>  
.made by calisyj  

0. Git bash 설치  

1. 깃허브 HandongFarmers/Web-Visualization 페이지 접속  
링크: https://github.com/HandongFarmers/Web-Visualization  

2. 깃허브 페이지와 Local PC clone하기  
- 페이지의 Code(초록색 버튼)을 누르면 나오는web URL 복사  
- Local PC의 Django파일 우클릭 후 Git Bash Here 클릭  
- (참고)git 붙여넣기 단축키: Shift + Insert  
- (참고)git 복사하기 단축키: Ctrl + Insert  
- 클릭 후 생성된 창에 아래의 코드 입력 후 Enter  
git clone 복사한url붙여넣기  
Cloning into 'Web-Visualization'... 와 Username입력창이 떠야 정상 | 안뜨면 처음부터 다시  
- github username 입력: 본인 프로필 들어가면 동그란 프사 밑에 적힌 이름  
- github password 입력: 그냥 패스워드 입력X 본인 깃허브 아이디의 토큰 번호를 입력   
-> <본인 토큰 번호 확인하는법>  
-> 깃허브 페이즈 우측 상단 알람버튼 옆 프사를 누르면 나오는 메뉴바 맨 하단의 settings 클릭  
-> 클릭 후 이동된 페이지 왼쪽 메뉴바 맨 하단의 developer settings 클릭  
-> 클릭 후 이동된 페이지 왼쪽 메뉴바 맨 하단의 Personal access tokens의 Tokens(classic)클릭 후 토큰 생성  
-> 생성된 토큰은 따로 메모장에 적어두는 것을 추천함.  
- 토큰 번호를 입력하면 Receiving objects: 100% (3/3), done. 초기입력상태로 돌아옴.  
- 아래의 코드 입력  
git init   
git remote add origin 2번의url붙여넣기  
git remote update  
git 창 닫기  
---------------- git clone 성공적으로 했고 코드 업데이트만 시킬 경우는 아래의 내용부터시작하면 됨 ----------  
3. 작업 중인 코드 깃허브에 업로드하기  
- Django폴더 우클릭 후 Git bash here  
- Django폴더 들어가면 Web-Visualization 폴더가 생성된 것을 확인할 수 있다.  
- 해당 폴더에 작업한(혹은 업데이트한) 코드를 넣어주거나 삭제해준 후 업로드하면 폴더 내용대로 깃허브 페이지에 최신화가 된다.  
  
아래는 Organization repository commit 작업 git 명령어 순서이다.  
git checkout main -> main 브렌치로 switch(switched to a new branch 'main'이 떠야 정상진행된것임)  
git pull origin main -> main 브렌치의 변경사항 내려받음  
git checkout -b 본인깃허브닉네임(소문자) (switched to a new branch '본인닉네임'이 떠야 정상.)  
로컬 파일 창에서 소스 코드 파일 구조에 맞게 파일 생성 (ex. Web-Visualization폴더 내에 calisyj-> practice1, venv 폴더 넣기(=생성된 폴더 안에 코드 넣기))  
git add .  
git commit -m "양식내용" (양식: [작성자] 문제이름) (ex) [calisyj] 날짜버튼생성)  
git push origin 본인깃허브닉네임(소문자) (id랑 password입력창 뜨면 본인id pd 입력)  
[깃허브 페이지에서]Pull request 생성 ->repository하려는 github 페이지 상단에 뜬 Compare& pull request 클릭 후 양식 양식 내용 보완하여 Create pull request 초록버튼 클릭  
[깃허브 페이지에서]merge 진행하고 delete 브렌치 수행  
[git 창에서]git checkout main  
[git 창에서]git pull origin main  
[git 창에서]git branch -d 본인깃허브닉네임(소문자)  

4. 현재 작업 branch가 과거 작업과 꼬여 삭제해야 할 경우  


git checkout main ->현재 branch main으로  
git branch -d 본인깃허브닉네임(소문자)  ->-d는 delect를 의미  
git pull origin main -> 현재 시점의 변경사항을 다운로드  
git checkout -b 본인깃허브닉네임(소문자) -> 본인깃허브닉네임(소문자) branch 재생성하고 다시 작업 시작. (3번 내용) add., commit, pr생성, merge, 브렌치삭제, 등등    
