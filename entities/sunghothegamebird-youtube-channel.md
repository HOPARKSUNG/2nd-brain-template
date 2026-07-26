---
title: "@sunghothegamebird YouTube Channel"
created: 2026-07-26
updated: 2026-07-26
type: entity
tags:
  - research
  - workflow
sources:
  - raw/youtube/sunghothegamebird-channel.md
confidence: high
contested: false
contradictions: []
---

# @sunghothegamebird 유튜브 채널

HOPARKSUNG(이 저장소 소유자)이 직접 운영하는 개인 유튜브 채널이다. ^[raw/youtube/sunghothegamebird-channel.md]

## 채널 정보

- **핸들:** [@sunghothegamebird](https://www.youtube.com/@sunghothegamebird)
- **운영 주체:** 이 2nd-Brain 저장소와 동일한 운영자
- **활용 목적:** 개인 콘텐츠 아카이브, 영상 자막·스크립트의 지식 원본으로 활용

## 2nd-Brain과의 연결

이 채널에서 제작된 영상의 자막과 스크립트는 [[ai-knowledge-workflow]] 원칙에 따라
`raw/youtube/` 폴더에 원본(Raw Evidence)으로 보존한다.
보존된 자막은 [[llm-wiki]] 방식으로 `concepts/` 또는 `queries/` 정식 지식으로 컴파일된다.
전체 운영 절차는 [[llm-wiki-git-workflow]]를 따른다.

## 향후 활용 방안

- 영상 업로드 시: 자막 파일(`.srt` → `.md` 변환)을 `raw/youtube/` 에 저장
- 유의미한 영상 내용: `concepts/` 또는 `queries/` 정식 지식으로 컴파일
- `index.md` 및 `log.md` 동기화 후 `dev-260726` 브랜치에 Push
