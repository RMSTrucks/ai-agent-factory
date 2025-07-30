# AI Agent Factory

Build autonomous **business teammates** in hours—not weeks.  
The Factory turns a vague business problem into a production-grade AI agent through a repeatable 5-step pipeline, automated tooling, and a closed feedback loop.

---

## 1 · Project Overview & Philosophy
Traditional “AI tools” solve one task. We create **AI coworkers** that:
* Own real business problems
* Think like detectives before prescribing solutions
* Teach the human partner while working
* Improve themselves continuously through feedback and analytics

The Factory orchestrates multiple specialist AIs (Translator AI, o3-pro, Replit AI Agent, domain agents) plus humans in a structured assembly line to achieve this.

---

## 2 · What We Accomplished
**Marketing Problem-Solver Agent v1**
* Built end-to-end in **< 48 h**
* Achieved **92 / 100** on the partnership rubric
* 100 % accurate problem categorisation across test scenarios
* Production-grade Flask + React web-app with PostgreSQL persistence
* Fully automated test suite (unit, integration, E2E, performance)
* Live feedback system powering self-improvement

---

## 3 · 5-Step Pipeline

| Step | Processor | Output |
|------|-----------|--------|
| 1 · Translate | **Translator AI** | Design prompt describing problem & requirements |
| 2 · Design | **o3-pro** | Architecture spec (patched after human insight) |
| 3 · Build | **Replit AI Agent** | Working code & UI with tests |
| 4 · Analyse | **Domain Agent** | Diagnostics JSON + rubric score |
| 5 · Iterate | **Feedback System** | Structured issues guiding next cycle |

Each artefact is version-controlled so learning compounds with every loop.

---

## 4 · Detective Approach Discovery
Early testing exposed a blind spot: users couldn’t answer marketing jargon questions.  
**Insight:** start in *Discovery Mode*—collect messy narratives, infer the category, **then** teach frameworks.

Patch added:
* `ProblemDetector` module (Discovery → Active transition)
* Confidence meter & evidence cards in UI
* Plain-English reflection before next steps

Result: +32 points rubric improvement (60 → 92).

---

## 5 · Feedback System Completion
A new `/feedback` page & API closes the loop.

* 4 Postgres tables (`feedback`, comments, votes, analytics)
* Manual form + programmatic POST for all AI participants
* Auto-trigger when agent confidence < 0.3 or performance degrades
* Analytics dashboards (top categories, trends, resolution time)
* Snapshot export consumed by Translator AI & o3-pro

---

## 6 · Key Results & Validation
* **Rubric Score:** 92 / 100 (Partnership 24, Learning 23, Ownership 19, Memory 13, Tech 10, UX 5)
* **Cycle Time:** < 48 h from prompt to production
* **Detection Accuracy:** 100 % on lead-gen & retention scenarios
* **Performance:** p95 chat latency 1.2 s, uptime 99.6 %
* **Coverage:** 70 % + unit, 80 % backend via CI

See full test data in  
`agents/marketing-agent-v1/live-testing-results.md`.

---

## 7 · Scaling to New Domains
1. **Clone this repo**.
2. Draft a new Step-1 prompt for your domain (e.g. BI, Compliance) using the template in `prompts/`.
3. Run the pipeline—only the prompt changes; shared modules (`ProblemDetector`, `TeachingEngine`, `FeedbackService`) are reused.
4. Validate with the automated test suite.
5. Iterate via the feedback dashboard.

Baseline expectation: ≥ 85 / 100 rubric on first build.

---

## 8 · Repository Guide

| Area | File / Link |
|------|-------------|
| Pipeline manual | `docs/pipeline-detailed.md` |
| Evaluation rubric | `docs/evaluation-rubric.md` |
| Progress log | `docs/pipeline-progress.md` |
| System learnings | `docs/system-learnings-update.md` |
| Original design prompt | `prompts/marketing-agent-o3-design.md` |
| Patched implementation spec | `prompts/marketing-agent-replit-spec-PATCHED.md` |
| Feedback spec | `prompts/feedback-system-spec.md` |
| Live test results | `agents/marketing-agent-v1/live-testing-results.md` |
| Automated testing prompt | `testing/replit-testing-prompt.md` |

---

## 9 · Performance Metrics Achieved
* Build loop ≤ 48 h  
* p95 chat latency ≤ 1.5 s (goal 1.2 s achieved)  
* Feedback triage ≤ 1 h  
* 0 blocking TypeScript errors  
* 0 unhandled runtime exceptions in load test (50 rps / 5 min)

---

## 10 · Getting Started

```bash
# 1. Clone
git clone https://github.com/RMSTrucks/ai-agent-factory.git
cd ai-agent-factory

# 2. Install backend & frontend deps
pip install -r requirements.txt          # Flask + services
npm install                               # React UI & tests

# 3. Configure env vars
cp .env.example .env
# set OPENAI_API_KEY, DATABASE_URL, etc.

# 4. Run migrations
python manage.py migrate

# 5. Start dev server
npm run dev           # frontend (port 3000)
flask run             # backend (port 5000)

# 6. Run automated tests
npm run test:all      # unit + integration + E2E
pytest                # backend tests
```

Navigate to:
* `/` – Marketing Agent chat  
* `/dashboard` – Experiments & teaching  
* `/feedback` – Feedback portal  
* `/diagnostics/marketing_agent.json` – Live metrics  

---

### Contributing
1. Fork ➜ branch ➜ PR.  
2. All PRs must pass CI test suite.  
3. High-priority feedback items should reference a PR.  

---

**Welcome to the AI Agent Factory—let’s build your next AI teammate!**
