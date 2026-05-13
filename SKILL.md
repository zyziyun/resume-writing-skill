---
name: resume-writing
description: Use this skill whenever a user provides a resume OR raw career materials — experience notes, project descriptions, transcripts, LinkedIn export, or a long unstructured brain-dump from a notes app like Typeless / Obsidian / Bear / Notion / Apple Notes — and asks for a US-market job-application resume. Triggers include "help me rewrite my resume", "structure my brain-dump into a resume", "turn these notes into a resume", "review my CV for SDE / AI / DS / PM / UX / Marketing / TPM / MLE", "make my resume better for [role]", or any upload of a resume or raw career notes (PDF / DOCX / MD) with intent to apply for US roles. The skill outputs three per-run files: a Markdown resume, a moderncv-banking LaTeX resume, and a personalized teaching handbook calibrated to the student's diagnosis (a top-tier student gets a thin handbook, a structurally weak one gets a thick handbook focused on experience-building rather than line-level rewrites). Do NOT use this skill for cover letters, LinkedIn rewrites, interview-prep materials, or non-US markets — those have their own workflows.
---

# Resume Writing Skill

## When to invoke

Trigger this skill when ALL of the following hold:

- User has a resume, OR a brain-dump of raw career materials (notes, project write-ups, transcripts, LinkedIn export) they want turned into a resume.
- The target market is the US (default assumption unless user says otherwise).
- User has named — or can be quickly asked to confirm — a target role direction.

Do NOT invoke for: cover letters, LinkedIn About sections, interview prep, recruiter outreach drafts, or non-US-market resumes.

## Recommended upstream workflow (before invoking this skill)

If the student is starting from scratch — or even if they have a resume but it feels constrained or thin — the strongly recommended pre-step is to brain-dump everything into a low-structure notes tool first:

- Use **Typeless** (or any free-form notes app — Obsidian, Bear, Apple Notes, Notion, plain Markdown files).
- Target **~30 pages of raw content** before any structuring.
- No bullets, no formatting rules, no length limits — dump every project, decision, win, failure, technology, metric, stakeholder, anecdote, and number you can recall.
- Do NOT try to write resume-style sentences during the dump; that prematurely constrains thinking and consistently causes students to under-recall their strongest material while over-including weak material.

This skill is built to take that brain-dump as input and handle structurization, role-targeted prioritization, and rewriting. The "resume" itself is the output of a separate structurize-then-rewrite pass, not the medium in which content is recalled.

When the student arrives with a brain-dump rather than a polished resume, Step 1 of the workflow does an extended intake to extract roles, dates, projects, and technologies before scoring against the rubric.

## Files in this skill

- `SKILL.md` — this file (workflow + methodology summary)
- `resume_template.tex` — LaTeX template (moderncv banking), populated each run
- `handbook_template.md` — teaching handbook template, filled in each run with this student's specific diagnosis and Before/After

## Required inputs (block on these before producing output)

Before generating any rewrite, confirm:

1. **Target role direction** — specific (e.g. "Product DS" not just "Data Scientist"; "AI Engineer (RAG/Agent)" not just "AI Engineer").
2. **Company-tier preference** — Big Tech / mid / startup / contractor / FTE.
3. **Years of experience tier** — new grad / 2–4 YOE / 5+ YOE / Senior+.
4. **Sponsor status** — international student / OPT / H1B / GC / citizen / no preference.
5. **Cross-industry transition vs. vertical deepening** — affects Summary framing and story arc.

If anything is missing, ask once before doing the rewrite. Do NOT fill gaps with assumptions.

## Per-run outputs (what the user receives)

Three files, named after the student's last name and target role:

1. `[LastName]_Resume_[Role].md` — final resume in Markdown
2. `[LastName]_Resume_[Role].tex` — final resume in LaTeX (moderncv banking)
3. `[LastName]_Handbook_[Role].md` — personalized teaching handbook based on this resume

