# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Remediation	| Incident + diagnosis + remediation + outcome| Better remediation decisions  | Y/N | active  |
| Reliability	| Failures + red-team findings + HITL corrections|Better evals, guardrails and safety | Y/N | active |
| Network Intelligence |Telemetry + topology + incidents + outcomes| Better detection and root-cause intelligence| Y/N | active |


**Broken loop identified by partner:**
**Fix plan:**
Feed successful and failed outcomes into regression tests, remediation intelligence and future evaluation.

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
EU AI Act status: High-risk — Annex III(2), confirmed, (safety component in critical-infrastructure management).

**Scope:** Read-only detection, correlation, remediation drafting. No execution credentials to network devices.

**Autonomy:** Agent reads, diagnoses, and drafts freely. Every execution action — config change, reroute, restart, firewall rule, ticket close — requires human approval, no exceptions. This design satisfies Art. 14 (human oversight) directly.

**Escalation:** Human review triggers at <85% confidence, >2-device blast radius (or any critical-path device), security-pattern matches (→ Security team), SLA-impacting outages (5-min page).

**Audit:** Real-time logging of every proposal/decision; weekly drift reports; monthly sampled human audit; quarterly review per Art. 61 post-market monitoring. Logs retained 12 months — the Art. 26(6) floor, with shorter retention possible where GDPR minimization applies to personal-data subsets.



## Agent Topology
Topology is:
Detect > Diagnose > Risk/Confidence > Policy Gate > Approve/Autonomous > Execute > Validate > Learn.


<!-- If using agents: what can each agent do? 
Agents can Detect - Monitor telemetry, detect anomalies, correlate events, 
Can diagonise, - Identify probable root cause, gather evidence, assign confidence.
Can remediate, - Recommend remediation and expected outcome. 
Can execute - Execute approved low-risk, reversible actions.

What can't it do? Who approves what? --> 
Agents cant - Change network state, Bypass policy/safety controls and Cant directly modify production network nor override human approval rules.


## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
|Raw alert/log dumps into CoPilot to get a plain-English root-cause explanation | **Capability gap** — LogicSee's hypothesis output is technical, not narrative| H | **keep** / govern / kill |
|Team leads use Copilot to draft post-incident reports from raw logs |**Capability gap** / pricing gap — native reporting either doesn't exist or sits behind a tier they haven't bought | M | keep / **govern** / kill |
|On-call engineers run a custom script to remap LogicSee's default severity levels to match internal SLA tiers |**Workflow gap** — the product's taxonomy doesn't match how the business actually defines "critical" | H | keep / govern / **kill** |



**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
