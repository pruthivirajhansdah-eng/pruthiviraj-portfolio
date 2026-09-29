# Sample root-cause review: fictional VPN access queue

**Scenario:** Fictional simulation, not based on a real employer incident or dataset.

## Problem statement
A sample VPN-support queue shows a cluster of requests waiting longer than the simulated target. The immediate question is whether the delay comes from demand, missing information, routing, or resolver capacity. No real incident is represented here.

## Evidence to collect before concluding
Compare created, assigned, first-response, reassigned, and resolved timestamps; inspect request completeness by intake channel; group by error symptom and priority; check approved change windows and service health; sample reopen reasons; and interview the service desk and network resolver. Validate definitions and time zones first.

## Five Whys (working hypothesis, to validate)
1. **Why did some tickets wait?** The resolver received requests without the device state and connection context needed for triage.
2. **Why was context missing?** The intake form treated different VPN symptoms as one generic category.
3. **Why did the form remain generic?** Category and routing rules were not reviewed against recent incident patterns.
4. **Why was review missed?** No named owner or cadence existed for the intake taxonomy.
5. **Why was there no owner/cadence?** The service improvement process did not assign governance for form and knowledge content.

**Candidate root cause:** weak ownership and maintenance of intake taxonomy and guidance. This remains a hypothesis until timestamps, ticket samples, and stakeholder interviews confirm it.

## Corrective actions
- Short term: add a triage checklist for symptom, network type, device, and safe diagnostic result; do not ask for passwords or MFA codes.
- Medium term: separate common VPN symptom paths and route by validated category and priority.
- Prevention: assign an owner and quarterly review for categories, routing rules, and related articles.
- Measure: monitor missing-information rate, reassignment rate, first response, reopen rate, and median resolution time by category. Agree definitions and baseline before setting targets.

## Validation plan
Run a limited pilot with synthetic or approved non-sensitive records; compare the agreed measures before and after; review misroutes and user feedback; obtain security/accessibility approval; retain a rollback path. No impact figure is claimed in this sample.
