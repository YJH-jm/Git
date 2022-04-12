## 기본 설정
- 현재 폴더의 파일 확인
   - ``` ls``` (리눅스 기반 명령어, 윈도우 command  창에서는 쓸 수 없었으니 powershell에서는 가능)
   - ``` ls -a```
        - 더 자세하게 보고싶은 경우 
<br>

- git 버전 확인
   - ```git --version```

- 사용자 관련 정보 설정
   - ```git config --global user.name "user_name"```
   
   <!--    - ```git config --global user.name "YJH-jm"``` -->
   
   - ``` git config --global user.email "email@gmail.com"```

   <!--    - ``` git config --global user.email "jmjhjob13@gmail.com"``` -->
   - ``` git config user.name (확인)```
   - 만약 등록된 정보를 바꾸는 경우 Window에서는 '제어판' >> '사용자 계정' >> '자격 증명 관리' 에 들어가서 기존의 정보 삭제

- 터미널에서 환경설정 확인
   - ```git config --list```
        - git을 설치하면 git에 관련된 모든 환경설정이 .gitconfig 라는 파일에 저장

- 입력한 모든 명령어 확인
    - ```history```

- 새로운 디렉토리 만들고 이 폴더를 깃허브에 연결하기 위해 설정 
    - ```mkdir [폴더명] ```
    - ```cd [폴더명]```
    - ```git init```
      -  master로 변환이 됨

- 폴더와 git 연결 끊기
    - ```rm -rf .git``` 
        - .git을 제거하여 더이상 git 프로젝트가 아님

- git 현재 상태 확인
   - ```git status``` 
        - file이 add되었는지, commit 되었는지

- git log 확인
    - ```git log``` 


- 해당 PC에 설정한 폴더(로컬 저장소, git init로 설정한 폴더)와 github의 저장소를 연결
   -  ```git remote add origin https://github.com/YJH-jm/hello-world.git```
    
    - ```git remote -v```
        - 등록된 저장소 이름과 URL 표시해줌
- 폴더와 github repos 연결 끊기
    - ```git remote remove origin```

- 파일 올리기 
    - ```git add README.md```
    - ```git commit -m 'README.md file 생성'```
        - 'README.md file 생성' 라는 메세지와 함께 README.md 파일 commit 
    
    *cf>

    - ```git push -u origin master```

- github에서 파일 다운받기
    - ```git pull origin master```

## Clone
- 특정 branch clone
   - ```git clone -b {branch_name} --single-branch {저장소 URL}```

- 하위 폴더 clone
   -  ```git remote add origin {저장소주소}```
      - 저장소 연결
   - ```git config core.sparsecheckout true```
      - git sparse checkout 활성화
   - ```git {폴더경로}/* >> .git/info/sparse-checkout```
      - clone 하기 위한 폴더 경로를 설정
      - 폴더 경로에 "" 작성하면 실행 안됨
      - A라는 저장소에서 a_test 폴더의 a_test_test 폴더를 다운받고 싶으면 **a_test/a_test_test/src/*** 이렇게 작성
   - ```git pull origin master```         

## branch
- branch 확인
   - ```git branch```
      - 현재 내가 위치한 branch 확인
        
- branch 생성
   - ```git branch```
    
   - ~~```git checkout -b {branchname}```~~
   - ```git switch -c {branchname}
      - branch를 생성하고 이동 
      - git 2.23 버전부터 git checkout을 대신하여 switch와 restore 나옴
      
   - ```git push origin {branchname}```
      - local branch와 같은 이름으로 remote branch가 생성되고 local branch의 내용이 push 됨

   - ```git switch -t origin/{origin branchname}```
      - remote branch와 같은 이름으로 로컬 브랜치를 생성하고 switch
       
- branch 연동
   - ```git branch --set-upstream-to origin/{branchname}``` 
             
- branch 이동
   - ~~```git checkout {branchname}```~~
   - ```git switch {branchname}```
      - git 2.23 버전부터 git checkout을 대신하여 switch와 restore 나옴

- branch 조회
   - ```git branch```
      - local에 존재하는 local branch 조회
   - ```git branch -r```
      - local에 저장된 remote branch 조회 
    - ```git branch -a```
      - 모든 branch 정보 조회    

- branch 삭제
   - ```git push origin --delete {branchname}```
      - remote branch 삭제 방법
   - ```git branch -D {branchname}```
      - local branch 삭제 방법
