# resume-writing-skill

An [Anthropic Claude skill](https://docs.claude.com/en/docs/claude-code/skills) for rewriting US-market job-application resumes. Drop it into Claude Code (or any Claude environment that loads skills from a directory) and it turns a raw resume + a target role into three artifacts: a Markdown resume, a moderncv-banking LaTeX resume, and a personalized teaching handbook calibrated to how strong the resume actually is.

This was originally a Next.js + AWS Lambda SaaS at `knflow.com/resume-ai`. The skill version replaces it — same coaching methodology, packaged so it runs locally inside your own Claude.

## What makes it different from a generic resume prompt

- **Four-tier diagnosis rubric.** Every resume gets scored 2–3 / 5–6 / 7–8 / 9–10 against US-market interview-rate expectations (~0% / <5% / ~10% / ~20%). The score gates how aggressive the rewrite is.
- **Tier-calibrated output size.** A 9/10 student receives a tight ~4-page handbook that confirms what's working. A 2/3 student receives a 30-page handbook dominated by *经验补强* (experience-building) recommendations rather than line-by-line rewrites, because rewriting weak material does not fix a structural gap.
- **Live JD scan.** Pulls 2–3 currently-active US job descriptions (mix of Big Tech / mid / startup), extracts repeated keywords, and targets ≥75% coverage in the rewrite.
- **Fatal-flaw checklist.** Five named failure modes (information density, missing quantification, keyword mismatch, no personal brand, timeline confusion). Every flagged flaw quotes the student's actual bullet — no generic advice.
- **`[Needs verification]` flagging.** Any quantified claim the student cannot defend under interview probing gets marked rather than carried forward, to neutralize fabrication risk before submission.
- **Three per-run outputs.** Markdown for fast iteration and copy-paste, moderncv-banking LaTeX for the polished PDF, and a personalized handbook that uses the student's own Before/After as teaching material.

## Install

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/zyziyun/resume-writing-skill.git ~/.claude/skills/resume-writing
```

Then in any Claude Code session, upload or paste your resume and say something like *"help me rewrite my resume for an AI Engineer role"* — Claude will auto-invoke the skill based on the description in [SKILL.md](SKILL.md).

### Other Claude environments

Any setup that loads skills from a directory works the same way. Point it at this repo's root; `SKILL.md` is the entry point.

## Files

| File | Purpose |
|------|---------|
| [`SKILL.md`](SKILL.md) | Skill entry point — workflow, methodology, calibration matrix |
| [`resume_template.tex`](resume_template.tex) | moderncv-banking LaTeX template, populated each run |
| [`handbook_template.md`](handbook_template.md) | Teaching handbook template — filled with the student's own diagnosis and Before/After each run |

## Scope

**Use this for:** US-market resume rewrites for SDE, AI Engineer, Applied Scientist, ML Engineer, Data Scientist, PM, TPM, UX, Marketing roles. Works for new grad through Senior+.

**Do not use this for:** cover letters, LinkedIn About sections, interview prep, recruiter outreach drafts, non-US-market resumes — those need their own workflows.

## License

MIT. See [LICENSE](LICENSE).

## Author

Built by [Yun Zi](https://github.com/zyziyun) — AI Engineer at Amazon, GenAI curriculum lead at Pilot Technologies / Zhitong Silicon Valley. The methodology behind this skill is the same one used in the curriculum and in 1:1 senior-engineer mentoring sessions.

Issues and PRs welcome.
