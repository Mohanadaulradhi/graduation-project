# AGENTS.md — Team Contract & Shared Context (Graduation Project)

This file is the single shared reference for every human teammate AND for the AI
assistant (opencode). Whenever anyone opens a session with the assistant inside
this repository, this file is read automatically. Keep it updated as team rules change.

## 1. Project
- **Display name:** Graduation Project — Telehealth Platform (المنصة الصحية عن بُعد)
- **Idea:** Mobile app (Flutter) for patients to book appointments / consultations +
  web dashboard (Laravel) for doctors & admins + a **Digital Health Twin**
  (rule-based risk engine built from patient data, doctor diagnoses, and treatment response).
- **Repo (after setup):** `graduation-project` (private, GitHub).

## 2. Team (fair distribution — effort target ≈ 305h per member, ±3%)
| ID | Real name | Owner type |
|----|-----------|------------|
| S1 | Mohannad (مهند) | Repo owner |
| S2 | Zakaria (زكريا) | Member |
| S3 | Ahmed (أحمد) | Member |
| S4 | Malik (مالك) | Member |
| SUP | Dr. Saleh (د. صالح) | Supervisor — Write access |

- **ALWAYS** map task ownership to these names, never to generic "one person".
- Rebalance load if any member exceeds ±5% of the average weekly hours.

## 3. Tech stack & tools
- Mobile: Flutter (Dart) — patient app.
- Web/API: Laravel (PHP), REST API, Sanctum auth, MySQL.
- Admin/doctor dashboard: Laravel (Blade or API + frontend as agreed).
- Digital Twin: weighted rule engine (risk score 0–100, treatment-response trend,
  auto recommendations/alerts). NO machine learning for the BSc scope.
- Communication: Telegram (primary), WhatsApp (secondary).
- Remote pair work: Chrome Remote Desktop / RustDesk.

## 4. Git workflow (mandatory)
- Protected: `main` (no direct pushes) ← merge via PR on `develop` branches.
- Branch pattern: `feature/<scope>` e.g. `feature/twin-engine`, `feature/mobile-booking`.
- One logical change per commit. Conventional Commits, imperative, ≤72 chars, English:
  `feat(api): add POST /appointments`, `fix(twin): round risk score`,
  `test(engine): add rule cases`, `docs(report): draft chapter 3`.
- Pull request rules: author ≠ reviewer (rotate reviewers). Merge only after
  reviewer approval AND CI passes (when CI is added).
- Every member sets own identity: `git config user.name/user.email` (distinct emails).
- Never commit `.env`, secrets, keys, or runtime artifacts (`.gitignore` enforced).

## 5. Daily cadence
- Daily stand-up ~10 min on Telegram: done / to-do / blockers.
- Before consulting the assistant: run `git pull origin develop` so it works on
  the latest code. After the assistant changes files, they must be committed and
  pushed by the responsible member (assistant never pushes without approval).
- AI-assisted edits appear under the local git identity on this machine; if you
  want to credit the assistant in history, add `Co-Authored-By:` trailer on commit.

## 6. Task distribution (from the plan — full matrix lives in docs/)
| # | Task | Owner(s) | Est. h |
|---|------|----------|-------:|
| T14 | Twin engine spec (formulas/rules) | S1 + S3 | 36 |
| T18 | Laravel setup + migrations | S2 + S3 (+S4) | 36 |
| T19 | Backend auth & roles | S2 + S3 | 28 |
| T20 | Flutter auth screens | S1 + S4 | 28 |
| T21 | Booking module (mobile) | S1 (S4 helps) | 32 |
| T22 | Consultation module (mobile) | S4 (S1 helps) | 32 |
| T23 | Health profile + twin page (mobile) | S4 + S1 (+S3) | 40 |
| T24 | Doctor dashboard | S2 (+S3) | 38 |
| T25 | Admin dashboard | S3 (+S4) | 24 |
| T26 | **Twin engine (backend)** | S3 + S1 + S2 | 44 |
| T27 | REST API + endpoint docs | S2 + S3 | 36 |
| T28 | Integration + notifications | S1 + S4 (+S2) | 44 |
| T30 | PHPUnit tests | S2 (+S3, S4) | 28 |
| T31 | Flutter tests | S1 + S4 | 28 |
| T32 | Integration + UAT | all | 40 |
| T34 | V&V documentation | S4 (+S2) | 24 |
| T36 | Chapter 6 conclusions | S1 + S3 (+S4) | 32 |

## 7. Deliveries (chapter map of the official project structure)
- Phase 1 Analysis (W1–6): Ch1 (intro, problem, objectives, scope, methodology, feasibility, Gantt/PERT) + Ch2 (literature review + comparison) + Ch3 (requirements F/NF, use cases, activity, sequence, class, DFD).
- Phase 2 Design (W6–9): Ch4 (ERD, schema, data dictionary, queries, UI hierarchy/forms/reports, twin spec).
- Phase 3 Development (W9–19): Ch5 implementation (DB, UI, engine, API, integration).
- Phase 4 Testing (W20–23): V&V, UAT, bug fixes.
- Phase 5 Delivery (W24–26): Ch6 + full report formatting + defense (March 2027).

## 8. Critical path
T14→T26→T27→T28→T32→T35(supervision; Marg: March 2027 defense).
Any +1 week slip on the engine delays the whole end. Protect buffer weeks on impossible dates.