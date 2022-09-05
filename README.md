# Git 작업 규칙

`Git`[^git] 과 `GitHub` 를 사용할 때의 규칙을 정리한다. 필요할 때마다 업데이트하도록 한다.[^commit]

## Commit 메시지 작성 규칙

`Git` 에서 `commit` 할 때 메시지를 작성하는 규칙이다. 

### 1. 최대한 본문을 작성한다

* 본문을 작성하려면 제목 뒤에 빈 줄을 넣으면 된다.
* 본문을 매 번 쓰기 힘들 땐, 반드시 제목으로 `commit` 이유를 알 수 있게 한다.
* `commit` 메시지 본문에 상세한 정보를 넣으면 `git blame` 으로 코드 문서화 효과를 볼 수 있다.

### 2. 제목은 최대한 간단하게 작성한다

* 제목은 한 줄에 들어갈 수 있도록 최대한 간단하게 작성한다.
* 본문 없이 제목만 `commit` 할 때는, `규칙 1` 에 따라 반드시 제목에 이유를 넣는다.

### 3. 제목은 명령문으로 작성한다

* 제목은 영어로 명령문이 된다.
* 제목을 영어로 작성할 때는 첫글자를 무조건 대문자로 시작한다.
* 제목 끝에 마침표를 달지 않는다.

### 4. 본문은 간단한 문장 집합으로 구성한다

* 본문은 줄넘침이 발생하지 않게 적절하게 끊어준다.
* 적절한 특수 문자 (`-`, `*`, `` ` ``) 를 사용하여 읽기 쉽도록 한다.
* 위의 특수 문자들로 강조한 구문들 사이에는 빈 줄을 넣는다.

### 5. 본문은 무엇을 어떻게 했는지가 아니라 왜 했는지를 설명한다

* 무엇을 어떻게 했는지는 `code` 자체가 설명할 것이다.[^commit-guide]
* 그러므로 왜 이 `commit` 을 했는지 그 이유를 설명하도록 한다.
* `commit` 으로 인한 부수 효과가 있을 수 있다면 본문에서 이를 설명한다.

### 6. 본문에서 이슈 추적기 (Issue Tracker) 를 사용한다

* 이슈 추적기를 사용할 땐 본문 끝에 참조를 넣는다.
* `Close #123` 과 같은 문법으로 이슈를 닫을 수 있다.[^how-to]
* `GitHub` 이슈를 닫고 `push` 하면 그 브랜치에서 자동으로 이슈가 닫힌다.
    - `close`: 일반 개발 이슈를 닫을 때 사용함
    - `fix`: 버그나 핫픽스 이슈를 고칠 때 사용함
    - `resolve`: 문의 및 요청 사항을 해결할 때 사용함

## 참고 자료

[^git]: [Pro Git](https://git-scm.com/book/en/v2) ([한글 번역](https://git-scm.com/book/ko/v2))
[^commit-guide]: [Commit messages guide](https://github.com/RomuloOliveira/commit-messages-guide/blob/master/README.md) ([한글 번역](https://github.com/RomuloOliveira/commit-messages-guide/blob/master/README_ko-KR.md))
[^how-to]: [How to Write a Git Commit Message](https://cbea.ms/git-commit/) ([한글 번역](https://meetup.toast.com/posts/106))
[^commit]: [commit 과 pull request에 대한 고민](https://octob.medium.com/commit-과-pull-request에-대한-고민-66e1e05722f9)
