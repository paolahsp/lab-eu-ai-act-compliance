# EU AI Act Approval Pack - Paola Hintze

## Part 1 - Private answer key

### Case 1 - Prohibited

**Client brief**

A European customer-support company wants to reduce employee turnover and improve the allocation of premium client accounts.  
During short weekly video check-ins, an AI tool would analyse employees' facial movements, vocal patterns, speaking pace, and pauses.  
The system would estimate each agent's stress, frustration, motivation, and confidence levels.  
It would produce a client-readiness score and recommend coaching, account assignments, and promotion opportunities.  
These recommendations would affect approximately 2,000 customer-support agents working across several EU offices.  
Team supervisors could override the recommendations, but they would need to record a reason for doing so.

**Why we chose it:** The system infers employees' emotions from facial and vocal biometric signals in a workplace context, which is prohibited under Article 5(1)(f).

### Case 2 - High-risk

**Client brief**

A network of private vocational academies receives around 8,000 applications each year for subsidised professional retraining programmes.  
The organisation wants to reduce application-review time and predict which candidates are most likely to complete each programme successfully.  
An AI system would rank applicants using their educational history, employment gaps, application answers, placement-test results, and estimated commuting distance.  
The resulting score would determine the admissions shortlist, scholarship priority, and recommended course level.  
Applications below a fixed threshold would not normally reach the admissions team.  
Admissions officers could review borderline cases and override the score, while adult jobseekers across Germany would be affected by the results.

**Why we chose it:** The AI system evaluates and ranks applicants to determine access to vocational education, making it a high-risk education use under Annex III, point 3(a).

### Case 3 - Limited risk / transparency

**Client brief**

A regional railway company wants to provide passengers with faster support during delays and cancellations.  
It plans to introduce a conversational assistant on its website and WhatsApp channel using live schedules, ticket conditions, refund rules, and passengers' booking details.  
The assistant would answer questions, recommend alternative routes, and prepare ticket changes or refund requests.  
Exceptional refunds and formal complaints would be transferred to a human customer-service agent for approval.  
The assistant would use the name "Mila" and communicate in the same conversational style as the company's human agents.  
The company has not yet decided whether the interface should identify Mila as an automated system.

**Why we chose it:** Mila interacts directly with natural persons, so the system triggers the AI disclosure obligation under Article 50(1) without falling into a high-risk area.

### Case 4 - Minimal risk

**Client brief**

A five-store zero-waste grocery chain wants to reduce food spoilage and prevent products from being out of stock.  
A forecasting tool would analyse historical product sales, current stock levels, public weather forecasts, holidays, and local-event calendars.  
It would generate daily replenishment recommendations for each product and store.  
The system would not use customer profiles or make decisions about individual shoppers, employees, or suppliers.  
Store managers would review and adjust the recommendations before placing orders.  
Customers could be indirectly affected through product availability, but the system would not determine individual eligibility, access, or prices.

**Why we chose it:** The system supports an internal operational decision without evaluating people or interacting directly with them, so it has no specific AI Act obligations.

## Part 2 - Consulting response

### Case 1

A European customer-support company wants to reduce employee turnover and improve the allocation of premium client accounts.  
During short weekly video check-ins, an AI tool would analyse employees' facial movements, vocal patterns, speaking pace, and pauses.  
The system would estimate each agent's stress, frustration, motivation, and confidence levels.  
It would produce a client-readiness score and recommend coaching, account assignments, and promotion opportunities.  
These recommendations would affect approximately 2,000 customer-support agents working across several EU offices.  
Team supervisors could override the recommendations, but they would need to record a reason for doing so.

### Case 2

A network of private vocational academies receives around 8,000 applications each year for subsidised professional retraining programmes.  
The organisation wants to reduce application-review time and predict which candidates are most likely to complete each programme successfully.  
An AI system would rank applicants using their educational history, employment gaps, application answers, placement-test results, and estimated commuting distance.  
The resulting score would determine the admissions shortlist, scholarship priority, and recommended course level.  
Applications below a fixed threshold would not normally reach the admissions team.  
Admissions officers could review borderline cases and override the score, while adult jobseekers across Germany would be affected by the results.

### Case 3

A regional railway company wants to provide passengers with faster support during delays and cancellations.  
It plans to introduce a conversational assistant on its website and WhatsApp channel using live schedules, ticket conditions, refund rules, and passengers' booking details.  
The assistant would answer questions, recommend alternative routes, and prepare ticket changes or refund requests.  
Exceptional refunds and formal complaints would be transferred to a human customer-service agent for approval.  
The assistant would use the name "Mila" and communicate in the same conversational style as the company's human agents.  
The company has not yet decided whether the interface should identify Mila as an automated system.

