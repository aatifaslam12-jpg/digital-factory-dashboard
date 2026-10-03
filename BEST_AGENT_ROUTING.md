# Best-Agent Routing Architecture

Status: LOCKED design decision (2026-10-01)

## Principle
Use the best validated agent/model for each job rather than forcing one model to do everything. Routing may evolve as models improve, but safety and human-approval boundaries do not weaken.

## Roles
- **Supervisor / orchestrator:** Dot when available and validated for the workflow; otherwise the best available orchestration agent.
- **Software engineering:** Codex or the strongest validated coding agent for implementation, debugging, tests, repository work and automation.
- **Deep audit / difficult reasoning:** Astra High or the strongest validated high-reasoning model for architecture reviews, safety audits, conflict analysis and difficult milestones.
- **Specialists:** TimesFM, NVIDIA models, research/search, media-generation and future specialist models only where benchmarks show incremental value.
- **Owner:** Aslam remains final authority for consequential approvals.

## Dynamic routing policy
1. Route by task quality, reliability, latency, cost and available credits.
2. Benchmark challengers before replacing a proven component.
3. Prefer low-cost/fast models for routine work; reserve premium reasoning for hard/high-impact work.
4. Keep an evidence trail for important changes.
5. If a model/tool is unavailable, fail over to the best validated alternative rather than redesigning the whole project.
6. New models are candidates, not automatic upgrades. Test first, promote after evidence.

## Project-specific policy

### Alpha Genesis / Gold Lab / AFSA
Dot may supervise research, monitoring, maintenance and delegation after controlled validation. Codex may implement/test code. Astra High may perform deep safety/architecture audits. Heavy LLMs remain OFF the live execution path.

Live trading remains deterministic/local:
Market/MT5 data -> feed validation -> signal purification/validated quant logic -> Risk Governor -> execution safety -> position/trade survival management.

Hard boundaries:
- Risk Governor and kill switch cannot be overridden by an AI agent.
- Demo activation and Live activation require separate explicit owner approval.
- Real-money authority is never granted merely because an AI supervisor is connected.
- Champion/Challenger promotion requires leakage-safe testing, OOS/walk-forward/stress/shadow/demo evidence as applicable and owner approval.
- Legacy `alpfa_bot_v8` is abandoned and must not be touched, merged, run or reused unless the owner explicitly reverses that decision.

### CurioNova TV
Supervisor may coordinate trend/topic research, scripting, media-provider routing, generation QA, packaging, analytics and recovery. Coding/automation work routes to the strongest coding agent. Creative/media generation routes to benchmarked providers. Cost/credit-aware fallbacks are preferred.
- Auto-publish remains OFF.
- Human approval is mandatory before publishing.
- Existing working modules, triggers, SAFE_WAIT and pipeline/library compatibility must be preserved unless an approved migration replaces them.

### Digital Factory
Supervisor may coordinate departments, agents, opportunity research, operations, quality, finance reporting and task delegation. Specialized agents should be assigned by demonstrated capability and cost.
- Start capital-efficient: free/low-cost validated tools first where quality is adequate.
- High-impact financial/account/security actions require appropriate human approval.
- Maintain auditability, rollback and clear ownership of automated actions.

## Adoption path for Dot
1. Read-only / monitoring / research supervision.
2. Delegation to coding/research agents with logs.
3. Controlled maintenance actions after validation.
4. Broader orchestration only after reliability is demonstrated.
5. Never use expanded permissions to bypass project-specific approval or safety gates.

## Governance
This document records architecture policy, not permission to execute consequential actions. Production code changes must be tested and reviewed according to each project's existing safeguards.


## Intelligence & Autonomy Roadmap

### V1 — Foundation (build/retain now)
- **AI Router Score Engine:** choose agents using measured quality, reliability, latency, cost, credit availability and task risk.
- **Evidence & Confidence Gate:** important outputs carry evidence/provenance and confidence/uncertainty; uncertainty triggers review or WAIT rather than invention.
- **Permission Matrix / Least Privilege:** each agent gets only the tools/actions required for its role; consequential permissions are time/task scoped.
- **Immutable Decision & Experiment Ledger:** record important decisions, tests, failures, model/provider versions, costs, approvals and rollback points.
- **Universal Health Monitor:** detect stale data, API/model outages, latency spikes, quota exhaustion, corrupted artifacts, unexpected state and security anomalies.
- **Safe Rollback:** every consequential deployment/config change has a known-good restore point.
- **Data Quality Firewall:** validate freshness, completeness, schema, duplicates, leakage/contamination and source conflicts before downstream AI use.

