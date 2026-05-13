<!--
================================================================
HANDBOOK TEMPLATE  (per-run output of the resume-writing skill)
================================================================
This file is a TEMPLATE, not a finished document. Each run of the
skill produces a personalized handbook for ONE student by:
  1. Replacing every {{PLACEHOLDER}} with student-specific data
  2. Replacing every <!-- GENERATE: ... --> block with freshly
     generated content following the embedded instructions
  3. Keeping all STATIC sections (附录 A / C / D) verbatim
  4. Customizing 附录 B based on the student's role direction

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
| 7–8   | full diagnosis + 差异化 gap | 1–2 flaws        | always include | 2–4 sections         | balanced              | full       |
| 5–6   | full diagnosis              | 3–4 flaws        | always include | 4–6 sections         | strong on data verify + keyword补强 | full       |
| 2–3   | full + structural diagnosis | 4–5 flaws        | full but reframed (current resume can't realistically clear ATS) | thin or skipped — rewriting won't fix structural gap | dominated by 经验补强 recommendations | full       |

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

Audience: the student. Tone: peer-professional Mandarin, direct.
Resume content stays in English. No internal references to
"course" / "1:1" / "your coach". Stand-alone document.
================================================================
-->

# {{STUDENT_NAME}} 的简历改写讲义（{{ROLE_DIRECTION}} 方向）

> 这份讲义基于你 {{DATE}} 提交的简历生成，结合了今天抓取的 3 份美国市场 {{ROLE_DIRECTION}} 岗位 JD。
> 配套文件：`{{LastName}}_Resume_{{Role}}.md` 和 `{{LastName}}_Resume_{{Role}}.tex`（你最终的简历）。

<!-- GENERATE:
A 1-line summary of how to read this handbook, calibrated to tier:
  - Tier 9–10: "你的简历已经在 9/10 区间。这份讲义重点是 keyword 微调和下一步策略。"
  - Tier 7–8: "你的简历在 7–8 区间。这份讲义会指出和顶档简历的差距，重点是差异化人设。"
  - Tier 5–6: "你的简历在 5–6 区间。这份讲义会逐 section 改写并解释每一步原理。"
  - Tier 2–3: "你的简历目前在 2–3 区间，瓶颈是结构性的。这份讲义会先讲清楚问题在哪，再给出补经验的具体方向。"
-->

---

## 目录

<!-- GENERATE:
Output ONLY the TOC entries for sections actually included in this
handbook. Skip entries for skipped sections. Always include
appendices A, B, C; include D unless it's been omitted.
-->

---

## 第一部分：你的简历诊断

<!-- GENERATE:
Two short paragraphs (max ~250 字 total).

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

### Tier 评级的判断标准（参考）

| 分数  | 面试转化率 | 典型特征 |
|-------|-----------|----------|
| 2–3 分 | ≈ 0%      | 内容稀薄；过不了 AI 初筛；看不出做过什么、要找什么方向 |
| 5–6 分 | < 5%      | 内容齐全但没有量化数据；看不出复杂度和影响力 |
| 7–8 分 | ≈ 10%     | 量化清晰、能力可见；但和同类候选人差异不明显 |
| 9–10 分 | ≈ 20%    | 在 7–8 分基础上具备**差异化人设**——HR 在 30 秒内就能记住你是谁 |

---

## 第二部分：你简历上的致命问题

<!-- GENERATE:
SKIP THIS PART ENTIRELY (omit the heading too) if no fatal flaws
apply to this student. This is the common case for 9–10 tier.

Otherwise, for each fatal flaw that applies (out of the 5 below),
output one subsection in the format:

  ### 致命问题 N: [问题名]

  **为什么重要**

  [2–3 句话解释这个问题为什么是面试杀手。]

  **你简历上的现状**

  [指向 student 简历里具体的 bullet 或段落。Quote the original text
   verbatim (in English). 解释 why it's an instance of this fatal flaw.]

  **怎么改**

  [具体的修复方向。如果第四部分会展示 Before/After 改写，这里可以
   说"详见第四部分 4.x"; 如果是不会改写的部分（比如时间线问题），
   这里直接给具体动作。]

The 5 fatal flaws to check:
  1. 信息密度太低，描述项目而非自己的部分
  2. 没有量化数据，影响力不可见（Endorsement / Scope / Marketing 三维都缺）
  3. 关键词不匹配目标 JD（< 75% 覆盖率）
  4. 看不出人设、没有亮点（Summary 平淡 / 整体读起来像 AI 机器人）
  5. 时间线混乱 / 经验降级为项目（用 Project 隐藏 Experience）

Only output flaws that genuinely apply. If a student only has 2
fatal flaws, output 2 subsections, not 5. Do NOT pad.

If 1–2 flaws apply, end with one short sentence noting which fatal
flaws do NOT apply (so they know what they're already doing right).
If this part is skipped entirely, do not add such a note here —
mention the strengths in Part 1 instead.
-->

> 5 大致命问题的完整清单与原理，参见附录 D。

---

## 第三部分：目标 JD 与关键词覆盖率

### 我们今天抓的 3 份 JD

<!-- GENERATE:
For each of the 3 JDs pulled via web_search at Step 2, output:

  #### JD {{N}}: {{COMPANY}} — {{ROLE_TITLE}}
  - 来源: {{URL}}
  - 公司层级: Big Tech / 中型 / 创业（标一个）
  - 关键 Required: [list 5–8 most important required skills/keywords]
  - 关键 Preferred: [list 3–5]
  - 薪资带（如披露）: {{SALARY_RANGE_OR_NA}}

Three JDs total, mixed tiers when possible.
-->

### 高信号关键词（≥ 2 份 JD 中出现）

<!-- GENERATE:
A clean comma-separated list of high-signal keywords — those
appearing in 2 or more of the 3 JDs. These are the must-cover
keywords.
-->

### 你当前简历的覆盖率

<!-- GENERATE:
A markdown table with two columns: 关键词 | 是否在简历中出现 (✓/✗).
List the high-signal keywords from above. End with the overall
percentage coverage rate (e.g. "覆盖率: 11/15 = 73%").

If coverage is < 75%, flag it and list the 3–5 highest priority
keywords to add.

For 9–10 tier where coverage is already strong, just show the
table and a one-line confirmation. No extended commentary.
-->

### 改写后的覆盖率

<!-- GENERATE:
Re-run the coverage check against the rewritten resume. Show the
new percentage and which keywords were closed.

If certain keywords were intentionally NOT added (no defensible
experience), call that out: "我们没有强行添加 X 关键词因为你目前
没有相关项目经验; 见第五部分 action items 关于补这块经验的建议."

Skip this subsection if the resume wasn't rewritten this run
(e.g., 9–10 tier where only minor polish was applied).
-->

---

## 第四部分：你的简历改写 Before / After

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

  **改了什么、为什么这样改**

  | 改动 | 方法论 reason |
  |------|--------------|
  | [具体改动 1] | [原理引用] |
  | [具体改动 2] | [原理] |
  | ... | ... |

The 'why' column must reference one of:
  - Specific methodology principles (verb tier, 三维量化, Summary 公式 etc.)
  - Specific JD keywords being inserted to close coverage gap
  - Specific fatal flaw being fixed (reference Part 2 of this handbook)

Aim for 4–8 rows per change table. Don't list trivial wording polish
unless it changes meaning.
-->

---

## 第五部分：你的下一步 action items

<!-- GENERATE:
A practical, prioritized list of next steps for THIS student.
Group into 4 buckets, only include buckets that apply.
Skip any bucket that has no items — do NOT pad.

  ### A. 数据 verify
  - List every number in the rewritten resume that is currently
    marked [Needs verification].
  - For each, give a specific instruction:
    "去查 GitHub commit / Slack 记录 / 内部 dashboard / 老板的 1:1 笔记..."
  - Must be done BEFORE submitting the resume.

  ### B. 关键词补强
  - List 2–3 highest-priority missing keywords from Part 3 that the
    student should be able to add by reframing existing experience.
  - For each, suggest specific bullet rewrites or which existing
    role can absorb the keyword.

  ### C. 经验补强（structural gap 才需要）
  - Only include this bucket if Part 1 diagnosed a structural gap.
  - For each recommended project / experience direction:
    - 项目方向: [name]
    - 为什么 (link to JD keyword or market gap): [reason]
    - 时间投入估算: [duration]
    - 完成后的 sample bullet (English):
      ```
      [Strong verb + what built + tech + outcome]
      ```
  - Reference current 2026 market signals — do NOT recommend stale
    project ideas. For AI roles in 2026: production RAG with eval,
    MCP-based multi-agent, vLLM perf benchmarking, eval harness,
    not "build a chatbot".

  ### D. 投递相关
  - Sponsor 状态填写建议（如学生提到自己的 visa 状况）
  - 投递时间窗口（这个方向是海投还是 network）
  - 是否需要再准备 backup 方向的简历

For 9–10 tier students, this part often becomes shorter and pivots
toward career navigation: "你简历已经过关，下一步是 sponsor 答复
策略 / 内推 timing / 是否需要 backup 方向" rather than verify-data
or 关键词补强.

For 2–3 tier students, this part is the heaviest section of the
handbook — bucket C dominates, with concrete project recommendations
that map to current 2026 JD keywords.
-->

---

## 附录 A：强动词 / 弱动词词库

### 强动词（适合作为 bullet 的第一个词）

**领导 / 推动类：** Led, Drove, Spearheaded, Mentored, Managed, Owned, Established, Founded, Initiated, Authored, Pioneered, Championed.

**交付 / 执行类：** Shipped, Launched, Delivered, Productionized, Released, Deployed, Rolled out, Migrated, Refactored, Architected, Engineered, Implemented, Built.

**优化 / 改进类：** Optimized, Reduced, Cut, Lifted, Boosted, Increased, Accelerated, Streamlined, Automated, Consolidated.

**分析 / 决策类：** Diagnosed, Investigated, Identified, Evaluated, Benchmarked, Validated, Audited, Reconciled, Forecasted.

**协作 / 谈判类：** Negotiated, Aligned, Coordinated, Orchestrated, Partnered, Influenced, Brokered.

### 中性动词（能用，但少用——容易"灰化"）

Developed, Created, Improved, Designed, Implemented, Modernized, Completed, Updated, Built（在中性偏强之间，看上下文）。

### 弱动词（避免）

Worked, Helped, Assisted, Used, Participated, Contributed to, Supported, Was responsible for, Was involved in, Took part in.

每条 bullet 第一个词如果落在弱动词列表里，重写。

### 副词配额（整份简历 ≤ 5 个）

Independently, Proactively, Successfully, End-to-end, Single-handedly, Personally, Directly.

每个用一次都要值——能换成具体事实就换。例如 "Independently designed" 改成 "Sole designer for"——后者是事实，前者是评价。

---

## 附录 B：{{ROLE_DIRECTION}} 高频关键词速查

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

> 这是 2026 年初市场的快照，每次改简历前请重新抓最新 JD 验证关键词。第三部分中你这次抓的 3 份 JD 反映的是更新的市场信号。

### AI Engineer / GenAI Engineer

**核心：** RAG, Hybrid retrieval, Reranking, ReAct agents, Tool calling, MCP, LangChain / LangGraph, OpenAI / Anthropic SDKs, Vector DB (Pinecone / Chroma / Weaviate / pgvector), Embeddings, BM25, RRF.

**模型 / 推理：** vLLM, Triton, PyTorch, HuggingFace Transformers, FlashAttention, PagedAttention, KV cache, GPTQ / AWQ quantization, QLoRA / PEFT, LoRA hot-swap, Multi-GPU.

**评估 / 安全：** LLM-as-Judge, RAGAS, DeepEval, Prompt injection defense, Guardrails, Pydantic structured output, Eval harness.

**工程：** FastAPI, Python, gRPC, SSE, WebSockets, Redis, Kafka, Docker, Kubernetes, AWS Bedrock / SageMaker, Lambda.

### SDE / Backend / Fullstack

**Languages：** Java, Python, Go, TypeScript, Rust, C++, SQL.
**Backend：** Spring Boot, FastAPI, gRPC, REST, GraphQL, Microservices, Event-driven, Kafka, Redis, PostgreSQL, MongoDB, DynamoDB.
**Frontend：** React, Next.js, TypeScript, Redux / RTK, Tailwind, GraphQL, Web Workers, SSR / ISR.
**Cloud / Infra：** AWS (Lambda, S3, DynamoDB, CDK), Docker, Kubernetes, Terraform, CI/CD (GitHub Actions, Jenkins).
**System Design：** Caching, Sharding, Replication, Consistency, Circuit breaker, Backpressure, Distributed locking, Idempotency.

### Data Scientist (Product)

**Statistics & Causal：** A/B testing, Hypothesis testing, Confidence intervals, Multiple testing correction, Causal inference, Diff-in-diff, Synthetic control, Instrumental variables.
**Modeling：** Logistic regression, XGBoost, LightGBM, Time-series forecasting, Survival analysis, Recommendation systems, Embedding-based ranking.
**Tools：** Python (pandas, scikit-learn, statsmodels), R, SQL, Spark, Snowflake / BigQuery, Airflow / dbt, Tableau / Looker.
**Communication：** Stakeholder, Roadmap, Cross-functional, Insight, Decision, Trade-off.

### Data Scientist (Quant / ML Modeling)

**Math & Stats：** Bayesian inference, Stochastic processes, Optimization, Time-series, GARCH, Kalman filter.
**ML：** Deep learning, Reinforcement learning, Graph neural networks, Causal ML, Probabilistic programming.
**Engineering：** Python, C++, Rust, PyTorch, JAX, Numba, Distributed training (DDP, FSDP), MLflow, Feature store.

### Data Analyst

**Tools：** SQL, Python, Excel, Tableau, Looker, Power BI, dbt.
**Methods：** A/B testing, Cohort analysis, Funnel analysis, Retention curves, LTV / CAC, Forecasting.
**Domain：** Marketing analytics, Product analytics, Operations, Finance.

### Product Manager

**Methods：** Roadmap, OKR, North-star metrics, KPI, A/B testing, User research, GTM, PRD, Scrum / Agile.
**Skills：** Stakeholder management, Cross-functional, Trade-off, Prioritization, Storytelling.
**Tools：** Jira, Linear, Figma, Amplitude, Mixpanel, Looker, SQL, Notion.

### UX / UI Designer

**Methods：** User research, Heuristic evaluation, Usability testing, Information architecture, Wireframing, Prototyping, Design system.
**Tools：** Figma, FigJam, Sketch, Adobe XD, Zeplin, Maze, UserTesting.
**Crossover：** HTML / CSS, Tailwind, Accessibility (WCAG), React basics.

### Marketing

**Funnel：** CAC, LTV, ROAS, MQL, SQL (sales-qualified lead), Conversion rate, Retention.
**Channels：** SEO, SEM, Paid social, Lifecycle (email / push), Content, Influencer, Affiliate.
**Tools：** GA4, Mixpanel, Amplitude, HubSpot, Salesforce, Mailchimp, Segment.
**Methods：** GTM, Brand positioning, Persona, Attribution modeling, Multi-touch attribution, Incrementality testing.

### TPM (Technical Program Manager)

**Methods：** Roadmap, Risk register, Cross-team coordination, Dependency mapping, RAID log, OKR.
**Skills：** Stakeholder management, Executive communication, Trade-off, Escalation, Status reporting.
**Domain：** SDLC, Agile / Scrum, Release management, Incident management.

### ML Engineer

**Modeling：** PyTorch, TensorFlow, scikit-learn, XGBoost, LightGBM, Transformers.
**Infrastructure：** MLflow, Kubeflow, Airflow, Ray, Distributed training (DDP / FSDP / DeepSpeed), Feature store (Feast, Tecton), Model serving (TorchServe, Triton, vLLM, Ray Serve).
**MLOps：** CI/CD for ML, Data versioning (DVC), Experiment tracking, Drift detection, Online evaluation.
**Cloud：** AWS SageMaker / Bedrock, GCP Vertex AI, Azure ML.

---

## 附录 C：一岗一简历 checklist

下次自己改简历或者投递新岗位时，对照这个 checklist 自查：

### 抓 JD（动笔前）

- [ ] 抓了 3 份目标方向 JD（Big Tech / 中型 / 创业公司各一份）。
- [ ] 提取了 Required + Preferred 两个段落的关键词。
- [ ] 标出了在 ≥ 2 份 JD 同时出现的高信号关键词。
- [ ] 检查了简历当前关键词覆盖率 → 目标 ≥ 75%。
- [ ] 替换了过时技术栈词。

### Summary

- [ ] 1–2 行，~ 25–40 字。
- [ ] 第一句直接定位——你是谁、做什么、目标方向。
- [ ] 包含至少一个**可验证锚点**（URL、数字、权威背书）。
- [ ] 没有空话副词（passionate, results-driven, motivated 等）。

### Experience

- [ ] 每条 bullet 第一个词是强动词。
- [ ] 每条 bullet 提到至少一个具体技术词或方法名。
- [ ] 每条 bullet 挂在 Endorsement / Scope / Marketing 三个维度的至少一个上。
- [ ] 整份简历 ≥ 5 个具体数字。
- [ ] Independently / Proactively / Successfully / End-to-end 加起来 ≤ 5 个。
- [ ] 没有 Worked / Helped / Assisted / Used / Participated 这类弱动词作为开头。

### 时间线

- [ ] 倒序排列，最新在上面。
- [ ] 每段都有 月+年 起止时间。
- [ ] Gap > 3 个月的时段有合理说明。
- [ ] 重叠期用清晰 title 标签。
- [ ] 没有把 Experience 降级为 Project。

### Skills

- [ ] 类别按目标 JD 优先级排序。
- [ ] 每个类别下是具体的产品/库名，不是模糊词。
- [ ] 删掉了和目标岗位无关的、过时的技术。

### Education

- [ ] 新毕业生放在 Experience 之前。
- [ ] 2+ YOE 放在简历后部。
- [ ] GPA 仅在 ≥ 3.5/4.0 时列出。
- [ ] Coursework 仅新毕业生且课程直接相关时列出。

### 数据校验

- [ ] 每个数字都能在 30 秒内说清楚来源。
- [ ] 不能 defend 的数字标了 [Needs verification] 或者删掉了。

### 文件输出

- [ ] 文件名清楚标明姓名和方向：`LastName_Resume_<Role>.pdf`。
- [ ] 一页（除非 8+ YOE 且有强信号要塞）。
- [ ] PDF 用 ATS-friendly 格式导出（不要复杂多栏 / 不要嵌入图标 / 不要加密）。
- [ ] 自己用 jobscan.co 或类似 ATS 模拟工具跑一次，看解析后是不是和原文一致。

---

<!-- GENERATE:
INCLUDE 附录 D by default. OMIT it (drop heading and all content)
only when the student is clearly senior+ AND has demonstrated
fluency with the methodology in this conversation already. In
that narrow case, end the handbook at 附录 C.
-->

## 附录 D：方法论完整参考

这一部分是这套方法论的总结——之后你自己改其他方向的简历时回头看这一节。

### D.1 简历四档分级

参见第一部分开头的 tier 表。核心判断：**你卡在哪一档，决定了你下一步该做什么**。

- 卡在 2–3 分：通常是**结构性问题**（经验本身不够），死磕简历无效，要去补项目 / 实习。
- 卡在 5–6 分：通常是**包装问题**（没有量化），整份简历需要重写每条 bullet 加数字。
- 卡在 7–8 分：通常缺**差异化人设**，要重写 Summary，挖掘自己的独特信号。
- 9–10 分：保持，每次新方向重新抓 JD 调整关键词覆盖。

### D.2 5 大致命问题

1. **信息密度太低，描述项目而非自己的部分** — bullet 写"团队做了什么"而不是"我做了什么"，把"我"换成任何人都成立。
2. **没有量化数据，影响力不可见** — 缺少 Endorsement / Scope / Marketing 三维。
3. **关键词不匹配目标 JD** — 覆盖率 < 75%，过不了 ATS / HR 关键词搜索。
4. **看不出人设、没有亮点** — Summary 平淡，整体读起来像一个被分配任务的 AI 机器人。
5. **时间线混乱 / 经验降级为项目** — 用 Project 隐藏 Experience，HM 一眼看出。

### D.3 影响力的三个维度

每条 bullet 至少要挂在下面三个维度的**一个**上：

| 维度          | 内涵                         | 适合的角色         | 典型表达 |
|---------------|------------------------------|-------------------|---------|
| Endorsement   | 谁参与了、谁背书了、谁认可了 | 客户向 / 销售向    | "Co-led with Principal Engineer"; "Featured at re:Invent"; "Selected by VP-name to lead..." |
| Scope         | 项目规模、团队大小、跨度     | 管理向 / TPM       | "Tech-led an 8-engineer team"; "Coordinated 3 product surfaces and 5 dependent teams" |
| Marketing     | 用户量、收入、成本、性能指标 | 工程向 / 产品向    | "5M DAU"; "Lifted conversion by 7%"; "Reduced infra cost by $1.2M annually" |

工程岗 bullet 偏 Marketing；管理岗偏 Scope；客户/销售/PM 偏 Endorsement。

### D.4 改写七个动作

1. **定 section 优先级** — 新毕业生 Education 在前；2+ YOE Experience 在前。
2. **改写 Summary** — 1–2 行 25–40 字，包含可验证锚点。
3. **改写每条 Experience bullet** — `[强动词] + [具体做的事] + [关键决策/技术] + [量化结果]`。
4. **用强动词，控制副词** — 弱动词重写；副词配额 ≤ 5。
5. **Skills 重排** — 按目标 JD 优先级排序，类别名专业，删过时词。
6. **处理时间线和重叠** — 不靠隐藏，用清晰 title 标签。
7. **数据校验** — 每个数字能 30 秒内说清来源，否则改保守值或删除。

### D.5 投递与策略

**一岗一简历，主推 + 备选 + 泛化**。文件名 `LastName_Resume_Role.pdf`。

**Sponsor 回答**：大公司诚实回答，小公司诚实回答（无论怎么答结局都不变），节省双方时间。

**投递时间窗口**：

- 职位多、覆盖面广（SDE / UX / DA / DS）：海投，JD post 1 小时内投递，24 小时内争取内推。
- 职位少、专业性强：不海投，靠 network，前同事 / 校友 / 领域社群优先。
- 夕阳方向：快速试水，普遍石沉大海就尽快换赛道。

**内推**：附针对性简历 + 写清楚目标 role / location / sponsor 状态，不要群发。

### D.6 经验真的不够怎么办

**结构性瓶颈死磕简历无效，得去补经验。** 每个方向有自己的 2026 高 ROI 项目方向；本讲义第五部分如果识别到 structural gap，会给出针对你目标方向的具体推荐项目和完成后的 sample bullet。

补项目优先级：**Deployed > Open source > Hackathon > 课程 project**。简历上能放 deployed URL 的项目最有杀伤力——HM 真的会去点。

---

> 这份讲义是基于你这次提交的简历生成的，反映了你当时简历的具体状态和当时的市场 JD 信号。
> 半年后你的经验有更新、市场有变化时，重新跑一次 skill 会得到新的诊断和新的简历版本。
