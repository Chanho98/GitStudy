# Git Study

## 0. Git 명령어 / 개념
* `git pull origin main --allow-unrelated-histories` 서로 다른 Histories 가진 Merge `refusing to merge unrelated histories` Error Code 해결
    * [Merge Commit 입력방법](https://velog.io/@ssmin0606/%EA%B0%9C%EB%B0%9C%ED%88%B4-Please-enter-a-commit-message-to-explain-why-this-merge-is-necessary-especially-if-it-merges-an-updated-upstream-into-a-topic-branch-%ED%95%B4%EA%B2%B0%ED%95%98%EA%B8%B0-git-bash)
* FastForward 방식 Merge 현재 브랜치의 HEAD가 대상 브랜치의 HEAD까지로 옮기는 Merge
  * Ex) 커밋을 분기로 2개의 Branch가 있다면
  * 우선 Main이 No.1 Branch로 FastForward되며 같은 Pointer를 갖는다.
  * 이루 No.1 Branch를 삭제하고 No.2 Branch와 Merge한다.
* Merge 하기 이전에 No2. Branch에 commit하여 이상 유무를 확인하고 main Branch에 commit한다.
* Pull Request를 통해서 Merge Process를 진행할 수 있다.


 __참고 링크__
* Branch Graphic Viewer [source tree GUI](https://www.sourcetreeapp.com/)
* 누구나 쉽게 이해할 수 있는 Git에 입문 : [https://backlog.com/git-tutorial/kr/](https://backlog.com/git-tutorial/kr/)  
* readme MD 문법 : [https://abled.tistory.com/39](https://abled.tistory.com/39)

## 1. Git 시작하기

### Git Flow
![image](https://user-images.githubusercontent.com/78125194/212982529-f58f691c-bb13-41af-9a6f-c9e69838737f.png)

__1.1.1. config 계정 정보 입력하기__
```
git config --global user.name "Max Kim"
git config --global user.email hwaseen@gmail.com
```
  
  > 커밋에 쓰일 이름 입력(꼭 깃헙 아이디일 필요는 없습니다.)
  > 깃헙에 가입 이메일 입력
    >> --global 설정하면 Defalut값으로 정해진다.
    

__1.1.2. config --list로 계정정보 확인__
```
git config --list
```

  > 이름, 이메일 등 관련 정보 확인이 가능하다.
  >> ___확인이 끝나고 난 뒤 Q 키를 통해 Exit 가능___

__1.2. Git 경로 이동__
```
cd /c                  # C 드라이브
cd /d                  # D 드라이브
cd ~/Downloads/        # 다운로드 폴더
```
  > cd -> Change Directory, C -> C drive, D -> D drive
  >>  ~ -> Home directory 사용자 디렉토리
  
  __1.3.1. Git 시작하기__
```
git init
```
  
  > 작업할 디렉토리로 이동하여 init 실행
    
__1.3.2. Github 레포지토리 연결__
```
# 리모트 저장소 연결 명령어
git remote add origin 레포지토리 링크
```
  > origin은 리모트 저장소의 약칭으로 다른이름을 사용할  수 있다.


__1.3.3. Commit 하기__
```
git status    # 상태 변화 감지

>> 아래와 같이 변경 사항이 표시된다.
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        BasicCoding.py
```
  > status로 변경된 사항 확인
  
```
# 지금까지 변형된 모든 파일을 스테이지 위에 올림
git add .
# 특정 파일만 스테이지 위에 올림
git add 특정 파일명
```
  > add 를 통해서 Stage에 파일 올리기

```
# 커밋 명령어
git commit -m "커밋명"
```
  > Commit 할 시 커밋명 꼭 입력하기

```
# 푸쉬 명령어 : git push (리모트 저장소 별칭) (브랜치명)
git push origin master
```
  > 레포지토리에 푸쉬하기

__1.4.1 Checkout 이용하기__
```
git log    -> commit 된 내역을 검색한다. 
git checkout <Serial Number>    -> Serial 넘버를 통해  원하는 commit으로 이동 가능
git checkout -     -> 가장 최신 커밋으로 돌아갈 수 있다.
```





## 2. Git Version 관리

****
