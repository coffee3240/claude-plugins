---
allowed-tools:
  - "Bash(git checkout --branch:*)"
  - "Bash(git add:*)"
  - "Bash(git status:*)"
  - "Bash(git push:*)"
  - "Bash(git commit:*)"
  - "Bash(gh pr create:*)"
description: "Commit, push, and open a PR"
---

## Context

- Current git status: !`git status`
- Current git diff: !`git diff HEAD`
- Current branch: !`git branch --show-current`

## Your task

1. 현재 브랜치가 main이면 새 브랜치를 생성하세요.
2. 적절한 메시지와 함께 모든 변경 사항을 커밋하세요.
3. 해당 브랜치를 origin으로 푸시하세요.
4. `gh pr create`를 사용하여 PR을 생성하세요.
5. 모든 작업은 단일 메시지 내에서 도구 호출(Tool Call)로 수행하며, 사담은 생략하세요.