The handbook is NOT a static methodology document. It uses the student's own Before/After as case material, flags fatal flaws found on their actual resume, lists keyword coverage against the JDs sampled this run, and gives action items specific to where this student is. **The handbook is calibrated to the student's diagnosed tier — a 9/10 student gets a tight, confidence-confirming handbook; a 2/3 student gets a thick handbook dominated by补经验 recommendations rather than line-by-line rewrites.** Static appendices (verb library, keyword speedrun, checklist, methodology reference) come bundled by default so the student can self-serve future iterations on other role directions.

## Workflow

### Step 1 — Intake & target-role lock

Read whatever the user uploaded. Two intake paths:

- **Polished resume input** — proceed to diagnosis directly.
- **Brain-dump input (~30 pages of raw notes, Typeless / Obsidian / etc.)** — do an extended intake first: extract roles, date ranges, projects, technologies, metrics, and stakeholders into a working outline before any rewriting. Flag gaps the dump did not cover (e.g. quantified impact, scope numbers, team size) so the student can fill them before Step 5. The handbook's Part 1 should note "starting from raw materials, not from an existing resume" so the diagnosis is read in that context.

If the role direction is unclear, ask. A typical user actually needs 2–3 versions (primary + backup + generalist); confirm whether they want all of them or just the primary today.

### Step 2 — JD market scan (web_search)

Pull 2–3 currently-active US JDs matching the target role. Use queries that include the current year so results don't pull stale 2024-era postings.

Mix sources: 1 Big Tech, 1 mid-sized, 1 startup when possible.

For each JD, capture:
- Source URL and company tier label
- Required skills (must-have)
- Preferred / nice-to-have skills
- Repeated keywords (terms appearing in 2+ JDs are high-signal)
- Salary range if disclosed (informs seniority calibration)

Save these — they get cited verbatim in the handbook's Part 3.

Build a keyword coverage checklist. Target ≥ 75% coverage in the rewritten resume. Flag any technologies in the user's draft that have been replaced in market (e.g. older frameworks, deprecated tools).

### Step 3 — Diagnose against the rubric

Score the current draft against the four-tier rubric:

| Tier | Interview funnel signal | Symptoms |
|------|-------------------------|----------|
| 2–3  | essentially zero        | Sparse content, no impact data, role direction unclear, won't pass AI screening |
| 5–6  | very low                | Coverage looks complete but no quantification, can't tell complexity or ownership |
| 7–8  | moderate                | Quantified and clear, but indistinguishable from peer candidates |
| 9–10 | strong                  | Above + a personal-brand differentiator that lands in the recruiter's first 30 seconds |

These are qualitative coaching heuristics, not measured outcomes — use as relative calibration, not predictive guarantee.

