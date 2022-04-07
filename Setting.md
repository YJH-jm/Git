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


- 특정 branch clone
   - ```git clone -b {branch_name} --single-branch {저장소 URL}```
