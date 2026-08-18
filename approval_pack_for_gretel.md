# EU AI Act Approval Pack - Gretel's Client Cases

**Consultant:** Paola Hintze  
**Purpose:** First-pass EU AI Act assessment based on the four unlabeled client briefs provided by Gretel.

## Executive summary

One proposal should be denied and redesigned, while three may proceed only with controls. Case 1 creates a continuous customer profile using cross-context behaviour and may meet the Article 5 social-scoring prohibition; its device-financing component also raises high-risk creditworthiness concerns. Case 2 is a high-risk employment system. Case 3 is an interactive AI system subject to Article 50 transparency. Case 4 is outside the high-risk categories, but the provider may still have Article 50(2) marking duties because the system generates text shown to consumers.

## Case 1 - Telecommunications customer profile

**Inferred category:** Prohibited social scoring under Article 5(1)(c); the financing component would also be high-risk.  
**Decision:** **Deny and redesign.**

**Why:** The system continuously profiles customers using payment history, complaints, cancellations, call-centre activity and public online behaviour. It then uses the score for potentially unfavourable treatment in financing, payment flexibility, offers and support. A technical override is not meaningful oversight when staff are expected to follow the recommendation.

**Lawful architecture:** Do not deploy one unified customer-value score. Separate device-financing assessment from support routing. The financing model should use only relevant financial data and require human review before an adverse result. Support routing should use the current request and urgency, not perceived customer value. Log inputs, recommendations, final decisions and overrides.

**Roles:** Assuming an external vendor supplies the system, the vendor is the provider and the telecom operator is the deployer. The operator becomes the provider if it rebrands or substantially modifies the system.

**Controls:** Remove public online behaviour; apply purpose limitation, data minimisation, risk management, data governance, technical documentation, effective oversight, logging, monitoring and a GDPR DPIA. Legal counsel should confirm whether the full Article 5 social-scoring test is met.

## Case 2 - Hospitality recruitment screening

**Inferred category:** High-risk employment system under Annex III.  
**Decision:** **Approve with controls.**

**Why:** The tool analyses and filters job applications and scores candidates. Applicants below the threshold are normally excluded before meaningful human review.

**Architecture:** Application received -> CV, form responses, skills assessment and vacancy requirements analysed -> suitability score and rationale generated -> trained recruiter reviews both positive and adverse outputs before rejection -> final decision and override logged.

**Roles:** The recruitment-software vendor is the provider and the hospitality group is the deployer, unless the group develops, rebrands or substantially modifies the system.

**Controls:** Require representative data and bias testing, risk management, technical documentation, instructions for use, automatic logging, human oversight, accuracy, robustness, cybersecurity, conformity assessment, registration and post-market monitoring. The deployer should complete a GDPR DPIA, inform applicants, monitor outcomes and provide an appeal path.

## Case 3 - Satellite-internet voice agent

**Inferred category:** Limited risk with Article 50 transparency obligations.  
**Decision:** **Approve with controls.**

**Why:** The system interacts directly with customers through a voice interface. Human escalation is available, but the brief does not confirm that callers are informed from the beginning that they are interacting with AI.

**Architecture:** Incoming call -> audible AI disclosure -> request interpretation using necessary account and service data -> approved routine answer or routing -> human handling for billing disputes, cancellations, complaints and commercial changes. Log disclosures, transfers, summaries and corrections.

**Roles:** The voice-agent vendor is the provider and the satellite-internet company is the deployer. Rebranding or substantial modification may move provider responsibility to the company.

**Controls:** Clear and accessible disclosure at the start, immediate human transfer, strict scope boundaries, data minimisation, retention limits, accuracy testing, security, monitoring and compliance with GDPR and consumer-protection rules.

## Case 4 - Marketplace review summaries

**Inferred category:** Limited risk at provider level; potentially minimal for the marketplace as deployer.  
**Decision:** **Approve with controls.**

**Why:** The system does not rank people or determine eligibility, so it is not high-risk. However, it generates synthetic text shown to consumers. Under Article 50(2), the provider may need to make the output machine-readable and detectable as AI-generated. Whether the marketplace itself has that obligation depends on the role allocation and any applicable standard-editing exception.

**Architecture:** Product reaches a sufficient review threshold -> published reviews are summarised -> quality and contradiction checks run -> source-linked summary displayed with appropriate AI notice or marking -> merchandising staff monitor and remove misleading outputs. Log source reviews, model version, output and corrections.

**Roles:** If the marketplace develops or rebrands the summariser, it is the provider and deployer. If an external product is used, the vendor is the provider and the marketplace is the deployer.

**Controls:** Confirm provider status and the standard-editing exception; implement machine-readable marking where Article 50(2) applies; preserve source links; monitor hallucinations and review manipulation; and assess GDPR and consumer-protection implications. A visible AI-summary notice is recommended as a trust control.

## Client response requested

For the debrief, please respond to the following:

1. Do you **accept**, **challenge**, or request a **redesign** for these recommendations?
2. For Case 4, do you accept the distinction between your intended minimal-risk classification and the possible Article 50(2) provider obligation?
3. What, if anything, should change after our client discussion?

## Sources

- [EU AI Act - Regulation (EU) 2024/1689](https://eur-lex.europa.eu/eli/reg/2024/1689/oj)
- [AI Act Service Desk - Article 5](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-5)
- [European Commission - AI Act risk categories](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
- [European Commission - Article 50 guidance](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content)
