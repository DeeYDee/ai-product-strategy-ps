# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | AWS bedrock- No contractual lock-in; currently in exploration/validation phase.|  M | CDocument provider/model dependencies and identify 2 viable alternative model providers/models. Confirm data, logging, retention, and exit requirements.
| **Abstraction** | requires validation that prompts, APIs, guardrails,| H | | Audit is required.
| **Routing** | no dynamic routing | H | depend on direction of organization on provider, a dynamic route implmenetion with priority.
| **Eval** | evaluations are urrently manually tested| H | implement an auntomation test build

## Portability Score
<!-- Ready / Partial / Locked --> Locked (not ready)

## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? --> Pause service, Implement Audit, explore vendor lock-in neutral option, transition initiated.

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