State explicitly: which tier, why, and whether the bottleneck is **structural** (the experience genuinely isn't there yet) or **packaging** (the experience is there but poorly told). These are very different conversations.

Also run the fatal-flaw checklist:

1. **Information density too low** — bullets describing a project's scope but not the candidate's specific contribution.
2. **No quantification** — bullets with no Endorsement, Scope, or Marketing dimension attached.
3. **Keyword mismatch** — < 75% coverage of the JD's high-frequency terms.
4. **No personal brand / no differentiator** — reads like an "AI assistant who took orders", no signal of who this person actually is.
5. **Timeline confusion / Experience demoted to Project** — overlapping roles hidden by structure rather than labeled clearly.

For each fatal flaw that applies: explain in three parts — **why it matters → current state on this student's resume (quote specific bullets) → how to fix.** Save these — they get reformatted into the handbook's Part 2.

If zero flaws apply (common for 9–10 tier), record that explicitly. Part 2 of the handbook will be skipped in that case.

### Step 4 — Pause and confirm direction

Before launching into the full rewrite, pause and surface the diagnosis. The user may want to discuss a specific finding (e.g. "I don't think bullet 3 is actually weak, here's why it lands well") before getting a finished draft.

Skip the pause only if the user has explicitly asked for "just rewrite it, don't explain".

### Step 5 — Rewrite section-by-section

For every section that gets rewritten, capture three things (these become both the chat-side explanation AND the handbook's Part 4):

- **Before:** the user's verbatim original
- **After:** the rewrite
- **What changed and why:** a short table — column 1 the change, column 2 the methodology reason

The "why" column is non-negotiable. The user is here to learn the methodology, not just to receive output.

**Don't rewrite for the sake of rewriting.** If a section is already strong, leave it alone and skip it from Part 4 entirely. If the resume is already at 9/10 tier, only 0–2 sections may need polish — do not invent reasons to touch the rest.

Apply these rules during rewrite:

- Section ordering: Summary → (Education-first if new grad, else Experience-first) → Experience → Projects (if any) → Skills → Education (if 2+ YOE).
- Strong verbs only on the lead position of each bullet (Architected / Shipped / Drove / Spearheaded / Productionized / Refactored / Benchmarked / Orchestrated / Delivered / Negotiated / Launched).
- Limit total intensifier adverbs (Independently / Proactively / Successfully / End-to-end) to ≤ 5 across the entire resume.
- Each bullet attaches to at least one impact dimension (Endorsement / Scope / Marketing).
- Re-prioritize Skills categories so the JD's most-weighted category leads.
- Keep Summary to 1–2 lines, ~25–40 words, anchored to a concrete proof point.

### Step 6 — Data calibration

For every quantified claim — percentages, user counts, QPS, latency, revenue, growth, cost savings — ask the user to confirm the number traces to a defensible source (commit history, dashboards, internal docs, manager confirmation, public press release).

If the user can't defend a number under interview probing ("how did you measure that 40%?"), mark it `[Needs verification: <specific note>]` rather than carrying the claim forward unchecked. Inflated numbers on a resume put the entire interview at risk — the recruiter or HM will probe, and a single fabrication breaks trust on every other claim.

Save the list of `[Needs verification]` flags — they go into the handbook's Part 5 action items (or get skipped entirely if there are none).

### Step 7 — Generate resume outputs (MD + LaTeX)

**Markdown version** (`[LastName]_Resume_[Role].md`):
- Plain headers, no decorative formatting.
- Useful for fast iteration, version control, and copy-paste into job-board forms.

**LaTeX version** (`[LastName]_Resume_[Role].tex`):
- Open `resume_template.tex` and replace every `[YOUR_xxx]` placeholder with the student's data.
- Drop sections that don't apply (e.g. comment out Projects for PM/Marketing direction).
- The student compiles with `pdflatex` or Overleaf to produce the PDF.
- Filenames must clearly differentiate role direction when the user has multiple versions.

### Step 8 — Generate the personalized handbook (calibrated to tier)

Open `handbook_template.md`. The template defines the MAXIMUM possible structure. For each per-run handbook, **size every dynamic section to what this student actually needs based on their diagnosed tier**.

#### Calibration matrix

| Tier  | Handbook depth         | Part 1 | Part 2 (fatal flaws) | Part 3 (JD coverage) | Part 4 (Before/After) | Part 5 (action items) | Appendices |
|-------|------------------------|--------|----------------------|----------------------|-----------------------|-----------------------|------------|
| 9–10  | tight, ~4–6 pages incl. appendices | brief — confirm strengths | usually skipped | always include | 0–2 polish items only | thin; pivots toward career nav | A, B, C kept; D optional |
| 7–8   | moderate, ~10–15 pages | full diagnosis + 差异化 gap | 1–2 flaws | always include | 2–4 sections | balanced | full |
| 5–6   | full, ~20–25 pages     | full diagnosis | 3–4 flaws | always include | 4–6 sections | strong on data verify + 关键词补强 | full |
| 2–3   | full but rebalanced, ~20–30 pages | full + structural diagnosis | 4–5 flaws | full but reframed | thin or skipped — rewriting weak material won't fix it | dominated by 经验补强 (bucket C) | full |

#### Skipping rules

- **Skip a Part entirely** (drop the heading too) when no content applies. Do NOT leave empty headings, "N/A" notes, or placeholder filler.
- **Skip subsections within a Part** under the same logic — e.g. only output Part 5 buckets that have items.
- **Always include** Part 1, Part 3, and appendices A/B/C — these have value at every tier.
- **Optional** is appendix D (full methodology reference) — include by default; omit only when the student has demonstrated methodology fluency in conversation.
- **Update the TOC** at the top of the handbook to reflect what's actually in the document. Don't list skipped sections.

#### Where each section's content comes from

| Section | Source material |
|---------|-----------------|
| Header (name, date, role) | Step 1 intake |
| Part 1 (diagnosis) | Step 3 (tier rating + bottleneck) |
| Part 2 (fatal flaws) | Step 3 (only output flaws that apply; quote student's actual bullets verbatim) |
| Part 3 (JD + keyword coverage) | Step 2 (cite each JD URL; show before/after coverage tables) |
| Part 4 (Before/After) | Step 5 (verbatim Before, rewrite After, change table for each rewritten section — only sections actually rewritten) |
| Part 5 (action items) | Step 6 (verify list) + Step 3 structural-gap diagnosis if any; output only buckets that apply |
| 附录 B (keyword speedrun) | Pick the role-direction-matching subsection from the template's static keyword library; drop the others |

Output filename: `[LastName]_Handbook_[Role].md`

#### Quality checks before delivering

- Every Part 2 fatal flaw must quote the student's actual original text — no generic descriptions.
- Every Part 4 change-table row must reference a specific methodology principle (verb tier, three-dimension impact, Summary formula, JD keyword coverage, fatal-flaw fix).
- Part 5 action items must be specific and dated/scoped — not vague "improve quantification".
- Static appendices must remain verbatim — do not paraphrase them.
- Length should match tier per the calibration matrix. If a 9/10 student's handbook is over 10 pages, you're padding — cut it.

### Step 9 — Deliver

Present all three files together:

```
[LastName]_Resume_[Role].md
[LastName]_Resume_[Role].tex
[LastName]_Handbook_[Role].md
```

Tell the student:
- Resume MD is for copy-paste into job forms and version control.
- Resume LaTeX compiles to a polished PDF — recommend Overleaf if they don't have a local LaTeX install.
- Handbook should be read once after delivery to internalize the methodology; they can refer back to it next time they iterate.

If the student wants a backup or generalist version of the resume, run the skill again with the new target direction — it produces a fresh handbook each time, calibrated to that direction's JDs.

## Output style (chat side)

- Diagnosis and rewrite explanation in chat go in Mandarin Chinese (default for this coach's students).
- Resume content itself stays in English (US market). No exceptions.
- Keep technical terms in English even in Mandarin explanation (do not translate "RAG", "A/B testing", "stakeholder", etc.).
- No preachy openers ("Resume writing is an art..."). Lead with diagnosis, then rewrite.
- No emoji.
- Don't expose internal tool calls in the final user-facing answer — search and read silently, surface conclusions.

## Edge cases

- **User uploads only raw notes, no formal resume yet** — this is now a first-class path, not an edge case; see the "Recommended upstream workflow" and Step 1's brain-dump branch above. Build from the dump, flag uncovered gaps before Step 5, and have the student fill them in before finalizing.
- **User's experience genuinely doesn't match the target role** — be direct in Part 1 (structural gap). Don't paper over with packaging. Recommend specific high-ROI projects in Part 5 (reference 2026 market signals, not stale 2023 project ideas).
- **User insists on numbers they can't defend** — push back once, explain interview-risk, and if they still want them, mark with `[Needs verification]` so they at least see the flag before submission. Part 5 of the handbook lists every such number.
- **User has 2+ overlapping roles in the timeline** — never solve this by demoting a role to Projects. Use clear title labels: "Visiting Researcher (Remote, Part-time)", "Concurrent Role", "Consulting Engagement (Part-time)". Note this resolution in the handbook's Part 4 (or Part 2 if the resume isn't being rewritten).
- **User asks about Sponsor question on application forms** — give the current US market reality, not 2024 advice. Note the recommendation in Part 5 bucket D.
- **User asks the skill to run again with a different target direction** — generate a NEW set of three files for the new direction. Don't reuse the previous handbook; the JDs and keyword coverage will differ. File names auto-disambiguate by role.
- **Student's resume is already 9/10** — don't manufacture problems to justify a long handbook. Output a short handbook confirming what's working, run keyword coverage against today's JDs (which may have shifted), suggest 0–2 polish items at most, and pivot Part 5 toward submission strategy / sponsor handling / backup direction prep.
