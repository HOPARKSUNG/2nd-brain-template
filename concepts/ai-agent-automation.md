---
title: AI 에이전트 자동화
created: 2026-07-26
updated: 2026-07-26
type: concept
tags:
  - automation
  - workflow
  - pkm
sources:
  - raw/articles/ai-agent-automation.md
confidence: medium
contested: false
contradictions: []
---

# AI 에이전트 자동화

AI 에이전트(Agent)는 도구 사용, 메모리, 계획 수립 기능을 갖추고 자율적으로 작업을 실행하는 시스템이다. ^[raw/articles/ai-agent-automation.md]

## 에이전트의 핵심 구성 요소

1. **도구 사용(Tool Use):** 파일 시스템, 터미널, 웹 검색 등 외부 시스템과 상호작용하여 정보를 수집하고 변경을 적용한다.
2. **메모리(Memory):** 대화 이력과 작업 컨텍스트를 유지하여 장기적 맥락 속에서 일관된 작업을 수행한다.
3. **계획 수립(Planning):** 복잡한 작업을 하위 단계로 분해하고, 중간 결과를 평가하며 순차적으로 실행한다.
4. **자율 실행(Autonomous Execution):** 사용자의 지속적 개입 없이 실행-평가-수정 루프를 반복하여 작업을 완수한다.

## 지식 관리에서의 에이전트 역할

[[ai-knowledge-workflow]]의 수집 → 정리 → 컴파일 단계에서 에이전트는 다음을 자동화한다:

- **원본 수집:** 웹 클리핑, 유튜브 자막, 논문 등을 `raw/` 폴더에 불변 원본으로 보존
- **지식 컴파일:** [[llm-wiki]] 원칙에 따라 원본을 분석하고 `concepts/`, `entities/` 정식 노드로 변환
- **메타데이터 동기화:** `index.md` 총 페이지 갱신, `log.md` 이력 기록, 위키링크 무결성 검증

## Git 기반 협업 워크플로

에이전트와 사용자가 협력하는 [[llm-wiki-git-workflow]]에서 에이전트는:

1. 현재 브랜치 상태를 확인하고
2. SCHEMA 규칙에 맞게 정식 페이지를 생성하며
3. [[ai-personal-knowledge-management]] 3계층 구조(raw → canonical → metadata)를 유지한다

## 관련 도구 비교

[[knowledge-tool-roles]]에서 정리한 바와 같이, 에이전트 기반 자동화는 수동 PKM 도구(Obsidian, Zotero)와 보완적으로 작동한다.
