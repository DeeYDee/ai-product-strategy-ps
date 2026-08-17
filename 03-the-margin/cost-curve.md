# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-Device/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | TBD|Frontier-model usage for complex diagnosis, root-cause analysis, and high-risk remediation decisions. |
| Inference (cascading/triage) | TBD | Lower-cost model usage for event classification, anomaly triage, deduplication, known failure patterns, and routine analysis.|
| Infrastructure |TBD | Compute and platform infrastructure required to ingest, process, correlate, and serve network monitoring and self-healing workloads|
| Data/storage |TBD |Storage for telemetry, network context, incidents, topology, remediation history, and outcome data used by the learning flywheel. |
| Human-in-the-loop |TBD| Operational review for low-confidence, high-risk, or failed autonomous remediation; should decline as automation improves.|
| **Total AI COGS** |TBD| Sum of inference + infrastructure + data/storage + human-in-the-loop costs per device/month |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:** Fast/low-cost model + deterministic rules.

**Frontier model:** Complex diagnosis and high-risk remediation only.

**Routing rule:** Use the cheapest validated and safe method capable of completing the task.

**Expected cascade ratio:** 70–85% triage/deterministic, 10–25% advanced reasoning, <5% human intervention

## Pricing Model

**Current pricing:**
**Proposed AI pricing:**
**Model:** seat-based / usage-based / outcome-based / **hybrid**

Base platform + included usage + usage bands + premium autonomy tier.
Since Pricing is Device based, it would look something like this:

**For Example:**
"Pricing Strategy
- Strategy posture: Maximize
- Pricing model: Seat-Device / Access
- Unit of work metered: Switches, Access points, Routers, AI capabilities
- Base fee ($/month): 0
- Price per unit: $15
- Estimated units/user/Devices/month: 3000
- Implied revenue/user/month: $45000.00"

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | Potential significant "cost sold" expansion on high-AI workloads| Increase cascading, shift to validated lower-cost models, cache/reuse reasoning|
| Heaviest segment doubles |Margin compression if pricing is uncapped | Usage bands and enterprise overage economics; optimize telemetry compression|
| Model provider raises prices 50% |Moderate/high depending on provider concentration | Activate alternative provider routing and renegotiate volume pricing|

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):** Connectivity device-based SaaS with predictable infrastructure costs.
**After (AI-enabled):** Network + autonomy-based pricing where AI "cost sold" is controlled through routing, cascading and automation.
**Net margin shift:** would expect the margin shift gradually from Near-term negative > medium-term neutral > long-term positive