### Case 4

A five-store zero-waste grocery chain wants to reduce food spoilage and prevent products from being out of stock.  
A forecasting tool would analyse historical product sales, current stock levels, public weather forecasts, holidays, and local-event calendars.  
It would generate daily replenishment recommendations for each product and store.  
The system would not use customer profiles or make decisions about individual shoppers, employees, or suppliers.  
Store managers would review and adjust the recommendations before placing orders.  
Customers could be indirectly affected through product availability, but the system would not determine individual eligibility, access, or prices.

## Part 3 - Partner case review

The following classifications were made without access to Gretel's private answer key.

| Case | Likely category | Why this is your first-pass call | Proposed AI architecture | Provider / deployer / vendor | Required obligations or controls | Decision |
|---|---|---|---|---|---|---|
| 1 | Prohibited under Article 5(1)(c); the device-financing component would also be high-risk | The system continuously profiles customers using social behaviour and personal characteristics, including online behaviour unrelated to the telecom service. The score can produce unfavourable treatment in financing, payment options, offers, and access to support. A nominal human override is insufficient when staff are expected to follow the score. | Redesign as two purpose-limited systems. The financing model uses only relevant financial data, while support routing uses the current request and urgency. A human reviews adverse financing recommendations. Log inputs, scores, decisions, and overrides. | Assumption: the external vendor is the provider and the telecom operator is the deployer. The operator becomes the provider if it rebrands or substantially modifies the system. | Remove public online behaviour and the unified customer-value score. Apply risk management, data governance, documentation, effective oversight, logging, monitoring, data minimisation, purpose limitation, and a GDPR DPIA. Legal counsel should confirm whether all Article 5 social-scoring conditions are met. | **Deny and redesign** |
| 2 | High-risk employment system under Annex III | The tool analyses and filters job applications and evaluates candidates. Applicants below the threshold are normally excluded before meaningful human review. | Trigger: receipt of an application. The model compares CVs, responses, assessments, and vacancy requirements. A recruiter reviews recommended and adverse outputs before rejection. Produce a shortlist and rationale while logging inputs, scores, final decisions, and overrides. | Assumption: the recruitment-software vendor is the provider and the hospitality group is the deployer. The group becomes the provider if it develops, rebrands, or substantially modifies the system. | Require risk management, representative data, bias testing, technical documentation, instructions, logging, human oversight, accuracy, robustness, cybersecurity, conformity assessment, registration, and post-market monitoring. The deployer should complete a GDPR DPIA and maintain an oversight protocol. | **Approve with controls** |
| 3 | Limited risk with Article 50 transparency obligations | The voice agent interacts directly with customers. Customers can request a person, but the brief does not state that callers are informed from the start that they are interacting with AI. | Trigger: incoming customer call. The system discloses that it is AI, interprets the request, retrieves account and service information, answers routine questions, or routes the caller. Humans handle disputes, cancellations, complaints, and commercial changes. Log disclosures, routing, transfers, summaries, and corrections. | Assumption: the voice-agent vendor is the provider and the satellite-internet company is the deployer. The company may become the provider if it markets the agent under its own name or substantially modifies it. | Give a clear audible AI disclosure at the beginning, preserve immediate human transfer, restrict the agent's scope, minimise account data, define retention, test accuracy and accessibility, monitor failures, secure call records, and comply with GDPR and consumer-protection rules. | **Approve with controls** |
| 4 | Limited risk / transparency at provider level; potentially minimal for the marketplace as deployer | The system generates synthetic text that customers will read. The lack of ranking or eligibility decisions keeps it outside the high-risk categories, but Article 50(2) may require the provider to make the generated summary machine-readable and detectable as AI-generated. | Trigger: a product reaches a defined review threshold. The system summarises published reviews, runs quality and contradiction checks, and produces a source-linked summary. Merchandising staff monitor and can remove misleading outputs. Log source reviews, model version, summary, corrections, and removal decisions. | If the marketplace develops or rebrands the summariser, it is the provider and deployer. If it uses an external product, the vendor is the provider and the marketplace is the deployer. | Confirm the role allocation and whether the standard-editing exception applies. If the marketplace is the provider, implement machine-readable marking. Add a visible AI-summary notice as a consumer-trust control, preserve source links, monitor hallucinations and manipulation, and review GDPR and consumer-protection implications. | **Approve with controls** |

