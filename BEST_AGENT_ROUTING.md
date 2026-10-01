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
