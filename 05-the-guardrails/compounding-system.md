# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| | | | Y/N | active / broken / missing |
| | | | Y/N | active / broken / missing |
| | | | Y/N | active / broken / missing |

**Broken loop identified by partner:**
**Fix plan:**

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

**LogicSee AI Governance Policy — Summary**

**System:** Network Performance Monitoring Agent, deployed on critical digital infrastructure.
EU AI Act status: High-risk — Annex III(2), confirmed (safety component in critical-infrastructure management).

**Scope:** Read-only detection, correlation, remediation drafting. No execution credentials to network devices.

**Autonomy:** Agent reads, diagnoses, and drafts freely. Every execution action — config change, reroute, restart, firewall rule, ticket close — requires human approval, no exceptions. This design satisfies Art. 14 (human oversight) directly.

**Escalation:** Human review triggers at <85% confidence, >2-device blast radius (or any critical-path device), security-pattern matches (→ Security team), SLA-impacting outages (5-min page).

**Audit:** Real-time logging of every proposal/decision; weekly drift reports; monthly sampled human audit; quarterly review per Art. 61 post-market monitoring. Logs retained 12 months — the Art. 26(6) floor, with shorter retention possible where GDPR minimization applies to personal-data subsets.



## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
|Raw alert/log dumps into CoPilot to get a plain-English root-cause explanation | **Capability gap** — LogicSee's hypothesis output is technical, not narrative| H | **keep** / govern / kill |
|Team leads use Copilot to draft post-incident reports from raw logs |**Capability gap** / pricing gap — native reporting either doesn't exist or sits behind a tier they haven't bought | M | keep / **govern** / kill |
|On-call engineers run a custom script to remap LogicSee's default severity levels to match internal SLA tiers |**Workflow gap** — the product's taxonomy doesn't match how the business actually defines "critical" | H | keep / govern / **kill** |



**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
