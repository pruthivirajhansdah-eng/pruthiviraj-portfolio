# Sample requirements brief: Northstar self-service support portal

**Status:** Fictional practice artifact. Northstar Support, its users, and the requirements below are invented for demonstration.

## 1. Problem and objective
Employees need a consistent way to find approved support guidance, submit a request with enough diagnostic context, and see what happens next. The prototype should reduce avoidable rework caused by incomplete requests and unclear ownership. This is a proposed objective, not a measured result.

## 2. Scope
**In scope:** searchable knowledge articles; guided request forms for access, device, network, and application issues; confirmation with a reference number; status and next-update visibility; accessible mobile-first layout; basic request and article reporting.

**Out of scope:** automated account unlocks, password collection, payment or HR workflows, direct access to production systems, and any change to real enterprise identity controls.

## 3. Stakeholders
Employees, service desk analysts, resolver-group leads, knowledge owners, service manager, security and privacy reviewers, and product owner.

## 4. User stories and acceptance criteria
### Find relevant help
As an employee, I want to search approved articles by symptom so that I can try safe steps before submitting a ticket.
- Search results show title, service category, last-reviewed date, and estimated reading time.
- Keyboard users can reach search, results, and article actions in a logical order.
- If no result is relevant, the user can continue to request submission without losing their description.

### Submit a complete request
As an employee, I want a guided form that asks only for relevant details so that support can route my request correctly.
- Required fields vary by service category and are explained in plain language.
- The form never requests a password, MFA code, or secret recovery answer.
- Before submission, the user can review category, impact, contact preference, and entered details.
- Successful submission creates a reference ID and displays the expected next update.

### See request progress
As an employee, I want a status and owner group so that I know the request has not disappeared.
- Status labels use a documented lifecycle and have a plain-language explanation.
- The page displays last updated time and a safe contact path for stalled requests.

## 5. Functional requirements
FR-01 Search articles by keyword and category. FR-02 Show the article review date. FR-03 Suggest relevant articles before request submission. FR-04 Collect minimum routing fields. FR-05 Validate category-specific mandatory fields. FR-06 Issue a request reference after successful submit. FR-07 Show lifecycle status and timestamp. FR-08 Record an auditable category and routing decision. FR-09 Provide a human-support fallback.

## 6. Non-functional requirements
Meet the organization’s accessibility standard; protect data in transit and at rest; enforce role-based access; use approved retention rules; support current mobile and desktop browsers; log administrative changes; and present errors in actionable language. Security review defines technical controls before implementation.

## 7. Measures and definitions
Track form completion rate, requests returned for missing information, article helpfulness, median time to first human response, and request volume by category. Define numerator, denominator, exclusions, time zone, and reporting cadence with service owners before baselining. Do not use sample values as production targets.

## 8. Assumptions, risks, and open questions
- Assumption: an approved source of article content and request categories exists.
- Risk: poor categorization can make routing and reporting misleading.
- Risk: collecting unnecessary personal or device details increases privacy exposure.
- Open: Which identity and ITSM integrations are approved? Which request types require immediate human triage? Who owns article review and expiry? What accessibility standard applies?

## 9. Traceability
A real delivery would connect each accepted requirement to a process flow, test case, security review, and release decision. This brief is a practice sample, not a client deliverable.
