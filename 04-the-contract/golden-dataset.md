# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | Normal behavior| No false alert | N | rule |
| 2 | Known anomaly| Correct diagnosis| N | rule / LLM |
| 3 | Known failure|Correct remediation | N | rule / LLM |
| 4 | Correct remediation|Refuse / HITL | Y | rule  |
| 5 | 	Failed remediation| Detect + rollback/escalate| Y | rule |


**Adversarial rows included:** 5

**Coverage gaps identified by partner:**
New failures, conflicting telemetry, unsafe actions, failed remediation, regression.

## Confidence UX Design

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger

**High confidence (>90%):** Autonomous action if low-risk and pre-approved.

**Medium confidence (70-90%):** Validate further / approval required.

**Low confidence (<70%):** No autonomous change; HITL.

**User control surface:**
Approve/Reject, Autonomy level, Confidence thresholds and Configure blast radius, Allowed/Prohibited actions, Rollback Changes, Set device and Site Criticality.


## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Incident Detection Accuracy | >95% |Golden dataset + production incidents |<90% |
| Remediation success rate | >95% | Successful recovery / autonomous actions| <90%|
| Hallucination rate | <1%| Unsupported diagnosis/action claims| >2%|
| Latency (p95) | <5 Sec| for triage	Production telemetry | >10 Sec |
| Drift velocity |<2% |Rolling eval performance |>5% degradation |
| Rollback rate |<2% |Remediations requiring rollback |>5% |

North-star metric:
Autonomous Recovery Rate — % of incidents successfully detected, diagnosed, remediated and validated without human intervention.

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
