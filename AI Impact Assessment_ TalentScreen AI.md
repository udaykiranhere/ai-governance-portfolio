## Section 1: System Description and Classification

System Name: TalentScreen AI

System Description: An AI-powered resume screening tool that uses natural  
language processing to analyze, rank, and filter job applications. It assigns  
each candidate a suitability score (0-100) and automatically advances  
candidates above a threshold to the interview stage.

Intended Purpose: Recruitment and selection of natural persons, specifically  
to analyse and filter job applications and to evaluate candidates.

EU AI Act Classification: High-Risk (Annex III, Area 4(a): "AI systems  
intended to be used for the recruitment or selection of natural persons, in  
particular to place targeted job advertisements, to analyse and filter job  
applications, and to evaluate candidates")

Applicable Obligations: Article 9 (Risk Management System), Article 10  
(Data Governance), Articles 13-14 (Transparency and Human Oversight),  
Article 26(7) (Worker Information)

## 

## Section 2: Stakeholder and Context Mapping (NIST AI RMF MAP)

Stakeholder and Context Mapping (NIST AI RMF MAP 1.1, MAP 5.1)

Primary Users (deployers): HR teams, hiring managers, talent acquisition  
specialists

Affected Individuals: Job applicants (candidates), including protected  
groups (based on gender, age, ethnicity, disability status)

Organizational Context: The deploying organization's mission, the specific  
roles being hired for, and the volume of applications processed

Deployment Setting: Integrated into applicant tracking system (ATS), used  
as first-pass filter before human review

Applicable Laws and Norms: EU AI Act, GDPR (data processing of personal  
data), national anti-discrimination laws, organizational diversity and inclusion policies.  
 Benefits

\- Faster processing of high-volume applications  
\- Consistency in initial screening criteria  
\- Reduced time-to-hire

 Potential Harms

\- Discriminatory filtering based on proxies for protected characteristics  
  (e.g., names, universities, gaps in employment history)  
\- Lack of transparency for rejected candidates  
\- Reduced access to employment opportunities for marginalized groups  
\- Perpetuation of historical hiring biases encoded in training data

## 

## Section 3: Risk Measurement and Evaluation (NIST AI RMF MEASURE)

### **Identified Risks by Trustworthiness Characteristic**.

* **Fairness and Bias (MEASURE 2.11)**: The system may discriminate against candidates from underrepresented groups due to biased training data from historical hiring decisions.  
* **Transparency and Accountability (MEASURE 2.8)**: Candidates cannot understand why they were rejected because the scoring algorithm is not explainable.  
* **Privacy (MEASURE 2.10)**: The system processes sensitive personal data (employment history, education, potentially inferring protected characteristics) without adequate data minimization.  
* **Validity and Reliability (MEASURE 2.5)**: The system may not generalize well across different job types, industries, or candidate populations.  
* **Safety (MEASURE 2.6)**: Incorrect rejections at scale can systematically exclude qualified candidates, causing widespread harm to livelihoods.

### **Prioritized Risk Summary**.

* **Which risks scored highest and why.** RISK-001 (Bias) and RISK-002 (Transparency) both scored 20 out of 25, making them the highest-priority risks. Bias is likely because the training data reflects decades of unequal hiring. Lack of transparency is almost certain because NLP-based scoring models are inherently difficult to explain in plain language.  
* **Which stakeholder group faces the most concentrated harm.** Job applicants from underrepresented groups bear the greatest risk. They are the ones who are filtered out by biased algorithms and simultaneously denied any explanation for the decision.  
* **How the risks interact.** Bias combined with a lack of transparency creates a compounding effect. Affected candidates cannot challenge discriminatory outcomes because they have no visibility into the reasoning behind their rejection.

### 

## 

## Section 4: Risk Treatment and Mitigation Controls (NIST AI RMF MANAGE)

 High-Priority Risk Mitigation Controls

RISK-001 — Bias

Run regular bias audits using selection rates and error rates broken down by relevant protected characteristics, where lawful. Conduct disparate impact testing before deployment. If testing reveals material disparities, investigate the cause, retrain on balanced and representative datasets, and retest before release.

EU AI Act mapping — Article 9 (Risk Management System).

 RISK-002 — Transparency

Publish a plain-language summary of the system’s logic, the main assessment criteria, and how HR uses its output. Give candidates a clear, individualized explanation of how their application was assessed. Where Article 86 applies, explain the AI system’s role and the main elements of the decision.

EU AI Act mapping — Articles 13–14 (Transparency and Human Oversight) and Article 86 (Right to Explanation of Individual Decision-Making), where applicable.

RISK-005 — Safety

Set a rejection-volume threshold for a defined period. When the threshold is exceeded, pause the affected rejections and route them to a human reviewer authorized to overturn the recommendation and record the reason. Establish a candidate appeals process with a clear submission channel, a response timeframe, and authority to correct outcomes.

EU AI Act mapping — Article 9 (Risk Management System).

Residual Risks and Escalation

For RISK-002 a public summary and an individual explanation may still leave candidates without enough information to challenge their outcome. Escalate this gap to legal counsel to confirm when Article 86 applies, what explanations should include, and how candidates can request a review. For RISK-001, small subgroup samples can mask disparities. For RISK-005, the volume threshold can miss isolated erroneous rejections, so candidates should be able to appeal even when the threshold is never reached.

## 

## Section 5: Recommendations and Ongoing Monitoring

Monitoring Frequency

Conduct quarterly bias audits and a full AI Impact Assessment (AIIA) review annually. Continuously monitor key performance metrics, including rejection rates and score distributions across demographic groups, where lawful.

Trigger Conditions

Initiate an immediate reassessment when any of the following occurs:

\- The model is retrained.  
\- The system is expanded to new job categories.  
\- A candidate submits a complaint about the system or its role in a hiring decision.  
\- Relevant regulatory guidance changes.

Accountability

The AI Governance Committee makes the final decision on whether deployment may proceed, continue, or resume. It has authority to block a launch or suspend an existing deployment if risks exceed the organization’s risk tolerance.  
