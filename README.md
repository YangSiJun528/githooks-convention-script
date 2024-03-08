# githooks-convention-script

_githooks-convention-script_ 은 [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)을 따르는데 도움을 주는 Git Hooks `commit-msg` 스크립트를 제공합니다.

이 프로젝트에서 구현하는 commit-msg script 코드는 [sailr](https://github.com/craicoverflow/sailr)를 기반으로 합니다.

## How to use?

1. `.git/hooks`에 [`commit-msg`](./commit-msg) 스크립트를 넣어주세요.
2. 다음 명령어를 실행하여 [`commit-msg`](./commit-msg) 스크립트에 실행 권한을 부여합니다. `chmod +x .git/hooks/commit-msg`

## How to set environment variable?

[`commit-msg`](./commit-msg) 스크립트에서 다음과 같은 환경 변수 값을 변경할 수 있습니다.

```sh
revert=true
min_length=1
max_length=52
max_line_length=72  
types="build ci docs feat fix perf refactor style test chore"
```

- revert: 커밋 메시지가 "revert"나 "merge" 로 시작하는 것을 허용할지 여부를 결정합니다. 기본 값은 true입니다.
- min_length: 커밋 제목의 최소 길이를 설정합니다. 기본 값은 1입니다.
- max_length: 커밋 제목의 최대 길이를 설정합니다. 기본 값은 52입니다.
- max_line_length: 커밋 본문의 각 줄의 최대 길이를 제한합니다. 기본 값은 72입니다.
- types=: 허용되는 커밋 유형 접두사를 나열합니다. 유효한 커밋 메시지는 이 접두사 중 하나로 시작해야 합니다. 기본 값은 `"build ci docs feat fix perf refactor style test chore"`입니다.

