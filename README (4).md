# AI Agent Factory

Build autonomous **business teammates** in hours—not weeks.  
The Factory turns a vague business problem into a production-ready AI agent through a proven 5-step pipeline, automated tooling, and a closed feedback loop.

---

## 🚀 Results from the First Loop

| Metric | Outcome |
|--------|---------|
| Partnership rubric score | **92 / 100** |
| Build cycle time | **< 48 h** (prompt → production) |
| Problem-detection accuracy | **100 %** (lead-gen & retention scenarios) |
| p95 chat latency | **1.2 s** (target ≤ 1.5 s) |
| Blocking errors | **0** (TypeScript & runtime) |

The inaugural agent—a **Marketing Problem-Solver** for SaaS founders—launched with a detective onboarding flow, Kanban experiment engine, PostgreSQL persistence, full CI test suite, and a live feedback portal.

---

## 🏗️ 5-Step Factory Pipeline

| Step | Goal | Primary AI | Key Output |
|------|------|------------|-----------|
| 1 Translate | Convert messy narrative into a structured design prompt | **Translator AI** | `*-o3-design.md` |
| 2 Design | Generate architecture spec | **o3-pro** | `*-replit-spec-PATCHED.md` |
| 3 Build | Produce working code, tests, CI | **Replit AI Agent** | Running web-app |
| 4 Analyse | Score agent vs rubric | **Domain Agent** | Diagnostics JSON + 92/100 report |
| 5 Iterate | Capture & act on feedback | **Feedback System** | Prioritised feedback DB, analytics |

_Total target time: ≤ 48 hours._

### Detective Insight  
Early testing showed users can’t answer jargon-heavy questions.  
**Patch:** a *Discovery Mode* that asks open-ended questions, infers the problem category, then teaches in plain English.  
Result: +32 rubric points (60 → 92).

### Feedback Loop  
A `/feedback` page + API lets humans **and** AIs submit issues.  
Auto-triggers fire when agent confidence < 0.3 or performance degrades, turning the Factory into a self-improving system.

---

## 📂 Repository Highlights

```
README.md                   ← you are here
docs/                       ← pipeline & process docs
prompts/                    ← design & build prompts
agents/marketing-agent-v1/  ← implementation analyses & results
testing/                    ← automated test harness prompt
```

---

## ⚡ Getting Started

```bash
# 1. Clone
git clone https://github.com/<your-org>/ai-agent-factory.git
cd ai-agent-factory

# 2. Install backend & frontend deps
pip install -r requirements.txt      # Flask services
npm install                          # React UI & tests

# 3. Configure env vars
cp .env.example .env                 # set OPENAI_API_KEY, DATABASE_URL, etc.

# 4. Run DB migrations
python manage.py migrate

# 5. Start dev servers
npm run dev      # frontend (port 3000)
flask run        # backend  (port 5000)

# 6. Launch tests
npm run test:all # unit + E2E
pytest           # backend tests
```

Navigate to:  
* `/` — Marketing Agent chat  
* `/dashboard` — Experiments & teaching  
* `/feedback` — Feedback portal  
* `/diagnostics/marketing_agent.json` — Live metrics

---

## 🔭 Scaling to New Domains

1. Copy `prompts/marketing-agent-o3-design.md` → draft new domain prompt.  
2. Run the pipeline—shared modules (`ProblemDetector`, `TeachingEngine`, `FeedbackService`) reuse automatically.  
3. Aim for ≥ 85/100 on first build; iterate via feedback portal.

---

### Contributing
1. Fork ➜ branch ➜ PR.  
2. All PRs must pass the CI test suite.  
3. Link high-priority feedback items to your PR.

---

**Welcome to the AI Agent Factory—let’s build your next AI teammate!**
