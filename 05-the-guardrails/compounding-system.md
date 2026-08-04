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

NetMon AI Governance Policy — Summary

System: Network Performance Monitoring Agent, deployed on critical digital infrastructure.
EU AI Act status: High-risk — Annex III(2), confirmed (safety component in critical-infrastructure management).

Scope: Read-only detection, correlation, remediation drafting. No execution credentials to network devices.

Autonomy: Agent reads, diagnoses, and drafts freely. Every execution action — config change, reroute, restart, firewall rule, ticket close — requires human approval, no exceptions. This design satisfies Art. 14 (human oversight) directly.

Escalation: Human review triggers at <85% confidence, >2-device blast radius (or any critical-path device), security-pattern matches (→ Security team), SLA-impacting outages (5-min page), repeated overrides within 5 business days.

Audit: Real-time logging of every proposal/decision; weekly drift reports; monthly sampled human audit; quarterly review per Art. 61 post-market monitoring. Logs retained 6 months — the Art. 26(6) floor, with shorter retention possible where GDPR minimization applies to personal-data subsets.

Obligations resolved via the Act:

Conformity assessment (Art. 43): Internal control under Annex VI applies by default. NetMon isn't a safety component of an Annex I-regulated product, so third-party notified-body assessment isn't triggered unless a harmonized standard says otherwise.
Risk management + technical documentation (Art. 9, 11): Provider's continuous obligation through the system's lifecycle — this is the critical-path blocker, not the DPIA.
DPIA: Required, not discretionary. Art. 26(9) obligates you as deployer to use the provider's Art. 13 instructions to satisfy your GDPR Art. 35 DPIA duty — the AI Act feeds the DPIA, it doesn't substitute for it.
Accuracy declaration (Art. 15): The 85% confidence threshold needs documented test evidence, not an asserted number — it gets declared in the technical file and EU database registration.

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
