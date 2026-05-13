# resume-writing-skill

An [Anthropic Claude skill](https://docs.claude.com/en/docs/claude-code/skills) that turns **either a polished resume or a ~30-page unstructured brain-dump** into a US-market job-application resume. Drop it into Claude Code (or any Claude environment that loads skills from a directory) and it produces three artifacts: a Markdown resume, a moderncv-banking LaTeX resume, and a personalized teaching handbook calibrated to how strong the input actually is.

This was originally a Next.js + AWS Lambda SaaS at `knflow.com/resume-ai`. The skill version replaces it — same coaching methodology, packaged so it runs locally inside your own Claude.

## Recommended workflow

The strongest resumes don't come from sitting down to "write a resume". They come from:

1. **Brain-dump first** — open [Typeless](https://typeless.app/) (or Obsidian / Bear / Apple Notes / Notion / plain Markdown) and dump everything: every project, decision, win, failure, technology, metric, stakeholder, anecdote, number. Target ~30 pages of raw content. No bullets, no length limits, no resume-style sentences — that constrains your thinking prematurely and causes you to under-recall your best material.
2. **Run this skill on the dump** — it does the structurization, role-targeted prioritization, and rewriting for you, and outputs the three artifacts above.

If you already have a resume, you can skip step 1 and feed the resume directly — but if the resume feels thin or constrained, doing a brain-dump pass usually surfaces material the polished version was hiding.

## What makes it different from a generic resume prompt

- **Accepts unstructured brain-dump as input.** ~30 pages of raw notes from Typeless / Obsidian / Bear works as well as a polished resume — the skill handles structurization, role-targeted prioritization, and rewriting in one pass.
- **Four-tier diagnosis rubric.** Every input gets scored 2–3 / 5–6 / 7–8 / 9–10 against US-market interview funnel signals (essentially zero / very low / moderate / strong). The score gates how aggressive the rewrite is.
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
