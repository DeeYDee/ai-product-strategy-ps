# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | | |
| Inference (cascading/triage) | | |
| Infrastructure | | |
| Data/storage | | |
| Human-in-the-loop | | |
| **Total AI COGS** | | |

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
Base platform + included usage + usage bands + premium autonomy tier

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
