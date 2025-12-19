---
allowed-tools: Bash(git add:*), Bash(git status:*), Bash(git commit:*)
description: Create a git commit
---

## Context

- Current git status: !`git status`
- Current git diff (staged and unstaged changes): !`git diff HEAD`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -10`

## Your task

Based on the above changes, create a single git commit.

You have the capability to call multiple tools in a single response. Stage and create the commit using a single message. Do not use any other tools or do anything else. Do not send any other text or messages besides these tool calls.

## Instructions
이 명령어가 호출되면 반드시 다음 가이드를 준수하세요:

### 커밋 메시지 규칙 (기존 REFERENCE.md 내용)
* **형식**: `feat:`, `bugfix:`, `hotfix:`, `refactor:`, `chore:`의 접두사를 사용합니다.
* **언어**: 한국어로 작성하되, 기술 용어는 원문을 유지합니다.
* **본문**: 변경 이유가 복잡할 경우 반드시 본문에 설명을 포함합니다.
