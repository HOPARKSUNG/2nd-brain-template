# Wiki Log

> Chronological record of wiki actions. This file is append-only: add entries at
> the end and never rewrite or remove an earlier entry.
>
> Entry heading format: `## [YYYY-MM-DD] <action> | <subject>`
>
> Allowed actions: `ingest`, `create`, `update`, `query`, `lint`, `archive`,
> `delete`, `map`, and `repair`.
>
> Each entry lists every affected repository-relative path. After 500 entries,
> rotate the completed file to `log-YYYY.md` and begin a new `log.md`; preserve the
> completed file unchanged.

## [2026-07-21] ingest | 2nd-Brain 개인지식 관리 원본 배치

- Selection: `understand-chat` identified the 2nd-Brain PKM core subgraph and its one-hop canonical neighbors; their leading frontmatter referenced 13 unique raw sources.
- Created:
  - `raw/notebooklm/2026-07-16-all-notes.md`
  - `raw/notebooklm/codegraph-github.md`
  - `raw/notebooklm/graphify-github.md`
  - `raw/notebooklm/llm-wiki-skill-github.md`
  - `raw/notebooklm/llm-wiki-zotero-notebooklm-youtube.md`
  - `raw/notebooklm/notebooklm-py-github.md`
  - `raw/notebooklm/understand-anything-github.md`
  - `raw/notebooklm/zotero-mcp-github.md`
  - `raw/web/NomaDamasslides-grab Best harness + editor + linter for generating slides in Claude Code  Codex - Claude Design Open Source Alternative.md`
  - `raw/web/stablyaiorca Orca is the ADE for working with a fleet of parallel agents. Run any coding agent with your own subscription. Available on desktop and mobile..md`
  - `raw/youtube/📺 How To Build LLM Wiki In Obsidian 🧠 A Memory Layer For Any Agentic AI.md`
  - `raw/youtube/📺 LLM Wiki를 업그레이드하는 외부 지식 시스템! 연구자를 위한 최강의 조합 Zotero × Notebook × Obsidian x Claude Code.md`
  - `raw/youtube/📺 Orca Is the Free Cursor Killer Nobody's Talking About!.md`
- Updated: `SCHEMA.md`, `AGENTS.md` to register importer-preserved raw directories and legacy hash-coverage handling.
- Integrity: all 13 target files are byte-identical to the source vault; all 8 recorded post-frontmatter body hashes match; 5 legacy web/video captures have no recorded `sha256` and retain their original missing final LF as explicit coverage and format gaps.
- Canonical state: unchanged at 0 pages; `index.md` was not modified.

## [2026-07-21] lint | 0 issues found

- Raw files in the imported source set: 13.
- Source/target byte-identical files: 13.
- Recorded post-frontmatter body hashes checked and matched: 8.
- Documented legacy hash-coverage and final-LF format gaps: 5.
- Invalid UTF-8, BOM, CRLF, body-hash drift, missing ingest-log paths, and unregistered importer directories: 0.
- Canonical pages and index entries: 0; no canonical navigation update was required.

## [2026-07-21] create | 2nd-Brain canonical 지식 코어

- Evidence: the existing 13-file raw source set was mapped to eight central, reusable PKM subjects; no raw record was duplicated or mutated.
- Created:
  - `concepts/ai-knowledge-workflow.md`
  - `concepts/ai-personal-knowledge-management.md`
  - `concepts/llm-wiki.md`
  - `concepts/research-feedback-loop.md`
  - `concepts/second-brain-research-workflow.md`
  - `comparisons/knowledge-tool-roles.md`
  - `queries/notebooklm-query-compounding.md`
  - `queries/ua-knowledge-graph-workflow.md`
- Updated:
  - `SCHEMA.md`
  - `index.md`
  - `log.md`
- Navigation: the eight-page graph uses only resolvable canonical wikilinks, with at least two distinct non-self links per page.
- Provenance: every source and claim marker resolves to an existing repository-relative raw Markdown path.

## [2026-07-21] lint | 0 issues found

