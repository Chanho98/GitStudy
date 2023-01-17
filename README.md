# Git Study

* __참고 링크__

            누구나 쉽게 이해할 수 있는 Git에 입문 : [https://backlog.com/git-tutorial/kr/](https://backlog.com/git-tutorial/kr/)  
            readme MD 문법 : [https://abled.tistory.com/39](https://abled.tistory.com/39)

## 1. Git 시작하기
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
  
****