### Borderline arguments and next operational artifacts

| Case | Borderline argument or counter-argument | Legal verification | Next operational artifact |
|---|---|---|---|
| 1 | Lawful customer evaluation remains possible when it is purpose-specific, uses relevant data, and produces proportionate treatment. The unrelated online data and unified score push this proposal toward prohibited social scoring. | Confirm whether the Article 5(1)(c) unrelated-context or unjustified-treatment test is satisfied. | Lawful-redesign specification and DPIA |
| 2 | A tool performing only narrow administrative support might avoid high-risk classification, but this system materially filters and evaluates candidates. | Confirm the final intended purpose and whether any Article 6 exception could apply. | Human-oversight and bias-testing protocol |
| 3 | Disclosure may not be necessary when interaction with AI is obvious, but a natural voice agent should not rely on that exception without evidence. | Verify the Article 50 disclosure design and accessibility requirements. | Voice disclosure and escalation script |
| 4 | The marketplace may have no deployer-facing labelling duty if the text is not a matter of public interest and a third-party provider handles Article 50(2). However, summarisation may exceed the standard-editing exception. | Confirm provider status, marking responsibility, and applicability of the standard-editing exception. | AI-summary marking and quality-monitoring policy |

## Part 4 - Approval pack

### Executive summary

The four proposals do not share the same launch profile. Case 1 should not launch as proposed because its continuous customer score combines unrelated online behaviour with decisions affecting support, payment flexibility, and financing. Case 2 is a high-risk employment system and may proceed only after provider and deployer controls are implemented. Case 3 can proceed with Article 50 disclosure, strict escalation boundaries, and data controls. Case 4 can proceed with controls, but its final classification depends on who provides the summarisation system and whether Article 50(2) marking applies. The overall recommendation is one denial and redesign and three conditional approvals.

### Case 1 - Telecommunications customer profile

**Client request:** Combine commercial history, call-centre activity, and public online behaviour into a score affecting offers, financing, payment flexibility, and support priority.

**Category and decision:** Prohibited social scoring under Article 5(1)(c), with a separate high-risk creditworthiness component. **Deny and redesign.**

**Architecture and roles:** Do not deploy the unified score. Separate a purpose-limited financing model from service routing. Financing should use relevant financial data and require human review before an adverse result. Support routing should depend on the current request and urgency, not customer value. Assuming an external vendor supplies the system, it is the provider and the telecom operator is the deployer.

**Compliance implications:** Remove public online behaviour, document purpose limitation, perform a DPIA, and log recommendations, final decisions, and overrides. The redesigned financing model must follow the high-risk requirements. Legal counsel should verify the Article 5 analysis.

### Case 2 - Hospitality recruitment screening

**Client request:** Score and shortlist applicants using CVs, application responses, assessments, and vacancy requirements.

**Category and decision:** High-risk employment system under Annex III. **Approve with controls.**

**Architecture and roles:** The system may support screening, but a trained recruiter must review both positive and adverse outputs before an applicant is excluded. The system should record the evidence used, score, explanation, recruiter decision, and override. Assuming a third-party recruitment vendor supplies the tool, the vendor is the provider and the hospitality group is the deployer.

**Compliance implications:** Require risk management, representative data, bias and accuracy testing, technical documentation, automatic logs, meaningful oversight, robustness, cybersecurity, conformity assessment, registration, and post-market monitoring. The deployer should conduct a DPIA, inform applicants appropriately, monitor local outcomes, and establish an appeal route.

### Case 3 - Satellite-internet voice agent

**Client request:** Use an AI voice agent for routine installation, availability, troubleshooting, summarisation, and call routing.

**Category and decision:** Limited risk with Article 50 transparency obligations. **Approve with controls.**

**Architecture and roles:** The agent should disclose its AI nature at the start, retrieve only necessary account and service information, answer approved routine topics, and transfer material matters to a human. Logs should record the disclosure, routing, transfers, summaries, and corrections. The voice-agent vendor is assumed to be the provider and the internet company the deployer.

**Compliance implications:** Implement an audible and accessible disclosure, immediate human escalation, data minimisation, retention limits, accuracy testing, security, monitoring, and safe-response boundaries. GDPR, consumer protection, and communications-confidentiality requirements apply in parallel.

### Case 4 - Marketplace review summaries

