# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A personal **Obsidian vault** of Korean-language study notes — not a software project. There is **no build, test, or lint step**; work here means reading, writing, and reorganizing Markdown notes. All prose is Korean; match that when authoring or editing. Notes follow the 큐스터디 권태원 강사 lecture series.

`.obsidian/` (both the root one and the nested `mathmatic/.obsidian/`) and `.DS_Store` are git-ignored, so Obsidian config is **not** tracked — don't rely on it being present for other instances.

## Structure

```
mathmatic/              # the only active area
  basic/                # 기초 수학        ← 썡기초수학 강의 (N-topic.md)
  basic-calculus/       # 기초 미적분학    ← 대학기초수학 강의 (NN-topic.md + images/)
  calculus-1/           # 미적분학1        ← 대학미적분학1 강의
  analysis-1/           # 해석학 (placeholder, empty — upcoming)
  memory.md             # learning log (see below)
dev/                    # 개발, planned/empty
```

The README also lists 경제 (economics) and 금융공학 (financial engineering) as planned vaults; no folders exist for them yet.

`mathmatic/basic-calculus/images/` holds figures grouped by topic (`01-function-limit/`, etc.).

## Note conventions

- **Filenames**: kebab-case, lowercase English + hyphens, prefixed by lecture order (`16-derivative-1.md`, `01-function-limit-1.md`).
- **Paired files in `basic-calculus/`**: most lessons exist as a pair — `NN-topic.md` is the full annotated note (rich frontmatter: `id`, `aliases`, `tags`, plus `title`, `pages`, `subject`, `topics`), and `NN-topic-note.md` is a condensed companion holding the LaTeX formulas/derivations (minimal frontmatter). When extending a lesson, keep both halves in sync rather than merging them.
- **Frontmatter**: YAML with `id`, `aliases` (Korean + symbol aliases for search), `tags` (Korean topic tags like `미분법`, `적분법`). `id` is sometimes a UUID, sometimes a slug — match the neighboring file.
- **Math**: heavy LaTeX, inline `$...$` and display `$$...$$`. The vault uses the latex-suite, tikzjax, and excalidraw Obsidian plugins, so notes may contain TikZ or Excalidraw blocks — preserve them verbatim.
- **Cross-links**: Obsidian wikilinks `[[note-id]]` (e.g. `[[calculus-1/epsilon-N-delta]]`); a link to a not-yet-created note is intentional.
- **Tables with `|`**: math content (absolute-value bars `|x|`) frequently breaks Obsidian table rendering by mis-splitting cells. Watch for and fix this when editing math-containing tables.

## Learning memory (`mathmatic/.claude/memory/`)

A multi-file learning-memory store mirroring Claude Code's native memory format (one fact per file + a `MEMORY.md` index). It lives in the repo (git-tracked → remote-backed) and is hidden from the Obsidian UI by the dot-folder. The index is auto-loaded every session via the import below:

@mathmatic/.claude/memory/MEMORY.md

Read individual files on demand. Files: `study-style.md` (how to tutor — grilling, weakness-spotting over praise), `weaknesses.md`, `proof-tools.md`, `next-session.md`, and per-session logs `log-YYYY-MM-DD-*.md`. Topic notes hold the actual math; this store records *what was studied, where it's weak, and what's next*.

**Single source of truth — never duplicate.** Record learning memory ONLY here, never in the `~/.claude/.../memory/` agent store; writing to both double-loads the same content into the context window. When a session ends: add/append the relevant file(s), add an index line to `MEMORY.md`, convert relative dates to absolute, and check `study-style.md` before tutoring. The user's workflow: 강의 → 어려운 부분 추출 → 그릴링(Q&A) → 정리 파일 작성 → 메모리 갱신.

## Git conventions

Commit messages are short Korean descriptions of the lecture/topic covered (`미적분학1 엡실론 논법`, `58~65강 정리파일`, `52 53 54강`). No Conventional Commits prefixes.
