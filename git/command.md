# 명령어 정리
- 코드
    - config
        - git config --global user.name juhyunlee (사용자 이름 설정)
        - git config --glober user.mail 메일주소
    (사용자 이메일 설정)


## `git init` (새로운 Git 저장소 만들기)
- 현재 디렉토리에 `.git` 폴더를 생성하여 새로운 Git 저장소를 초기화한다.

## `git clone` (Git 저장소 복제하기)
- 현재 디렉토리에 원격저장소 폴더를 복제
```
git clone {remote_url}
git clone {remote_url} {directory_name}
```
- 내가 설정한 directory_name 으로 저장할 수 있음

## `git status`
- 현재 git의 상태를 확인
- tracked, untracked 파일을 구분하여 표시

## `git add`
- working directory에서 변경된 파일을 staging area에 이동
```
git add {file_name 혹은 directory_name}
git add . 
```
- git add . 은 현재 나의 위치를 기준으로 모든 파일과 폴더를 staging area로 옮김

## `git commit`
- staging area에 있는 변경사항을 커밋하여 스냅샷 생성
```
git commmit -m {"메시지"} 
```

## `git log`
- 커밋의 히스토리를 조회
- 사진 찍은 사람, 커밋메시지, 시간 등등을 보여준다
    - 결과
    commit 593733983e7b92ca3718522538153872de5d7133 (origin/master)
Author: 이주현 <ljh01099014032@gmail.com>
Date:   Mon Feb 10 17:07:28 2025 +0900
- option
```
git log --oneline
git log --graph
```

## `git remote`
- 원격 저장소 관리 명령어

- 원격 저장소 생성

    - 일반적으로 remote name은 origin을 사용
```
git remote add {remote_name} {remote_url}
git remote add origin https://github.com/Lejuhyun/Lejuhyun.github.io

```
- 원격 저장소 확인
```
git remote -v
```
- 원격 저장소 삭제
```
git remote remove origin
````

## `git push`
-  master 브랜치를 origin(원격저장소)에 전송해준다
```
 git push origin master
```

## `git pull`
-git pull 명령은 Clone한 서버에서 데이터를 가져온다
```
git pull origin master
```

## 끝말잇기
1. git init
2. git add .
3. git commit -m "첫번째"
4. git remote add origin https://주소 (원격저장소 생성)
5. git push origin master (원격저장소에 데이터 전송)
6. git pull origin master (원격저장소에서 데이터 가져옴)