### V2 — Automation & resilience
- **AI Champion–Challenger:** benchmark incumbent vs new models/providers on hidden representative tasks before promotion.
- **Multi-Agent Jury:** separate Builder, Reviewer and Red-Team roles for critical changes; creator cannot self-certify high-impact work.
- **Self-Healing Loop:** detect -> diagnose -> isolated repair -> deterministic tests -> compare -> approval gate -> deploy -> monitor -> rollback if degraded.
- **Digital Twin / Sandbox:** simulate project workflows and failures before production changes.
- **Budget Brain:** optimize model/API/GPU/video-provider selection against quality targets, quotas and monthly budget.
- **Failure Prediction:** use health history and telemetry to identify rising error/latency/quota/storage risks before failure.
- **Cross-Project Shared Services:** common model registry, cost ledger, secrets policy, health monitoring and technology watch; keep project data/permissions isolated.

### V3 — Controlled autonomous evolution
- **24/7 Technology & Opportunity Radar:** discover relevant models, algorithms, APIs, research and business opportunities; score relevance before testing.
- **Automatic Skill Factory:** repeated successful workflows become versioned reusable skill candidates after validation.
- **Capability Registry:** maintain what each agent/provider is proven to do, benchmark date, limits, cost and fallback.
- **Drift & Regression Sentinel:** continuously detect degradation in model outputs, prompts, APIs, data, business KPIs and project behavior.
- **Counterfactual / Shadow Evaluation:** compare what the new agent would have done without letting it control production.
- **Automatic Retirement:** quarantine models/providers/workflows that become unreliable, too expensive, deprecated or consistently inferior; retain rollback evidence.
- **Knowledge Distillation:** turn validated project lessons into compact playbooks so future agents inherit decisions without re-reading entire chat histories.

## Additional project algorithms

### Alpha Genesis
- Regime-aware model routing: specialists may change by validated market regime, but no AI model alone can authorize a trade.
- Signal disagreement/uncertainty gate: conflict reduces confidence and can force NO_TRADE.
- Execution anomaly sentinel: detect slippage, broker mismatch, stale quotes, abnormal latency, order/position divergence and immediately apply existing fail-closed controls.
- Research models remain asynchronous/off the deterministic live path.

### CurioNova TV
- Content Portfolio Optimizer: balance evergreen, trend-responsive and experimental topics instead of chasing every trend.
- Pre-publish Quality Gate: evidence/factuality, originality, brand consistency, thumbnail/title promise-match and policy checks before human approval.
- Provider Quality/Cost Router: benchmark video/image/voice providers and route each scene/job to the best validated quality-cost option.
- Learning Loop: feed approved analytics back into topic, hook, retention and packaging experiments without auto-publishing.

### Digital Factory
- Opportunity Scoring Engine: score legal opportunities by demand, margin potential, startup cost, time-to-first-revenue, automation potential, competition, evidence quality and downside.
- Small-Bet Experiment Engine: validate opportunities cheaply before allocating meaningful capital.
- Unit-Economics Guard: track acquisition cost, tool/API cost, labor/time, gross margin, cash conversion and payback before scaling.
- Agent Workforce Scheduler: allocate tasks to AI/human resources based on capability, urgency, cost, dependency and risk.

## Complexity rule
Do not implement every feature merely because it is documented. Add a layer only when its measurable benefit exceeds complexity, latency, maintenance and cost. V1 stability takes priority over V2/V3 autonomy.


## Model Challenger Note — 2026-10-03

Gemini 4 Argon is registered as an **unvalidated candidate** for future benchmarking. Evaluate it on coding, large-context analysis, review quality, reliability, latency and cost before any promotion. Existing approval and rollback controls remain unchanged. Re-verify current provider availability and capabilities before integration.
