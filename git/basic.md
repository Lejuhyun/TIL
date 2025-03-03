# Git 기본 개념

## 분산버전 관리 시스템
- 클라이언트와 서버 모두가 똑같은 데이터를 유지하여 버전을 관리하는 시스템

## 파일의 세가지 상태
![areas](../assets/areas.png)
- 영역
    - working directory : 작성하고 있는 코드
    - staging area : add 명령어로 무대위로 올라간 파일들 (git add . )
    - .git directory (repository) : commit 명령어로 찍힌 스냅샷들을 저장 (git commit -m "요약메시지")

## 파일의 라이프사이클
![라이프사이클](../assets/lifecycle.png)
- Tracked(관리대상임), Untracked(관리대상이 아님)
    - Tracked: 이미 스냅샷에 포함돼 있던 파일이다
        -Unmodified(수정하지 않음), modified(수정함), Staged(커밋으로 저장소에 기록할) 
    - Untracked: 워킹 디렉토리에 있는 파일 중 스냅샷에도 staging area에도 포함되지 않은 파일이다.
- untracked 상태의 파일을 add 시키면 staged 상태가 된다. 
- staged 상태의 파일을 커밋하면 unmodified 상태가 된다
- 수정하면 modified 상태가 된다
- modified 상태의 파일은 1. add 시켜서 staged 상태로 만들기 2. commit하여 unmodified 상태가 만들기