**Client request:** Generate source-linked summaries of recurring themes in published customer reviews without changing rankings, seller eligibility, or publication decisions.

**Category and decision:** Minimal risk at the system-use level, with potential Article 50 duties at provider level. **Approve with controls.**

**Architecture and roles:** Generate a summary only after a product reaches a sufficient review threshold. Run quality checks, preserve links to the source reviews, allow human removal, and log the source set, model version, output, and corrections. If the marketplace develops or rebrands the system, it is the provider; otherwise, the external summarisation vendor is the provider.

**Compliance implications:** Confirm provider status and whether the output qualifies for the standard-editing exception. Where Article 50(2) applies, implement machine-readable marking. A visible AI-generated-summary notice is also recommended to prevent misleading claims and support consumer trust.

## Part 5 - Client discussion and debrief

### Intended vs inferred classifications

| Case | Gretel's intended category | Our inferred category | Match? | What the comparison revealed |
|---|---|---|---|---|
| 1 | Prohibited | Prohibited; financing component also high-risk | Yes | The intended social-scoring boundary was correctly identified. Our review additionally separated the financing component as a high-risk use requiring its own controls after redesign. |
| 2 | High-risk | High-risk | Yes | Both reviews identified the material role of AI in recruitment screening and the lack of meaningful human review before exclusion. |
| 3 | Limited risk / transparency | Limited risk / transparency | Yes | Both reviews identified direct interaction with customers and the need for clear AI disclosure from the beginning of the call. |
| 4 | Minimal risk | Limited risk at provider level; potentially minimal for the deployer | Partial | The discussion clarified that the use case can remain outside the high-risk categories while the provider may separately have Article 50 obligations for AI-generated output. |

### Client response

Gretel accepted the recommendations for Cases 1, 2 and 3.

For Case 4, she accepted the distinction between the system's risk classification and role-specific obligations but retained the original minimal-risk classification at the system-use level. The review-summary system does not make consequential decisions about individuals or fall within an Annex III high-risk use case. However, she agreed that the provider may separately have Article 50 obligations relating to AI-generated output and would add that provider-level obligation without treating the use case itself as high-risk.

### What changed after the client discussion?

The main change concerns Case 4. The initial review described it as limited risk at provider level and potentially minimal risk for the marketplace as deployer. After the discussion, the recommendation was refined: the use case remains minimal risk because it does not make consequential decisions or fall within an Annex III category, while any Article 50 marking obligation should be analysed separately at provider level.

This distinction does not change the launch decision: the system may proceed with controls. It improves the analysis by separating the system's risk category from the obligations attached to each actor.

For Cases 1, 2 and 3, the discussion confirmed the original classifications and recommendations. It also reinforced the need to distinguish legal classification from the architecture, human oversight, and operational controls required for deployment.

## Stretch - High-risk implementation roadmap

### Selected case: Hospitality recruitment screening

**Provider responsibilities before market placement**

The provider should define the intended purpose and prohibited uses; implement a quality and risk-management system; document data provenance, representativeness, limitations, bias testing, and accuracy; design automatic logs and meaningful human oversight; test robustness, cybersecurity, and resistance to manipulated applications; prepare technical documentation and instructions; complete the applicable conformity assessment and registration; and establish post-market monitoring and incident-reporting processes.

**Deployer responsibilities before first use**

The hospitality group should complete vendor due diligence and a GDPR DPIA; verify that use for its roles matches the provider's intended purpose; test performance across relevant applicant groups and locations; assign trained recruiters with authority to disregard the score; require human review before rejection; inform applicants appropriately; define retention and access controls; retain required logs; monitor outcomes; and establish complaint, appeal, and incident-escalation procedures.

**Evidence requested from the vendor**

Request the declaration of conformity and registration evidence; instructions for use; relevant technical-documentation summaries; model and data documentation; bias, accuracy, robustness, and cybersecurity test results; logging specifications; human-oversight guidance; post-market monitoring and incident commitments; change-management records; the Data Processing Agreement; subprocessors and data locations; retention and deletion terms; and evidence supporting any claimed Article 6 exception.

## Sources

- [Regulation (EU) 2024/1689 - Artificial Intelligence Act](https://eur-lex.europa.eu/eli/reg/2024/1689/oj)
- [European Commission - AI Act and risk-based approach](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
- [AI Act Service Desk - Article 5 prohibited practices](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-5)
- [European Commission - Article 50 transparency obligations](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content)
