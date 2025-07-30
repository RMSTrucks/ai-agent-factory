# AI Agent Factory – Pipeline Overview

A repeatable 5-step assembly line that turns a messy business problem into a production-grade, self-improving AI teammate in ≤ 48 hours.

---

## 1 Pipeline at a Glance

| Step | Goal | Primary Processor | Typical Time-box | Quality Gate |
|------|------|------------------|------------------|--------------|
| 1 Translate | Convert raw narrative into a structured design prompt | **Translator AI** | 2 h | Prompt completeness checklist |
| 2 Design | Produce architecture spec | **o3-pro** | 4 h | Human insight review & predicted rubric ≥ 70 |
| 3 Build | Generate working code, tests, CI | **Replit AI Agent** | 24 h | All automated tests green |
| 4 Analyse | Measure performance vs rubric | **Domain Agent** | 4 h | Rubric ≥ 80 & detection accuracy ≥ 90 % |
| 5 Iterate | Capture & resolve feedback | **Feedback System** | 2 h | Priority ≥ 80 items < 10 open |

_Total cycle target: **≤ 48 h**._

---

## 2 Detailed Step Breakdown

### Step 1 · Problem Translation
* **Input:** `problem_narrative.txt`
* **Process:** Translator AI drafts `*-o3-design.md`, assumes zero domain knowledge, lists unknowns.
* **Output:** Design prompt ready for o3-pro.
* **Gate:** 12-point completeness checklist.

### Step 2 · Architecture Design
* **Input:** Design prompt.
* **Process:** o3-pro creates folder layout, modules, schemas, UI wireframe.
* **Patch Loop:** Human/Translator inject insights (e.g. detective onboarding) –> `*-replit-spec-PATCHED.md`.
* **Output:** Implementation spec.
* **Gate:** Insight review, predicted rubric ≥ 70.

### Step 3 · Implementation Build
* **Input:** Patched spec.
* **Process:** Replit AI Agent scaffolds code, writes tests, sets up CI, shows visual preview, then full build.
* **Artifacts:** Running service, `/diagnostics/*.json`, test reports.
* **Gate:** All unit/integration/E2E tests pass; p95 latency ≤ 1.5 s; zero blocking errors.

### Step 4 · Performance Analysis
* **Input:** Live agent instance.
* **Process:** Domain agent runs scripted scenarios, evaluates rubric, logs metrics.
* **Output:** `live-testing-results.md`, updated rubric scores.
* **Gate:** Rubric ≥ 80; no rubric sub-category < 70; detection accuracy ≥ 90 %.

### Step 5 · Iteration & Feedback
* **Input:** Open feedback items and diagnostics gaps.
* **Process:** Feedback System ingests manual + auto-triggered entries, scores priority, surfaces to pipeline.
* **Output:** Prioritised feedback DB, new backlog tasks, analytics trend.
* **Gate:** All priority ≥ 80 items triaged within 24 h; open count < 10.

---

## 3 AI Participants & Roles

| Participant | Role | Key Actions |
|-------------|------|-------------|
| **Translator AI** | Problem interpreter | Draft prompt, patch specs, embed feedback |
| **o3-pro** | Architect | Generate technical design, accept deltas |
| **Replit AI Agent** | Engineer | Build code, tests, CI, fix feedback tasks |
| **Domain Agent** (e.g. Marketing) | Operative | Chat, teach, run experiments, emit diagnostics & auto-feedback |
| **Feedback System** | Orchestrator | Store feedback, compute priority, export snapshot |

---

## 4 Input / Output Specifications

| Step | Input Object | Output Artifact |
|------|--------------|-----------------|
| 1 | `problem_narrative.txt` | `*-o3-design.md` |
| 2 | Design prompt | `*-replit-spec-PATCHED.md` |
| 3 | Patched spec | Running web-app + diagnostics JSON |
| 4 | Running app | `live-testing-results.md`, updated rubric |
| 5 | Diagnostics + feedback POSTs | Prioritised feedback DB, backlog tasks |

---

## 5 Quality Gates & Validation Checklist

1. **Prompt Completeness (Step 1)** – problem, partnership, teaching, diagnostics sections present.  
2. **Insight Review (Step 2)** – detective layer included; assumptions audited.  
3. **Automated Test Suite (Step 3)** – unit ≥ 70 % coverage; integration + E2E all green.  
4. **Rubric Evaluation (Step 4)** – total ≥ 80, no category < 70.  
5. **Feedback Closure (Step 5)** – priority ≥ 80 items resolved or in progress.

---

## 6 Adapting the Pipeline to New Domains

1. **Swap the Problem Narrative** – write a new Step-1 prompt using the template in `prompts/`.  
2. **Extend Taxonomies** – add domain categories to `ProblemDetector`.  
3. **Update Teaching Content** – supply framework examples relevant to the new domain.  
4. **Adjust Diagnostics Schema** – include domain-specific KPIs.  
5. **Refresh Test Fixtures** – craft new E2E scenarios; regression harness re-runs automatically.

With shared modules reused, a new domain agent typically scores ≥ 85/100 on its first build.

---

## 7 Timeline Expectations

```
0-2 h   : Step 1 prompt drafted
2-6 h   : Step 2 design + patch
6-30 h  : Step 3 build, tests, CI
30-34 h : Step 4 analysis
34-36 h : Step 5 feedback triage
```
Buffer (12 h) reserved for contingencies → **Total ≤ 48 h**.

---

## 8 Success Metrics per Step

| Step | Metric | Target |
|------|--------|--------|
| 1 | Prompt completeness | 100 % |
| 2 | Predicted rubric | ≥ 70 |
| 3 | Test suite pass | 100 % |
| 4 | Actual rubric | ≥ 80 |
| 5 | Critical feedback open | < 10 |
| All | Cycle time | ≤ 48 h |

---

**Follow this pipeline to create partnership-grade AI agents rapidly, with continuous learning built in.**
