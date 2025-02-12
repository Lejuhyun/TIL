# 명령어 정리
## `git config` (사용자 정보 설정)
- 사용자 이름 설정
```
git config --global user.name {juhyunlee} 
``` 
- 사용자 메일 설정
```
git config --glober user.email {ljh0109901@gmail.com}
``` 


## `git init` (새로운 Git 저장소 만들기)
- 현재 디렉토리에 `.git` 폴더를 생성하여 새로운 Git 저장소를 초기화한다.

## `git clone` (Git 저장소 복제하기)
- 현재 디렉토리에 원격저장소 폴더를 복제
```
git clone {remote_url}
```
- 내가 설정한 directory_name 으로 저장할 수 있음
```
git clone {remote_url} {directory_name}
```


## `git status` (현재 git 상태 확인)
- 현재 git의 상태를 확인
- tracked, untracked 파일을 구분하여 표시

## `git add` (무대로 올리기)
- working directory에서 변경된 파일을 staging area에 이동
```
git add {file_name 혹은 directory_name}
git add . 
```
- git add . 은 현재 나의 위치를 기준으로 모든 파일과 폴더를 staging area로 옮김

## `git commit` (캡쳐하기)
- staging area에 있는 변경사항을 커밋하여 스냅샷 생성
```
git commmit -m {"메시지"} 
```
- git commit만 쓰는 경우
```
git commit
```

- i를 눌러서 메시지 입력
- esc 눌러서 나가기
- :wq 눌러서 저장

## `git log` (히스토리 조회)
- 커밋의 히스토리를 조회
- 사진 찍은 사람, 커밋메시지, 시간 등등을 보여준다
    - 결과
    - commit 593733983e7b92ca3718522538153872de5d7133 (origin/master)
Author: 이주현 <ljh0109@gmail.com>
Date:   Mon Feb 10 17:07:28 2025 +0900

```
git log --oneline
```
```
git log --graph
```
- log 나가려면 q를 누른다

## `git remote` (원격저장소 관리)
1. 원격 저장소 생성

    - 일반적으로 remote name은 origin을 사용
```
git remote add {remote_name} {remote_url}
```

```
git remote add origin https://github.com/Lejuhyun/Lejuhyun.github.io
```

2. 원격 저장소 확인
```
git remote -v
```
3. 원격 저장소 삭제
```
git remote remove origin
```


## `git push` (원격저장소에 커밋을 업로드)
-  master 브랜치를 origin(원격저장소)에 전송해준다
```
git push origin master
```

## `git pull` (원격저장소에 커밋을 다운로드)
- Clone한 서버에서 데이터를 가져온다
```
git pull origin master

```

## 끝말잇기
1. 첫번째 단어 입력
2. git init
3. git add .
4. git commit -m "첫번째"
5. git remote add origin https://주소 (원격저장소 생성)
6. git push origin master (원격저장소에 데이터 전송)
7. git pull origin master (원격저장소에서 데이터 가져옴)
8. 두번째 단어 입력
9. git add .
10. git commit -m "두번째"
11. git push origin master

## 끝말잇기 충돌
1. 단어 쓰기
2. git add .
3. git commit -m "update"
4. git push origin master(A), git push origin master(B)
5. 충돌 발생
6. git pull origin master 
7. 단어 둘 중 선택
8. git push origin master

# 3일차

## git branch (브랜치 생성)
- `git branch` : branch 목록확인 
- `git branch {branch_name}` : branch 생성
    - `git branch testing` : testing 이라는 브랜치를 생성한다
- `git branch -d {branch_name}` : branch 삭제

## git switch (다른 브랜치로 이동)
- `git checkout {branch_name}` : branch_name으로 이동
- `git switch {branch_name}` : branch_name으로 이동 (최신 명령어)
    - 예시 `git switch master` : master로 이동

## git merge (브랜치 병합)
- `git merge {target_branch_name}` : 현재 branch로 target_branch_name을 가져와서 병합
- teting 브랜치도 add commit하고 동시에 master 브랜치도 add commit하면 충돌발생 -> merge