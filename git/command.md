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
- tacked, untracked 파일을 구분하여 표시

## `git add`
- working directory에서 변경된 파일을 staging area에 이동
```
git add {file_name 혹은 directory_name}
git add . 
```
- git add . 은 현재 나의 위치를 기준으로 모든 파일과 폴더를 staging area로 옮김

## `git commit`
- staging area에 있는 변경사항을 커밋하여 스냅샷 생성