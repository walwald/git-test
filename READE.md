#Git command 정리

- `git init`
  > 현재 위치한 디렉토리에서 git 관리를 시작한다는 명령어. 초기화를 뜻하기도 한다.    
  > 해당 명령어를 실행하면 현재 폴더 전체가 git으로 관리되기 시작하므로, git으로 관리하지 않을 디렉토리/파일들은 해당 명령어를 입력하기 전 미리 .gitignore에 작성하여 저장해두도록 하자.      
      
- `git remote add origin <remote repository url>`
  > 현재 git으로 관리되고 있는 local의 디렉토리를 online 상의 git hub remote repository와 연결한다는 의미의 명령어이다.   
  > 여기서 origin은 매번 긴 url을 직접 입력할 수 없기에 쓰는 일종의 별칭이며, origin으로 쓰는 것이 일반적인 convention이다.   
  > <reomote repository url> 위치에 연결하고자 하는 git hub repository의 주소를 적으면 된다.   
  
- `git add <file name>`
  > git에 commit을 남기기 전 commit할 파일을 준비시키는 명령어이다.   
  > commit할 파일의 이름을 <file name>에 적을 수 있고, .을 입력하면 현재 폴더에 있는 모든 파일/디렉토리가 add 된다. (.gitignore에 입력된 파일/디렉토리 제외)   
  
- `git commit`
  > git으로 관리되고 있는 현재의 디렉토리 내의 변경사항을 기록한다는 의미이다.   
  > commit된 내용은 git log로 확인할 수 있다.   
  > commit을 남기면 특정 commit 시점으로 디렉토리를 되돌릴 수도 있고, 다른 branch의 내용을 가져와 합칠 수도 있다.
  
- `git push origin <branch name>`
  > git remote add origin으로 연결해준 remote repository에 local의 특정 브랜치를 업로드한다는 의미의 명령어이다.   
  > 모든 commit 내역이 담겨 업로드된다.
  
- `git pull origin <branch name>`
  > remote repository 상의 branch를 local branch에 다운로드 받는 명령어이다.   
  > remote repository 상 branch와 local branch 간에 다른 부분이 있었다면, 그러한 부분이 업데이트된다. 
  
- `git merge <branch name>`
  > 특정 branch에서 다른 branch를 끌어와 병합시키는 명령어이다.   
  > 서로 충돌되는 내용이 있을 경우, conflict가 발생할 수 있으며 이 때는 conflict를 살펴보고, 
  merge로 인해 incoming 되는 부분과 현재 보유하고 있던 부분을 비교하여 필요한 부분을 남기는 방식으로 resolve conflict 해줄 수 있다.
