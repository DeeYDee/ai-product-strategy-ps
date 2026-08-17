# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | AWS bedrock- No contractual lock-in; currently in exploration/validation phase.|  M | Document provider/model dependencies and identify 2 viable alternative model providers/models. Confirm data, logging, retention, and exit requirements.
| **Abstraction** | Application logic currently depends on provider-specific prompts, APIs, guardrails, and response formats. Portability has not yet been validated.| H | Audit is required. |  
| **Routing** | no dynamic routing, Requests are effectively tied to the selected provider/model. | H | depend on direction of organization on provider, a dynamic route implmenetion with priority. Define routing policy with priority/fallback rules based on availability, latency, cost, capability, and risk tier.
| **Eval** | evaluations are urrently manually tested| H | implement an auntomation test build, covering diagnosis accuracy, remediation recommendation, hallucination/unsafe-action rate, latency, cost, and regression detection.

## Portability Score
<!-- Ready / Partial / Locked --> Partial (Alternative exists conceptually but has not been validated.)
We can replace the primary AI provider without rewriting the product, but might be losing our accumulated learning, weakening safety controls, or interrupting autonomous network operations.

## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? --> Pause service, Implement Audit, explore vendor lock-in neutral option, transition initiated.

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
