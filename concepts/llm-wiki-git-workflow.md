---
title: LLM Wiki Git 실습 워크플로
created: 2026-07-26
updated: 2026-07-26
type: concept
tags:
  - workflow
  - pkm
  - automation
sources:
  - raw/articles/ai-agent-automation.md
confidence: high
contested: false
contradictions: []
---

# LLM Wiki Git 실습 워크플로

LLM Wiki 지식 베이스 구축 시스템에서 AI 에이전트(Antigravity)와 사용자가 협력하여 원본 자료를 보존하고, 정식 지식을 컴파일하며, Git 원격 저장소와 안전하게 동기화하는 실행 지침이다. ^[raw/articles/ai-agent-automation.md]

## 1. 사전 준비 및 브랜치 상태 확인

작업을 시작하기 전, 사용자는 현재 내 작업 브랜치(`dev-260726`)에 위치해 있는지 확인한다. 원본(upstream) 저장소 대신 개인 포크(Fork) 저장소를 독립적으로 다룬다.

```bash
git branch
# * dev-260726 브랜치 확인
```

## 2. 지식 컴파일 및 무결성 관리

[[ai-personal-knowledge-management]] 및 [[llm-wiki]] 원칙에 따라:
1. `raw/` 폴더에 변경 불가능한 원본 증거(Raw Evidence)를 보존하고 SHA-256 무결성을 계산한다.
2. [[ai-agent-automation]] 기능을 활용하여 `concepts/` 및 `entities/`에 출처(`sources`, `^[raw/...]`)가 명시된 정식 노트를 컴파일한다.
3. [[ai-knowledge-workflow]] 품질 관문에 맞춰 `index.md` 총 페이지 수와 목차를 갱신하고, `log.md`에 추적 변경 이력을 기록한다.

## 3. 원격 저장소 동기화 (Git Push)

작업이 완료되면 아래 순서로 원격 깃허브(`origin/dev-260726`)에 푸시한다.

```bash
# 1. 원격 최신 변경사항 반영 (Rebase)
git pull origin dev-260726 --rebase

# 2. 스테이징 및 커밋
git add .
git commit -m "feat: sync llm-wiki canonical memory and metadata"

# 3. 내 원격 저장소에 업로드
git push origin dev-260726
```

## 4. PR (Pull Request) 및 AI 코드 리뷰 (PR-Agent)

원격 저장소에 푸시한 후, `main` 브랜치로 병합하기 위해 깃허브에서 Pull Request를 생성한다.
이 프로젝트는 코드 리뷰와 품질 검증을 자동화하기 위해 **CodiumAI PR-Agent**를 도입하여 사용한다.

- PR을 생성하거나 새로운 커밋을 푸시(synchronize)하면, 깃허브 액션에 설정된 PR-Agent가 자동으로 트리거된다.
- Gemini 2.5 Pro 모델 기반으로 변경 사항(코드 및 마크다운)을 분석하여 PR 코멘트에 리뷰와 요약을 남긴다.
- 설정 파일(`.pr_agent.toml`)을 통해 프로젝트에 맞는 최적의 LLM 모델을 강제 지정하여 무결성을 보장한다.
- 검토가 완료되고 안전성이 검증된 PR만 `main` 브랜치로 머지(Merge)하여 지식 베이스를 갱신한다.
