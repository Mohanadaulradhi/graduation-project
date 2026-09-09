# Docs — مَنطقة الكتابة الأكاديمية المشتركة

This folder is the **shared academic writing workspace** of the graduation project.
Every chapter of the official report structure (هيكل المشروع) gets a file here.
All four members contribute here through git — never write directly in `main`, use a
branch + PR (or push on a team-accepted workflow) so the assistant and peers review.

## Chapter ownership (rotating authors — balance enforced)
| File | Chapter | Lead author | Co-author / reviewer |
|------|---------|-------------|----------------------|
| ch1-introduction.md | Ch1: Introduction | Mohannad (S1) | Malik (S4) |
| ch2-background-literature.md | Ch2: Background & Literature Review | Zakaria (S2) | Ahmed (S3) |
| ch3-requirements-modeling.md | Ch3: Requirements Analysis & Modeling | Ahmed (S3) | Malik (S4) |
| ch4-design.md | Ch4: Design | Zakaria (S2) | Ahmed (S3) |
| ch5-implementation.md | Ch5: Implementation | all (split by feature) | all |
| ch6-conclusions.md | Ch6: Conclusions & Recommendations | Mohannad (S1) | Ahmed (S3), Malik (S4) |

## How to write with the assistant (سير عمل موحّد)
1. Before opening a session: `git pull origin develop` (or `main`).
2. Open opencode **inside your clone folder** — it auto-reads `AGENTS.md` + this README.
3. Tell the assistant clearly: *"ساعدني في كتابة القسم X من doc/chY"* — I write Markdown
   directly into the chapter file.
4. You review, the assistant revises per your notes, then you `commit` (with
   `Co-Authored-By:` if you want credit shared) and `push`.
5. Another member reviews the PR. Merge to `develop`, weekly to `main`.

## Writing rules (mechanical)
- Report language: **English** (official structure is English); Arabic only in
  Arabic abstract/cover mirrors.
- Follow the exact section numbering from the official project structure.
- Keep figures/tables numbered: `Figure 1.1`, `Table 3.2`, each with a caption.
- Cite consistently (APA) — add references in `references.md` as you go.
- Never invent data: mark placeholders as `[TBD: ...]` so everyone knows what remains.

## Handbook of milestones (جدول زمني)
- M1 end of Week 6: Ch1–3 draft → supervisor.
- M2 end of Week 9: Ch4 + twin-engine spec → supervisor.
- M3 end of Week 19: Ch5 implementation draft.
- M4 end of Week 23: V&V/Testing sections.
- M5 end of Week 25: full report assembled, formatted.
- M6 mid-March 2027: defense (المناقشة).