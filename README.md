# Hi, I'm Priyan Sabarish👋

Master of Artificial Intelligence student at **Monash University** (Melbourne). I build AI systems end to end — model layer, backend APIs, evals and observability — mostly to learn how things work in production.

 -🎓 Master of AI, Monash University (2025–2026)
 -💼 Mobile App Developer Intern, Chemins Pvt Ltd, Puducherry (2023)
 -🔭 Currently building an on-call incident triage agent
 -📫 Reach me: [LinkedIn](https://www.linkedin.com/in/priyansabarish) · priyansabarish@gmail.com

---

## 🛠 Projects

### [Incident Triage Agent](https://github.com/PriyanSabarish/REPO-NAME) — _in progress_

An on-call assistant that retrieves runbooks and queries metrics and logs to triage incidents. It recommends remediation but never executes it.

- Provider-agnostic model layer with a conformance test suite
- Synthetic incident corpus (40 incidents, 15 runbooks) with labels for evaluation
- Evals and OpenTelemetry tracing, MCP tools

### [Pay Code Auditor](https://github.com/PriyanSabarish/REPO-NAME)

An AI agent that helps businesses comply with Australia's new Payday Super rules, where super must be paid with wages every pay cycle. Built at the Forward: AI in Business Hackathon (Sep 2026) — shortlisted in our track.

- Checks a business's pay codes against ATO rules; clear-cut cases are classified immediately
- Ambiguous codes go to an investigating agent, which pauses to ask the bookkeeper (human-in-the-loop) when it gets stuck, then resumes
- Produces a draft client letter for the bookkeeper, with the cost of each error
- My role: backend and AI harness — everything between the model and the rest of the app

**Under the hood**

- RAG over ATO guidance with hybrid search (BM25 + embeddings, reciprocal rank fusion) — keyword search alone missed codes like `FDV LEAVE`
- Function-calling agent kept on a short leash: read-only tools and a step limit enforced in code
- Model escalation plus LLM-as-a-judge, with disagreements routed to human review
- Pydantic structured outputs, so a malformed response falls back to "unclear" instead of crashing; provider-agnostic LLM layer
- Guardrails that keep the LLM away from the numbers — cost calculations stay in deterministic code
- Evaluation harness that runs the same audit in five modes, from keyword-only to the full agent

### [Quietway — Sensory-Aware Wayfinding](https://github.com/PriyanSabarish/REPO-NAME)

Web app that routes people through Melbourne CBD along less-crowded paths, using City of Melbourne pedestrian count data.

- Dijkstra routing over a crowd-weighted street graph
- Adjustable crowd tolerance (people/min), route cards with peak counts and over-limit warnings
- Nearby quiet refuge locations
- Python + FastAPI backend, logic ported to JS for the frontend

### DFlash Draft Model for Gemma 4 12B — _coming soon_

A DFlash-style (block-diffusion) speculative decoding draft model to speed up inference for Gemma 4 12B.

---

## 🏆 Competitions

- **2nd place** — Inter-University Datathon (Sep 2026), Team Epoch Drift. Next-hour PM2.5 forecasting on Beijing multi-site air quality data.
- **Shortlisted** — Forward: AI in Business Hackathon (Sep 2026), Pay Code Auditor.

---

## 🧰 Tech

**Languages:** Python, JavaScript **Backend:** FastAPI, REST APIs **AI/ML:** LLM agents, evals, speculative decoding, time-series regression **Tooling:** Git, OpenTelemetry, MCP

---

<!-- Optional stats cards — delete if you don't want them -->

![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=PriyanSabarish&layout=compact&hide_border=true)
