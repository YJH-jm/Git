
1. 현재 폴더의 파일 확인
    * ls (리눅스 기반 명령어, 윈도우 command  창에서는 쓸 수 없었으니 powershell에서는 가능)
    * ls -a
        - 더 자세하게 보고싶은 경우 

2. 버전 확인
    * git --version

3. 사용자 관련 정보 설정
    * git config --global user.name "YJH-jm"
    * git config --global user.email "jmjhjob13@gmail.com"
    * git config user.name (확인)

4. 터미널에서 환경설정 확인
    * git config --list
        - git을 설치하면 git에 관련된 모든 환경설정이 .gitconfig 라는 파일에 저장

5. 지금까지 입력한 모든 명령어 확인
    * history

6. 새로운 디렉토리 만들고 이 폴더를 깃허브에 연결하기 위해 설정 
    * mkdir myproject 
    * cd myproject
    * git init
        -> master로 변환이 됨

    cf)
    * open .git
    * rm -rf .git 
        - 더 이상 git 프로젝트가 아님
    ---------> 잘못 설정해서 인터넷 찾아봄

    * pwd
        - 현재 폴더의 경로를 얻을 수 있음

    * git status 
        - 현재 상태를 알 수 있음
        - file이 add되었는지, commit 되었는지

    * git log 
        - log 확인이 가능


7. github에 파일 올리기 및 폴더 연결

    *  git remote add origin https://github.com/YJH-jm/hello-world.git
        - 해당 PC에 설정한 폴더(로컬 저장소, git init로 설정한 폴더)와 github의 저장소를 연결한다
        - 여기서 origin은 원격 github를 의미한다고 간주 
    
    * git remote -v
        - 등록된 저장소 이름과 URL 표시해줌
        - 결과값
        origin  https://github.com/YJH-jm/hello-world.git (fetch)
        origin  https://github.com/YJH-jm/hello-world.git (push)
        
    * git remote remove origin
        - 폴더(여기서는 myproject)와 github repos 연결 끊기
    
    * git add README.md
    * git commit -m 'README.md file 생성'
        - 'README.md file 생성' 라는 메세지와 함께 README.md 파일 commit 
    
    *cf>

    * git push -u origin master
        - 최종 업로드!

8. github에서 파일 다운받기
    * git pull origin master

9. exit
    * 나가기 
