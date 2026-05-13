# resume-writing-skill

An [Anthropic Claude skill](https://docs.claude.com/en/docs/claude-code/skills) that turns either a ~30-page unstructured brain-dump **or** an existing resume into a US-market job-application resume — with three artifacts produced per run:

- A clean Markdown resume
- A moderncv-banking LaTeX resume (compiles with `pdflatex`)
- A personalized teaching handbook that walks you through the diagnosis, the rewrites, and your next action items — designed to stay useful long after the run

The skill replaces an earlier Next.js + AWS Lambda SaaS at `knflow.com/resume-ai`. Same coaching methodology — packaged so it runs locally inside your own Claude.

---

## Why this exists

Most resume "rewriters" are line-level prompt wrappers: paste a bullet in, get a polished bullet back. That fixes nothing if the underlying material is thin, the role direction is wrong, the keywords don't match the JDs employers are actually posting today, or the candidate can't defend their own numbers in an interview.

This skill is built around five ideas the methodology has spent years pressure-testing on real US-market job seekers:

1. **Brain-dump beats resume-writing for recall.** Writing directly into "résumé format" forces premature decisions about ordering, density, and emphasis — people consistently under-recall their strongest material when they start in résumé mode. A separate dump-then-structure pass produces materially stronger resumes.
2. **Different problems need different fixes.** A resume with weak packaging needs rewriting. A resume with weak underlying experience needs new projects — rewriting won't help. The skill diagnoses which one you are before deciding how aggressive to be.
3. **Keywords aren't optional.** Below ~75% coverage of the keywords repeated across current JDs, the ATS and 30-second recruiter scan both fail. The skill pulls live JDs and measures coverage explicitly.
4. **Unverifiable numbers break interview trust.** A single number you can't defend under probing breaks credibility for every other claim. The skill marks un-defensible quantification with `[Needs verification]` and lists them as pre-submission action items.
5. **The handbook is the actual teaching.** The rewrite is one-shot value; the handbook is how you internalize the methodology so the next time you iterate, you don't need this skill.

---

## How to use it

```text
Step 0  — Brain-dump (recommended, ~30 pages)
            in Typeless / Obsidian / Bear / Apple Notes / Notion / Markdown
            (or skip if you already have a resume you trust)

Step 1  — Run this skill in Claude with your dump or resume
            plus a specific target role (e.g. "AI Engineer (RAG/Agent)")

Step 2  — Receive three files:
            LastName_Resume_<Role>.md
            LastName_Resume_<Role>.tex
            LastName_Handbook_<Role>.md

Step 3  — Read the handbook. Act on Part 5 first.
            Verify any [Needs verification] numbers. Then submit.
```

---

## Install

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/zyziyun/resume-writing-skill.git ~/.claude/skills/resume-writing
```

In any Claude Code session, upload or paste your resume (or brain-dump) and say something like *"help me rewrite my resume for an AI Engineer role"* — Claude auto-invokes the skill from the description in [SKILL.md](SKILL.md).

### Other Claude environments

Any setup that loads skills from a directory works the same way. Point it at this repo's root; `SKILL.md` is the entry point.

---

## What makes it different

| Feature | What it does |
|---|---|
| **Accepts brain-dump input** | A ~30-page unstructured dump from Typeless / Obsidian / Bear works as well as a polished resume |
| **Four-tier diagnosis rubric** | Every input is scored 2–3 / 5–6 / 7–8 / 9–10 against US-market interview-rate heuristics (≈ 0% / < 5% / ≈ 10% / ≈ 20%) — coaching-observed, not controlled-study, used to calibrate where you're stuck |
| **Tier-calibrated output** | A top-tier resume gets a tight ~4-page handbook confirming strengths; a structurally weak resume gets a ~30-page handbook focused on experience-building, not line-level rewrites |
| **Live JD scan** | Pulls 2–3 currently-active US JDs (Big Tech / mid / startup mix), extracts repeated keywords, targets ≥75% coverage |
| **Fatal-flaw checklist** | Five named failure modes (info density, missing quantification, keyword mismatch, no personal brand, timeline confusion). Each flagged flaw quotes your actual bullet |
| **`[Needs verification]` flagging** | Any quantified claim you can't defend under interview probing gets marked, not silently carried forward |
| **Dual-language handbook** | English by default (`handbook_template_en.md`); Mandarin available (`handbook_template.md`) when the student is a Mandarin speaker |
| **Dual-mode handbook** | Same handbook works whether you ran the skill yourself or a coach is walking you through it |

---

## Files

| File | Purpose |
|------|---------|
| [`SKILL.md`](SKILL.md) | Skill entry point — workflow, methodology, calibration matrix |
| [`resume_template.tex`](resume_template.tex) | moderncv-banking LaTeX template, populated each run |
| [`handbook_template_en.md`](handbook_template_en.md) | English handbook template — default for most users |
| [`handbook_template.md`](handbook_template.md) | Mandarin handbook template — used when the student prefers Chinese |

---

## Scope

**Use this for:** US-market resume rewrites for SDE, AI Engineer, Applied Scientist, ML Engineer, Data Scientist, Data Analyst, PM, TPM, UX, Marketing roles. Works for new grad through Senior+.

**Don't use this for:** cover letters, LinkedIn About sections, interview prep, recruiter outreach drafts, non-US-market resumes — those need their own workflows.

---

## License

MIT. See [LICENSE](LICENSE).

## Author

Built by [Wendy Yun](https://github.com/zyziyun) — AI Engineer at Amazon, GenAI curriculum lead at Pilot Technologies and Zhitong Silicon Valley. The methodology behind this skill is the same one used in the curriculum and in 1:1 senior-engineer mentoring sessions.

Issues and PRs welcome.
