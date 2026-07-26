# 🧠 LLM-Wiki 실습 & Git 순서 가이드

## 1. 실습 시작 전 브랜치 확인
작업을 시작하기 전 항상 내가 작업 브랜치(`dev-260726`)에 있는지 확인합니다.

```bash
git branch
# * dev-260726 이어야 함
```

만약 `main`으로 되어 있다면 작업 브랜치로 이동합니다:
```bash
git checkout dev-260726
```

---

## 2. LLM-Wiki 실습 (Antigravity AI와 함께)
1. `raw/articles/` 폴더에 원본 문서(`.md`) 수집 및 보관.
2. AI(Antigravity)에게 지시하여 지식 컴파일 및 동기화 수행:
   > 💬 "raw/articles/ 문서를 읽고 SCHEMA.md 규칙대로 concepts/ 지식 노드를 작성한 뒤 index.md와 log.md를 갱신해줘."

---

## 3. 작업 내역 깃허브(GitHub)로 올리는 순서
작업이 끝난 후 Git Bash에서 아래 3단계 명령어를 실행하여 내 깃허브로 업로드합니다.

```bash
# 1단계: 원격 저장소 최신 상태 당겨오기 (동기화)
git pull origin dev-260726 --rebase

# 2단계: 변경된 파일 담기 & 커밋 메시지 작성
git add .
git commit -m "feat: llm-wiki note update"

# 3단계: 내 깃허브(GitHub)로 업로드 (푸시)
git push origin dev-260726
```
