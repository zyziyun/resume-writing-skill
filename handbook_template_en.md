<!--
================================================================
HANDBOOK TEMPLATE — ENGLISH  (per-run output of the resume-writing skill)
================================================================
This file is a TEMPLATE, not a finished document. Each run of the
skill produces a personalized handbook for ONE student by:
  1. Replacing every {{PLACEHOLDER}} with student-specific data
  2. Replacing every <!-- GENERATE: ... --> block with freshly
     generated content following the embedded instructions
  3. Keeping all STATIC sections (Appendix A / C / D) verbatim
  4. Customizing Appendix B based on the student's role direction

This is the DEFAULT handbook template. Use this for any student
unless they explicitly prefer Mandarin — in that case use
handbook_template.md.

================================================================
CRITICAL CALIBRATION RULE — read before generating
================================================================
This template defines the MAXIMUM possible structure, not a
minimum. Every dynamic section is OPTIONAL — output a section
only when it adds real value for THIS student. Do NOT pad. Do
NOT generate sections just because the template has slots.

Roughly how depth should scale with the student's diagnosed tier:

| Tier  | Part 1 | Part 2 (fatal flaws)        | Part 3 (JD coverage) | Part 4 (Before/After) | Part 5 (action items) | Appendices |
|-------|--------|-----------------------------|----------------------|-----------------------|-----------------------|------------|
| 9–10  | brief, confirm strengths | usually skipped or 1 minor item | always include | only sections actually polished, often 0–2 | thin; mostly career nav / next direction | A, B, C kept; D optional |
| 7–8   | full diagnosis + differentiation gap | 1–2 flaws        | always include | 2–4 sections         | balanced              | full       |
| 5–6   | full diagnosis              | 3–4 flaws        | always include | 4–6 sections         | strong on data verify + keyword fill-in | full       |
| 2–3   | full + structural diagnosis | 4–5 flaws        | full but reframed (current resume can't realistically clear ATS) | thin or skipped — rewriting won't fix structural gap | dominated by experience-building recommendations | full       |

A 9/10 student should get a tight, confidence-confirming handbook
(maybe 4–6 pages including appendices), not a 30-page tome they
don't need. A 2/3 student should get a structural-pivot handbook
that doesn't waste pages on line-level rewrites that won't matter
until the underlying experience is there.

When a section is skipped, omit it entirely (heading and all) —
do NOT leave an empty heading or a placeholder note. The TOC at
the top is just a roadmap; remove TOC entries for skipped sections.

Output filename:
  [LastName]_Handbook_[Role].md
  e.g.  Smith_Handbook_AIEngineer.md

Audience: the student. Tone: peer-professional English, direct.
Resume content stays in English. No internal references to
"course" / "1:1" / "your coach". Stand-alone document that works
whether the student is reading it solo or being walked through
it by a coach.
================================================================
-->

# {{STUDENT_NAME}}'s Resume Rewrite Handbook ({{ROLE_DIRECTION}})

> Generated from the resume you submitted on {{DATE}}, against 3 currently-active US-market {{ROLE_DIRECTION}} job descriptions pulled today.
> Companion files: `{{LastName}}_Resume_{{Role}}.md` and `{{LastName}}_Resume_{{Role}}.tex` (your finished resume).

### How to use this handbook

This handbook is designed to work in two contexts:

- **On your own (self-serve):** Read in order. Part 1 tells you where the resume stands, Part 2 names the fatal flaws, Part 3 shows what employers actually want right now, Part 4 walks through every rewrite with reasoning, Part 5 is your action checklist. The appendices stay useful every future time you update your resume — keep Appendix C (per-role resume checklist) and Appendix D (methodology reference) as long-term references.
- **Walked through by a coach:** Same content, but the coach surfaces tradeoffs in real time and tells you which appendix entries are worth memorizing. After the session, switch to self-serve mode to keep iterating.

Either way, this is yours to keep. Re-run the skill in 6 months when your experience updates or you target a different role — you'll get a fresh diagnosis and a fresh resume.

<!-- GENERATE:
A 1-line summary of how to read this handbook, calibrated to tier:
  - Tier 9–10: "Your resume is already in the 9/10 range. This handbook focuses on keyword fine-tuning and next-step strategy."
  - Tier 7–8: "Your resume is in the 7–8 range. This handbook surfaces the gap to top-tier resumes and focuses on differentiated positioning."
  - Tier 5–6: "Your resume is in the 5–6 range. This handbook rewrites it section by section and explains the methodology behind each change."
  - Tier 2–3: "Your resume is currently in the 2–3 range. The bottleneck is structural — this handbook first names what's wrong, then gives you concrete directions for building the experience you're missing."
-->

---

## Table of Contents

<!-- GENERATE:
Output ONLY the TOC entries for sections actually included in this
handbook. Skip entries for skipped sections. Always include
appendices A, B, C; include D unless it's been omitted.
-->

---

## Part 1: Resume Diagnosis

<!-- GENERATE:
Two short paragraphs (max ~250 words total).

Paragraph 1 — Tier rating:
  - State explicitly which tier the original resume falls into.
  - Give 2–3 concrete reasons drawn from THIS student's actual
    resume content. Quote specific bullets they wrote or specific
    gaps you saw.
  - Do NOT give a generic "lack of quantification" — point to the
    specific bullet.

Paragraph 2 — Bottleneck:
  - Structural (experience genuinely insufficient) or packaging
    (experience is there but poorly told)?
  - This determines what the rest of this handbook can and can't fix.

Length scales with tier:
  - 9–10: 2–3 sentences total — confirm tier and call out the
    one or two strengths driving it. No "bottleneck" framing
    needed; instead note "what to keep doing".
  - 7–8: full two paragraphs as described above.
  - 5–6: full two paragraphs.
  - 2–3: full two paragraphs + an extra sentence calling out
    that the rest of this handbook will be heavier on action
    items (Part 5) than on rewrites (Part 4).
-->

### Tier rubric (reference)

| Tier  | Interview funnel signal | Typical symptoms |
|-------|-------------------------|------------------|
| 2–3   | essentially zero        | Sparse content; won't clear ATS / AI screening; can't tell what you've done or what direction you're targeting |
| 5–6   | very low                | Content is complete but no quantified impact; can't tell complexity or ownership |
| 7–8   | moderate                | Quantified and clear, but indistinguishable from peer candidates |
| 9–10  | strong                  | Above + a **differentiated personal brand** — a recruiter remembers who you are within 30 seconds |

These are qualitative coaching heuristics, not measured outcomes — use as relative calibration, not predictive guarantees.

---

## Part 2: Fatal Flaws On Your Resume

<!-- GENERATE:
SKIP THIS PART ENTIRELY (omit the heading too) if no fatal flaws
apply to this student. This is the common case for 9–10 tier.

Otherwise, for each fatal flaw that applies (out of the 5 below),
output one subsection in the format:

  ### Fatal flaw N: [name]

  **Why it matters**

  [2–3 sentences explaining why this is an interview-killer.]

  **Current state on your resume**

  [Point to a specific bullet or section on the student's resume.
   Quote the original text verbatim (in English). Explain why it's
   an instance of this fatal flaw.]

  **How to fix**

  [Concrete fix direction. If Part 4 will show a Before/After
   rewrite, write "see Part 4 §4.x"; if it's a non-rewrite fix
   (like a timeline issue), give the specific action here.]

The 5 fatal flaws to check:
  1. Information density too low — describing the project's scope rather than your specific contribution
  2. No quantified impact — bullets have no Endorsement / Scope / Marketing dimension attached
  3. Keyword mismatch — < 75% coverage of the high-frequency JD terms
  4. No personal brand / no differentiator — reads like a generic "AI assistant who took orders"
  5. Timeline confusion / Experience demoted to Projects — overlapping roles hidden by structure rather than labeled

Only output flaws that genuinely apply. If a student only has 2
fatal flaws, output 2 subsections, not 5. Do NOT pad.

If 1–2 flaws apply, end with one short sentence noting which fatal
flaws do NOT apply (so they know what they're already doing right).
If this part is skipped entirely, do not add such a note here —
mention the strengths in Part 1 instead.
-->

> The full 5-flaw checklist with reasoning is in Appendix D.

---

## Part 3: Target JDs and Keyword Coverage

### The 3 JDs we sampled today

<!-- GENERATE:
For each of the 3 JDs pulled via web_search at Step 2, output:

  #### JD {{N}}: {{COMPANY}} — {{ROLE_TITLE}}
  - Source: {{URL}}
  - Company tier: Big Tech / mid-sized / startup (pick one)
  - Required keywords: [list 5–8 most important required skills/keywords]
  - Preferred keywords: [list 3–5]
  - Salary band (if disclosed): {{SALARY_RANGE_OR_NA}}

Three JDs total, mixed tiers when possible.
-->

### High-signal keywords (appearing in ≥ 2 JDs)

<!-- GENERATE:
A clean comma-separated list of high-signal keywords — those
appearing in 2 or more of the 3 JDs. These are the must-cover
keywords.
-->

### Coverage on your current resume

<!-- GENERATE:
A markdown table with two columns: Keyword | Present in resume (✓/✗).
List the high-signal keywords from above. End with the overall
percentage coverage rate (e.g. "Coverage: 11/15 = 73%").

If coverage is < 75%, flag it and list the 3–5 highest priority
keywords to add.

For 9–10 tier where coverage is already strong, just show the
table and a one-line confirmation. No extended commentary.
-->

### Coverage after rewrite

<!-- GENERATE:
Re-run the coverage check against the rewritten resume. Show the
new percentage and which keywords were closed.

If certain keywords were intentionally NOT added (no defensible
experience), call that out: "We did not force-add the X keyword
because you don't yet have relevant project experience — see
Part 5 action items for how to build it."

Skip this subsection if the resume wasn't rewritten this run
(e.g., 9–10 tier where only minor polish was applied).
-->

---

## Part 4: Your Resume Rewrites — Before / After

<!-- GENERATE:
SKIP THIS PART ENTIRELY (heading too) if no sections were rewritten
this run.

Otherwise, output ONE subsection per rewritten section. Common
rewrite targets: Summary, individual Experience roles, Skills.

For 9–10 tier: typically 0–2 subsections (light polish only).
For 7–8 tier: 2–4 subsections.
For 5–6 tier: 4–6 subsections.
For 2–3 tier: usually skip this part — rewriting weak material
doesn't make it strong, and the action items in Part 5 matter more.
At most output 1 representative subsection to demonstrate the
methodology, then redirect attention to Part 5.

Each subsection format:

  ### 4.{{N}} {{SECTION_LABEL}}
  (e.g. "4.1 Summary" / "4.2 Experience: Amazon Software Engineer")

  **Before**
  ```
  [Student's original verbatim text]
  ```

  **After**
  ```
  [Rewritten text]
  ```

  **What changed and why**

  | Change | Methodology reason |
  |--------|--------------------|
  | [specific change 1] | [principle reference] |
  | [specific change 2] | [principle reference] |
  | ... | ... |

The 'why' column must reference one of:
  - Specific methodology principles (verb tier, three-dimension impact, Summary formula, etc.)
  - Specific JD keywords being inserted to close coverage gap
  - Specific fatal flaw being fixed (reference Part 2 of this handbook)

Aim for 4–8 rows per change table. Don't list trivial wording polish
unless it changes meaning.
-->

---

## Part 5: Your Next Action Items

<!-- GENERATE:
A practical, prioritized list of next steps for THIS student.
Group into 4 buckets, only include buckets that apply.
Skip any bucket that has no items — do NOT pad.

  ### A. Verify the data
  - List every number in the rewritten resume currently marked
    [Needs verification].
  - For each, give a specific instruction:
    "Check GitHub commits / Slack history / internal dashboard /
     your manager's 1:1 notes..."
  - Must be done BEFORE submitting the resume.

  ### B. Close keyword gaps
  - List 2–3 highest-priority missing keywords from Part 3 that the
    student should be able to add by reframing existing experience.
  - For each, suggest specific bullet rewrites or which existing
    role can absorb the keyword.

  ### C. Build missing experience (only if there's a structural gap)
  - Only include this bucket if Part 1 diagnosed a structural gap.
  - For each recommended project / experience direction:
    - Project direction: [name]
    - Why (link to JD keyword or market gap): [reason]
    - Time investment estimate: [duration]
    - Sample bullet once completed (English):
      ```
      [Strong verb + what built + tech + outcome]
      ```
  - Reference current 2026 market signals — do NOT recommend stale
    project ideas. For AI roles in 2026: production RAG with eval,
    MCP-based multi-agent, vLLM perf benchmarking, eval harness —
    not "build a chatbot".

  ### D. Submission strategy
  - Sponsor status guidance (if the student mentioned visa status)
  - Submission timing window (mass apply vs. network-based for this direction)
  - Whether to prepare a backup-direction resume

For 9–10 tier students, this part often becomes shorter and pivots
toward career navigation: "Your resume is already through the gate;
next is sponsor-response strategy / referral timing / whether you
need a backup direction" rather than verify-data or keyword fill-in.

For 2–3 tier students, this part is the heaviest section of the
handbook — bucket C dominates, with concrete project recommendations
that map to current 2026 JD keywords.
-->

---

## Appendix A: Strong Verbs / Weak Verbs

### Strong verbs (good first word in a bullet)

**Leadership / drive:** Led, Drove, Spearheaded, Mentored, Managed, Owned, Established, Founded, Initiated, Authored, Pioneered, Championed.

**Delivery / execution:** Shipped, Launched, Delivered, Productionized, Released, Deployed, Rolled out, Migrated, Refactored, Architected, Engineered, Implemented, Built.

**Optimization / improvement:** Optimized, Reduced, Cut, Lifted, Boosted, Increased, Accelerated, Streamlined, Automated, Consolidated.

**Analysis / decision:** Diagnosed, Investigated, Identified, Evaluated, Benchmarked, Validated, Audited, Reconciled, Forecasted.

**Collaboration / negotiation:** Negotiated, Aligned, Coordinated, Orchestrated, Partnered, Influenced, Brokered.

### Neutral verbs (usable but easy to over-rely on)

Developed, Created, Improved, Designed, Implemented, Modernized, Completed, Updated, Built (lives between neutral and strong depending on context).

### Weak verbs (avoid)

Worked, Helped, Assisted, Used, Participated, Contributed to, Supported, Was responsible for, Was involved in, Took part in.

If a bullet's first word lands in the weak list, rewrite it.

### Adverb budget (≤ 5 across the whole resume)

Independently, Proactively, Successfully, End-to-end, Single-handedly, Personally, Directly.

Every use needs to earn its place — if a specific fact replaces the adverb, prefer the fact. Example: "Independently designed" → "Sole designer for" (the latter is a fact, the former is self-evaluation).

---

## Appendix B: High-Frequency Keywords for {{ROLE_DIRECTION}}

<!-- GENERATE:
Pick ONE of the following keyword sets that matches {{ROLE_DIRECTION}}
and output it verbatim under this heading. Drop the other sets.

If the student's direction crosses two areas (e.g. "AI Engineer +
Data Scientist"), output both sets under separate sub-subheadings.

If direction is none of the below (rare), generate a fresh keyword
set based on the JDs sampled in Part 3 of this handbook.

Available sets (in this template — pick the right one and copy
verbatim):
- AI Engineer / GenAI Engineer
- SDE / Backend / Fullstack
- Data Scientist (Product)
- Data Scientist (Quant / ML Modeling)
- Data Analyst
- Product Manager
- UX / UI Designer
- Marketing
- TPM (Technical Program Manager)
- ML Engineer
-->

> This is a snapshot of the 2026 market. Each time you update your resume, re-pull fresh JDs to validate keywords. The 3 JDs you sampled in Part 3 reflect the most current signal.

### AI Engineer / GenAI Engineer

**Core:** RAG, Hybrid retrieval, Reranking, ReAct agents, Tool calling, MCP, LangChain / LangGraph, OpenAI / Anthropic SDKs, Vector DB (Pinecone / Chroma / Weaviate / pgvector), Embeddings, BM25, RRF.

**Modeling / inference:** vLLM, Triton, PyTorch, HuggingFace Transformers, FlashAttention, PagedAttention, KV cache, GPTQ / AWQ quantization, QLoRA / PEFT, LoRA hot-swap, Multi-GPU.

**Evaluation / safety:** LLM-as-Judge, RAGAS, DeepEval, Prompt injection defense, Guardrails, Pydantic structured output, Eval harness.

**Engineering:** FastAPI, Python, gRPC, SSE, WebSockets, Redis, Kafka, Docker, Kubernetes, AWS Bedrock / SageMaker, Lambda.

### SDE / Backend / Fullstack

**Languages:** Java, Python, Go, TypeScript, Rust, C++, SQL.
**Backend:** Spring Boot, FastAPI, gRPC, REST, GraphQL, Microservices, Event-driven, Kafka, Redis, PostgreSQL, MongoDB, DynamoDB.
**Frontend:** React, Next.js, TypeScript, Redux / RTK, Tailwind, GraphQL, Web Workers, SSR / ISR.
**Cloud / Infra:** AWS (Lambda, S3, DynamoDB, CDK), Docker, Kubernetes, Terraform, CI/CD (GitHub Actions, Jenkins).
**System Design:** Caching, Sharding, Replication, Consistency, Circuit breaker, Backpressure, Distributed locking, Idempotency.

### Data Scientist (Product)

**Statistics & Causal:** A/B testing, Hypothesis testing, Confidence intervals, Multiple testing correction, Causal inference, Diff-in-diff, Synthetic control, Instrumental variables.
**Modeling:** Logistic regression, XGBoost, LightGBM, Time-series forecasting, Survival analysis, Recommendation systems, Embedding-based ranking.
**Tools:** Python (pandas, scikit-learn, statsmodels), R, SQL, Spark, Snowflake / BigQuery, Airflow / dbt, Tableau / Looker.
**Communication:** Stakeholder, Roadmap, Cross-functional, Insight, Decision, Trade-off.

### Data Scientist (Quant / ML Modeling)

**Math & Stats:** Bayesian inference, Stochastic processes, Optimization, Time-series, GARCH, Kalman filter.
**ML:** Deep learning, Reinforcement learning, Graph neural networks, Causal ML, Probabilistic programming.
**Engineering:** Python, C++, Rust, PyTorch, JAX, Numba, Distributed training (DDP, FSDP), MLflow, Feature store.

### Data Analyst

**Tools:** SQL, Python, Excel, Tableau, Looker, Power BI, dbt.
**Methods:** A/B testing, Cohort analysis, Funnel analysis, Retention curves, LTV / CAC, Forecasting.
**Domain:** Marketing analytics, Product analytics, Operations, Finance.

### Product Manager

**Methods:** Roadmap, OKR, North-star metrics, KPI, A/B testing, User research, GTM, PRD, Scrum / Agile.
**Skills:** Stakeholder management, Cross-functional, Trade-off, Prioritization, Storytelling.
**Tools:** Jira, Linear, Figma, Amplitude, Mixpanel, Looker, SQL, Notion.

### UX / UI Designer

**Methods:** User research, Heuristic evaluation, Usability testing, Information architecture, Wireframing, Prototyping, Design system.
**Tools:** Figma, FigJam, Sketch, Adobe XD, Zeplin, Maze, UserTesting.
**Crossover:** HTML / CSS, Tailwind, Accessibility (WCAG), React basics.

### Marketing

**Funnel:** CAC, LTV, ROAS, MQL, SQL (sales-qualified lead), Conversion rate, Retention.
**Channels:** SEO, SEM, Paid social, Lifecycle (email / push), Content, Influencer, Affiliate.
**Tools:** GA4, Mixpanel, Amplitude, HubSpot, Salesforce, Mailchimp, Segment.
**Methods:** GTM, Brand positioning, Persona, Attribution modeling, Multi-touch attribution, Incrementality testing.

### TPM (Technical Program Manager)

**Methods:** Roadmap, Risk register, Cross-team coordination, Dependency mapping, RAID log, OKR.
**Skills:** Stakeholder management, Executive communication, Trade-off, Escalation, Status reporting.
**Domain:** SDLC, Agile / Scrum, Release management, Incident management.

### ML Engineer

**Modeling:** PyTorch, TensorFlow, scikit-learn, XGBoost, LightGBM, Transformers.
**Infrastructure:** MLflow, Kubeflow, Airflow, Ray, Distributed training (DDP / FSDP / DeepSpeed), Feature store (Feast, Tecton), Model serving (TorchServe, Triton, vLLM, Ray Serve).
**MLOps:** CI/CD for ML, Data versioning (DVC), Experiment tracking, Drift detection, Online evaluation.
**Cloud:** AWS SageMaker / Bedrock, GCP Vertex AI, Azure ML.

---

## Appendix C: One-Resume-Per-Role Checklist

The next time you update your resume or target a new role, run through this checklist:

### JD prep (before you touch the resume)

- [ ] Pulled 3 target-direction JDs (one each from Big Tech / mid-sized / startup).
- [ ] Extracted Required + Preferred keyword lists.
- [ ] Marked the high-signal keywords (appearing in ≥ 2 JDs).
- [ ] Measured current keyword coverage → target ≥ 75%.
- [ ] Replaced any outdated tech-stack terms.

### Summary

- [ ] 1–2 lines, ~25–40 words.
- [ ] First sentence locates you — who you are, what you do, target direction.
- [ ] Includes at least one **verifiable anchor** (URL, number, authoritative endorsement).
- [ ] No empty adverbs (passionate, results-driven, motivated, etc.).

### Experience

- [ ] Every bullet starts with a strong verb.
- [ ] Every bullet mentions at least one concrete technology or named method.
- [ ] Every bullet attaches to at least one of Endorsement / Scope / Marketing.
- [ ] The resume has ≥ 5 specific numbers overall.
- [ ] Independently / Proactively / Successfully / End-to-end usage sums to ≤ 5.
- [ ] No bullets start with weak verbs (Worked / Helped / Assisted / Used / Participated).

### Timeline

- [ ] Reverse-chronological order, most recent at the top.
- [ ] Each role has a month-and-year start and end.
- [ ] Gaps > 3 months are accounted for.
- [ ] Concurrent roles are labeled clearly in the title line.
- [ ] No Experience demoted to Projects.

### Skills

- [ ] Categories ordered by target-JD priority.
- [ ] Each category lists specific product/library names, not vague terms.
- [ ] Removed irrelevant or outdated technologies.

### Education

- [ ] New grads: placed before Experience.
- [ ] 2+ YOE: placed near the bottom.
- [ ] GPA listed only when ≥ 3.5/4.0.
- [ ] Coursework listed only for new grads with directly relevant courses.

### Data validation

- [ ] Every number can be explained in 30 seconds (source clear).
- [ ] Un-defensible numbers are either marked `[Needs verification]` or removed.

### File output

- [ ] Filename includes name and target direction: `LastName_Resume_<Role>.pdf`.
- [ ] One page (unless 8+ YOE with strong signal to include).
- [ ] PDF exported in ATS-friendly format (no complex multi-column layout / no embedded icons / no encryption).
- [ ] Run through jobscan.co or a similar ATS-simulator and confirm parsed text matches the original.

---

<!-- GENERATE:
INCLUDE Appendix D by default. OMIT it (drop heading and all content)
only when the student is clearly senior+ AND has demonstrated
fluency with the methodology in this conversation already. In
that narrow case, end the handbook at Appendix C.
-->

## Appendix D: Full Methodology Reference

This is the standalone methodology — refer back to it the next time you iterate on a different role direction.

### D.1 The four-tier rubric

See the tier table at the top of Part 1. Core principle: **the tier you're stuck at determines what your next move is.**

- Stuck at 2–3: usually a **structural problem** (experience genuinely insufficient). Rewriting the resume won't fix it — build projects / get an internship.
- Stuck at 5–6: usually a **packaging problem** (no quantification). The whole resume needs a bullet-by-bullet rewrite with numbers.
- Stuck at 7–8: usually missing a **differentiated personal brand**. Rewrite the Summary; find the unique signal you're not surfacing.
- 9–10: maintain it. Each new direction, re-pull JDs and adjust keyword coverage.

### D.2 The five fatal flaws

1. **Information density too low — describing the project rather than your contribution.** Bullet describes "what the team did" rather than "what I did". If you replace "I" with anyone else's name and the bullet still reads true, it's wrong.
2. **No quantified impact — invisibility on Endorsement / Scope / Marketing.** Without numbers, the recruiter has no way to gauge complexity, ownership, or significance.
3. **Keyword mismatch — < 75% coverage of the target JD.** ATS rejects, and recruiter keyword scans miss you.
4. **No personal brand / no differentiator.** Summary is bland, the whole resume reads like a generic engineer who took orders. HM can't form an impression in 30 seconds.
5. **Timeline confusion / Experience demoted to Projects.** Using Projects to hide an overlap looks evasive — HMs spot this instantly.

### D.3 The three impact dimensions

Every bullet must attach to at least one of these:

| Dimension     | What it captures                              | Best fit         | Typical phrasing |
|---------------|-----------------------------------------------|------------------|------------------|
| Endorsement   | Who participated, who endorsed, who validated | Customer-facing / sales | "Co-led with Principal Engineer"; "Featured at re:Invent"; "Selected by VP-name to lead..." |
| Scope         | Project size, team size, span                 | Management / TPM  | "Tech-led an 8-engineer team"; "Coordinated 3 product surfaces and 5 dependent teams" |
| Marketing     | User count, revenue, cost, performance        | Engineering / product | "5M DAU"; "Lifted conversion by 7%"; "Reduced infra cost by $1.2M annually" |

Engineering bullets lean Marketing; management bullets lean Scope; customer/sales/PM bullets lean Endorsement.

### D.4 The seven rewrite moves

1. **Set section priority.** New grad: Education first. 2+ YOE: Experience first.
2. **Rewrite the Summary.** 1–2 lines, 25–40 words, anchored to a verifiable proof point.
3. **Rewrite every Experience bullet.** Formula: `[strong verb] + [what you did] + [key decision/tech] + [quantified outcome]`.
4. **Use strong verbs, throttle adverbs.** Replace weak openers; adverb budget ≤ 5 for the whole resume.
5. **Reorder Skills.** By target-JD priority, with specific product/library names, removing outdated tech.
6. **Resolve timelines and overlaps.** Don't hide — use clear title labels.
7. **Validate data.** Every number defensible in 30 seconds, otherwise revise down or remove.

### D.5 Submission and strategy

**One resume per role, with a primary + backup + generalist version.** Filename: `LastName_Resume_Role.pdf`.

**Sponsor question:** Big companies — answer honestly. Small companies — answer honestly (no matter how you answer, the outcome doesn't change; honesty saves both sides' time).

**Submission timing:**

- High-volume, broad-coverage roles (SDE / UX / DA / DS): mass-apply within 1 hour of JD posting, secure a referral within 24 hours.
- Niche, specialized roles: don't mass-apply; rely on network — former colleagues / alumni / domain communities first.
- Declining direction: probe quickly; if applications go nowhere across the board, switch lanes.

**Referrals:** attach a role-specific resume + clearly state target role / location / sponsor status. Don't blast generic messages.

### D.6 When experience genuinely isn't enough

**A structural bottleneck can't be packaged-around — you have to build experience.** Each direction has its own high-ROI 2026 project areas; if Part 5 of this handbook identified a structural gap, it already gave you direction-specific project recommendations and sample bullets.

Priority for building experience: **Deployed > Open source > Hackathon > Coursework project**. A deployed URL on a resume is the most lethal — HMs really do click through.

---

> This handbook was generated from the specific resume you submitted this run, against the JD signal observable on {{DATE}}.
> When your experience updates or the market shifts (6 months from now is a reasonable trigger), run the skill again for a fresh diagnosis and a fresh resume.
