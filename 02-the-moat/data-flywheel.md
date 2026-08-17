# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 3/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 3/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 3/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 2/5 |

### Correction Loop - 3/5
**What you capture today:**
Network alerts, anomalies, performance degradation, and incidents.
The network state immediately before, during, and after an incident.
Metrics such as latency, packet loss, jitter, throughput, errors, utilization, availability, retransmissions, CPU/memory, interface health, and application response time.

**How it compounds:**
Every incident becomes a labeled state > action > outcome training example, becoming the growing corpus of network conditions paired with remediation outcomes. Transitioning into this flow: Detect > Diagnose > Predict outcome > Remediate > Validate > Learn > Prevent recurrence.


### Preference Loop - 3/5
**What you capture today:**
Device, interface, application, service, site, and user context.
Network topology and dependency graphs.
Historical performance baselines.
Normal operating ranges by device, site, application, time, and traffic pattern.
Change history and configuration state.

**How it compounds:**
The platform becomes increasingly environment-aware rather than relying on generic thresholds.

### Domain Context Loop - 3/5
**What you capture today:**
Failure patterns across LAN, WAN, Wi-Fi, SD-WAN, cloud, data center, security, and application environments.
Correlations between network and application performance.
Common combinations of symptoms.
Device/vendor/model/firmware-specific failure signatures.

**How it compounds:**
Yes, a failure discovered in one part of the network can become intelligence for another. Thesystem gradually builds a failure-pattern graph:
Symptom/Failure > Correlation > Root Cause > Remediation > Expected Outcome
This allows the platform to recognize failure modes earlier and diagnose them with fewer observations.

### Network Loop - 2/5
**What you capture today:**
Anonymized/normalized network telemetry patterns.
Incident and failure signatures.
Device and infrastructure characteristics.
Successful and unsuccessful remediation patterns.
Recovery times and remediation effectiveness.
Vendor/model/firmware-specific behaviors.

**How it compounds:**
Every new monitored environment contributes additional to the root cause, the fix, what worked and what didnt.
eventually evolving to a better product per time. but this seems like a long way to go...

**Total Flywheel Score: 11/20**
**Weakest Loop:** Network Loop
The gap: Convert customer-specific incidents and remediation history into privacy-safe, reusable global intelligence...hence telemetry.

**Fix for weakest loop:**
Build a centralized remediation intelligence layer that normalizes incidents across customers and infrastructure environments into reusable patterns:
but most importantly.. this is more dependent on telemetry over time.

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** Cisco
**Vector:** Acquiscitions and Product Expansion
Cisco is building a solution that is structurally close to the autonomous self-healing value proposition. with a couple of acquisitions already completed.
**Time-to-threat:** 24 Months/ 36months
**% of value at risk:** 33% / 50%

### 2. Vertical Competitor
**Attacker:**Solarwinds
**Vector:** Expanding to cloud native monitoring, broader observability across network, application, infrastructure and cloud environments. 
**Time-to-threat:** 12-24 months
**% of value at risk:** 30%

### 3. Adjacent Expansion
**Attacker:** Dynatrace
**Vector:**
Cloud observability moving into network observability including AI SRE and autonomous operations.
**Time-to-threat:** 12 months
**% of value at risk:** 20%

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:**
**Attack vector (target the weakest loop):**
**Weeks 1-4 - what they ship:**
**Weeks 5-8 - how they poach users:**
**Weeks 9-12 - why users don't come back:**
**Your defense:**
