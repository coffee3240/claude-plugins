---
allowed-tools:
  - "Bash(git push:*)"
  - "Bash(git branch:*)"
description: "Force push current branch to origin (safely)"
---

## Context

- Current branch: !`git branch --show-current`

## Your task

현재 브랜치를 `git push --force-with-lease`로 origin에 강제 푸시하세요. 단일 메시지 내에서 도구 호출(Tool Call)로 수행하며, 사담은 생략하세요.
