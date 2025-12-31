---
allowed-tools:
  - "Bash(git branch:*)"
  - "Bash(git log:*)"
  - "Bash(git diff:*)"
  - "Bash(git status:*)"
  - "Bash(gh pr create:*)"
description: "Create a PR with meaningful description"
---

## Context

  - Current branch: !`git branch --show-current`
  - Branch status: !`git status -sb`
  - Base branch: $ARGUMENTS (default: `main`)

  ## Your task

  1. Base 브랜치를 확인하세요 ($ARGUMENTS가 비어있으면 `main` 사용).

  2. 현재 브랜치명에서 정보를 추출하세요:
     - 지라 티켓 번호 추출 (ITD-XXXX 형식, 정규식 사용)
     - 브랜치 prefix 추출 (`/` 앞부분)
     - prefix를 대문자로 변환 (예: bugfix → BUGFIX)

  3. 변경사항을 분석하세요:
     - 모든 커밋 목록: `git log <base-branch>..HEAD --pretty=format:"%s"`
     - 전체 코드 변경: `git diff <base-branch>..HEAD`

  4. 분석 결과를 바탕으로 **의미있는 PR description**을 작성하세요:
     - **Title 형식**: `[PREFIX][ITD-XXXX] 변경사항 요약`
       - 예시: `[BUGFIX][ITD-5252] Gausium 로봇 modelFamilyCode 필드 매핑 추가`
     
     - **Body** (다음 섹션 포함):
       ```
       ## 관련 이슈
       - [ITD-XXXX](https://bigwaverobotics.atlassian.net/browse/ITD-XXXX)
       
       ## 변경 배경
       - 왜 이 작업이 필요했는지
       
       ## 주요 변경사항
       - 실제 코드에서 무엇이 바뀌었는지 (파일/클래스/메서드 수준)
       
       ## 커밋 목록
       - [커밋 메시지들을 bullet point로]
       ```

  5. `gh pr create`로 PR을 생성하세요 (--base, --title, --body 옵션 사용).

  6. 모든 작업은 단일 메시지 내에서 도구 호출(Tool Call)로 수행하며, 사담은 생략하세요.
