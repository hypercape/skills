# Hypercape Skills

하이퍼케이프(Hypercape)가 업무에 쓰는 AI 에이전트 스킬 모음입니다. 누구나 가져다 쓸 수 있도록 공개하고, 하이퍼케이프가 계속 유지보수합니다.

A collection of agent skills that Hypercape uses at work, published for anyone to use.

## 스킬 목록

| 스킬 | 하는 일 |
|---|---|
| [document-design](skills/document-design/SKILL.md) | 새 문서를 흑백, Helvetica, 간결한 인쇄물 느낌, 합니다체로 만듭니다. 참고 문서를 올리면 그 문서의 여백, 글자 크기, 제목, 표, 페이지 구성을 새 문서에 적용합니다. |

## 사용법

스킬 하나는 폴더 하나이고, 폴더 안의 `SKILL.md`가 스킬 본문입니다.

- **Claude Code**: 쓰려는 스킬 폴더를 `~/.claude/skills/`(모든 프로젝트) 또는 프로젝트의 `.claude/skills/`에 복사합니다.

  ```bash
  git clone https://github.com/hypercape/skills.git
  mkdir -p ~/.claude/skills
  cp -R skills/skills/document-design ~/.claude/skills/
  ```

- **다른 에이전트나 채팅 도구**: `SKILL.md`의 내용을 지침(시스템 프롬프트, 사용자 지침 등)에 붙여 넣어 씁니다.

## 폴더 구조

```text
skills/
  <스킬 이름>/
    SKILL.md        필수. 맨 위 frontmatter에 name, description
    (보조 파일)      선택. 예시, 템플릿 등
```

- 폴더 이름과 frontmatter의 `name`은 같게, 영문 소문자와 하이픈으로 씁니다.
- `description`에는 무엇을 하는 스킬인지와 언제 쓰는지를 씁니다. 에이전트는 이 문장을 보고 스킬을 고릅니다.

## 기여와 유지보수

- 새 스킬과 수정은 모두 Pull Request로 받습니다. 자세한 기준은 [CONTRIBUTING.md](CONTRIBUTING.md)를 봐 주세요.
- 공개 저장소이므로 비밀값(토큰, 키, 비밀번호)과 회사 내부 정보는 올리지 않습니다.
- 스킬을 고칠 때는 README의 스킬 목록도 함께 고칩니다.

## 라이선스

[Apache License 2.0](LICENSE)