- Canonical pages: 8 total (5 concepts, 1 comparison, and 2 queries); all required frontmatter fields, types, dates, confidence values, contestation fields, and contradiction lists are valid.
- Taxonomy and navigation: 9 registered tags, 8 exact alphabetical index entries, 33 canonical links, minimum 3 outbound links per page, and minimum 2 inbound links per page.
- Provenance: 27 source references and 17 claim-level markers resolve to existing raw Markdown records; no marker is absent from its page source list.
- Raw integrity: 13 Markdown records checked, 8 recorded body hashes matched, and 5 importer-preserved legacy hash/final-LF coverage gaps remain documented.
- Formatting, duplicate slugs, broken links, self-links, orphan pages, source drift, and lint warnings: 0.

## [2026-07-21] repair | lint source-reference count correction

- Correction: the immediately preceding lint entry reports 27 source references, but the measured canonical frontmatter total is 30.
- Unchanged measurements: 17 claim-level markers, 33 canonical links, 8 canonical pages, and 0 lint errors or warnings.
- Updated: `log.md` only; no raw or canonical page was changed.

## [2026-07-26] ingest | AI 에이전트와 지식 자동화 원본 수집

- Created: `raw/articles/ai-agent-automation.md`
- Source URL: https://example.com/ai-agent-automation
- Body SHA-256: `0b0df0d692b26136b32677e778be97085139ebd006a7a7e5b114a49ffb897d31`

## [2026-07-26] create | AI 에이전트 자동화 및 Git 실습 워크플로 정식 지식 코어

- Created:
  - `concepts/ai-agent-automation.md`
  - `concepts/llm-wiki-git-workflow.md`
- Sources: `raw/articles/ai-agent-automation.md`
- Wikilinks: `[[llm-wiki]]`, `[[ai-personal-knowledge-management]]`, `[[ai-knowledge-workflow]]`
- Updated:
  - `SCHEMA.md`
  - `index.md` (Total pages: 10)
  - `log.md`

## [2026-07-26] ingest | 개인 유튜브 채널 원본 수집

- Created: `raw/youtube/sunghothegamebird-channel.md`
- Source URL: https://www.youtube.com/@sunghothegamebird
- Note: sha256 pending-manual-verification (채널 페이지 JavaScript 렌더링 제한으로 수동 수집)

## [2026-07-26] create | @sunghothegamebird 유튜브 채널 정식 개체 노드

- Created: `entities/sunghothegamebird-youtube-channel.md`
- Sources: `raw/youtube/sunghothegamebird-channel.md`
- Wikilinks: `[[ai-knowledge-workflow]]`, `[[llm-wiki]]`, `[[llm-wiki-git-workflow]]`
- Updated:
  - `index.md` (Total pages: 11)
  - `log.md`

## [2026-07-26] repair | 누락된 파일 복구 및 메타데이터 수정

- Created:
  - `raw/articles/ai-agent-automation.md` (누락된 원본 기록 생성)
  - `concepts/ai-agent-automation.md` (누락된 정식 노트 생성)
- Updated:
  - `concepts/llm-wiki-git-workflow.md` (제목 한글 통일 및 연결 강화)
  - `concepts/ai-knowledge-workflow.md` (그래프 연결 강화)
  - `raw/youtube/sunghothegamebird-channel.md` (수동 수집 파일의 sha256 무결성 계산 완료)
- Moved:
  - `test-note.md` -> `inbox/test-note.md` (비정식 테스트 파일을 inbox로 격리)
- Integrity: `raw/youtube/sunghothegamebird-channel.md` 파일의 body hash를 `8c9a930806bc96b6ff8a642613077eeb4e6db478367041f5f20bf75ad25ce19d`로 갱신함.
- Canonical state: `index.md`에 등록된 11개의 페이지가 모두 파일시스템과 일치함을 확인.

## [2026-07-26] update | PR-Agent 코드 리뷰 자동화 인프라 도입

- Created:
  - `.github/workflows/pr-agent.yml` (PR-Agent 깃허브 액션 설정)
  - `.pr_agent.toml` (Gemini 2.5 Pro 모델 강제 지정)
- Updated:
  - `README.md` (AI Automation Tools 목록에 PR-Agent 추가)
  - `concepts/llm-wiki-git-workflow.md` (PR 생성 및 AI 코드 리뷰 자동화 과정 명시)
- Note: PR-Agent의 환경변수 인식 버그를 회피하기 위해 `.pr_agent.toml` 물리적 설정 파일을 도입하여 모델(gemini-2.5-pro)을 고정하고, `OPENAI_KEY` 시크릿 연동 오류를 해결함.
