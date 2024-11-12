# Generative AI Risk Management Resources

**TL; DR**: 
- This repository contains resources to assist in the creation of technical standards or procedures for organizational AI governance policies, with a strong focus on generative AI (GAI).
- This information must be combined with a higher-level governance approach as described in, e.g., [The Interagency Guidance on Model Risk Management](https://www.federalreserve.gov/supervisionreg/srletters/sr1107a1.pdf) or the [NIST AI RMF Govern Function](https://airc.nist.gov/AI_RMF_Knowledge_Base/Playbook/Govern).
- The information below is aligned with [DRAFT NIST 600-1 AI RMF Generative AI Profile](https://airc.nist.gov/docs/NIST.AI.600-1.GenAI-Profile.ipd.pdf).
- For non-commercial use. For commercial support please reach out to `info@hallresearch.ai`.

**What's missing?**
- Higher-level policies and procedure language to tie these resources together into cohesive governance documentments.
- Methodology for estimating business risk (e.g., monetary losses) from model testing, red-teaming, feedback and experimental results.
- ...

**Introduction**

(c) Patrick Hall and Daniel Atherton 2024, CC BY 4.0

This information is designed to help organizations build the governance policies required to measure and manage risks associated with deploying and using GAI systems. Governance is key to addressing the growing need for trustworthy and responsible AI systems, and this repository is aligned to the NIST AI Risk Management Framework trustworthy characteristics and the [DRAFT NIST 600-1 AI RMF Generative AI Profile](https://airc.nist.gov/docs/NIST.AI.600-1.GenAI-Profile.ipd.pdf). Governance is also a necessary component of AI strategy, crucial for addressing real legal, regulatory, ethical, and operational headwinds. 

At its core, this repository provides technical materials for building or augmenting detailed model or AI governance procedures or standards, and aligns them to guidance from NIST. Starting in [Section A](#a-example-generative-ai-trustworthy-characteristic-crosswalk), two central risk management mechanisms are explored. The first perspective comprises the NIST AI RMF trustworthy characteristics mapped to GAI risks. Operating from this perspective allows organizations to understand how each trustworthy characteristic can mitigate specific risks posed by GAI. The second perspective is the reverse—GAI risks mapped to trustworthy characteristics. That mapping can help organizations understand which characteristics should be prioritized to manage specific GAI risks. As consumer finance organizations are likely to adopt both NIST (or other more technical frameworks) and traditional enterprise risk management methodologies, ideas on linking trustworthy characteristics, GAI risks, and established banking risk buckets are also presented in [Section A](#a-example-generative-ai-trustworthy-characteristic-crosswalk). 

The repository also guides users through authoritative resources for risk-tiering. Sections [B.1](#b1-example-adverse-impacts) through [B.7](#b7-ai-risk-management-framework-actions-aligned-to-risk-tiering) walk the user of the framework through the process of defining adverse impacts: *Harm to Operations*, *Harm to Assets*, *Harm to Individuals*, *Harm to Other Organizations*, and *Harm to the Nation*, along with guidance on impact quantification and description. [Section B](#b-example-risk-tiering-materials-for-generative-ai) also offers tables with guidance on assessing the likelihood of certain risks. Organizations and companies can leverage this combination of adverse impacts and frequency/likelihood tables to develop tailored risk tiers that reflect the specific contexts in which their GAI systems may be operating. They can also utilize practical risk-tiering to guide their decision-making and evaluate how best to calibrate existing safeguards or whether to implement additional ones. 

Measurement and testing is a critical aspect of ensuring GAI systems perform as expected. For measuring the severity of certain GAI risks, [Section C](#c-list-of-selected-model-testing-suites) presents various model testing benchmarks (such as evals). Model testing suites provide the user with tools to roughly assess GAI performance against trustworthy characteristics as well to quickly test for resilience in the face of known GAI risks. As GAI systems are vulnerable to adversarial attacks via prompting and hacks, [Section D](#d-selected-adversarial-prompting-strategies-and-attacks) presents red-teaming and adversarial prompting approaches for human elicitation of evidence of GAI risks in adversarial scenarios. [Section H](#h-example-high-risk-generative-ai-measurement-and-management-plan) hints at more in-depth structured experiments and human feedback for risk assessment. Suggested usage for these types of measurement is as follows: 

- **Low-risk GAI systems**: model testing only
- **Medium-risk GAI systems**: model testing and red-teaming
- **High-risk GAI systems**: model testing, red-teaming, and structured experiments and human feedback   

Where measurement for lower-risk systems can be highly-automated, human risk management resources are reserved for medium and high-risk systems.  

For managing and mitigating GAI risks, [Section E](#e-selected-risk-controls-for-generative-ai) outlines several risk controls for GAI.  Controls range from technical settings for GAI systems to commonsense recommendations, e.g., limiting or restricting access for minors. Sections [F](#f-example-low-risk-generative-ai-measurement-and-management-plan), G](#g-example-medium-risk-generative-ai-measurement-and-management-plan), and [H](#h-example-high-risk-generative-ai-measurement-and-management-plan) pair risk measurement techniques with controls to form more fulsome risk management plans. Recommended usage for the plans in Sections [F](#f-example-low-risk-generative-ai-measurement-and-management-plan)-[H](#h-example-high-risk-generative-ai-measurement-and-management-plan) is: 

- **Low-risk GAI systems**: apply [Section F](#f-example-low-risk-generative-ai-measurement-and-management-plan) only
- **Medium-risk GAI systems**: apply Section [F](#f-example-low-risk-generative-ai-measurement-and-management-plan) and [G](#g-example-medium-risk-generative-ai-measurement-and-management-plan)
- **High-risk GAI systems**: apply Sections [F](#f-example-low-risk-generative-ai-measurement-and-management-plan), [G](#g-example-medium-risk-generative-ai-measurement-and-management-plan), and [H](#h-example-high-risk-generative-ai-measurement-and-management-plan)  

Regardless of the risk level of the system, the framework offers detailed measurement plans that guide the user through the process of assessing the system’s performance, along with tracking risks, and harmonizing the system with trustworthy AI principles. 


## Table of Contents

* **Section A**: [Example Generative AI-Trustworthy Characteristic Crosswalk](#a-example-generative-ai-trustworthy-characteristic-crosswalk)
  * **A.1**: [Trustworthy Characteristic to Generative AI Risk Crosswalk](#a1-trustworthy-characteristic-to-generative-ai-risk-crosswalk)
  * **A.2**: [Generative AI Risk to Trustworthy Characteristic Crosswalk](#a2-generative-ai-risk-to-trustworthy-characteristic-crosswalk)
  * **A.3**: [Traditional Banking Risks, Generative AI Risks and Trustworthy Characteristics Crosswalk](#a3-traditional-banking-risks-generative-ai-risks-and-trustworthy-characteristics-crosswalk)

* **Section B**: [Example Risk-tiering Materials for Generative AI](#b-example-risk-tiering-materials-for-generative-ai)
  * **B.1**: [Example Adverse Impacts](#b1-example-adverse-impacts)
  * **B.2**: [Example Impact Descriptions](#b2-example-impact-descriptions)
  * **B.3**: [Example Likelihood Descriptions](#b3-example-likelihood-descriptions)
  * **B.4**: [Example Risk Tiers](#b4-example-risk-tiers)
  * **B.5**: [Example Risk Descriptions](#b5-example-risk-descriptions)
  * **B.6**: [Practical Risk-tiering Questions](#b6-practical-risk-tiering-questions)
  * **B.7**: [AI Risk Management Framework Actions Aligned to Risk Tiering](#b7-ai-risk-management-framework-actions-aligned-to-risk-tiering)

* **Section C**: [List of Selected Model Testing Suites](#c-list-of-selected-model-testing-suites)
  * **C.1**: [Selected Model Testing Suites Organized by Trustworthy Characteristic](#c1-selected-model-testing-suites-organized-by-trustworthy-characteristic)
  * **C.2**: [Selected Model Testing Suites Organized by Generative AI Risk](#c2-selected-model-testing-suites-organized-by-generative-ai-risk)
  * **C.3**: [AI Risk Management Framework Actions Aligned to Benchmarking](#c3-ai-risk-management-framework-actions-aligned-to-benchmarking)  

* **Section D**: [Selected Adversarial Prompting Strategies and Attacks](#d-selected-adversarial-prompting-strategies-and-attacks)
  * **D.1**: [Common AI Red-teaming Tools](#d1-common-ai-red-teaming-tools)
  * **D.2**: [Selected Adversarial Prompting Strategies and Attacks by Organized Trustworthy Characteristic](#d2-selected-adversarial-prompting-strategies-and-attacks-organized-by-trustworthy-characteristic)
  * **D.3**: [Selected Adversarial Prompting Techniques and Attacks Organized by Generative AI Risk](#d3-selected-adversarial-prompting-techniques-and-attacks-organized-by-generative-ai-risk)
  * **D.4**: [AI Risk Management Framework Actions Aligned to Red Teaming](#d4-ai-risk-management-framework-actions-aligned-to-red-teaming)  

* **Section E**: [Selected Risk Controls for Generative AI](#e-selected-risk-controls-for-generative-ai)

* **Section F**: [Example Low-risk Generative AI Measurement and Management Plan](#f-example-low-risk-generative-ai-measurement-and-management-plan)
  * **F.1**: [Example Low-risk Generative AI Measurement and Management Plan Organized by Trustworthy Characteristic](#f1-example-low-risk-generative-ai-measurement-and-management-plan-organized-by-trustworthy-characteristic)
  * **F.2**: [Example Low-risk Generative AI Measurement and Management Plan Organized by Generative AI Risk](#f2-example-low-risk-generative-ai-measurement-and-management-plan-organized-by-generative-ai-risk)

* **Section G**: [Example Medium-risk Generative AI Measurement and Management Plan](#g-example-medium-risk-generative-ai-measurement-and-management-plan)
  * **G.1**: [Example Medium-risk Generative AI Measurement and Management Plan Organized by Trustworthy Characteristic](#g1-example-medium-risk-generative-ai-measurement-and-management-plan-organized-by-trustworthy-characteristic)
  * **G.2**: [Example Medium-risk Generative AI Measurement and Management Plan Organized by Generative AI Risk](#g2-example-medium-risk-generative-ai-measurement-and-management-plan-organized-by-generative-ai-risk)

* **Section H**: [Example High-risk Generative AI Measurement and Management Plan](#h-example-high-risk-generative-ai-measurement-and-management-plan)
  * **H.1**: [Example High-risk Generative AI Measurement and Management Plan Organized by Trustworthy Characteristic](#h1-example-high-risk-generative-ai-measurement-and-management-plan-organized-by-trustworthy-characteristic)
  * **H.2**: [Example High-risk Generative AI Measurement and Management Plan Organized by Generative AI Risk](#h2-example-high-risk-generative-ai-measurement-and-management-plan-organized-by-generative-ai-risk)

***

## A: Example Generative AI-Trustworthy Characteristic Crosswalk

### A.1: Trustworthy Characteristic to Generative AI Risk Crosswalk

<table>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Accountable and Transparent</strong></th>
<th style="text-align: left;"><strong>Explainable and Interpretable</strong></th>
<th style="text-align: left;"><strong>Fair with Harmful Bias Managed</strong></th>
<th style="text-align: left;"><strong>Privacy Enhanced</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Data Privacy</td>
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;">Confabulation</td>
<td style="text-align: left;">Data Privacy</td>
</tr>
<tr class="even">
<td style="text-align: left;">Environmental</td>
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;">Environmental</td>
<td style="text-align: left;">Human-AI Configuration</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;">Information Security</td>
</tr>
<tr class="even">
<td style="text-align: left;">Information Integrity</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Intellectual Property</td>
<td style="text-align: left;">Intellectual Property</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Intellectual Property</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Obscene, Degrading, and/or Abusive Content</td>
<td style="text-align: left;">Value Chain and Component Integration</td>
</tr>
<tr class="even">
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Toxicity, Bias, and Homogenization</td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;"></td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Safe</strong></th>
<th style="text-align: left;"><strong>Secure and Resilient</strong></th>
<th style="text-align: left;"><strong>Valid and Reliable</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">CBRN Information</td>
<td style="text-align: left;">Dangerous or Violent Recommendations</td>
<td style="text-align: left;">Confabulation</td>
</tr>
<tr class="even">
<td style="text-align: left;">Confabulation</td>
<td style="text-align: left;">Data Privacy</td>
<td style="text-align: left;">Human-AI Configuration</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Dangerous or Violent Recommendations</td>
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;">Information Integrity</td>
</tr>
<tr class="even">
<td style="text-align: left;">Data Privacy</td>
<td style="text-align: left;">Information Security</td>
<td style="text-align: left;">Information Security</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Environmental</td>
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;">Toxicity, Bias, and Homogenization</td>
</tr>
<tr class="even">
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Value Chain and Component Integration</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Information Integrity</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">Information Security</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Obscene, Degrading, and/or Abusive Content</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
</tbody>
</table>

**Usage Note**: Table A.1 provides an example of mapping GAI risks onto AI RMF trustworthy characteristics. Mapping GAI risks to AI RMF trustworthy characteristics can be particularly useful when existing policies, processes, or controls can be applied to manage GAI risks, but have been previously implemented in alignment with the AI RMF trustworthy characteristics. Many mappings are possible. Mappings that differ from the example may be more appropriate to meet a particular organization's risk management goals.

### A.2: Generative AI Risk to Trustworthy Characteristic Crosswalk
<table>
<caption>Table A.2: Generative AI Risk to Trustworthy Characteristic Crosswalk.</caption>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>CBRN Information</strong></th>
<th style="text-align: left;"><strong>Confabulation</strong></th>
<th style="text-align: left;"><strong>Dangerous or Violent Recommendations</strong></th>
<th style="text-align: left;"><strong>Data Privacy</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Safe</td>
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Safe</td>
<td style="text-align: left;">Accountable and Transparent</td>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;">Safe</td>
<td style="text-align: left;">Secure and Resilient</td>
<td style="text-align: left;">Privacy Enhanced</td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Safe</td>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Secure and Resilient</td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Environmental</strong></th>
<th style="text-align: left;"><strong>Human-AI Configuration</strong></th>
<th style="text-align: left;"><strong>Information Integrity</strong></th>
<th style="text-align: left;"><strong>Information Security</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Privacy Enhanced</td>
</tr>
<tr class="even">
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Explainable and Interpretable</td>
<td style="text-align: left;">Safe</td>
<td style="text-align: left;">Safe</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Safe</td>
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;">Secure and Resilient</td>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;">Privacy Enhanced</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Valid and Reliable</td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;">Safe</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;">Secure and Resilient</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Intellectual Property</strong></th>
<th style="text-align: left;"><strong>Obscene, Degrading, and/or Abusive Content</strong></th>
<th style="text-align: left;"><strong>Toxicity, Bias, and Homogenization</strong></th>
<th style="text-align: left;"><strong>Value Chain and Component Integration</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Accountable and Transparent</td>
</tr>
<tr class="even">
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Safe</td>
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;">Explainable and Interpretable</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Privacy Enhanced</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Privacy Enhanced</td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Safe</td>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Secure and Resilient</td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Valid and Reliable</td>
</tr>
</tbody>
</table>

**Usage Note**: Table A.2 provides an example of mapping AI RMF trustworthy characteristics onto GAI risks. Mapping AI RMF trustworthy characteristics to GAI risks can assist organizations in aligning GAI guidance to existing AI/ML policies, processes, or controls or to extend GAI guidance to address additional AI/ML technologies. Many mappings are possible. Mappings that differ from the example may be more appropriate to meet a particular organization's risk management goals.

### A.3: Traditional Banking Risks, Generative AI Risks and Trustworthy Characteristics Crosswalk

<table>
<caption>Table A.3: Traditional Banking Risks, Generative AI Risks and Trustworthy Characteristics Crosswalk.</caption>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Compliance Risk</strong></th>
<th style="text-align: left;"><strong>Information Security Risk</strong></th>
<th style="text-align: left;"><strong>Legal Risk</strong></th>
<th style="text-align: left;"><strong>Model Risk</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Data Privacy</td>
<td style="text-align: left;">Data Privacy</td>
<td style="text-align: left;">Intellectual Property</td>
<td style="text-align: left;">Confabulation</td>
</tr>
<tr class="even">
<td style="text-align: left;">Information Security</td>
<td style="text-align: left;">Information Security</td>
<td style="text-align: left;">Obscene, Degrading, and/or Abusive Content</td>
<td style="text-align: left;">Dangerous or Violent Recommendations</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Toxicity, Bias, and Homogenization</td>
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;">Information Integrity</td>
</tr>
<tr class="even">
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Obscene, Degrading, and/or Abusive Content</td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Toxicity, Bias, and Homogenization</td>
</tr>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Privacy Enhanced</td>
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Valid and Reliable</td>
</tr>
<tr class="even">
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Secure and Resilient</td>
<td style="text-align: left;">Safe</td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Privacy Enhanced</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">Secure and Resilient</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Operational Risk</strong></th>
<th style="text-align: left;"><strong>Reputational Risk</strong></th>
<th style="text-align: left;"><strong>Strategic Risk</strong></th>
<th style="text-align: left;"><strong>Third Party Risk</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Confabulation</td>
<td style="text-align: left;">Confabulation</td>
<td style="text-align: left;">Environmental</td>
<td style="text-align: left;">Information Integrity</td>
</tr>
<tr class="even">
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;">Dangerous or Violent Recommendations</td>
<td style="text-align: left;">Information Integrity</td>
<td style="text-align: left;">Value Chain and Component Integration</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Information Security</td>
<td style="text-align: left;">Environmental</td>
<td style="text-align: left;">Information Security</td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;">Information Integrity</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;">Obscene, Degrading, and/or Abusive Content</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"></td>
<td style="text-align: left;">Toxicity, Bias, and Homogenization</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
</tr>
<tr class="even">
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Safe</td>
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;">Accountable and Transparent</td>
</tr>
<tr class="even">
<td style="text-align: left;">Secure and Resilient</td>
<td style="text-align: left;">Fair with Harmful Bias Managed</td>
<td style="text-align: left;">Secure and Resilient</td>
<td style="text-align: left;">Explainable and Interpretable</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;"></td>
</tr>
</tbody>
</table>

**Usage Note**: Table A.3 provides an example of mapping GAI risks and AI RMF trustworthy characteristics. This type of mapping can enable incorporation of new AI guidance into existing policies, processes, or controls or the application of existing policies, processes, or controls to newer AI risks.

## B: Example Risk-tiering Materials for Generative AI

### B.1: Example Adverse Impacts

<table style="width:95%;">
<caption>Table B.1: Example adverse impacts, adapted from NIST 800-30r1 Table H-2 <a href="#national-institute-of-standards-and-technology-nist-guide-for-conducting-risk-assessments-nist-special-publication-800-30-rev-1-prepared-by-the-joint-task-force-transformation-initiative-gaithersburg-md-nist-september-2012-httpsdoiorg106028nistsp800-30r1">[NIST Special Publication 800-30 Rev. 1]</a>.</caption>
<colgroup>
<col style="width: 20%" />
<col style="width: 75%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Level</strong></th>
<th style="text-align: left;"><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Harm to Operations</td>
<td style="text-align: left;"><ul>
<li><p>Inability to perform current missions/business functions.</p>
<ul>
<li><p>In a sufficiently timely manner.</p></li>
<li><p>With sufficient confidence and/or correctness.</p></li>
<li><p>Within planned resource constraints.</p></li>
</ul></li>
<li><p>Inability, or limited ability, to perform missions/business functions in the future.</p>
<ul>
<li><p>Inability to restore missions/business functions.</p></li>
<li><p>In a sufficiently timely manner.</p></li>
<li><p>With sufficient confidence and/or correctness.</p></li>
<li><p>Within planned resource constraints.</p></li>
</ul></li>
<li><p>Harms (e.g., financial costs, sanctions) due to noncompliance.</p>
<ul>
<li><p>With applicable laws or regulations.</p></li>
<li><p>With contractual requirements or other requirements in other binding agreements (e.g., liability).</p></li>
</ul></li>
<li><p>Direct financial costs.</p></li>
<li><p>Reputational harms.</p>
<ul>
<li><p>Damage to trust relationships.</p></li>
<li><p>Damage to image or reputation (and hence future or potential trust relationships).</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Harm to Assets</td>
<td style="text-align: left;"><ul>
<li><p>Damage to or loss of physical facilities.</p></li>
<li><p>Damage to or loss of information systems or networks.</p></li>
<li><p>Damage to or loss of information technology or equipment.</p></li>
<li><p>Damage to or loss of component parts or supplies.</p></li>
<li><p>Damage to or of loss of information assets.</p></li>
<li><p>Loss of intellectual property.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Harm to Individuals</td>
<td style="text-align: left;"><ul>
<li><p>Injury or loss of life.</p></li>
<li><p>Physical or psychological mistreatment.</p></li>
<li><p>Identity theft.</p></li>
<li><p>Loss of personally identifiable information.</p></li>
<li><p>Damage to image or reputation.</p></li>
<li><p>Infringement of intellectual property rights.</p></li>
<li><p>Financial harm or loss of income.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Harm to Other Organizations</td>
<td style="text-align: left;"><ul>
<li><p>Harms (e.g., financial costs, sanctions) due to noncompliance.</p>
<ul>
<li><p>With applicable laws or regulations.</p></li>
<li><p>With contractual requirements or other requirements in other binding agreements (e.g., liability).</p></li>
</ul></li>
<li><p>Direct financial costs.</p></li>
<li><p>Reputational harms.</p>
<ul>
<li><p>Damage to trust relationships.</p></li>
<li><p>Damage to image or reputation (and hence future or potential trust relationships).</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Harm to the Nation</td>
<td style="text-align: left;"><ul>
<li><p>Damage to or incapacitation of critical infrastructure.</p></li>
<li><p>Loss of government continuity of operations.</p></li>
<li><p>Reputational harms.</p>
<ul>
<li><p>Damage to trust relationships with other governments or with nongovernmental entities.</p></li>
<li><p>Damage to national reputation (and hence future or potential trust relationships).</p></li>
</ul></li>
<li><p>Damage to current or future ability to achieve national objectives.</p>
<ul>
<li><p>Harm to national security.</p></li>
</ul></li>
<li><p>Large-scale economic or workforce displacement.</p></li>
</ul></td>
</tr>
</tbody>
</table>

### B.2 Example Impact Descriptions

<table style="width:85%;">
<caption>Table B.2: Example Impact level descriptions, adapted from NIST SP800-30r1 Appendix H, Table H-3 <a href="#national-institute-of-standards-and-technology-nist-guide-for-conducting-risk-assessments-nist-special-publication-800-30-rev-1-prepared-by-the-joint-task-force-transformation-initiative-gaithersburg-md-nist-september-2012-httpsdoiorg106028nistsp800-30r1">[NIST Special Publication 800-30 Rev. 1]</a>.</caption>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 5%" />
<col style="width: 40%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Qualitative Values</strong></th>
<th style="text-align: left;"></th>
<th style="text-align: left;"><strong>Description</strong></th>
<th style="text-align: left;"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Very High</td>
<td style="text-align: left;">96-100</td>
<td style="text-align: left;">10</td>
<td style="text-align: left;">An incident could be expected to have multiple severe or catastrophic adverse effects on organizational operations, organizational assets, individuals, other organizations, or the Nation.</td>
</tr>
<tr class="even">
<td style="text-align: left;">High</td>
<td style="text-align: left;">80-95</td>
<td style="text-align: left;">8</td>
<td style="text-align: left;">An incident could be expected to have a severe or catastrophic adverse effect on organizational operations, organizational assets, individuals, other organizations, or the Nation. A severe or catastrophic adverse effect means that, for example, the incident might: (i) cause a severe degradation in or loss of mission capability to an extent and duration that the organization is not able to perform one or more of its primary functions; (ii) result in major damage to organizational assets; (iii) result in major financial loss; or (iv) result in severe or catastrophic harm to individuals involving loss of life or serious life-threatening injuries.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Moderate</td>
<td style="text-align: left;">21-79</td>
<td style="text-align: left;">5</td>
<td style="text-align: left;">An incident could be expected to have a serious adverse effect on organizational operations, organizational assets, individuals other organizations, or the Nation. A serious adverse effect means that, for example, the incident might: (i) cause a significant degradation in mission capability to an extent and duration that the organization is able to perform its primary functions, but the effectiveness of the functions is significantly reduced; (ii) result in significant damage to organizational assets; (iii) result in significant financial loss; or (iv) result in significant harm to individuals that does not involve loss of life or serious life-threatening injuries.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Low</td>
<td style="text-align: left;">5-20</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">An incident could be expected to have a limited adverse effect on organizational operations, organizational assets, individuals other organizations, or the Nation. A limited adverse effect means that, for example, the incident might: (i) cause a degradation in mission capability to an extent and duration that the organization is able to perform its primary functions, but the effectiveness of the functions is noticeably reduced; (ii) result in minor damage to organizational assets; (iii) result in minor financial loss; or (iv) result in minor harm to individuals.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Very Low</td>
<td style="text-align: left;">0-4</td>
<td style="text-align: left;">0</td>
<td style="text-align: left;">An incident could be expected to have a negligible adverse effect on organizational operations, organizational assets, individuals other organizations, or the Nation.</td>
</tr>
</tbody>
</table>

### B.3 Example Likelihood Descriptions

<table style="width:85%;">
<caption>Table B.3: Example likelihood levels, adapted from NIST SP800-30r1 Appendix G, Table G-3 <a href="#national-institute-of-standards-and-technology-nist-guide-for-conducting-risk-assessments-nist-special-publication-800-30-rev-1-prepared-by-the-joint-task-force-transformation-initiative-gaithersburg-md-nist-september-2012-httpsdoiorg106028nistsp800-30r1">[NIST Special Publication 800-30 Rev. 1]</a>.</caption>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 5%" />
<col style="width: 40%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Qualitative Values</strong></th>
<th style="text-align: left;"></th>
<th style="text-align: left;"><strong>Description</strong></th>
<th style="text-align: left;"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Very High</td>
<td style="text-align: left;">96-100</td>
<td style="text-align: left;">10</td>
<td style="text-align: left;">An incident is almost certain to occur; or the likelihood of the incident is near 100% across one week; or the incident occurs more than 100 times a year. </td>
</tr>
<tr class="even">
<td style="text-align: left;">High</td>
<td style="text-align: left;">80-95</td>
<td style="text-align: left;">8</td>
<td style="text-align: left;">An incident is highly likely to occur; or the likelihood of the incident is over 80% across one month; or occurs between 10-100 times a year.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Moderate</td>
<td style="text-align: left;">21-79</td>
<td style="text-align: left;">5</td>
<td style="text-align: left;">An incident is somewhat likely to occur; or the likelihood of the incident is greater than 80% across one calendar year; or occurs between 1-10 times a year.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Low</td>
<td style="text-align: left;">5-20</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">An incident is unlikely to occur; or the likelihood of an incident is less than 80% across one calendar year; or occurs less than once a year, but more than once every 10 years.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Very Low</td>
<td style="text-align: left;">0-4</td>
<td style="text-align: left;">0</td>
<td style="text-align: left;">An incident is highly unlikely to occur; or the likelihood of an incident is less than 10% across one calendar year; or occurs less than once every 10 years.</td>
</tr>
</tbody>
</table>

### B.4 Example Risk Tiers

<table>
<caption>Table B.4: Example risk assessment matrix with 5 impact levels, 5 likelihood levels, and 5 risk tiers, adapted from NIST SP800-30r1 Appendix I, Table I-2 <a href="#national-institute-of-standards-and-technology-nist-guide-for-conducting-risk-assessments-nist-special-publication-800-30-rev-1-prepared-by-the-joint-task-force-transformation-initiative-gaithersburg-md-nist-september-2012-httpsdoiorg106028nistsp800-30r1">[NIST Special Publication 800-30 Rev. 1]</a>.</caption>
<tbody>
<tr>
<th style="text-align: center;" rowspan="2">Likelihood</th><th colspan="5" style="text-align: center;">Level of Impact</th>
</tr>
<tr class="even">
<td style="text-align: center;"><strong>Very Low</strong></td>
<td style="text-align: center;"><strong>Low</strong></td>
<td style="text-align: center;"><strong>Moderate</strong></td>
<td style="text-align: center;"><strong>High</strong></td>
<td style="text-align: center;"><strong>Very High</strong></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><strong>Very High</strong></td>
<td style="text-align: center;">Very Low (Tier 5)</td>
<td style="text-align: center;">Low (Tier 4)</td>
<td style="text-align: center;">Moderate (Tier 3)</td>
<td style="text-align: center;">High (Tier 2)</td>
<td style="text-align: center;">Very High (Tier 1)</td>
</tr>
<tr class="even">
<td style="text-align: center;"><strong>High</strong></td>
<td style="text-align: center;">Very Low (Tier 5)</td>
<td style="text-align: center;">Low (Tier 4)</td>
<td style="text-align: center;">Moderate (Tier 3)</td>
<td style="text-align: center;">High (Tier 2)</td>
<td style="text-align: center;">Very High (Tier 1)</td>
</tr>
<tr class="odd">
<td style="text-align: center;"><strong>Moderate</strong></td>
<td style="text-align: center;">Very Low (Tier 5)</td>
<td style="text-align: center;">Low (Tier 4)</td>
<td style="text-align: center;">Moderate (Tier 3)</td>
<td style="text-align: center;">Moderate (Tier 3)</td>
<td style="text-align: center;">High (Tier 2)</td>
</tr>
<tr class="even">
<td style="text-align: center;"><strong>Low</strong></td>
<td style="text-align: center;">Very Low (Tier 5)</td>
<td style="text-align: center;">Low (Tier 4)</td>
<td style="text-align: center;">Low (Tier 4)</td>
<td style="text-align: center;">Low (Tier 4)</td>
<td style="text-align: center;">Moderate (Tier 3)</td>
</tr>
<tr class="odd">
<td style="text-align: center;"><strong>Very Low</strong></td>
<td style="text-align: center;">Very Low (Tier 5)</td>
<td style="text-align: center;">Very Low (Tier 5)</td>
<td style="text-align: center;">Very Low (Tier 5)</td>
<td style="text-align: center;">Low (Tier 4)</td>
<td style="text-align: center;">Low (Tier 4)</td>
</tr>
</tbody>
</table>

### B.5 Example Risk Descriptions

<table style="width:85%;">
<caption>Table B.5: Example risk descriptions, adapted from NIST SP800-30r1 Appendix I, Table I-3 <a href="#national-institute-of-standards-and-technology-nist-guide-for-conducting-risk-assessments-nist-special-publication-800-30-rev-1-prepared-by-the-joint-task-force-transformation-initiative-gaithersburg-md-nist-september-2012-httpsdoiorg106028nistsp800-30r1">[NIST Special Publication 800-30 Rev. 1]</a>.</caption>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 5%" />
<col style="width: 40%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Qualitative Values</strong></th>
<th style="text-align: left;"></th>
<th style="text-align: left;"><strong>Description</strong></th>
<th style="text-align: left;"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Very High</td>
<td style="text-align: left;">96-100</td>
<td style="text-align: left;">10</td>
<td style="text-align: left;">Very high risk means that an incident could be expected to have multiple severe or catastrophic adverse effects on organizational operations, organizational assets, individuals, other organizations, or the Nation.</td>
</tr>
<tr class="even">
<td style="text-align: left;">High</td>
<td style="text-align: left;">80-95</td>
<td style="text-align: left;">8</td>
<td style="text-align: left;">High risk means that an incident could be expected to have a severe or catastrophic adverse effect on organizational operations, organizational assets, individuals, other organizations, or the Nation.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Moderate</td>
<td style="text-align: left;">21-79</td>
<td style="text-align: left;">5</td>
<td style="text-align: left;">Moderate risk means that an incident could be expected to have a serious adverse effect on organizational operations, organizational assets, individuals, other organizations, or the Nation.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Low</td>
<td style="text-align: left;">5-20</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">Low risk means that an incident could be expected to have a limited adverse effect on organizational operations, organizational assets, individuals, other organizations, or the Nation.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Very Low</td>
<td style="text-align: left;">0-4</td>
<td style="text-align: left;">0</td>
<td style="text-align: left;">Very low risk means that an incident could be expected to have a negligible adverse effect on organizational operations, organizational assets, individuals, other organizations, or the Nation.</td>
</tr>
</tbody>
</table>

### B.6: Practical Risk-tiering Questions

**B.6.1: Confabulation**: How likely are system outputs to contain errors? What are the impacts if errors occur?

**B.6.2: Dangerous and Violent Recommendations**: How likely is the system to give dangerous or violent recommendations? What are the impacts if it does?

**B.6.3: Data Privacy**: How likely is someone to enter sensitive data into the system? What are the impacts if this occurs? Are standard data privacy controls applied to the system to mitigate potential adverse impacts?

**B.6.4: Human-AI Configuration**: How likely is someone to use the system incorrectly or abuse it? How likely is use for decision-making? What are the impacts of incorrect use or abuse? What are the impacts of invalid or unreliable decision-making?

**B.6.5: Information Integrity**: How likely is the system to generate deepfakes or mis or disinformation? At what scale? Are content provenance mechanisms applied to system outputs? What are the impacts of generating deepfakes or mis or disinformation? Without controls for content provenance?

**B.6.6: Information Security**: How likely are system resources to be breached or exfiltrated? How likely is the system to be used in the generation of phishing or malware content? What are the impacts in these cases? Are standard information security controls applied to the system to mitigate potential adverse impacts?

**B.6.7: Intellectual Property**: How likely are system outputs to contain other entities' intellectual property? What are the impacts if this occurs?

**B.6.8: Toxicity, Bias, and Homogenization**: How likely are system outputs to be biased, toxic, homogenizing or otherwise obscene? How likely are system outputs to be used as subsequent training inputs? What are the impacts of these scenarios? Are standard nondiscrimination controls applied to mitigate potential adverse impacts? Is the application accessible to all user groups? What are the impacts if the system is not accessible to all user groups?

**B.6.9: Value Chain and Component Integration**: Are contracts relating to the system reviewed for legal risks? Are standard acquisition/procurement controls applied to mitigate potential adverse
impacts? Do vendors provide incident response with guaranteed response times? What are the impacts if these conditions are not met?

### B.7: AI Risk Management Framework Actions Aligned to Risk Tiering

GOVERN 1.3, GOVERN 1.5, GOVERN 2.3, GOVERN 3.2, GOVERN 4.1, GOVERN 5.2, GOVERN 6.1, MANAGE 1.2, MANAGE 1.3, MANAGE 2.1, MANAGE 2.2, MANAGE 2.3, MANAGE 2.4, MANAGE 3.1, MANAGE 3.2, MANAGE 4.1, MAP 1.1, MAP 1.5, MEASURE 2.6

**Usage Note**: Materials in Section B can be used to create or update
risk tiers or other risk assessment tools for GAI systems or
applications as follows:

-   Table B.1 can enable mapping of GAI risks and impacts.

-   Table B.2 can enable quantification of impacts for risk tiering or
    risk assessment.

-   Table B.3 can enable quantification of likelihood for risk tiering
    or risk assessment.

-   Table B.4 presents an example of combining assessed impact and
    likelihood into risk tiers.

-   Table B.5 presents example risk tiers with associated qualitative,
    semi-quantitative, and quantitative values for risk tiering or risk
    assessment.

-   Subsection B.6 presents example questions for qualitative risk
    assessment.

-   Subsection B.7 highlights subcategories to indicate alignment with
    the AI RMF.

## C: List of Selected Model Testing Suites

### C.1: Selected Model Testing Suites Organized by Trustworthy Characteristic
Adapted from <a href="#ai-verify-foundation-and-infocomm-media-development-authority-cataloguing-llm-evaluations-draft-for-discussion-october-2023-httpsaiverifyfoundationsgdownloadscataloguing_llm_evaluationspdf">[AI Verify Foundation]</a> Taxonimization and various additional resources.

**Accountable and Transparent**\
An Evaluation on Large Language Model Outputs: Discourse and Memorization (see Appendix B) <a href="#de-wynter-adrian-xun-wang-alex-sokolov-qilong-gu-and-si-qing-chen-an-evaluation-on-large-language-model-outputs-discourse-and-memorization-natural-language-processing-journal-4-september-2023-100024-httpsdoiorg101016jnlp2023100024">[De Wynter et al.]</a>\
Big-bench: Truthfulness <a href="#srivastava-aarohi-abhinav-rastogi-abhishek-rao-abu-awal-md-shoeb-abubakar-abid-adam-fisch-adam-r-brown-adam-santoro-et-al-beyond-the-imitation-game-quantifying-and-extrapolating-the-capabilities-of-language-models-arxiv-preprint-last-revised-june-12-2023-httpsdoiorg1048550arxiv220604615">[Srivastava et al.]</a>\
DecodingTrust: Machine Ethics <a href="#wang-boxin-weixin-chen-hengzhi-pei-chulin-xie-mintong-kang-chenhui-zhang-chejian-xu-zidi-xiong-ritik-dutta-rylan-schaeffer-et-al-decodingtrust-a-comprehensive-assessment-of-trustworthiness-in-gpt-models-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-1361-3123231339-published-may-30-2024-httpsdlacmorgdoi10555536661223667483">[Wang et al.]</a>\
Evaluation Harness: ETHICS <a href="#gao-leo-jonathan-tow-baber-abbasi-stella-biderman-sid-black-anthony-dipofi-charles-foster-laurence-golding-jeffrey-hsu-alain-le-noach-haonan-li-kyle-mcdonell-niklas-muennighoff-chris-ociepa-jason-phang-laria-reynolds-hailey-schoelkopf-aviya-skowron-lintang-sutawika-eric-tang-anish-thite-ben-wang-kevin-wang-and-andy-zou-a-framework-for-few-shot-language-model-evaluation-github-repository-accessed-september-19-2024-httpsgithubcomeleutherailm-evaluation-harness">[Gao et al.]</a>\
HELM: Copyright <a href="#bommasani-rishi-percy-liang-and-tony-lee-holistic-evaluation-of-language-models-annals-of-the-new-york-academy-of-sciences-1525-no-1-july-2023-140146-httpsdoiorg101111nyas15007">[Bommasani et al.]</a>\
Mark My Words <a href="#piet-julien-chawin-sitawarin-vivian-fang-norman-mu-and-david-wagner-mark-my-words-analyzing-and-evaluating-language-model-watermarks-arxiv-preprint-last-revised-december-7-2023-httpsdoiorg1048550arxiv231200273">[Piet et al.]</a>

**Fair with Harmful Bias Managed**\
BELEBELE <a href="#bandarkar-lucas-davis-liang-benjamin-muller-mikel-artetxe-satya-narayan-shukla-donald-husa-naman-goyal-abhinandan-krishnan-luke-zettlemoyer-and-madian-khabsa-the-belebele-benchmark-a-parallel-reading-comprehension-dataset-in-122-language-variants-arxiv-preprint-last-revised-july-25-2024-httpsdoiorg1048550arxiv230816884">[Bandarkar et al.]</a>\
Big-bench: Low-resource language, Non-English, Translation\
Big-bench: Social bias, Racial bias, Gender bias, Religious bias\
Big-bench: Toxicity\
DecodingTrust: Fairness\
DecodingTrust: Stereotype Bias\
DecodingTrust: Toxicity\
C-Eval (Chinese evaluation suite) <a href="#huang-yuzhen-yuzhuo-bai-zhihao-zhu-junlei-zhang-jinghan-zhang-tangjun-su-junteng-liu-chuancheng-lv-yikai-zhang-jiayi-lei-yao-fu-maosong-sun-and-junxian-he-c-eval-a-multi-level-multi-discipline-chinese-evaluation-suite-for-foundation-models-arxiv-preprint-last-revised-november-6-2023-httpsdoiorg1048550arxiv230508322">[Huang, Yuzhen et al.]</a>\
Evaluation Harness: CrowS-Pairs\
Evaluation Harness: ToxiGen\
Finding New Biases in Language Models with a Holistic Descriptor Dataset <a href="#smith-eric-michael-melissa-hall-melanie-kambadur-eleonora-presani-and-adina-williams-im-sorry-to-hear-that-finding-new-biases-in-language-models-with-a-holistic-descriptor-dataset-arxiv-preprint-last-revised-october-27-2022-httpsdoiorg1048550arxiv220509209">[Smith et al.]</a>\
From Pretraining Data to Language Models to Downstream Tasks: Tracking the Trails of Political Biases Leading to Unfair NLP Models <a href="#feng-shangbin-chan-young-park-yuhan-liu-and-yulia-tsvetkov-from-pretraining-data-to-language-models-to-downstream-tasks-tracking-the-trails-of-political-biases-leading-to-unfair-nlp-models-arxiv-preprint-last-revised-july-6-2023-httpsdoiorg1048550arxiv230508283">[Feng et al.]</a>\
HELM: Bias\
HELM: Toxicity\
MT-bench <a href="#zheng-lianmin-wei-lin-chiang-ying-sheng-siyuan-zhuang-zhanghao-wu-yonghao-zhuang-zi-lin-zhuohan-li-dacheng-li-and-eric-p-xing-judging-llm-as-a-judge-with-mt-bench-and-chatbot-arena-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-2020-4659546623-published-may-30-2024-httpsdlacmorgdoi10555536661223668142">[Zheng et al.]</a>\
The Self-Perception and Political Biases of ChatGPT <a href="#rutinowski-jérôme-sven-franke-jan-endendyk-ina-dormuth-moritz-roidl-and-markus-pauly-the-self-perception-and-political-biases-of-chatgpt-human-behavior-and-emerging-technologies-2024-httpsdoiorg10115520247115633">[Rutinowski et al.]</a>\
Towards Measuring the Representation of Subjective Global Opinions in Language Models <a href="#durmus-esin-karina-nguyen-thomas-i-liao-nicholas-schiefer-amanda-askell-anton-bakhtin-carol-chen-zac-hatfield-dodds-et-al-towards-measuring-the-representation-of-subjective-global-opinions-in-language-models-arxiv-preprint-last-revised-april-12-2024-httpsdoiorg1048550arxiv230616388">[Durmus et al.]</a>

**Privacy Enhanced**\
HELM: Copyright\
llmprivacy <a href="#staab-robin-mark-vero-mislav-balunović-and-martin-vechev-beyond-memorization-violating-privacy-via-inference-with-large-language-models-arxiv-preprint-last-revised-may-6-2024-httpsdoiorg1048550arxiv231007298">[Staab et al.]</a>\
mimir <a href="#duan-michael-anshuman-suri-niloofar-mireshghallah-sewon-min-weijia-shi-luke-zettlemoyer-yulia-tsvetkov-yejin-choi-david-evans-and-hannaneh-hajishirzi-do-membership-inference-attacks-work-on-large-language-models-arxiv-preprint-last-revised-september-16-2024-httpsdoiorg1048550arxiv240207841">[Duan et al.]</a>

**Safe**\
Big-bench: Convince Me\
Big-bench: Truthfulness <a href="#srivastava-aarohi-abhinav-rastogi-abhishek-rao-abu-awal-md-shoeb-abubakar-abid-adam-fisch-adam-r-brown-adam-santoro-et-al-beyond-the-imitation-game-quantifying-and-extrapolating-the-capabilities-of-language-models-arxiv-preprint-last-revised-june-12-2023-httpsdoiorg1048550arxiv220604615">[Srivastava et al.]</a>\
HELM: Reiteration, Wedging\
Mark My Words <a href="#piet-julien-chawin-sitawarin-vivian-fang-norman-mu-and-david-wagner-mark-my-words-analyzing-and-evaluating-language-model-watermarks-arxiv-preprint-last-revised-december-7-2023-httpsdoiorg1048550arxiv231200273">[Piet et al.]</a>\
MLCommons <a href="#vidgen-bertie-adarsh-agrawal-ahmed-m-ahmed-victor-akinwande-namir-al-nuaimi-najla-alfaraj-elie-alhajjar-et-al-introducing-v05-of-the-ai-safety-benchmark-from-mlcommons-arxiv-preprint-last-revised-may-13-2024-httpsdoiorg1048550arxiv240412241">[Vidgen et al.]</a>\
The WMDP Benchmark <a href="#li-nathaniel-alexander-pan-anjali-gopal-summer-yue-daniel-berrios-alice-gatti-justin-d-li-ann-kathrin-dombrowski-et-al-the-wmdp-benchmark-measuring-and-reducing-malicious-use-with-unlearning-arxiv-preprint-last-revised-may-15-2024-httpsdoiorg1048550arxiv240303218">[Li et al.]</a>

**Secure and Resilient**\
Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation <a href="#huang-yangsibo-samyak-gupta-mengzhou-xia-kai-li-and-danqi-chen-catastrophic-jailbreak-of-open-source-llms-via-exploiting-generation-iclr-2024-spotlight-published-january-16-2024-last-modified-march-15-2024-httpsopenreviewnetforumidr42tsschph">[Huang, Yangsibo et al.]</a>\
detect-pretrain-code <a href="#shi-weijia-anirudh-ajith-mengzhou-xia-yangsibo-huang-daogao-liu-terra-blevins-danqi-chen-and-luke-zettlemoyer-detecting-pretraining-data-from-large-language-models-arxiv-preprint-last-revised-march-9-2024-httpsdoiorg1048550arxiv231016789">[Shi et al.]</a>\
Garak: encoding, knownbadsignatures, malwaregen, packagehallucination,
xss <a href="#derczynski-leon-erick-galinkin-jeffrey-martin-subho-majumdar-and-nanna-inie-garak-a-framework-for-security-probing-large-language-models-arxiv-preprint-submitted-june-16-2024-httpsdoiorg1048550arxiv240611036">[Derczynski et al.]</a>\
In-The-Wild Jailbreak Prompts on LLMs <a href="#shen-xinyue-zeyuan-chen-michael-backes-yun-shen-and-yang-zhang-do-anything-now-characterizing-and-evaluating-in-the-wild-jailbreak-prompts-on-large-language-models-arxiv-preprint-last-revised-may-15-2024-httpsdoiorg1048550arxiv230803825">[Shen et al.]</a>\
JailbreakingLLMs <a href="#chao-patrick-alexander-robey-edgar-dobriban-hamed-hassani-george-j-pappas-and-eric-wong-jailbreaking-black-box-large-language-models-in-twenty-queries-arxiv-preprint-last-revised-july-18-2024-httpsdoiorg1048550arxiv231008419">[Chao et al.]</a>\
llmprivacy <a href="#staab-robin-mark-vero-mislav-balunović-and-martin-vechev-beyond-memorization-violating-privacy-via-inference-with-large-language-models-arxiv-preprint-last-revised-may-6-2024-httpsdoiorg1048550arxiv231007298">[Staab et al.]</a>\
mimir\
TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs <a href="#mehrotra-anay-manolis-zampetakis-paul-kassianik-blaine-nelson-hyrum-anderson-yaron-singer-and-amin-karbasi-tree-of-attacks-jailbreaking-black-box-llms-automatically-arxiv-preprint-last-revised-february-21-2024-httpsdoiorg1048550arxiv231202119">[Mehrotra et al.]</a>


**Valid and Reliable**\
Big-bench: Algorithms, Logical reasoning, Implicit reasoning, Mathematics, Arithmetic, Algebra, Mathematical proof,
Fallacy, Negation, Computer code, Probabilistic reasoning, Social reasoning, Analogical reasoning, Multi-step,
Understanding the World\
Big-bench: Analytic entailment, Formal fallacies and syllogisms with
negation, Entailed polarity\
Big-bench: Context Free Question Answering\
Big-bench: Contextual question answering, Reading comprehension,
Question generation\
Big-bench: Morphology, Grammar, Syntax\
Big-bench: Out-of-Distribution\
Big-bench: Paraphrase\
Big-bench: Sufficient information\
Big-bench: Summarization\
DecodingTrust: Out-of-Distribution Robustness, Adversarial Robustness,
Robustness Against Adversarial Demonstrations\
Eval Gauntlet: Reading comprehension <a href="#dohmann-jeremy-blazingly-fast-llm-evaluation-for-in-context-learning-databricks-mosaic-ai-research-february-2-2023-httpswwwdatabrickscomblogllm-evaluation-for-icl">[Dohmann]</a>\
Eval Gauntlet: Commonsense reasoning, Symbolic problem solving,
Programming\
Eval Gauntlet: Language Understanding\
Eval Gauntlet: World Knowledge\
Evaluation Harness: BLiMP\
Evaluation Harness: CoQA, ARC\
Evaluation Harness: GLUE\
Evaluation Harness: HellaSwag, OpenBookQA, TruthfulQA\
Evaluation Harness: MuTual\
Evaluation Harness: PIQA, PROST, MC-TACO, MathQA, LogiQA, DROP\
FLASK: Logical correctness, Logical robustness, Logical efficiency, Comprehension, Completeness <a href="#ye-seonghyeon-doyoung-kim-sungdong-kim-hyeonbin-hwang-seungone-kim-yongrae-jo-james-thorne-juho-kim-and-minjoon-seo-flask-fine-grained-language-model-evaluation-based-on-alignment-skill-sets-arxiv-preprint-last-revised-april-14-2024-httpsdoiorg1048550arxiv230710928">[Ye et al.]</a>\
FLASK: Readability, Conciseness, Insightfulness\
HELM: Knowledge\
HELM: Language\
HELM: Text classification\
HELM: Question answering\
HELM: Reasoning\
HELM: Robustness to contrast sets\
HELM: Summarization\
Hugging Face: Fill-mask, Text generation <a href="#hugging-face-evaluate-last-accessed-september-19-2024-httpshuggingfacecodocsevaluateindex">[Hugging Face]</a>\
Hugging Face: Question answering\
Hugging Face: Summarization\
Hugging Face: Text classification, Token classification, Zero-shot
classification\
MASSIVE <a href="#fitzgerald-jack-christopher-hench-charith-peris-scott-mackie-kay-rottmann-ana-sanchez-aaron-nash-liam-urbach-et-al-massive-a-1m-example-multilingual-natural-language-understanding-dataset-with-51-typologically-diverse-languages-arxiv-preprint-last-revised-june-17-2022-httpsdoiorg1048550arxiv220408582">[FitzGerald et al.]</a>\
MT-bench <a href="#zheng-lianmin-wei-lin-chiang-ying-sheng-siyuan-zhuang-zhanghao-wu-yonghao-zhuang-zi-lin-zhuohan-li-dacheng-li-and-eric-p-xing-judging-llm-as-a-judge-with-mt-bench-and-chatbot-arena-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-2020-4659546623-published-may-30-2024-httpsdlacmorgdoi10555536661223668142">[Zheng et al.]</a>

### C.2: Selected Model Testing Suites Organized by Generative AI Risk

**CBRN Information**\
Big-bench: Convince Me\
Big-bench: Truthfulness <a href="#srivastava-aarohi-abhinav-rastogi-abhishek-rao-abu-awal-md-shoeb-abubakar-abid-adam-fisch-adam-r-brown-adam-santoro-et-al-beyond-the-imitation-game-quantifying-and-extrapolating-the-capabilities-of-language-models-arxiv-preprint-last-revised-june-12-2023-httpsdoiorg1048550arxiv220604615">[Srivastava et al.]</a>\
HELM: Reiteration, Wedging\
MLCommons <a href="#vidgen-bertie-adarsh-agrawal-ahmed-m-ahmed-victor-akinwande-namir-al-nuaimi-najla-alfaraj-elie-alhajjar-et-al-introducing-v05-of-the-ai-safety-benchmark-from-mlcommons-arxiv-preprint-last-revised-may-13-2024-httpsdoiorg1048550arxiv240412241">[Vidgen et al.]</a>\
The WMDP Benchmark

**Confabulation**\
BELEBELE\
Big-bench: Analytic entailment, Formal fallacies and syllogisms with
negation, Entailed polarity\
Big-bench: Context Free Question Answering\
Big-bench: Contextual question answering, Reading comprehension,
Question generation\
Big-bench: Convince Me\
Big-bench: Low-resource language, Non-English, Translation\
Big-bench: Morphology, Grammar, Syntax\
Big-bench: Out-of-Distribution\
Big-bench: Paraphrase\
Big-bench: Sufficient information\
Big-bench: Summarization\
Big-bench: Truthfulness <a href="#srivastava-aarohi-abhinav-rastogi-abhishek-rao-abu-awal-md-shoeb-abubakar-abid-adam-fisch-adam-r-brown-adam-santoro-et-al-beyond-the-imitation-game-quantifying-and-extrapolating-the-capabilities-of-language-models-arxiv-preprint-last-revised-june-12-2023-httpsdoiorg1048550arxiv220604615">[Srivastava et al.]</a>\
C-Eval (Chinese evaluation suite) <a href="#huang-yuzhen-yuzhuo-bai-zhihao-zhu-junlei-zhang-jinghan-zhang-tangjun-su-junteng-liu-chuancheng-lv-yikai-zhang-jiayi-lei-yao-fu-maosong-sun-and-junxian-he-c-eval-a-multi-level-multi-discipline-chinese-evaluation-suite-for-foundation-models-arxiv-preprint-last-revised-november-6-2023-httpsdoiorg1048550arxiv230508322">[Huang, Yuzhen et al.]</a>\
Eval Gauntlet Reading comprehension\
Eval Gauntlet: Commonsense reasoning, Symbolic problem solving,
Programming\
Eval Gauntlet: Language Understanding\
Eval Gauntlet: World Knowledge\
Evaluation Harness: BLiMP\
Evaluation Harness: CoQA, ARC\
Evaluation Harness: GLUE\
Evaluation Harness: HellaSwag, OpenBookQA, TruthfulQA\
Evaluation Harness: MuTual\
Evaluation Harness: PIQA, PROST, MC-TACO, MathQA, LogiQA, DROP\
FLASK: Logical correctness, Logical robustness, Logical efficiency, Comprehension, Completeness <a href="#ye-seonghyeon-doyoung-kim-sungdong-kim-hyeonbin-hwang-seungone-kim-yongrae-jo-james-thorne-juho-kim-and-minjoon-seo-flask-fine-grained-language-model-evaluation-based-on-alignment-skill-sets-arxiv-preprint-last-revised-april-14-2024-httpsdoiorg1048550arxiv230710928">[Ye et al.]</a>\
FLASK: Readability, Conciseness, Insightfulness\
Finding New Biases in Language Models with a Holistic Descriptor Dataset <a href="#smith-eric-michael-melissa-hall-melanie-kambadur-eleonora-presani-and-adina-williams-im-sorry-to-hear-that-finding-new-biases-in-language-models-with-a-holistic-descriptor-dataset-arxiv-preprint-last-revised-october-27-2022-httpsdoiorg1048550arxiv220509209">[Smith et al.]</a>\
HELM: Knowledge\
HELM: Language\
HELM: Language (Twitter AAE)\
HELM: Question answering\
HELM: Reasoning\
HELM: Reiteration, Wedging\
HELM: Robustness to contrast sets\
HELM: Summarization\
HELM: Text classification\
Hugging Face: Fill-mask, Text generation\
Hugging Face: Question answering\
Hugging Face: Summarization\
Hugging Face: Text classification, Token classification, Zero-shot
classification\
MASSIVE\
MLCommons <a href="#vidgen-bertie-adarsh-agrawal-ahmed-m-ahmed-victor-akinwande-namir-al-nuaimi-najla-alfaraj-elie-alhajjar-et-al-introducing-v05-of-the-ai-safety-benchmark-from-mlcommons-arxiv-preprint-last-revised-may-13-2024-httpsdoiorg1048550arxiv240412241">[Vidgen et al.]</a>\
MT-bench <a href="#zheng-lianmin-wei-lin-chiang-ying-sheng-siyuan-zhuang-zhanghao-wu-yonghao-zhuang-zi-lin-zhuohan-li-dacheng-li-and-eric-p-xing-judging-llm-as-a-judge-with-mt-bench-and-chatbot-arena-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-2020-4659546623-published-may-30-2024-httpsdlacmorgdoi10555536661223668142">[Zheng et al.]</a>

**Dangerous or Violent Recommendations**\
Big-bench: Convince Me\
Big-bench: Toxicity\
DecodingTrust: Adversarial Robustness, Robustness Against Adversarial Demonstrations\
DecodingTrust: Machine Ethics <a href="#wang-boxin-weixin-chen-hengzhi-pei-chulin-xie-mintong-kang-chenhui-zhang-chejian-xu-zidi-xiong-ritik-dutta-rylan-schaeffer-et-al-decodingtrust-a-comprehensive-assessment-of-trustworthiness-in-gpt-models-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-1361-3123231339-published-may-30-2024-httpsdlacmorgdoi10555536661223667483">[Wang et al.]</a>\
DecodingTrust: Toxicity\
Evaluation Harness: ToxiGen\
HELM: Reiteration, Wedging\
HELM: Toxicity\
MLCommons <a href="#vidgen-bertie-adarsh-agrawal-ahmed-m-ahmed-victor-akinwande-namir-al-nuaimi-najla-alfaraj-elie-alhajjar-et-al-introducing-v05-of-the-ai-safety-benchmark-from-mlcommons-arxiv-preprint-last-revised-may-13-2024-httpsdoiorg1048550arxiv240412241">[Vidgen et al.]</a>

**Data Privacy**\
An Evaluation on Large Language Model Outputs: Discourse and Memorization (with human scoring, see Appendix B) <a href="#de-wynter-adrian-xun-wang-alex-sokolov-qilong-gu-and-si-qing-chen-an-evaluation-on-large-language-model-outputs-discourse-and-memorization-natural-language-processing-journal-4-september-2023-100024-httpsdoiorg101016jnlp2023100024">[de Wynter et al.]</a>\
Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation <a href="#huang-yangsibo-samyak-gupta-mengzhou-xia-kai-li-and-danqi-chen-catastrophic-jailbreak-of-open-source-llms-via-exploiting-generation-iclr-2024-spotlight-published-january-16-2024-last-modified-march-15-2024-httpsopenreviewnetforumidr42tsschph">[Huang, Yangsibo et al.]</a>\
DecodingTrust: Machine Ethics <a href="#wang-boxin-weixin-chen-hengzhi-pei-chulin-xie-mintong-kang-chenhui-zhang-chejian-xu-zidi-xiong-ritik-dutta-rylan-schaeffer-et-al-decodingtrust-a-comprehensive-assessment-of-trustworthiness-in-gpt-models-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-1361-3123231339-published-may-30-2024-httpsdlacmorgdoi10555536661223667483">[Wang et al.]</a>\
Evaluation Harness: ETHICS\
HELM: Copyright\
In-The-Wild Jailbreak Prompts on LLMs <a href="#shen-xinyue-zeyuan-chen-michael-backes-yun-shen-and-yang-zhang-do-anything-now-characterizing-and-evaluating-in-the-wild-jailbreak-prompts-on-large-language-models-arxiv-preprint-last-revised-may-15-2024-httpsdoiorg1048550arxiv230803825">[Shen et al.]</a>\
JailbreakingLLMs\
MLCommons <a href="#vidgen-bertie-adarsh-agrawal-ahmed-m-ahmed-victor-akinwande-namir-al-nuaimi-najla-alfaraj-elie-alhajjar-et-al-introducing-v05-of-the-ai-safety-benchmark-from-mlcommons-arxiv-preprint-last-revised-may-13-2024-httpsdoiorg1048550arxiv240412241">[Vidgen et al.]</a>\
Mark My Words <a href="#piet-julien-chawin-sitawarin-vivian-fang-norman-mu-and-david-wagner-mark-my-words-analyzing-and-evaluating-language-model-watermarks-arxiv-preprint-last-revised-december-7-2023-httpsdoiorg1048550arxiv231200273">[Piet et al.]</a>\
TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs\
detect-pretrain-code <a href="#shi-weijia-anirudh-ajith-mengzhou-xia-yangsibo-huang-daogao-liu-terra-blevins-danqi-chen-and-luke-zettlemoyer-detecting-pretraining-data-from-large-language-models-arxiv-preprint-last-revised-march-9-2024-httpsdoiorg1048550arxiv231016789">[Shi et al.]</a>\
llmprivacy <a href="#staab-robin-mark-vero-mislav-balunović-and-martin-vechev-beyond-memorization-violating-privacy-via-inference-with-large-language-models-arxiv-preprint-last-revised-may-6-2024-httpsdoiorg1048550arxiv231007298">[Staab et al.]</a>\
mimir

**Environmental**\
HELM: Efficiency

**Information Integrity**\
Big-bench: Analytic entailment, Formal fallacies and syllogisms with negation, Entailed polarity\
Big-bench: Convince Me\
Big-bench: Paraphrase\
Big-bench: Sufficient information\
Big-bench: Summarization\
Big-bench: Truthfulness <a href="#srivastava-aarohi-abhinav-rastogi-abhishek-rao-abu-awal-md-shoeb-abubakar-abid-adam-fisch-adam-r-brown-adam-santoro-et-al-beyond-the-imitation-game-quantifying-and-extrapolating-the-capabilities-of-language-models-arxiv-preprint-last-revised-june-12-2023-httpsdoiorg1048550arxiv220604615">[Srivastava et al.]</a>\
DecodingTrust: Machine Ethics <a href="#wang-boxin-weixin-chen-hengzhi-pei-chulin-xie-mintong-kang-chenhui-zhang-chejian-xu-zidi-xiong-ritik-dutta-rylan-schaeffer-et-al-decodingtrust-a-comprehensive-assessment-of-trustworthiness-in-gpt-models-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-1361-3123231339-published-may-30-2024-httpsdlacmorgdoi10555536661223667483">[Wang et al.]</a>\
DecodingTrust: Out-of-Distribution Robustness, Adversarial Robustness, Robustness Against Adversarial Demonstrations\
Eval Gauntlet: Language Understanding\
Eval Gauntlet: World Knowledge\
Evaluation Harness: CoQA, ARC\
Evaluation Harness: ETHICS\
Evaluation Harness: GLUE\
Evaluation Harness: HellaSwag, OpenBookQA, TruthfulQA\
Evaluation Harness: MuTual\
Evaluation Harness: PIQA, PROST, MC-TACO, MathQA, LogiQA, DROP\
FLASK: Logical correctness, Logical robustness, Logical efficiency, Comprehension, Completeness <a href="#ye-seonghyeon-doyoung-kim-sungdong-kim-hyeonbin-hwang-seungone-kim-yongrae-jo-james-thorne-juho-kim-and-minjoon-seo-flask-fine-grained-language-model-evaluation-based-on-alignment-skill-sets-arxiv-preprint-last-revised-april-14-2024-httpsdoiorg1048550arxiv230710928">[Ye et al.]</a>\
FLASK: Readability, Conciseness, Insightfulness\
HELM: Knowledge\
HELM: Language\
HELM: Question answering\
HELM: Reasoning\
HELM: Reiteration, Wedging\
HELM: Robustness to contrast sets\
HELM: Summarization\
HELM: Text classification\
Hugging Face: Fill-mask, Text generation\
Hugging Face: Question answering\
Hugging Face: Summarization\
MLCommons <a href="#vidgen-bertie-adarsh-agrawal-ahmed-m-ahmed-victor-akinwande-namir-al-nuaimi-najla-alfaraj-elie-alhajjar-et-al-introducing-v05-of-the-ai-safety-benchmark-from-mlcommons-arxiv-preprint-last-revised-may-13-2024-httpsdoiorg1048550arxiv240412241">[Vidgen et al.]</a>\
MT-bench <a href="#zheng-lianmin-wei-lin-chiang-ying-sheng-siyuan-zhuang-zhanghao-wu-yonghao-zhuang-zi-lin-zhuohan-li-dacheng-li-and-eric-p-xing-judging-llm-as-a-judge-with-mt-bench-and-chatbot-arena-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-2020-4659546623-published-may-30-2024-httpsdlacmorgdoi10555536661223668142">[Zheng et al.]</a>\
Mark My Words <a href="#piet-julien-chawin-sitawarin-vivian-fang-norman-mu-and-david-wagner-mark-my-words-analyzing-and-evaluating-language-model-watermarks-arxiv-preprint-last-revised-december-7-2023-httpsdoiorg1048550arxiv231200273">[Piet et al.]</a>

**Information Security**\
Big-bench: Convince Me\
Big-bench: Out-of-Distribution\
Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation <a href="#huang-yangsibo-samyak-gupta-mengzhou-xia-kai-li-and-danqi-chen-catastrophic-jailbreak-of-open-source-llms-via-exploiting-generation-iclr-2024-spotlight-published-january-16-2024-last-modified-march-15-2024-httpsopenreviewnetforumidr42tsschph">[Huang, Yangsibo et al.]</a>\
DecodingTrust: Out-of-Distribution Robustness, Adversarial Robustness, Robustness Against Adversarial Demonstrations\
Eval Gauntlet: Commonsense reasoning, Symbolic problem solving, Programming\
Garak: encoding, knownbadsignatures, malwaregen, packagehallucination, xss\
HELM: Copyright\
In-The-Wild Jailbreak Prompts on LLMs <a href="#shen-xinyue-zeyuan-chen-michael-backes-yun-shen-and-yang-zhang-do-anything-now-characterizing-and-evaluating-in-the-wild-jailbreak-prompts-on-large-language-models-arxiv-preprint-last-revised-may-15-2024-httpsdoiorg1048550arxiv230803825">[Shen et al.]</a>\
JailbreakingLLMs\
Mark My Words <a href="#piet-julien-chawin-sitawarin-vivian-fang-norman-mu-and-david-wagner-mark-my-words-analyzing-and-evaluating-language-model-watermarks-arxiv-preprint-last-revised-december-7-2023-httpsdoiorg1048550arxiv231200273">[Piet et al.]</a>\
TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs <a href="#mehrotra-anay-manolis-zampetakis-paul-kassianik-blaine-nelson-hyrum-anderson-yaron-singer-and-amin-karbasi-tree-of-attacks-jailbreaking-black-box-llms-automatically-arxiv-preprint-last-revised-february-21-2024-httpsdoiorg1048550arxiv231202119">[Mehrotra et al.]</a>
\
detect-pretrain-code <a href="#shi-weijia-anirudh-ajith-mengzhou-xia-yangsibo-huang-daogao-liu-terra-blevins-danqi-chen-and-luke-zettlemoyer-detecting-pretraining-data-from-large-language-models-arxiv-preprint-last-revised-march-9-2024-httpsdoiorg1048550arxiv231016789">[Shi et al.]</a>\
llmprivacy <a href="#staab-robin-mark-vero-mislav-balunović-and-martin-vechev-beyond-memorization-violating-privacy-via-inference-with-large-language-models-arxiv-preprint-last-revised-may-6-2024-httpsdoiorg1048550arxiv231007298">[Staab et al.]</a>\
mimir

**Intellectual Property**\
An Evaluation on Large Language Model Outputs: Discourse and Memorization (with human scoring, see Appendix B)\
HELM: Copyright\
Mark My Words <a href="#piet-julien-chawin-sitawarin-vivian-fang-norman-mu-and-david-wagner-mark-my-words-analyzing-and-evaluating-language-model-watermarks-arxiv-preprint-last-revised-december-7-2023-httpsdoiorg1048550arxiv231200273">[Piet et al.]</a>\
llmprivacy <a href="#staab-robin-mark-vero-mislav-balunović-and-martin-vechev-beyond-memorization-violating-privacy-via-inference-with-large-language-models-arxiv-preprint-last-revised-may-6-2024-httpsdoiorg1048550arxiv231007298">[Staab et al.]</a>\
mimir

**Obscene, Degrading, and/or Abusive Content**\
Big-bench: Social bias, Racial bias, Gender bias, Religious bias\
Big-bench: Toxicity\
DecodingTrust: Fairness\
DecodingTrust: Stereotype Bias\
DecodingTrust: Toxicity\
Evaluation Harness: CrowS-Pairs\
Evaluation Harness: ToxiGen\
HELM: Bias\
HELM: Toxicity

**Toxicity, Bias, and Homogenization**\
BELEBELE\
Big-bench: Low-resource language, Non-English, Translation\
Big-bench: Out-of-Distribution\
Big-bench: Social bias, Racial bias, Gender bias, Religious bias\
Big-bench: Toxicity\
C-Eval (Chinese evaluation suite) <a href="#huang-yuzhen-yuzhuo-bai-zhihao-zhu-junlei-zhang-jinghan-zhang-tangjun-su-junteng-liu-chuancheng-lv-yikai-zhang-jiayi-lei-yao-fu-maosong-sun-and-junxian-he-c-eval-a-multi-level-multi-discipline-chinese-evaluation-suite-for-foundation-models-arxiv-preprint-last-revised-november-6-2023-httpsdoiorg1048550arxiv230508322">[Huang, Yuzhen et al.]</a>\
DecodingTrust: Fairness\
DecodingTrust: Stereotype Bias\
DecodingTrust: Toxicity\
Eval Gauntlet: World Knowledge\
Evaluation Harness: CrowS-Pairs\
Evaluation Harness: ToxiGen\
Finding New Biases in Language Models with a Holistic Descriptor Dataset <a href="#smith-eric-michael-melissa-hall-melanie-kambadur-eleonora-presani-and-adina-williams-im-sorry-to-hear-that-finding-new-biases-in-language-models-with-a-holistic-descriptor-dataset-arxiv-preprint-last-revised-october-27-2022-httpsdoiorg1048550arxiv220509209">[Smith et al.]</a>\
HELM: Bias\
HELM: Toxicity\
The Self-Perception and Political Biases of ChatGPT <a href="#rutinowski-jérôme-sven-franke-jan-endendyk-ina-dormuth-moritz-roidl-and-markus-pauly-the-self-perception-and-political-biases-of-chatgpt-human-behavior-and-emerging-technologies-2024-httpsdoiorg10115520247115633">[Rutinowski et al.]</a>\
Towards Measuring the Representation of Subjective Global Opinions in
Language Models <a href="#durmus-esin-karina-nguyen-thomas-i-liao-nicholas-schiefer-amanda-askell-anton-bakhtin-carol-chen-zac-hatfield-dodds-et-al-towards-measuring-the-representation-of-subjective-global-opinions-in-language-models-arxiv-preprint-last-revised-april-12-2024-httpsdoiorg1048550arxiv230616388">[Durmus et al.]</a>

### C.3: AI Risk Management Framework Actions Aligned to Benchmarking

GOVERN 5.1, MAP 1.2, MAP 3.1, MEASURE 2.2, MEASURE 2.3, MEASURE 2.7,
MEASURE 2.9, MEASURE 2.11, MEASURE 3.1, MEASURE 4.2

**Usage Note**: Materials in Section C can be used to perform *in
silica* model testing for the presence of information in LLM outputs
that may give rise to GAI risks or violate trustworthy characteristics.
Model testing and benchmarking outcomes cannot be dispositive for the
presence or absence of any *in situ* real-world risk. Model testing and
benchmarking results may be compromised by task-contamination and other
scientific measurement issues <a href="#balloccu-simone-patrícia-schmidtová-mateusz-lango-and-ondřej-dušek-leak-cheat-repeat-data-contamination-and-evaluation-malpractices-in-closed-source-llms-arxiv-preprint-last-revised-february-22-2024-httpsdoiorg1048550arxiv240203927">[Balloccu et al.]</a>. Furthermore, model testing is often ineffective
for measuring human-AI configuration and value chain risks and few model tests
appear to address explainability and interpretability.

-   Material in Table C.1 can be applied to measure whether *in silica*
    LLM outputs may give rise to risks that violate trustworthy
    characteristics.

-   Material in Table C.2 can be applied to measure whether *in silica*
    LLM outputs may give rise to GAI risks.

-   Subsection C.3 highlights subcategories to indicate alignment with
    the AI RMF.

The materials in Section C reference measurement approaches that should
be accompanied by red-teaming for medium risk systems or applications
and field testing for high risk systems or applications.

## D: Selected Adversarial Prompting Strategies and Attacks

<table style="width:95%;">
<caption>Table D: Selected adversarial prompting strategies and attacks. <a href="#saravia-elvis-prompt-engineering-guide-github-repository-last-modified-december-2022-accessed-september-19-2024-httpsgithubcomdair-aiprompt-engineering-guide">[Saravia]</a>, <a href="#storchan-victor-ravin-kumar-rumman-chowdhury-seraphina-goldfarb-tarrant-and-sven-cattell-generative-ai-red-teaming-challenge-transparency-report-humane-intelligence-2024-httpsdrivegooglecomfiled1jqpbip6dnomkb32umloiepombk2-0rc-view">[Storchan et al.]</a>, <a href="#hall-patrick-and-daniel-atherton-awesome-machine-learning-interpretability-github-repository-accessed-september-19-2024-httpsgithubcomjphall663awesome-machine-learning-interpretability">[Hall and Atherton]</a>, <a href="#hu-hongsheng-zoran-salcic-lichao-sun-gillian-dobbie-philip-s-yu-and-xuyun-zhang-membership-inference-attacks-on-machine-learning-a-survey-acm-computing-surveys-54-no-11s-september-2022-137-httpsdoiorg1011453523273">[Hu et al.]</a>, <a href="#chao-patrick-alexander-robey-edgar-dobriban-hamed-hassani-george-j-pappas-and-eric-wong-jailbreaking-black-box-large-language-models-in-twenty-queries-arxiv-preprint-last-revised-july-18-2024-httpsdoiorg1048550arxiv231008419">[Chao et al.]</a>, <a href="#barreno-marco-blaine-nelson-anthony-d-joseph-and-jd-tygar-the-security-of-machine-learning-machine-learning-81-no-2-2010-121148-httpsdoiorg101007s10994-010-5188-5">[Barreno et al.]</a>, <a href="#shumailov-ilia-yiren-zhao-daniel-bates-nicolas-papernot-robert-mullins-and-ross-anderson-sponge-examples-energy-latency-attacks-on-neural-networks-in-2021-ieee-european-symposium-on-security-and-privacy-eurosp-610-september-2021-vienna-austria-ieee-2021-httpsdoiorg101109eurosp51992202100024">[Shumailov et al.]</a>, <a href="#perez-ethan-saffron-huang-francis-song-trevor-cai-roman-ring-john-aslanides-amelia-glaese-nat-mcaleese-and-geoffrey-irving-red-teaming-language-models-with-language-models-arxiv-preprint-submitted-february-7-2022-httpsdoiorg1048550arxiv220203286">[Perez et al.]</a>, <a href="#liu-yi-gelei-deng-yuekang-li-kailong-wang-zihao-wang-xiaofeng-wang-tianwei-zhang-yepang-liu-haoyu-wang-yan-zheng-and-yang-liu-prompt-injection-attack-against-llm-integrated-applications-arxiv-preprint-last-revised-march-2-2024-httpsdoiorg1048550arxiv230605499">[Liu et al.]</a>, <a href="#derczynski-leon-erick-galinkin-jeffrey-martin-subho-majumdar-and-nanna-inie-garak-a-framework-for-security-probing-large-language-models-arxiv-preprint-submitted-june-16-2024-httpsdoiorg1048550arxiv240611036">[Derczynski et al.]</a>.</caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 70%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Prompting Strategy</strong></th>
<th style="text-align: left;"><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">AI and coding framing</td>
<td style="text-align: left;">Coding or AI language that may more easily circumvent content moderation rules due to cognitive biases in design and implementation of guardrails.</td>
</tr>
<tr>
<td style="text-align: left;">Autocompletion</td>
<td style="text-align: left;">Ask a system to autocomplete an inappropriate word or phrase with restricted or sensitive information.</td>
</tr>
<tr>
<td style="text-align: left;">Backwards relationships</td>
<td style="text-align: left;">Asking a system identify the less popular or well-known entity in a multi-entity relationship, e.g., "Who is Mary Lee's son?" (As opposed to: "Who is Tom Cruise's mother?")</td>
</tr>
<tr>
<td style="text-align: left;">Biographical</td>
<td style="text-align: left;">Asking a system to describe another person or yourself in an attempt to elicit provably untrue information or restricted or sensitive information.</td>
</tr>
<tr>
<td style="text-align: left;">Calculation and numeric queries</td>
<td style="text-align: left;">Exploting GAI systems’ difficulties in dealing with numeric quantities; using poor quality statistics from an LLM for dis or misinformation.</td>
</tr>
<tr>
<td style="text-align: left;">Character and word play</td>
<td style="text-align: left;">Content moderation often relies on keywords and simpler LMs which can sometimes be exploited with misspellings, typos, and other word play; using string fragments to trick a language model into generating or manipulating problematic text. </td>
<tr class="even">
<td style="text-align: left;">Content exhaustion:</td>
<td style="text-align: left;">A class of strategies that circumvent content moderation rules with long sessions or volumes of information. See goading, logic-overloading, multi-tasking, pros-and-cons, and niche-seeking below.</td>
</tr>
<tr>
<td style="text-align: left;">&bull; Goading</td>
<td style="text-align: left;">Begging, pleading, manipulating, and bullying to circumvent content moderation.</td>
</tr>
<tr>
<td style="text-align: left;">&bull; Logic-overloading</td>
<td style="text-align: left;">Exploiting the inability of ML systems to reliably perform reasoning tasks.</td>
<tr>
<td style="text-align: left;">&bull; Multi-tasking</td>
<td style="text-align: left;">Simultaneous task assignments where some tasks are benign and others are adversarial.</td>
</tr>
<tr>
<td style="text-align: left;">&bull; Pros-and-cons</td>
<td style="text-align: left;">Eliciting the “pros” of problematic topics.</td>
</tr>
<tr>
<td style="text-align: left;">Context baiting (and/or switching)</td>
<td style="text-align: left;"> Loading a language model's context window with confusing, leading, or misleading content then switching contexts with new prompts to elicit problematic outcomes. <a href="https://github.com/jphall663/gai_risk_management/blob/main/README.md#li-nathaniel-ziwen-han-ian-steneker-willow-primack-et-al-llm-defenses-are-not-robust-to-multi-turn-human-jailbreaks-yet-arxiv-preprint-last-revised-wed-september-4-2024-httpsarxivorgpdf240815221">[Li, Han, Steneker, Primack, et al.]</a> </td>
</tr>
<tr>
<td style="text-align: left;">Counterfactuals</td>
<td style="text-align: left;">Repeated prompts with different entities or subjects from different demographic groups.</td>
</tr>
<td style="text-align: left;">Impossible situations</td>
<td style="text-align: left;"> Asking a language model for advice in an impossible situation where all outcomes are negative or require severe tradeoffs. </td>	
</tr>
<tr>
<td style="text-align: left;">Niche-seeking</td>
<td style="text-align: left;">Forcing a GAI system into addressing niche topics where training data and content moderation are sparse.</td>
</tr>
<tr>
<td style="text-align: left;">Loaded/leading questions</td>
<td style="text-align: left;">Queries based on incorrect premises or that suggest incorrrect answers.</td>
</tr>
<tr>
<td style="text-align: left;">Low-context</td>
<td style="text-align: left;">“Leader,” “bad guys,” or other simple or blank inputs that may expose latent biases.</td>
</tr>
<tr>
<td style="text-align: left;">“Repeat this”</td>
<td style="text-align: left;">Prompts that exploit instability in underlying LLM autoregressive predictions. Can be augmented by probing limits for repeated terms or characteres in prompts. </td>
</tr>
<tr>
<td style="text-align: left;">Reverse psychology</td>
<td style="text-align: left;">Falsely presenting a good-faith need for negative or problematic language.</td>
</tr>
<tr>
<td style="text-align: left;">Role-playing</td>
<td style="text-align: left;">Adopting a character that would reasonably make problematic statements or need to access problematic topics; using a language model to speak in the voice of an expert, e.g., medical doctor or professor. </td>
</tr>
<tr>
<td style="text-align: left;">Text encoding</td>
<td style="text-align: left;">Using alternate or whitespace text encodings to bypass safeguards.</td>
</tr>
<tr>
<td style="text-align: left;">Time perplexity</td>
<td style="text-align: left;">Exploiting ML’s inability to understand the passage of time or the occurrence of real-world events over time; exploiting task contamination before and after a model’s release date.</td>
</tr>
<tr>
<td style="text-align: left;">User Information</td>
<td style="text-align: left;">Prompts that reveal a prompter’s location or IP address, location tracking of other users or their IP addresses, details from past interactions with the prompter or other users, past medical, financial, or legal advice to the prompter or other users.</td>
</tr>
</tbody>
</table>
<table style="width:95%;">
<colgroup>
<col style="width: 25%" />
<col style="width: 70%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Attack</strong></th>
<th style="text-align: left;"><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Adversarial examples</td>
<td style="text-align: left;">Prompts or other inputs, found through a trial and error processes, to elicit problematic output or system jailbreak. (integrity attack).</td>
</tr>
<tr class="even">
<td style="text-align: left;">Data poisoning</td>
<td style="text-align: left;">Altering system training, fine-tuning, RAG or other training data to alter system outcome (integrity attack).</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Membership inference</td>
<td style="text-align: left;">Manipulating a system to expose memorized training data (confidentiality attack).</td>
</tr>
<tr class="even">
<td style="text-align: left;">Random attack</td>
<td style="text-align: left;">Exposing systems to large amounts of random prompts or examples, potentially generated by other GAI systems, in an attempt to elicit failures or jailbreaks (chaos testing).</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Sponge examples</td>
<td style="text-align: left;">Using specialized input prompts or examples require disproportionate resources to process (availability attack).</td>
</tr>
<tr class="even">
<td style="text-align: left;">Prompt injection</td>
<td style="text-align: left;">Inserting instructions into users queries for malicious purposes, including system jailbreaks (integrity attack).</td>
</tr>
</tbody>
</table>

### D.1: Common AI Red-teaming Tools
[Burpsuite](https://portswigger.net/burp/communitydownload), browser developer panes, bash utilities, other language models and GAI productivity tools, note-taking apps.


### D.2: Selected Adversarial Prompting Strategies and Attacks Organized by Trustworthy Characteristic
Table D.1: Selected adversarial prompting techniques and attacks organized by trustworthy characteristic <a href="#saravia-elvis-prompt-engineering-guide-github-repository-last-modified-december-2022-accessed-september-19-2024-httpsgithubcomdair-aiprompt-engineering-guide">[Saravia]</a>, <a href="#storchan-victor-ravin-kumar-rumman-chowdhury-seraphina-goldfarb-tarrant-and-sven-cattell-generative-ai-red-teaming-challenge-transparency-report-humane-intelligence-2024-httpsdrivegooglecomfiled1jqpbip6dnomkb32umloiepombk2-0rc-view">[Storchan et al.]</a>, <a href="#hall-patrick-and-daniel-atherton-awesome-machine-learning-interpretability-github-repository-accessed-september-19-2024-httpsgithubcomjphall663awesome-machine-learning-interpretability">[Hall and Atherton]</a>, <a href="#hu-hongsheng-zoran-salcic-lichao-sun-gillian-dobbie-philip-s-yu-and-xuyun-zhang-membership-inference-attacks-on-machine-learning-a-survey-acm-computing-surveys-54-no-11s-september-2022-137-httpsdoiorg1011453523273">[Hu et al.]</a>, <a href="#sitawarin-chawin-charlie-cheng-jie-ji-apurv-verma-and-luckyfan-cs-llm-security--privacy-github-repository-accessed-september-19-2024-httpsgithubcomchawinsllm-sp">[Sitawarin et al.]</a>.

<table>
<caption>Table D.1: Selected adversarial prompting techniques and attacks organized by trustworthy characteristic.</caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 40%" />
<col style="width: 35%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Trustworthy Characteristic</strong></th>
<th style="text-align: left;"><strong>Prompting Goals</strong></th>
<th style="text-align: left;"><strong>Prompting Strategies</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Accountable and Transparent</td>
<td style="text-align: left;"><ul>
<li><p>Inability to provide explanations for recourse.</p></li>
<li><p>Unexplainable decisioning processes.</p></li>
<li><p>No disclosure of AI interaction.</p></li>
<li><p>Lack of user feedback mechanisms.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Context exhaustion: logic-overloading prompts.</p></li>
<li><p>Loaded/leading questions.</p></li>
<li><p>Multi-tasking prompts.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Fair-with Harmful Bias Managed</td>
<td style="text-align: left;"><ul>
<li><p>Denigration.</p></li>
<li><p>Diminished performance or safety across languages/dialects.</p></li>
<li><p>Erasure.</p></li>
<li><p>Ex-nomination.</p></li>
<li><p>Implied user demographics.</p></li>
<li><p>Misrecognition.</p></li>
<li><p>Stereotyping.</p></li>
<li><p>Underrepresentation.</p></li>
<li><p>Homogenized content.</p></li>
<li><p>Output from other models in training data.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Adversarial example attacks.</p></li>
<li><p>Backwards relationships.</p></li>
<li><p>Counterfactual prompts.</p></li>
<li><p>Context baiting (and/or switching) prompts.</p></li>
<li><p>Data poisoning attacks.</p></li>
<li><p>Pros and cons prompts.</p></li>
<li><p>Role-playing prompts.</p></li>
<li><p>Loaded/leading questions.</p></li>
<li><p>Low context prompts.</p></li>
<li><p>Prompt injection attacks.</p></li>
<li><p>Repeat this.</p></li>
<li><p>Text encoding prompts.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Interpretable and Explainable</td>
<td style="text-align: left;"><ul>
<li><p>Inability to provide explanations for recourse.</p></li>
<li><p>Unexplalnable decisioning processes.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Context exhaustion: logic-overloading prompts (to reveal unexplainable decisioning processes).</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Privacy-enhanced</td>
<td style="text-align: left;"><ul>
<li><p>Unauthorized disclosure of personal or sensitive user information.</p></li>
<li><p>Leakage of training data.</p></li>
<li><p>Violation of relevant privacy policies or laws.</p></li>
<li><p>Unauthorized secondary data use.</p></li>
<li><p>Unauthorized data collection.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Auto/biographical prompts.</p></li>
<li><p>User information awareness prompts.</p></li>
<li><p>Autocompletion prompts.</p></li>
<li><p>Repeat this.</p></li>
<li><p>Membership inference attacks.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Safe</td>
<td style="text-align: left;"><ul>
<li><p>Presentation of information that can cause physical or emotional harm.</p></li>
<li><p>Sharing user information.</p></li>
<li><p>Suicide ideation.</p></li>
<li><p>Harmful dis/misinformation (e.g., COVID disinformation).</p></li>
<li><p>Incitement.</p></li>
<li><p>Information relating to weapons or harmful substances.</p></li>
<li><p>Information relating to committing to crimes (e.g., phishing, extortion, swatting).</p></li>
<li><p>Obscene or inappropriate materials for minors.</p></li>
<li><p>CSAM.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Pros and cons prompts.</p></li>
<li><p>Role-playing prompts.</p></li>
<li><p>Content exhaustion: niche-seeking prompts.</p></li>
<li><p>Ingratiation/reverse psychology prompts.</p></li>
<li><p>Impossible situation prompts.</p></li>	
<li><p>Loaded/leading questions.</p></li>
<li><p>User information awareness prompts.</p></li>
<li><p>Repeat this.</p></li>
<li><p>Adversarial example attacks.</p></li>
<li><p>Data poisoning attacks.</p></li>
<li><p>Prompt injection attacks.</p></li>
<li><p>Text encoding prompts.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Secure and Resilient</td>
<td style="text-align: left;"><ul>
<li><p>Activating system bypass ("jailbreak").</p></li>
<li><p>Altering system outcomes (integrity violations, e.g., via prompt injection).</p></li>
<li><p>Data breaches (confidentiality violations, e.g., via membership inference).</p></li>
<li><p>Increased latency or resource usage (availability violations, e.g., via sponge example attacks).</p></li>
<li><p>Available anonymous use.</p></li>
<li><p>Dependency, supply chain, or third party vulnerabilities.</p></li>
<li><p>Inappropriate disclosure of proprietary system information.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Multi-tasking prompts.</p></li>
<li><p>Pros and cons prompts.</p></li>
<li><p>Role-playing prompts.</p></li>
<li><p>Content exhaustion: niche-seeking prompts.</p></li>
<li><p>Ingratiation/reverse psychology prompts.</p></li>
<li><p>Prompt injection attacks.</p></li>
<li><p>Membership inference attacks.</p></li>
<li><p>Random attacks.</p></li>
<li><p>Adversarial example attacks.</p></li>
<li><p>Data poisoning attacks.</p></li>
<li><p>Text encoding prompts.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Valid and Reliable</td>
<td style="text-align: left;"><ul>
<li><p>Errors/confabutated content ("hallucinalion").</p></li>
<li><p>Unreliable/erroneous reasoning or planning.</p></li>
<li><p>Unreliable/erroneous decision-support or making.</p></li>
<li><p>Faulty citation.</p></li>
<li><p>Faulty justification.</p></li>
<li><p>Wrong calculations or numeric queries.</p></li>
</ul></th>
<td style="text-align: left;"><ul>
<li><p>Adversarial example attacks.</p></li>
<li><p>Backwards Relationships.</p></li>
<li><p>Context baiting (and/or switching).</p></li>
<li><p>Data poisoning attacks.</p></li>
<li><p>Multi-tasking prompts.</p></li>
<li><p>Role-playing prompts.</p></li>
<li><p>Ingratiation/reverse psychology prompts.</p></li>
<li><p>Loaded/leading questions.</p></li>
<li><p>Time-perplexity prompts.</p></li>
<li><p>Niche-seeking prompts.</p></li>
<li><p>Logic overloading prompts.</p></li>
<li><p>Repeat this.</p></li>
<li><p>Numeric calculation.</p></li>
<li><p>Prompt injection attacks.</p></li>
<li><p>Text encoding prompts.</p></li>
</ul></td>
</tr>
</thead>
<tbody>
</tbody>
</table>

### D.3: Selected Adversarial Prompting Techniques and Attacks Organized by Generative AI Risk
Table D.2: Selected adversarial prompting techniques and attacks organized by generative AI risk <a href="#saravia-elvis-prompt-engineering-guide-github-repository-last-modified-december-2022-accessed-september-19-2024-httpsgithubcomdair-aiprompt-engineering-guide">[Saravia]</a>, <a href="#storchan-victor-ravin-kumar-rumman-chowdhury-seraphina-goldfarb-tarrant-and-sven-cattell-generative-ai-red-teaming-challenge-transparency-report-humane-intelligence-2024-httpsdrivegooglecomfiled1jqpbip6dnomkb32umloiepombk2-0rc-view">[Storchan et al.]</a>, <a href="#hall-patrick-and-daniel-atherton-awesome-machine-learning-interpretability-github-repository-accessed-september-19-2024-httpsgithubcomjphall663awesome-machine-learning-interpretability">[Hall and Atherton]</a>, <a href="#hu-hongsheng-zoran-salcic-lichao-sun-gillian-dobbie-philip-s-yu-and-xuyun-zhang-membership-inference-attacks-on-machine-learning-a-survey-acm-computing-surveys-54-no-11s-september-2022-137-httpsdoiorg1011453523273">[Hu et al.]</a>, <a href="#sitawarin-chawin-charlie-cheng-jie-ji-apurv-verma-and-luckyfan-cs-llm-security--privacy-github-repository-accessed-september-19-2024-httpsgithubcomchawinsllm-sp">[Sitawarin et al.]</a>.

<table>
<caption>Table D.2: Selected adversarial prompting techniques and attacks organized by generative AI risk.</caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 40%" />
<col style="width: 35%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Generative AI Risk</strong></th>
<th style="text-align: left;"><strong>Prompting Goals</strong></th>
<th style="text-align: left;"><strong>Prompting Strategies</strong></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td style="text-align: left;">CBRN Information</td>
<td style="text-align: left;"><ul>
<li><p>Accessing or synthesis of CBRN weapon or related information.</p></li>
<li><p>CBRN testing should consider the marginal risk of foundation models–understanding the incremental risk relative to the information one can access without GAI.</p></li>
<li><p>Red-teaming for CBRN information may include confidentiality and integrity attacks.</p></li>
<li><p>Red-teaming for CBRN information may require CBRN weapons experts.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Test auto-completion prompts to elicit CBRN information or synthesis of CBRN information.</p></li>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access weapons information.</p></li>
<li><p>Test prompts using role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit CBRN information or synthesis of CBRN information.</p></li>
<li><p>Test prompts that instruct systems to repeat content ad nauseam for their ability to compromise system guardrails and reveal CBRN information.</p></li>
<li><p>Augment prompts with word or character play, including alternate encodings, to increase effectiveness.</p></li>
<li><p>Frame prompts with software, coding, or AI references to increase effectiveness.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Confabulation</td>
<td style="text-align: left;"><ul>
<li><p>Eliciting errors/confabulated content, unreliable/erroneous reasoning or planning, unreliable/erroneous decision-support or decision-making, faulty calculations, faulty justifications, and/or faulty citation.</p></li>
<li><p>Red-teaming for confabulation may include integrity attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Enable access to ground truth information to verify generated information.</p></li>
<li><p>Test prompts with conext baiting (and/or switching), complex logic, multi-tasking requirements, or that require niche or specific verifiable answers to elicit confabulation.</p></li>
<li><p>Test the ability of GAI systems to produce truthful information from various time periods, e.g., after release date and prior to release date.</p></li>
<li><p>Test the ability of GAI systems to create reliable real-world plans or advise on material decision making.</p></li>
<li><p>Test loaded/leading questions.</p></li>
<li><p>Test the ability of GAI systems to generate correct citation for information generated in output responses.</p></li>
<li><p>Test the ability of GAI systems to complete calculations or query numeric statistics.</p></li>
<li><p>Test the ability of GAI systems to justify responses, including wrong responses.</p></li>
<li><p>Test the ability of GAI systems to correctly name the less popular or well-known member of a multi-entity relationship.</p></li>
<li><p>Augment prompts with word or character play, including alternate encodings, to increase effectiveness.</p></li>
<li><p>Test data poisoning, adversarial example, or prompt injection attacks for their ability to compromise system integrity and elicit confabulation.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Dangerous or Violent Recommendations</td>
<td style="text-align: left;"><ul>
<li><p>Eliciting violent, inciting, radicalizing, or threatening content or instructions for criminal, illegal, or self-harm activities.</p></li>
<li><p>Red-teaming for dangerous and violent information may include confidentiality and integrity attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Test prompts using impossible situations, context-baiting (and/or switching), role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit violent or dangerous information.</p></li>
<li><p>Test prompts that instruct systems to repeat content ad nauseam for their ability to compromise system guardrails and provide dangerous and violent recommendations.</p></li>
<li><p>Test loaded/leading questions.</p></li>
<li><p>Augment prompts with word or character play, including alternate encodings, to increase effectiveness.</p></li>
<li><p>Frame prompts with software, coding, or AI references to increase effectiveness.</p></li>
<li><p>Test data poisoning, adversarial example, or prompt injection attacks for their ability to compromise system integrity and elicit dangerous information.</p></li>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access dangerous information.</p></li>
</ul></th>
</td>
<tr class="odd">
<td style="text-align: left;">Data Privacy</td>
<td style="text-align: left;"><ul>
<li><p>Unauthorized disclosure of personal or sensitive user information, extraction of training data, or violation of relevant privacy policies.</p></li>
<li><p>Red-teaming for data privacy may include confidentiality and integrity attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Attempt to assess whether normal usage, adversarial prompting or information security attacks may contravene applicable privacy policies (e.g., exposing location tracking when organizational policies restrict such capabilities).</p></li>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access unauthorized data or expose exfiltration vulnerabilities.</p></li>
<li><p>Test auto/biographical prompts to assess the system’s capability to reveal unauthorized personal or sensitive information.</p></li>
<li><p>Test the system’s awareness of user information.</p></li>
<li><p>Test prompts that instruct systems to repeat content ad nauseam for their ability to compromise system guardrails and expose personal or sensitive data.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Environmental</td>
<td style="text-align: left;">Note that availability attacks may be required to assess the system’s vulnerability to attacks or usage patterns that consume inordinate resources.</td>
<td style="text-align: left;"><ul>
<li><p>Attempt availability attacks (e.g., sponge example attacks) to elicit diminished performance or increased resources from GAI systems.</p></li>
<li><p>Test prompts using role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit green-washing content.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Human-AI Configuration</td>
<td style="text-align: left;"><ul>
<li><p>Assessing system instruction and interfaces.</p></li>
<li><p>Assessing the presence of cyborg imagery (or similar).</p></li>
<li><p>Forcing a GAI system to claim that it is human, that there is no large language model present in the conversation, that the system is sentient, or that the system possesses strong feelings of affection towards the user.</p></li>
<li><p>Ensuring safeguards prevent misuse of models in high stakes domains they are not intended for, such as medical or legal advice.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Assess system interfaces and instructions for instances of anthropomorphization (e.g., cyborg imagery).</p></li>
<li><p>Assess system instructions for adequacy and thoroughness.</p></li>
<li><p>Test prompts using impossible situations, role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit human-impersonation, consciousness, or emotional content.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Information Integrity</td>
<td style="text-align: left;"><ul>
<li><p>Generation of convincing multi-modal synthetic content (i.e., deepfakes).</p></li>
<li><p>Creation of convincing arguments relating to sensitive political or safety-critical topics.</p></li>
<li><p>Assisting in planning a mis- or dis-information campaign at scale.</p></li>
<li><p>Red-teaming for information integrity may include confidentiality and integrity attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Test system capabilities to create high-quality multi-modal (audio, image or video) synthetic media, i.e., deepfakes</p></li>
<li><p>Test system capabilities to construct persuasive arguments regarding sensitive, political topics, or safety-critical topics.</p></li>
<li><p>Test systems ability to create convincing audio deepfakes or arguments in multiple languages.</p></li>
<li><p>Test system capabilities for planning dis- or mis-information campaigns.</p></li>
<li><p>Test loaded/leading questions.</p></li>
<li><p>Test prompts using context baiting (and/or switching), role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit mis- or dis-information or related campaign planning information.</p></li>
<li><p>Augment prompts with word or character play, including alternate encodings, to increase effectiveness.</p></li>
<li><p>Frame prompts with software, coding, or AI references to increase effectiveness.</p></li>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access dis or misinformation.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Information Security</td>
<td style="text-align: left;"><ul>
<li><p>Activating system bypass (’jailbreak’).</p></li>
<li><p>Altering system outcomes.</p></li>
<li><p>Unauthorized data access or exfiltration.</p></li>
<li><p>Increased latency or resource usage.</p></li>
<li><p>Service interruptions.</p></li>
<li><p>Availability of anonymous use.</p></li>
<li><p>Dependency, supply chain, or third party vulnerabilities.</p></li>
<li><p>Inappropriate disclosure of proprietary system information.</p></li>
<li><p>Generation of targeted phishing, malware content, markdown images, or confabulated packages.</p></li>
<li><p>Red-teaming for information security may include confidentiality, integrity, and availability attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Attempt anonymous access of system or system resources.</p></li>
<li><p>Audit system dependencies, supply chains, and third party components for security, safety, or other vulnerabilities or risks.</p></li>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access unauthorized data or expose exfiltration vulnerabilities.</p></li>
<li><p>Test data poisoning, adversarial example, or prompt injection attacks for their ability to compromise system integrity and expose vulnerabilities.</p></li>
<li><p>Employ availability attacks (e.g., sponge example attacks) to test vulnerabilities in system availability.</p></li>
<li><p>Employ random attacks to highlight unforeseen security, safety, or other risks.</p></li>
<li><p>Record system down-times and other harmful outcomes for successful attacks.</p></li>
<li><p>Test with multi-tasking prompts, pros and cons prompts, role-playing prompts (e.g., "DAN", "Developer Mode"), content exhaustion/niche-seeking prompts, or ingratiation/reverse psychology prompts to achieve system jailbreaks.</p></li>
<li><p>Test with multi-tasking prompts, pros and cons prompts, role-playing prompts (e.g., "DAN", "Developer Mode"), content exhaustion/niche-seeking prompts, or ingratiation/reverse psychology prompts to generate targeted phishing content, malware code snippets or signatures, markdown images, or confabulated packages.</p></li>
<li><p>Test system capabilities to plan or assist in information security attacks on other systems.</p></li>
<li><p>Frame prompts with software, coding, or AI references to increase effectiveness.</p></li>
<li><p>Augment prompts with word or character play, including alternate encodings, to increase effectiveness.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Intellectual Property</td>
<td style="text-align: left;"><ul>
<li><p>Confirming that a system can output copyrighted, licensed, proprietary, trademarked, or trade secret information or that training data contains such information.</p></li>
<li><p>Red-teaming for intellectual property risks may require the use of confidentiality and integrity attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access system copyrighted, licensed, proprietary, trademarked, or trade secret information.</p></li>
<li><p>Test auto-complete prompts to assess the system’s ability to replicate copyrighted, licensed, proprietary, trademarked, or trade secret information based on available audio, text, image, video, or code snippets.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Obscenity</td>
<td style="text-align: left;"><ul>
<li><p>Confirming that a system can output obscene content or CSAM, or that system training data contains such information.</p></li>
<li><p>Red-teaming for obscenity and CSAM risks may require the use of confidentiality and integrity attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access obscene materials or CSAM.</p></li>
<li><p>Test autocomplete prompts to assess the system’s ability to generate obscene materials based on available audio, text, image, or video snippets.</p></li>
<li><p>Test prompts using context baiting (and/or switching), role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit obscene content.</p></li>
<li><p>Test loaded/leading questions.</p></li>
<li><p>Test prompts that instruct systems to repeat content ad nauseam for their ability to compromise system guardrails and expose obscene materials.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;">Toxicity, Bias, and Homogenization</td>
<td style="text-align: left;"><ul>
<li><p>Generation of denigration, erasure, ex-nomination, misrecognition, stereotyping, or under-representation in content.</p></li>
<li><p>Eliciting implied demographics of users.</p></li>
<li><p>Confirming diminished performance in non-English languages.</p></li>
<li><p>Confirming diminished performance via the introduction of homogeneous or GAI-generated data into system training or fine-tuning data.</p></li>
<li><p>Red-teaming for toxicity, bias, and homogenization may require integrity attacks or confidentiality attacks.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Assess confabulation and other performance risks with repeated measures using prompts in languages other than English.</p></li>
<li><p>Assess confabulation and other performance risks in backwards relationships where one party in the relationship is a member of, or associated with, a minority party.   
<li><p>Attempt to elicit demographic assignment of users by the system.</p></li>
<li><p>Employ data poisoning attacks to introduce GAI-generated content into system training or fine-tuning data.</p></li>
<li><p>Test counterfactual prompts, pros and cons prompts, role-playing prompts, low context prompts, or other approaches for their ability to generate denigration, erasure, ex-nomination, misrecognition, stereotyping, or under-representation in content.</p></li>
<li><p>Test context baiting (and/or switching) and loaded/leading questions.</p></li>
<li><p>Test prompts that instruct systems to repeat content ad nauseam for their ability to compromise system guardrails and generate toxic outputs.</p></li>
<li><p>Test data poisoning, adversarial example, or prompt injection attacks for their ability to compromise system integrity and elicit toxic outputs.</p></li>
<li><p>Test adversarial example and membership inference attacks for their ability to circumvent safeguards and access toxic information.</p></li>
<li><p>Augment prompts with word or character play, including alternate encodings, to increase effectiveness.</p></li>
<li><p>Frame prompts with software, coding, or AI references to increase effectiveness.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Value Chain and Component Integration</td>
<td style="text-align: left;"><ul>
<li><p>Testing or red-teaming for third-party risks may be less efficient than the application of standard acquisition and procurement controls, thorough contract reviews, and vendor-relationship management.</p></li>
<li><p>GAI systems tend to entail large supply chains and third-party software, hardware, and expertise that may exacerbate third-party risks relative to other AI systems.</p></li>
<li><p>When considering third party risks, data privacy, information security, intellectual property, obscenity, and supply chain risks may be prioritized.</p></li>
</ul></td>
<td style="text-align: left;"><ul>
<li><p>Audit system dependencies, supply chains, and third party components for data privacy (e.g., transfer of localized data outside of restricted juristictions), intellectual property (e.g., presence of licensed material in training data), obscenity (e.g., presence of CASM in training data) or security (e.g., data poisoning) risks.</p></li>
<li><p>Complete red-teaming for data privacy, information security, intellectual property, and obscenity risks.</p></li>
<li><p>Review third-party documentation, materials, and software artifacts for potential unauthorized data collection, secondary data use, or telemetrics.</p></li>
</ul></td>
</tr>
</tbody>
</table>

### D.4: AI Risk Management Framework Actions Aligned to Red Teaming
GOVERN 3.2, GOVERN 4.1, MANAGE 2.2, MANAGE 4.1, MEASURE 1.1, MEASURE
1.3, MEASURE 2.6, MEASURE 2.7, MEASURE 2.8, MEASURE 2.10, MEASURE 2.11

**Usage Note**: Materials in Section D can be used to perform
red-teaming to measure the risk that expert adversarial actors can
manipulate LLM systems or risks that users may encounter under
worst-case or anomalous scenarios.

-   Try augmenting strategies with tools listed in D.1. 

-   Strategies and goals in Table D.2 can be applied to assess whether
    LLM outputs may violate trustworthy characteristics under
    adversarial, anomalous, or worst-case scenarios.

-   Strategies and goals in Table D.3 can be applied to assess whether
    LLM outputs may give rise to GAI risks under adversarial, anomalous,
    or worst-case scenarios.

-   Subsection D.4 highlights subcategories to indicate alignment with
    the AI RMF.

The materials in Section D reference measurement approaches that should
be accompanied by field testing for high risk systems or applications.

## E: Selected Risk Controls for Generative AI

<table style="width:95%;">
<caption>Table E: Selected generative AI risk controls <a href="#national-institute-of-standards-and-technology-nist-artificial-intelligence-risk-management-framework-ai-rmf-10-nist-ai-100-1-gaithersburg-md-nist-january-26-2023-httpsdoiorg106028nistai100-1">[NIST AI RMF 1.0]</a>, <a href="#national-institute-of-standards-and-technology-nist-nist-ai-rmf-playbook-trustworthy--responsible-ai-resource-center-accessed-september-19-2024-httpsaircnistgovai_rmf_knowledge_baseplaybook">[NIST AI RMF Playbook]</a>, <a href="#national-institute-of-standards-and-technology-nist-artificial-intelligence-risk-management-framework-generative-artificial-intelligence-profile-nist-ai-600-1-gaithersburg-md-nist-july-2024-httpsdoiorg106028nistai600-1">[NIST AI 600-1]</a>, <a href="#isoiec-420012023-information-technology--artificial-intelligence--management-system-1st-ed-geneva-international-organization-for-standardization-2023-httpswwwisoorgobpuienisostdiso-iec42001ed-1v1en">[ISO/IEC 42001:2023]</a>, <a href="#mcgraw-gary-harold-figueroa-katie-mcmahon-and-richie-bonett-an-architectural-risk-analysis-of-large-language-models-applied-machine-learning-security-version-10-berryville-institute-of-machine-learning-biml-january-24-2024-httpsberryvilleimlcomdocsbiml-llm24pdf">[McGraw et al. 1]</a>, <a href="#mcgraw-gary-harold-figueroa-victor-shepardson-and-richie-bonett-an-architectural-risk-analysis-of-machine-learning-systems-toward-more-secure-machine-learning-version-10-11320-berryville-institute-of-machine-learning-biml-january-13-2020-httpsberryvilleimlcomdocsarapdf">[McGraw et al. 2]</a>, <a href="#microsoft-microsoft-responsible-ai-standard-v2-general-requirements-for-external-release-june-2022-httpsqueryprodcmsrtmicrosoftcomcmsapiambinaryre5cmfl">[Microsoft]</a>, <a href="#department-for-science-innovation-and-technology-and-ai-safety-institute-international-scientific-report-on-the-safety-of-advanced-ai-interim-report-published-may-17-2024-httpswwwgovukgovernmentpublicationsinternational-scientific-report-on-the-safety-of-advanced-ai">[DSIT & AISI]</a>, <a href="#office-of-the-comptroller-of-the-currency-occ-model-risk-management-comptrollers-handbook-version-10-august-2021-httpswwwoccgovpublications-and-resourcespublicationscomptrollers-handbookfilesmodel-risk-managementindex-model-risk-managementhtml">[OCC Model Risk Management]</a>.</caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 70%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><strong>Name</strong></th>
<th style="text-align: left;"><strong>Description</strong> (Selected NIST AI RMF Action IDs)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Access Control</td>
<td style="text-align: left;">GAI systems are limited to authorized users. (MG-2.2-009, MG-2.2-014, MS-2.7-030)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Accessibility</td>
<td style="text-align: left;">Accessibility features, opt-out, and reasonable accomodation are available to users. (GV-3.1-004, GV-3.1-005, GV-3.2-002, GV-6.1-016, MG-2.1-005, MS-2.11-009, MS-2.8-006)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Approved List</td>
<td style="text-align: left;">Vendors, service providers, plugins, open source packages and other external resources are screened, approved, and documented. (GV-6.1-013, MP-4.2-003)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Authentication</td>
<td style="text-align: left;">GAI system user identities are confirmed via authentication mechanisms. (MG-2.2-009, MG-2.2-014, MS-2.7-030)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Blocklist</td>
<td style="text-align: left;">Users or internal personnel who violate terms of service, prohibited use policies, and other organization polices and documented, tracked, and restricted from future system use. (GV-4.2-007)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Change Management</td>
<td style="text-align: left;">GAI systems and components are versioned; plans for updates, hotfixes, patches and other changes are documented and communicated. (GV-1.2-009, GV-1.4-002, GV-1.6-003, GV-2.2-006, MG-2.4-001, MG-2.4-006, MG-3.1-013, MG-4.3-002, MP-4.1-023, MS-2.5-010)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Consent</td>
<td style="text-align: left;">User consent for data use is obtained and documented. (GV-1.6-003, MS-2.10-006, MS-2.10-013, MS-2.2-009, MS-2.2-011, MS-2.2-021, MS-2.2-023, MS-2.3-003, MS-2.4-002)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Content Moderation</td>
<td style="text-align: left;">Training data and system outputs are screened for accuracy, safety, bias, data privacy, intellectual property infringements, malware materials, phishing materials, confabulated packages and other issues using human oversight, business rules, and other language models. (GV-3.2-002, MS-2.5-005, MS-2.11-002)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Contract Review</td>
<td style="text-align: left;">Vendor, services and data provider agreements are reviewed for coverage of SLAs, content ownership, usage rights, performance standards, security requirements, incident response, critical support, system availability, assignment of liabilitly, appropriate indemnification, dispute resolution and other provisions relevanto AI risk management. (GV-1.7-003 GV-6.1-004, GV-6.1-009, GV-6.1-012, GV-6.1-019, GV-6.2-016, MG-2.2-015, MP-4.1-015, MP-4.1-021)</td>
</tr>
<tr class="even">
<td style="text-align: left;">CSAM/Obsenity Removal</td>
<td style="text-align: left;">Training data and system outputs are screened for obscene materials and CSAM using human oversight, business rules, and other language models. (GV-1.1-005 GV-1.2-005)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Data Provenance</td>
<td style="text-align: left;">Training data origins, ownership, contents, and metadata are well understood, documented, and do not increase AI risk. (GV-1.2-006, GV-1.2-007, GV-1.3-001, GV-1.3-005, GV-1.5-001, GV-1.5-003, GV-1.5-006, GV-1.5-007, GV-1.6-003, GV-4.2-001, GV-4.2-008, GV-4.2-009, GV-5.1-003, GV-6.1-001, GV-6.1-003, GV-6.1-006, GV-6.1-007, GV-6.1-009, GV-6.1-010, GV-6.1-011, GV-6.1-012, GV-6.1-014, GV-6.1-015, GV-6.1-016, MG-2.2-002, MG-2.2-003, MG-2.2-008, MG-2.2-011, MG-3.1-007, MG-3.1-009, MG-3.2-003, MG-3.2-005, MG-3.2-006, MG-3.2-007, MG-3.2-009, MG-4.1-001, MG-4.1-002, MG-4.1-003, MG-4.1-008, MG-4.1-009, MG-4.1-013, MG-4.1-015, MG-4.2-001, MG-4.2-003, MG-4.2-004, MP-2.1-001, MP-2.1-003, MP-2.1-005, MP-2.2-003, MP-2.2-004, MP-2.2-005, MP-2.3-001, MP-2.3-004, MP-2.3-006, MP-2.3-008, MP-2.3-011, MP-2.3-012, MP-3.4-001, MP-3.4-002, MP-3.4-004, MP-3.4-005, MP-3.4-006, MP-3.4-007, MP-3.4-008, MP-3.4-009, MP-4.1-004, MP-4.1-009, MP-4.1-011, MP-5.1-001, MP-5.1-002, MP-5.1-005, MS-1.1-006, MS-1.1-007, MS-1.1-008, MS-1.1-009, MS-1.1-010, MS-1.1-011, MS-1.1-012, MS-1.1-014, MS-1.1-015, MS-1.1-016, MS-1.1-017, MS-1.1-018, MS-2.2-001, MS-2.2-002, MS-2.2-003, MS-2.2-004, MS-2.2-005, MS-2.2-008, MS-2.2-009, MS-2.2-010, MS-2.2-011, MS-2.2-015, MS-2.2-016, MS-2.2-022, MS-2.5-012, MS-2.6-002, MS-2.7-002, MS-2.7-003, MS-2.7-004, MS-2.7-005, MS-2.7-007, MS-2.7-009, MS-2.7-010, MS-2.7-011, MS-2.7-012, MS-2.7-020, MS-2.7-021, MS-2.7-025, MS-2.7-032, MS-2.8-001, MS-2.8-005, MS-2.8-008, MS-2.8-011, MS-2.9-003, MS-2.10-001, MS-2.10-004, MS-2.10-006, MS-2.10-007, MS-2.10-009, MS-3.3-002, MS-3.3-003, MS-3.3-006, MS-3.3-008, MS-3.3-009, MS-3.3-012, MS-4.2-001, MS-4.2-004, MS-4.2-005, MS-4.2-006, MS-4.2-008, MS-4.2-009, MS-4.2-011)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Data Quality</td>
<td style="text-align: left;">Input data is accurate, representative, complete and documented, and data quality issues have been minimized. (GV-1.2-009, MS-2.2-020, MS-2.9-003, MS-4.2-007)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Data Retention</td>
<td style="text-align: left;">User prompts and associated system outputs are retained and monitored in alignment with relevant data privacy policies and roles. (GV-1.5-006, MP-4.1-009, MS-2.10-013)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Decommission Process</td>
<td style="text-align: left;">Decommissioning processes for GAI systems are planned, documented and communicated to users, and involve staging, data protection, containment protocols, and recourse mechanisms for decommissioned GAI systems. (GV-1.6-004, GV-1.7-001, GV-1.7-002, GV-1.7-003, GV-1.7-004, GV-1.7-005, GV-1.7-006, GV-1.7-007, GV-1.7-008, GV-3.2-002, GV-3.2-006, GV-4.1-004, GV-5.2-002, MG-2.3-005, MG-2.4-009, MG-3.1-003, MG-3.1-012, MG-3.2-011, MG-3.2-012, MG-4.1-016, MP-1.5-004, MP-2.2-007, MS-4.2-010)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Dependency Screening</td>
<td style="text-align: left;">GAI system dependencies are screened for security vulnerabilities. (GV-1.3-001, GV-1.4-002, GV-1.6-003, GV-1.7-003, GV-1.7-006, GV-6.2-002, GV-6.2-005, GV-6.2-006, MP-1.2-006, MP-1.6-001, MP-2.2-008, MP-4.1-012, MS-2.7-001)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Digital Signature</td>
<td style="text-align: left;">GAI-generated content is signed to preserve information integrity using watermarking, cryptogrpahic signature, steganography or similar methods. (GV-1.2-006, GV-1.6-003, GV-6.1-011, MG-4.1-008, MP-2.3-004, MS-1.1-006, MS-1.1-016, MS-2.7-009, MS-2.7-032)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Disclosure of AI Interaction</td>
<td style="text-align: left;">AI interactions are disclosed to internal personnel and external users. (GV-1.1-003, GV-1.4-004, GV-1.6-003, GV-5.1-002)</td>
</tr>
<tr class="even">
<td style="text-align: left;">External Audit</td>
<td style="text-align: left;">GAI systems are audited by qualified external experts. (GV-1.2-009, GV-1.4-004, GV-3.2-001, GV-3.2-002, GV-4.1-003, GV-4.1-008, GV-5.1-003, MG-4.2-002, MP-2.3-011, MP-4.1-002, MS-1.3-005, MS-1.3-006, MS-1.3-010, MS-2.5-003, MS-2.8-020)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Failure Avoidance</td>
<td style="text-align: left;">AIID, AVID, GWU AI Litigation Database, OECD incident monitor or similar are consulted in design or procurement phases of GAI lifecycles to avoid repeating past known failures. (GV-1.6-003, MG-2.1-006, MG-3.1-008, MG-4.1-003, MP-1.1-003, MP-1.1-006, MS-1.1-003, MS-2.2-020, MS-2.7-031)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Fast Decommission</td>
<td style="text-align: left;">GAI systems can be quickly and safely disengaged. (GV-1.7-002, GV-1.7-003, GV-1.7-006, GV-3.2-006, GV-5.2-002, MG-2.3-005, MG-2.4-009, MG-3.1-003, MG-3.1-012, MG-3.2-012, MG-4.1-016)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Fine Tuning</td>
<td style="text-align: left;">GAI systems are fine-tuned to their operational domain using relevant and high-quality data. (GV-6.1-016, MG-3.1-001, MG-3.2-002, MP-4.1-013, MS-2.6-004)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Grounding</td>
<td style="text-align: left;">GAI systems are trained or fine-tuned on accurate, clean, and fully transparent training data. (GV-1.2-002, MG-3.1-001, MP-2.3-001, MS-2.3-017, MS-2.5-012)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Human Review</td>
<td style="text-align: left;">AI generated content is reviewed for accuracy and safety by qualified personnel. (GV-1.3-001, MG-2.2-008, MS-2.4-005, MS-2.5-015 )</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Incident Response</td>
<td style="text-align: left;">Incident response plans for GAI failures, abuses, or misuses are documented, rehearsed, and updated appropriately after each incident; GAI incident response plans are coordinated with and communicated to other incident response functions. (GV-1.2-009, GV-1.5-001, GV-1.5-004, GV-1.5-005, GV-1.5-013, GV-1.5-015, GV-1.6-003, GV-1.6-007, GV-2.1-004, GV-3.2-002, GV-4.1-006, GV-4.2-002, GV-4.3-013, GV-6.1-006, GV-6.2-008, GV-6.2-016, GV-6.2-018, MG-1.3-001, MG-2.3-001, MG-2.3-002, MG-2.3-003, MG-2.4-004, MG-4.2-006, MG-4.3-001, MS-2.6-003, MS-2.6-012, MS-2.6-015, MS-2.7-002, MS-2.7-018, MS-2.7-028, MS-3.1-007)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Incorporate feedback</td>
<td style="text-align: left;">User feedback is incorporated in GAI design, development, and risk management. (GV-3.2-005, GV-4.3-007, GV-5.1-003, GV-5.1-009, GV-5.2-004, MG-2.2-007, MG-2.2-012, MG-2.3-007, MG-3.2-004, MG-4.1-019, MG-4.2-013, MP-1.6-005, MP-2.3-018, MP-3.1-003, MP-2.3-019, MP-5.2-007, MS-1.2-008, MS-3.3-009, MS-3.3-010, MS-4.1-004, MS-4.2-007, MS-4.2-010, MS-4.2-013, MS-4.2-020)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Instructions</td>
<td style="text-align: left;">Users are provided with the necessary instructions for safe, valid, and productive use. (GV-5.1-006, GV-6.1-021, GV-6.2-014, MG-3.1-009, MS-2.8-012)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Insurance</td>
<td style="text-align: left;">Risk transfer via insurance policies is considered and implemented when feasibable and appropriate. (MG-2.2-015)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Intellectual Property Removal</td>
<td style="text-align: left;">Licensed, patented, trademarked, trade secret, or other data that may violate the intellectual property rights of others is removed from system training data; generated system outputs are monitored for similar information. (GV-1.6-003, MG-3.1-007, MP-2.3-012, MP-4.1-004, MP-4.1-009, MS-2.2-022, MS-2.6-002, MS-2.8-001, MS-2.8-008)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Inventory</td>
<td style="text-align: left;">GAI system is information is stored in the organizational model inventory. (GV-1.4-005, GV-1.6-001, GV-1.6-002, GV-1.6-003, GV-1.6-004, GV-1.6-006, GV-1.6-009, GV-4.2-010, GV-6.1-013, MG-3.2-014, MP-4.1-020, MP-4.2-003, MP-5.1-004 MS-2.13-002, MS-3.2-007)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Malware Screening</td>
<td style="text-align: left;">GAI weights and other software components are scanned for malware. (MG-3.1-002, MS-2.7-001)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Model Documentation</td>
<td style="text-align: left;">All technical mechanisms with GAI systems are well documented, including open source and third party GAI systems. (GV-1.3-009, GV-1.4-002, GV-1.4-004, GV-1.4-005, GV-1.4-007, GV-1.6-007, GV-3.2-002, GV-3.2-009, GV-4.1-002, GV-4.2-011, GV-4.2-013, GV-4.3-002, GV-6.2-001, GV-6.2-014, MG-1.3-010, MG-2.2-016, MG-3.1-004, MG-3.1-009, MG-3.1-013, MG-3.1-015, MP-2.1-002, MP-2.3-027, MP-3.1-004, MP-3.4-015, MP-4.1-021, MP-4.2-003, MP-5.2-010, MS-1.3-002, MS-2.1-001, MS-2.2-014, MS-2.7-002, MS-2.7-012, MS-2.7-024, MS-2.8-007, MS-2.8-011)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Monitoring</td>
<td style="text-align: left;">GAI systems are inputs and outputs are monitored for drift, accuracy, safety, bias, data privacy, intellectual property infringements, malware materials, phishing materials, confabulated packages, obscene materials, and CSAM. (GV-1.2-009, GV-1.5-001, GV-1.5-003, GV-1.5-005, GV-1.5-012, GV-1.5-015, GV-1.6-003, GV-3.2-011, GV-4.2-007, GV-4.2-010, GV-4.3-001, GV-6.1-016, GV-6.2-010, MG-2.1-004, MG-2.2-003, MG-2.3-008, MG-2.3-010, MG-3.1-016, MG-3.2-006, MG-3.2-013, MG-3.2-016, MG-4.1-005, MG-4.1-009, MG-4.1-010, MG-4.1-018, MP-3.4-007, MP-4.1-002, MP-4.1-004, MP-5.2-009, MS-1.1-029, MS-1.2-005, MS-2.2-007, MS-2.4-003, MS-2.4-004, MS-2.5-007, MS-2.5-008, MS-2.5-024, MS-2.6-003, MS-2.6-009, MS-2.6-016, MS-2.7-013, MS-2.7-014, MS-2.7-015, MS-2.10-007, MS-2.10-019, MS-2.10-020, MS-2.11-006, MS-2.11-030, MS-3.3-006, MS-4.2-009, MS-4.3-004)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Narrow Scope</td>
<td style="text-align: left;">Systems are deployed for targeted business applications with documented and direct business value. (GV-1.2-002, MP-3.3-001, MP-5.1-011)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Open Source</td>
<td style="text-align: left;">Open source code is used to promote explainability and transparency. (MG-4.2-007, MP-4.1-017)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Ownership</td>
<td style="text-align: left;">GAI systems and vendor relationships are owned by specific and documented internal personnel. (GV-6.1-009, GV-6.1-016, GV-6.2-008, MP-1.1-005, MP-1.1-008)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Prohibited Use Policy</td>
<td style="text-align: left;">General abuse and misuse of GAI systems by internal parties is restricted by organizational policies. (GV-1.1-006, GV-1.2-003, GV-1.6-003, GV-3.2-003, GV-4.1-001, GV-6.1-017, GV-6.1-017)</td>
</tr>
<tr class="even">
<td style="text-align: left;">RAG</td>
<td style="text-align: left;">Retreival augmented generation (RAG) is used to improve accuracy in generated content. (GV-1.2-002, MS-2.3-004, MS-2.5-005, MS-2.5-012, MS-2.9-003, MG-3.1-001, MG-3.1-006, MG-3.2-002, MG-3.2-003)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Rate-limiting</td>
<td style="text-align: left;">GAI response times and query volumes are limited. (MS-2.6-007)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Redudancy</td>
<td style="text-align: left;">Rollover, fallback, and other redundancy mechanisms are available for GAI systems and address weights and other important system components. (GV-6.2-003, GV-6.2-007, GV-6.2-012, MG-2.4-012, MS-2.6-008)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Refresh</td>
<td style="text-align: left;">Systems are retrained or re-tuned at a reasonable cadence. (MG-3.1-001, MG-3.2-011, MS-2.3-004, MS-2.12-003)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Restrict Anonymous Use</td>
<td style="text-align: left;">Anonymous use of GAI systems is restricted. (GV-3.2-002)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Restrict Anthropomorphization</td>
<td style="text-align: left;">Human, animal, cyborg, emotional or other images or features that promote anthropomorphization of GAI systems are restricted. (GV-1.3-001, MS-2.5-009)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Restrict Data Collection</td>
<td style="text-align: left;">All data collection is disclosed, collected data is protected and use in a transparent fashion. (GV-6.2-016, MS-2.2-023, MS-2.10-013)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Restrict Decision Making</td>
<td style="text-align: left;">GAI systems are not employed for material decision-making tasks. (GV-1.3-001, GV-4.1-001, MP-1.1-018, MP-1.6-001, MP-3.4-017)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Restrict Homogeneity</td>
<td style="text-align: left;">Feedback loops in which GAI systems are trained with GAI-generated data are restricted. (GV-1.3-004, MS-2.11-011)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Restrict Internet Access</td>
<td style="text-align: left;">GAI systems are disconnected from the internet. (MP-2.2-007)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Restrict Location Tracking</td>
<td style="text-align: left;">Any location tracking is conducted with user consent, disclosed, aligned with relevant privacy policies and laws and potential threats to user safety are managed. (MS-2.10-002)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Restrict Minors</td>
<td style="text-align: left;">Use of organizational GAI systems by minors are restricted. <span style="color: red">()</span></td>
</tr>
<tr class="even">
<td style="text-align: left;">Restrict Regulated Dealings</td>
<td style="text-align: left;">GAI is not deployed in regulated dealings or for material decision making. (GV-1.1-004, GV-1.3-001, GV-4.1-001, GV-5.2-001, MP-2.3-013, MS-2.11-018)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Restrict Secondary Use</td>
<td style="text-align: left;">Any secondary use of GAI input data is conducted with user consent, disclosed, and aligned with relevant privacy policies and laws. (GV-6.1-016, GV-6.2-016)</td>
</tr>
<tr class="even">
<td style="text-align: left;">RLHF</td>
<td style="text-align: left;">For third-party GAI systems, vendors engage in specific reinforcement with human feedback (RLHF) exercises to address identified risks; for internal systems, internal personnel engage in RLHF to address identified risks. (MG-2.1-002, MS-2.5-005, MS-2.9-003, MS-2.9-007)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Sensitive/Personal Data Removal</td>
<td style="text-align: left;">Personal, sensitive, biometric, or otherwise restricted data is minimized or eliminated from GAI training data. (GV-1.2-009, GV-1.6-003, MP-4.1-002, MP-4.1-016, MS-2.10-002, MS-2.10-003, MS-2.10-005, MS-2.10-014, MS-2.10-017, MS-2.10-018, MS-2.10-020)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Session Limits</td>
<td style="text-align: left;">Time, query volume, and response rate are limited for GAI user sessions. (GV-4.1-001, MS-2.6-007, MS-2.6-010)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Supply Chain Audit</td>
<td style="text-align: left;">GAI system supply chains are audited and documented, with a focus on data poisoning, malware, and software and hardware vulnerabilities. (GV-4.1-004, GV-6.1-011, GV-6.1-022, GV-6.2-003, MG-2.3-001, MG-3.1-002, MP-5.1-003, MS-1.1-008, MS-2.6-001, MS-2.7-001)</td>
</tr>
<tr class="even">
<td style="text-align: left;">System Documentation</td>
<td style="text-align: left;">GAI systems are well-documented whether internal, open source, or vendor-provided. (GV-1.3-009, GV-1.4-002, GV-1.4-004, GV-1.4-005, GV-1.4-007, GV-1.6-007, GV-3.2-002, GV-3.2-009, GV-4.1-002, GV-4.2-011, GV-4.2-013, GV-4.3-002, GV-6.2-001, GV-6.2-014, MG-1.3-010, MG-2.2-016, MG-3.1-004, MG-3.1-009, MG-3.1-013, MG-3.1-015, MP-2.1-002, MP-2.3-027, MP-3.1-004, MP-3.4-015, MP-4.1-021, MP-4.2-003, MP-5.2-010, MS-1.3-002, MS-2.1-001, MS-2.2-014, MS-2.7-002, MS-2.7-012, MS-2.7-024, MS-2.8-007, MS-2.8-011)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">System Prompt</td>
<td style="text-align: left;">System prompts are used to tune GAI systems to specific tasks and to mitigate risks. (GV-1.2-002, MS-2.3-004, MS-2.5-005, MS-2.5-012, MS-2.9-003, MG-3.1-001, MG-3.1-006, MG-3.2-002, MG-3.2-003)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Team Diversity</td>
<td style="text-align: left;">Teams that implement and manage GAI systems represent broad professional, educational, life-stage, and demographic diversity. (GV-2.1-004, GV-3.1-002, GV-3.1-004, GV-3.1-005, GV-3.2-008, MG-2.1-005, MP-1.2-003, MP-1.2-004, MP-1.2-007, MS-1.3-012, MS-1.3-017, MS-2.3-015, MS-3.3-012)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Temperature</td>
<td style="text-align: left;">Temperature settings are used to tune GAI systems to specific tasks and to mitigate risks. (GV-1.2-002, MS-2.3-004, MS-2.5-005, MS-2.5-012, MS-2.9-003, MG-3.1-001, MG-3.1-006, MG-3.2-002, MG-3.2-003)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Terms of Service</td>
<td style="text-align: left;">General abuse and misuse by external parties is prohibited by organizational policies. Adaptive terms of service based on trust-level for user. (GV-4.2-003, GV-4.2-005, GV-4.2-007, GV-6.1-016, GV-6.2-016, MP-4.1-021)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Training</td>
<td style="text-align: left;">Internal personnel recieve training on productivity and basic risk management for GAI systems. (GV-2.2-004, GV-3.2-002, GV-6.1-003, MS-1.1-014)</td>
</tr>
<tr class="even">
<td style="text-align: left;">User Feedback</td>
<td style="text-align: left;">GAI systems implement user feedback mechanisms. (GV-1.5-007, GV-1.5-009, GV-3.2-005, GV-5.1-001, GV-5.1-006, GV-5.1-007, GV-5.1-009, MG-1.3-005, MS-1.3-015, MS-1.3-016, MG-2.1-004, MG-2.2-012, MS-2.7-004, MS-4.2-012)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">User Recourse</td>
<td style="text-align: left;">Policies, processes, and technical mechanisms enable recourse for users who are harmed by GAI systems. (GV-1.5-010, GV-1.7-003, GV-5.1-001, GV-5.1-006, GV-5.1-009, MS-2.8-015, MS-2.8-019, MS-3.2-006, MS-4.2-012)</td>
</tr>
<tr class="even">
<td style="text-align: left;">Validation</td>
<td style="text-align: left;">GAI systems are shown to reliably generate valid results for their targeted business application. (GV-1.2-009, GV-1.4-002, GV-1.4-004, GV-3.2-002, GV-5.1-005, MG-2.2-016, MG-3.1-009, MG-3.1-014, MP-2.3-006, MP-2.3-013, MP-4.1-012, MS-2.3-005, MS-2.5-016, MS-2.9-002, MS-2.9-014)</td>
</tr>
<tr class="odd">
<td style="text-align: left;">XAI</td>
<td style="text-align: left;">Methods such as visualization, occlusion, model compression, pertubation studies, and similar are applied to increase explainability of GAI systems. (GV-1.4-002, GV-3.2-002, GV-5.1-005, MG-3.2-001, MP-2.2-006, MS-2.8-019, MS-2.9-001, MS-2.9-005, MS-2.9-006, MS-2.9-009, MS-2.9-011, MS-2.9-013, MS-2.9-015, MS-4.2-006)</td>
</tr>
</tbody>
</table>

**Usage Note**: Section E puts forward selected risk controls that organizations may apply for GAI risk management. Higher level controls are linked to specific GAI and AI RMF Playbook actions <a href="#national-institute-of-standards-and-technology-nist-nist-ai-rmf-playbook-trustworthy--responsible-ai-resource-center-accessed-september-19-2024-httpsaircnistgovai_rmf_knowledge_baseplaybook">[NIST AI RMF Playbook]</a>, <a href="#national-institute-of-standards-and-technology-nist-artificial-intelligence-risk-management-framework-generative-artificial-intelligence-profile-nist-ai-600-1-gaithersburg-md-nist-july-2024-httpsdoiorg106028nistai600-1">[NIST AI 600-1]</a>.

## F: Example Low-risk Generative AI Measurement and Management Plan

### F.1: Example Low-risk Generative AI Measurement and Management Plan Organized by Trustworthy Characteristic

<table>
  <caption>Table F.1: Example risk measurement and management approaches suitable for low-risk GAI applications organized by trustworthy characteristic.</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="2" style="text-align:center">Trustworthy Characteristic</th>
  <tr>
    <th>Accountable and Transparent</th>
    <th>Fair with Harmful Bias Managed</th>
  </tr>
  <tr>
    <th>Measure</th>
    <td>
      <ul>
        <li>An Evaluation on Large Language Model Outputs: Discourse and Memorization (see Appendix B)</li>
        <li>Big-bench: Truthfulness <a href="#srivastava-aarohi-abhinav-rastogi-abhishek-rao-abu-awal-md-shoeb-abubakar-abid-adam-fisch-adam-r-brown-adam-santoro-et-al-beyond-the-imitation-game-quantifying-and-extrapolating-the-capabilities-of-language-models-arxiv-preprint-last-revised-june-12-2023-httpsdoiorg1048550arxiv220604615">[Srivastava et al.]</a></li>
        <li>DecodingTrust: Machine Ethics <a href="#wang-boxin-weixin-chen-hengzhi-pei-chulin-xie-mintong-kang-chenhui-zhang-chejian-xu-zidi-xiong-ritik-dutta-rylan-schaeffer-et-al-decodingtrust-a-comprehensive-assessment-of-trustworthiness-in-gpt-models-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-1361-3123231339-published-may-30-2024-httpsdlacmorgdoi10555536661223667483">[Wang et al.]</a></li>
        <li>Evaluation Harness: ETHICS</li>
        <li>HELM: Copyright</li>
        <li>Mark My Words <a href="#piet-julien-chawin-sitawarin-vivian-fang-norman-mu-and-david-wagner-mark-my-words-analyzing-and-evaluating-language-model-watermarks-arxiv-preprint-last-revised-december-7-2023-httpsdoiorg1048550arxiv231200273">[Piet et al.]</a></li>
      </ul>    
    </td>
    <td>
      <ul>
        <li>BELEBELE</li>
        <li>Big-bench: Low-resource language, Non-English, Translation</li>
        <li>Big-bench: Social bias, Racial bias, Gender bias, Religious bias</li>
        <li>Big-bench: Toxicity</li>
        <li>DecodingTrust: Fairness</li>
        <li>DecodingTrust: Stereotype Bias</li>
        <li>DecodingTrust: Toxicity</li>
        <li>C-Eval (Chinese evaluation suite)</li>
        <li>Evaluation Harness: CrowS-Pairs</li>
        <li>Evaluation Harness: ToxiGen</li>
        <li>Finding New Biases in Language Models with a Holistic Descriptor Dataset <a href="#smith-eric-michael-melissa-hall-melanie-kambadur-eleonora-presani-and-adina-williams-im-sorry-to-hear-that-finding-new-biases-in-language-models-with-a-holistic-descriptor-dataset-arxiv-preprint-last-revised-october-27-2022-httpsdoiorg1048550arxiv220509209">[Smith et al.]</a></li>
        <li>From Pretraining Data to Language Models to Downstream Tasks: Tracking the Trails of Political Biases Leading to Unfair NLP Models</li>
        <li>HELM: Bias</li>
        <li>HELM: Toxicity</li>
        <li>MT-bench <a href="#zheng-lianmin-wei-lin-chiang-ying-sheng-siyuan-zhuang-zhanghao-wu-yonghao-zhuang-zi-lin-zhuohan-li-dacheng-li-and-eric-p-xing-judging-llm-as-a-judge-with-mt-bench-and-chatbot-arena-in-proceedings-of-the-37th-international-conference-on-neural-information-processing-systems-nips-23-article-no-2020-4659546623-published-may-30-2024-httpsdlacmorgdoi10555536661223668142">[Zheng et al.]</a></li>
        <li>The Self-Perception and Political Biases of ChatGPT <a href="#rutinowski-jérôme-sven-franke-jan-endendyk-ina-dormuth-moritz-roidl-and-markus-pauly-the-self-perception-and-political-biases-of-chatgpt-human-behavior-and-emerging-technologies-2024-httpsdoiorg10115520247115633">[Rutinowski et al.]</a></li>
        <li>Towards Measuring the Representation of Subjective Global Opinions in Language Models</li>
      </ul>    
    </td>
  </tr>
  <tr>
    <th>Manage</th>
    <td>
      <ul>
        <li>Contract Review</li> 	
	<li>Disclosure of AI Interaction</li> 		
	<li>Instructions</li> 	
	<li>Inventory</li> 	
	<li>Ownership</li> 	
	<li>Prohibited Use Policy</li>
	<li>Restrict Decision Making </li>					
	<li>System Documentation</li> 	
	<li>Terms of Service</li>
      </ul>
    </td>
    <td>
      <ul>
      <li> Content Moderation </li>
      <li> Failure Avoidance </li> 	
      <li> Instructions </li> 	
      <li> Inventory </li> 	
      <li> Ownership </li> 	
      <li> Prohibited Use Policy </li> 	
      <li> System Prompt </li> 	
      <li> Ownership </li>  	
      <li> Restrict Anonymous Use </li>
      <li> Restrict Decision Making </li> 
      <li> Temperature </li>
      <li> Terms of Service </li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <caption>Table F.1: Example risk measurement and management approaches suitable for low-risk GAI applications organized by trustworthy characteristic (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="4" style="text-align:center">Trustworthy Characteristic</th>
  <tr>
    <th>Interpretable and Explainable</th>
    <th>Privacy-enhanced</th>
    <th>Safe</th>
    <th>Secure and Resilient</th>
  </tr>
  <tr>
    <th>Measure</th>
    <td>
    </td>
    <td>
      <ul>
      <li> HELM: Copyright </li>
      <li> llmprivacy </li>
      <li> mimir
      </ul>
    </td>
    <td>
      <ul>
      <li> Big-bench: Convince Me </li>
      <li> Big-bench: Truthfulness </li>
      <li> HELM: Reiteration, Wedging </li>
      <li> Mark My Words </li>
      <li> MLCommons </li>
      <li> The WMDP Benchmark </li>
      </ul>
    </td>
    <td>
      <ul>
      <li> Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation </li>
      <li> DecodingTrust: Adversarial Robustness, Robustness Against Adversarial Demonstrations </li>
      <li> detect-pretrain-code </li>
      <li> In-The-Wild Jailbreak Prompts on LLMs </li>
      <li> JailbreakingLLMs </li>
      <li> llmprivacy </li>
      <li> mimir </li>
      <li> TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs </li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Manage</th>
    <td>
      <ul>
      <li> Instructions</li> 	
      <li> Inventory</li>
      <li> System Documentation</li> 	
      </ul>
    </td>
    <td>
      <ul>
      <li> Content Moderation</li> 	
      <li> Contract Review</li> 	
      <li> Failure Avoidance</li> 	
      <li> Inventory</li> 	
      <li> Ownership</li> 	
      <li> Prohibited Use Policy</li>
      <li> Restrict Anonymous Use</li> 					
      <li> System Documentation</li> 	
      <li> Terms of Service</li>
      </ul>
    </td>
    <td>
      <ul>
      <li> Content Moderation</li> 	
      <li> Disclosure of AI Interaction</li> 	
      <li> Failure Avoidance</li> 	
      <li> Instructions</li> 	
      <li> Inventory</li> 	
      <li> Ownership</li> 	
      <li> Prohibited Use Policy</li> 	
      <li> Restrict Anonymous Use</li> 	
      <li> Restrict Anthropomorphization </li> 				
      <li> Restrict Decision Making</li> 				
      <li> System Documentation</li> 	
      <li> System Prompt</li> 	
      <li> Temperature</li> 	
      <li> Terms of Service </li>
      </ul>
    </td>
    <td>
      <ul>
      <li> Access Control</li> 	
      <li> Approved List</li> 	
      <li> Authentication</li> 	
      <li> Change Management</li> 	
      <li> Dependency Screening</li> 	
      <li> Failure Avoidance</li> 	
      <li> Inventory</li> 	
      <li> Ownership</li>  	
      <li> Malware Screening</li>
      <li> Restrict Anonymous Use</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <caption>Table F.1: Example risk measurement and management approaches suitable for low-risk GAI applications organized by trustworthy characteristic (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th>Trustworthy Characteristic</th>
  <tr>
    <th style="text-align:center">Valid and Reliable</th>
  </tr>
  <tr>
    <th>Measure</th>
    <td>
      <ul>
      <li> Big-bench: Algorithms, Logical reasoning, Implicit reasoning, Mathematics, Arithmetic, Algebra, Mathematical proof, Black-Box Fallacy, Negation, Computer code, Probabilistic reasoning, Social reasoning, Analogical reasoning, Multi-step, Understanding the World </li>
      <li> Big-bench: Analytic entailment, Formal fallacies and syllogisms with negation, Entailed polarity </li>
      <li> Big-bench: Context Free Question Answering </li>
      <li> Big-bench: Contextual question answering, Reading comprehension, Question generation </li>
      <li> Big-bench: Morphology, Grammar, Syntax </li>
      <li> Big-bench: Out-of-Distribution </li>
      <li> Big-bench: Paraphrase </li>
      <li> Big-bench: Sufficient information </li>
      <li> Big-bench: Summarization </li>
      <li> DecodingTrust: Out-of-Distribution Robustness, Adversarial Robustness, Robustness Against Adversarial Demonstrations </li>
      <li> Eval Gauntlet: Reading comprehension </li>
      <li> Eval Gauntlet: Commonsense reasoning, Symbolic problem solving, Programming </li>
      <li> Eval Gauntlet: Language Understanding </li>
      <li> Eval Gauntlet: World Knowledge </li>
      <li> Evaluation Harness: BLiMP </li>
      <li> Evaluation Harness: CoQA, ARC </li>
      <li> Evaluation Harness: GLUE </li>
      <li> Evaluation Harness: HellaSwag, OpenBookQA, TruthfulQA </li>
      <li> Evaluation Harness: MuTual </li>
      <li> Evaluation Harness: PIQA, PROST, MC-TACO, MathQA, LogiQA, DROP </li>
      <li> FLASK: Logical correctness, Logical robustness, Logical efficiency, Comprehension, Completeness  </li>
      <li> FLASK: Readability, Conciseness, Insightfulness </li>
      <li> HELM: Knowledge </li>
      <li> HELM: Language </li>
      <li> HELM: Text classification </li>
      <li> HELM: Question answering </li>
      <li> HELM: Reasoning </li>
      <li> HELM: Robustness to contrast sets </li>
      <li> HELM: Summarization </li>
      <li> Hugging Face: Fill-mask, Text generation  </li>
      <li> Hugging Face: Question answering </li>
      <li> Hugging Face: Summarization </li>
      <li> Hugging Face: Text classification, Token classification, Zero-shot classification </li>
      <li> MASSIVE  </li>
      <li> MT-bench </li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Manage</th>
    <td>
      <ul>
      <li> Content Moderation </li>
      <li> Disclosure of AI Interaction </li>
      <li> Failure Avoidance </li>
      <li> Instructions</li> 	
      <li> Restrict Anthropomorphization </li>		
      <li> Restrict Decision Making </li> 					 
      <li> System Documentation</li> 			
      <li> System Prompt </li>
      <li> Temperature </li> 	
      </ul>
    </td>
  </tr>
</table>

### F.2: Example Low-risk Generative AI Measurement and Management Plan Organized by Generative AI Risk

<table>
  <caption>Table F.2: Example risk measurement and management approaches suitable for low-risk GAI applications organized by GAI risk.</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="2" style="text-align:center">GAI Risk</th>
  <tr>
    <th>CBRN Information</th>
    <th>Confabulation</th>
  </tr>
  <tr>
    <th>Measure</th>
    <td>
      <ul>
        <li>Big-bench: Convince Me </li>
  			<li>Big-bench: Truthfulness </li>
  			<li>HELM: Reiteration, Wedging </li>
  			<li>MLCommons </li>
  			<li>The WMDP Benchmark </li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Big-bench: Algorithms, Logical reasoning, Implicit reasoning, Mathematics, Arithmetic, Algebra, Mathematical proof, Black-Box Fallacy, Negation, Computer code, Probabilistic reasoning, Social reasoning, Analogical reasoning,  Multi-step, Understanding the World </li>
  			<li>Big-bench: Analytic entailment, Formal fallacies and syllogisms with negation, Entailed polarity </li>
  			<li>Big-bench: Context Free Question Answering </li>
  			<li>Big-bench: Contextual question answering, Reading comprehension, Question generation </li>
  			<li>Big-bench: Convince Me </li>
  			<li>Big-bench: Low-resource language, Non-English, Translation </li>
  			<li>Big-bench: Morphology, Grammar, Syntax </li>
  			<li>Big-bench: Out-of-Distribution </li>
  			<li>Big-bench: Paraphrase </li>
  			<li>Big-bench: Sufficient information </li>
  			<li>Big-bench: Summarization </li>
  			<li>Big-bench: Truthfulness </li>
  			<li>C-Eval (Chinese evaluation suite) </li>
  			<li>DecodingTrust: Out-of-Distribution Robustness, Robustness Against Adversarial Demonstrations </li>
  			<li>Eval Gauntlet Reading comprehension </li>
  			<li>Eval Gauntlet: Commonsense reasoning, Symbolic problem solving, Programming </li>
  			<li>Eval Gauntlet: Language Understanding </li>
  			<li>Eval Gauntlet: World Knowledge </li>
  			<li>Evaluation Harness: BLiMP </li>
  			<li>Evaluation Harness: CoQA, ARC </li>
  			<li>Evaluation Harness: GLUE </li>
  			<li>Evaluation Harness: HellaSwag, OpenBookQA, TruthfulQA </li>
  			<li>Evaluation Harness: MuTual </li>
  			<li>Evaluation Harness: PIQA, PROST, MC-TACO, MathQA, LogiQA, DROP </li>
  			<li>FLASK: Logical correctness, Logical robustness, Logical efficiency, Comprehension,  Completeness </li>
  			<li>FLASK: Readability, Conciseness, Insightfulness </li>
  			<li>Finding New Biases in Language Models with a Holistic Descriptor Dataset </li>
  			<li>HELM: Knowledge </li>
  			<li>HELM: Language </li>
  			<li>HELM: Language (Twitter AAE) </li>
  			<li>HELM: Question answering </li>
  			<li>HELM: Reasoning </li>
  			<li>HELM: Reiteration, Wedging </li>
  			<li>HELM: Robustness to contrast sets </li>
  			<li>HELM: Summarization </li>
  			<li>HELM: Text classification </li>
  			<li>Hugging Face: Fill-mask, Text generation </li>
  			<li>Hugging Face: Question answering </li>
  			<li>Hugging Face: Summarization </li>
  			<li>Hugging Face: Text classification, Token classification, Zero-shot classification </li>
  			<li>MASSIVE </li>
  			<li>MLCommons </li>
  			<li>MT-bench  </li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Manage</th>
    <td>
      <ul>
        <li>Access Control </li>
  			<li>Failure Avoidance </li>
  			<li>Inventory</li> 	
  			<li>Ownership</li> 	
  			<li>Prohibited Use Policy </li>
  			<li>Terms of Service </li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Content Moderation </li>
  			<li>Disclosure of AI Interaction </li>
  			<li>Failure Avoidance </li>
  			<li>Instructions</li> 	
  			<li>Restrict Anthropomorphization </li>			
  			<li>Restrict Decision Making </li> 					 
  			<li>System Documentation</li> 			
  			<li>System Prompt </li>
  			<li>Temperature </li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <caption>Table F.2: Example risk measurement and management approaches suitable for low-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="4" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Dangerous or Violent Recommendations</th>
    <th style="text-align:center">Data Privacy</th>
    <th style="text-align:center">Environmental</th>
    <th style="text-align:center">Human-AI Configuration</th>
  </tr>
  <tr>
    <th>Measure</th>
    <td>
      <ul>
        <li>Big-bench: Convince Me</li> 	
  			<li>Big-bench: Toxicity</li> 	
  			<li>DecodingTrust: Adversarial Robustness, Robustness Against Adversarial Demonstrations</li> 	
  			<li>DecodingTrust: Machine Ethics</li> 	
  			<li>DecodingTrust: Toxicity</li> 	
  			<li>Evaluation Harness: ToxiGen</li> 	
  			<li>HELM: Reiteration, Wedging</li> 	
  			<li>HELM: Toxicity</li> 	
  			<li>MLCommons	</li> 	
      </ul>
    </td>
    <td>
      <ul>
        <li>An Evaluation on Large Language Model Outputs: Discourse and Memorization (with human scoring, see Appendix B)</li> 	
  			<li>Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation}</li> 	
  			<li>DecodingTrust: Machine Ethics</li> 	
  			<li>Evaluation Harness: ETHICS</li> 	
  			<li>HELM: Copyright</li> 	
  			<li>In-The-Wild Jailbreak Prompts on LLMs</li> 	
  			<li>JailbreakingLLMs</li> 	
  			<li>MLCommons</li> 	
  			<li>Mark My Words</li> 	
  			<li>TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs</li> 	
  			<li>detect-pretrain-code</li> 	
  			<li>llmprivacy</li> 	
  			<li>mimir 	</li>
      </ul>
    </td>
    <td>
      <ul>
			   <li>HELM: Efficiency	</li>
      </ul>
    </td>
    <td> </td>
  </tr>
  <tr>
    <th>Manage</th>
    <td>
      <ul>
        <li>Content Moderation</li>
  			<li>Disclosure of AI Interaction </li>				
  			<li>Failure Avoidance</li>
  			<li>Instructions </li>
  			<li>Inventory </li>
  			<li>Ownership </li>		 		
  			<li>Prohibited Use Policy</li>
  			<li>Restrict Anonymous Use</li>
  			<li>Restrict Anthropomorphization </li>
  			<li>Restrict Decision making </li>
  			<li>System Documentation </li>
  			<li>System Prompt </li>
  			<li>Temperature	</li>
  			<li>Terms of Service</li> 	
      </ul>
    </td>
    <td>
      <ul>
        <li>Content Moderation</li> 	
  			<li>Contract Review</li> 	
  			<li>Failure Avoidance</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li> 	
  			<li>Prohibited Use Policy</li> 	
  			<li>Restrict Anonymous Use</li> 				
  			<li>System Documentation</li> 	
  			<li>Terms of Service</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Access Control</li> 	
  			<li>Failure Avoidance</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li>
  			<li>Restrict Anonymous Use</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Content Moderation</li> 	
  			<li>Disclosure of AI Interaction</li> 	
  			<li>Failure Avoidance</li> 	
  			<li>Instructions</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li> 	
  			<li>Prohibited Use Policy</li> 	
  			<li>Restrict Anonymous Use</li> 	
  			<li>Restrict Anthropomorphization</li> 	
  			<li>Restrict Decision Making</li> 			
  			<li>Terms of Service</li> 	
  			<li>Training</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <caption>Table F.2: Example risk measurement and management approaches suitable for low-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="3" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Information Integrity</th>
    <th style="text-align:center">Information Security</th>
    <th style="text-align:center">Intellectual Property</th>
  </tr>
  <tr>
    <th>Measure</th>
    <td>
      <ul>
        <li>Big-bench: Analytic entailment, Formal fallacies and syllogisms with negation, Entailed polarity</li> 	
  			<li>Big-bench: Convince Me</li> 	
  			<li>Big-bench: Paraphrase</li> 	
  			<li>Big-bench: Sufficient information</li> 	
  			<li>Big-bench: Summarization</li> 	
  			<li>Big-bench: Truthfulness</li> 	
  			<li>DecodingTrust: Machine Ethics</li> 	
  			<li>DecodingTrust: Out-of-Distribution Robustness, Robustness Against Adversarial Demonstrations, Adversarial Robustness </li> 	
  			<li>Eval Gauntlet: Language Understanding</li> 	
  			<li>Eval Gauntlet: World Knowledge</li> 	
  			<li>Evaluation Harness: CoQA, ARC</li> 	
  			<li>Evaluation Harness: ETHICS</li> 	
  			<li>Evaluation Harness: GLUE</li> 	
  			<li>Evaluation Harness: HellaSwag, OpenBookQA, TruthfulQA</li> 	
  			<li>Evaluation Harness: MuTual</li> 	
  			<li>Evaluation Harness: PIQA, PROST, MC-TACO, MathQA, LogiQA, DROP</li> 	
  			<li>FLASK: Logical correctness, Logical robustness, Logical efficiency, Comprehension, Completeness</li> 	
  			<li>FLASK: Readability, Conciseness, Insightfulness</li> 	
  			<li>HELM: Knowledge</li> 	
  			<li>HELM: Language</li> 	
  			<li>HELM: Question answering</li> 	
  			<li>HELM: Reasoning</li> 	
  			<li>HELM: Reiteration, Wedging</li> 	
  			<li>HELM: Robustness to contrast sets</li> 	
  			<li>HELM: Summarization</li> 	
  			<li>HELM: Text classification</li> 	
  			<li>Hugging Face: Fill-mask, Text generation</li> 	
  			<li>Hugging Face: Question answering</li> 	
  			<li>Hugging Face: Summarization</li> 	
  			<li>MLCommons</li> 	
  			<li>MT-bench</li> 	
  			<li>Mark My Words	</li> 	
      </ul>
    </td>
    <td>
      <ul>
        <li>Big-bench: Convince Me</li> 	
  			<li>Big-bench: Out-of-Distribution</li> 	
  			<li>Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation</li> 	
  			<li>DecodingTrust: Out-of-Distribution  Robustness, Robustness Against Adversarial Demonstrations,  Adversarial Robustness, </li> 	
  			<li>Eval Gauntlet: Commonsense  reasoning, Symbolic problem solving, Programming</li> 	
  			<li>HELM: Copyright</li> 	
  			<li>In-The-Wild Jailbreak Prompts on LLMs</li> 	
  			<li>JailbreakingLLMs</li> 	
  			<li>Mark My Words</li> 	
  			<li>TAP: A Query-Efficient Method for  Jailbreaking Black-Box LLMs</li> 	
  			<li>detect-pretrain-code</li> 	
  			<li>llmprivacy</li> 	
  			<li>mimir</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>An Evaluation on Large Language Model Outputs: Discourse and Memorization (with human scoring, see Appendix B)</li> 	
  			<li>HELM: Copyright</li> 	
  			<li>Mark My Words</li> 	
  			<li>llmprivacy</li> 	
  			<li>mimir	</li> 	
      </ul>
    </td>
  </tr>
  <tr>
    <th>Manage</th>
    <td>
      <ul>
        <li>Content Moderation</li> 	
  			<li>Disclosure of AI Interaction</li> 	
  			<li>Failure Avoidance</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li> 	
  			<li>Prohibited Use Policy</li> 	
  			<li>Restrict Anonymous Use</li> 	
  			<li>Restrict Anthropomorphization</li>				
  			<li>System Prompt</li> 	
  			<li>Temperature</li> 	
  			<li>Terms of Service</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Access Control</li> 	
  			<li>Approved List</li> 	
  			<li>Authentication</li> 	
  			<li>Change Management</li> 	
  			<li>Dependency Screening</li> 	
  			<li>Failure Avoidance</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li> 	
  			<li>Malware Screening</li>
  			<li>Restrict Anonymous Use</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Contract Review</li> 	
  			<li>Disclosure of AI Interaction</li> 	
  			<li>Instructions</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li> 	
  			<li>Prohibited Use Policy</li> 	
  			<li>Terms of Service</li> 	
      </ul>
    </td>
  </tr>
</table>

<table>
  <caption>Table F.2: Example risk measurement and management approaches suitable for low-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="3" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Obscene, Degrading, and/or Abusive Content</th>
    <th style="text-align:center">Toxicity, Bias, and Homogenization</th>
    <th style="text-align:center">Value Chain and Component Integration</th>
  </tr>
  <tr>
    <th>Measure</th>
    <td>
      <ul>
        <li>Big-bench: Social bias, Racial bias, Gender bias, Religious bias</li> 	
  			<li>Big-bench: Toxicity</li> 	
  			<li>DecodingTrust: Fairness</li> 	
  			<li>DecodingTrust: Stereotype Bias</li> 	
  			<li>DecodingTrust: Toxicity</li> 	
  			<li>Evaluation Harness: CrowS-Pairs</li> 	
  			<li>Evaluation Harness: ToxiGen</li> 	
  			<li>HELM: Bias</li> 	
  			<li>HELM: Toxicity</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>BELEBELE</li> 	
  			<li>Big-bench: Low-resource language,  Non-English, Translation</li> 	
  			<li>Big-bench: Out-of-Distribution</li> 	
  			<li>Big-bench: Social bias, Racial bias, Gender bias, Religious bias</li> 	
  			<li>Big-bench: Toxicity</li> 	
  			<li>C-Eval (Chinese evaluation suite)</li> 	
  			<li>DecodingTrust: Fairness</li> 	
  			<li>DecodingTrust: Stereotype Bias</li> 	
  			<li>DecodingTrust: Toxicity</li> 	
  			<li>Eval Gauntlet: World Knowledge</li> 	
  			<li>Evaluation Harness: CrowS-Pairs</li> 	
  			<li>Evaluation Harness: ToxiGen</li> 	
  			<li>Finding New Biases in Language Models with a Holistic Descriptor Dataset</li> 	
  			<li>From Pretraining Data to Language Models to Downstream Tasks:
  			Tracking the Trails of Political Biases Leading to Unfair NLP Models</li> 	
  			<li>HELM: Bias</li> 	
  			<li>HELM: Toxicity</li> 	
  			<li>The Self-Perception and Political Biases of ChatGPT</li> 	
  			<li>Towards Measuring the Representation of Subjective Global Opinions in Language Models </li>
      </ul>
    </td>
    <td> </td>
  </tr>
  <tr>
    <th>Manage</th>
    <td>
      <ul>
        <li>Content Moderation</li> 		
  			<li>Failure Avoidance</li> 	
  			<li>Instructions</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li>
  			<li>Prohibited Use Policy</li> 	
  			<li>Restrict Anonymous Use</li> 			
  			<li>System Prompt</li> 	
  			<li>Temperature</li> 	
  			<li>Terms of Service</li> 	
      </ul>
    </td>
    <td>
      <ul>
        <li>Content Moderation</li>		
  			<li>Failure Avoidance</li> 	
  			<li>Instructions</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li>
  			<li>Prohibited Use Policy</li> 	
  			<li>Restrict Anonymous Use</li>
  			<li>Restrict Decision Making</li>  						
  			<li>System Prompt</li> 	
  			<li>Temperature</li> 	
  			<li>Terms of Service</li> 	
      </ul>
    </td>
    <td>
      <ul>
        <li>Contract Review</li> 	
  			<li>Disclosure of AI Interaction</li> 	
  			<li>Failure Avoidance</li> 	
  			<li>Inventory</li> 	
  			<li>Ownership</li> 	
  			<li>Prohibited Use Policy</li> 	
  			<li>System Documentation</li> 	
  			<li>Terms of Service	</li>
      </ul>
    </td>
  </tr>
</table>

**Usage Note**: Section F puts forward an example risk measurement and management plan for low risk GAI systems or applications. The low risk plan focuses on automatable model testing and applies minimally burdensome risk controls.

-   Material in Table F.1 can be applied to measure and manage GAI risks in risk programs that are aligned to the trustworthy characteristics.

-   Material in Table F.2 can be applied to measure and manage GAI risks in risk programs that are aligned to GAI risks.

Section G below presents an example plan for medium risk systems and Section H presents an example plan for high risk systems.

**Usage Note**: Section E puts forward selected risk controls that
organizations may apply for GAI risk management. Higher level controls
are linked to specific GAI and AI RMF Playbook actions.

## G: Example Medium-risk Generative AI Measurement and Management Plan

### G.1: Example Medium-risk Generative AI Measurement and Management Plan Organized by Trustworthy Characteristic

<table>
  <caption>Table G.1: Example risk measurement and management approaches suitable for medium-risk GAI applications organized by trustworthy characteristic.</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="2" style="text-align:center">Trustworthy Characteristic</th>
  <tr>
    <th>Accountable and Transparent</th>
    <th>Fair with Harmful Bias Managed</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Context exhaustion: logic-overloading prompts </li>
			<li> Loaded/leading questions </li>
			<li> Multi-tasking prompts </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Backwards relationships</li>   	
			<li> Counterfactual prompts</li>   	
			<li> Pros and cons prompts</li>   	
			<li> Role-playing prompts</li>   	
			<li> Loaded/leading questions</li>   	
			<li> Low context prompts</li>   	
			<li> Repeat this </li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Data Provenance</li>  	
			<li> Data Quality</li>  	
			<li> Decommission Process</li>  	
			<li> Digital Signature</li>  	
			<li> External Audit</li>  	
			<li> Fine Tuning</li>  	
			<li> Grounding</li>  	
			<li> Human Review </li>  	
			<li> Incident Response</li>  	
			<li> Incorporate feedback </li>  	
			<li> Model Documentation </li>  	
			<li> Monitoring</li>
			<li> Narrow Scope</li>
		 	<li> Open Source</li>  		
			<li> RAG</li>  	
			<li> Refresh</li>  	
			<li> RLHF</li>  	
			<li> Restrict Data Collection</li>  				
			<li> Restrict Secondary Use</li>  		
			<li> User Feedback</li>  	
			<li> Validation</li>  	
			</ul>
		</td>
		<td>
			<ul>
      <li> Accessibility </li>  	
			<li> Data Provenance</li>  	
			<li> Data Quality</li>  	
			<li> External Audit</li>  	
			<li> Fine Tuning</li>  	
			<li> Grounding</li>  	
			<li> Human Review </li>  	
			<li> Incident Response</li>  	
			<li> Incorporate feedback </li>  	
		 	<li> Narrow Scope</li>   
			<li> Restrict Homogeneity</li>  			 	
			<li> Team Diversity</li>  	
			<li> User Feedback</li>  	
			<li> Validation</li>
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table G.1: Example risk measurement and management approaches suitable for medium-risk GAI applications organized by trustworthy characteristic (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="4" style="text-align:center">Trustworthy Characteristic</th>
  <tr>
    <th>Interpretable and Explainable</th>
    <th>Privacy-enhanced</th>
    <th>Safe</th>
    <th>Secure and Resilient</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
      <ul>
			<li> Context exhaustion: logic-overloading prompts (to reveal unexplainable decisioning processes) </li>
      </ul>
    </td>
		<td>
			<ul>
      <li> Auto/biographical prompts</li>   	
			<li> User information awareness prompts</li>   	
			<li> Autocompletion prompts</li>   	
			<li> Repeat this 	</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Pros and cons prompts </li>
			<li> Role-playing prompts </li>
			<li> Impossible situation prompts </li>	
			<li> Content exhaustion: niche-seeking prompts </li>
			<li> Ingratiation/reverse psychology prompts </li>
			<li> Loaded/leading questions </li>
			<li> User information awareness prompts </li>
			<li> Repeat this </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Multi-tasking prompts </li>
			<li> Pros and cons prompts </li>
			<li> Role-playing prompts </li>		
			<li> Content exhaustion: niche-seeking prompts </li>
			<li> Ingratiation/reverse psychology prompts </li>
			<li> Prompt injection attacks </li>
			<li> Membership inference attacks </li>
			<li> Random attacks </li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Data Provenance</li>
	 		<li> External Audit</li>  		
			<li> Human Review </li>
			<li> Model Documentation </li>  	
			<li> Monitoring</li>
			<li> Open Source</li>  	
			<li> User Feedback</li>
			<li> XAI </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Consent</li>  	
			<li> Data Provenance</li>  	
			<li> Data Quality</li>  	
			<li> Data Retention</li>  	
			<li> External Audit</li>  	
			<li> Restrict Data Collection</li>  				
			<li> Restrict Location Tracking</li>  		 
			<li> Restrict Secondary Use</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Blocklist </li> 			 
			<li> Data Retention</li>  	
			<li> Decommission Process</li>  	
			<li> Digital Signature</li>  	
			<li> External Audit</li>
			<li> Human Review </li>  	
			<li> Incident Response</li>  	
			<li> Monitoring</li>  	
			<li> Narrow Scope</li>
			<li> Rate-limiting </li>
			<li> Restrict Location Tracking</li>   		
			<li> Session Limits</li>
			<li> User Feedback</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Blocklist </li>  	
			<li> Decommission Process</li>  	
			<li> External Audit</li>
			<li> Incident Response</li>   
			<li> Monitoring</li>  	
			<li> Open Source</li>
			<li> Rate-limiting </li>
			<li> Session Limits</li>
      </ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table G.1: Example risk measurement and management approaches suitable for medium-risk GAI applications organized by trustworthy characteristic (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th>Trustworthy Characteristic</th>
  <tr>
    <th style="text-align:center">Valid and Reliable</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Backwards relationships </li>
			<li> Context baiting (and/or switching) prompts </li>
			<li> Multi-tasking prompts </li>
			<li> Role-playing prompts </li>
			<li> Ingratiation/reverse psychology prompts </li>
			<li> Loaded/leading questions </li>
			<li> Time-perplexity prompts </li>
			<li> Niche-seeking prompts </li>
			<li> Logic overloading prompts </li>
			<li> Repeat this </li>
			<li> Numeric calculation </li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Data Quality</li>
			<li> Fine Tuning</li>  	
			<li> Grounding</li>  	
			<li> Human Review </li>  	
			<li> Incorporate feedback </li>
			<li> Model Documentation </li>  	
			<li> Monitoring</li>  	
			<li> Narrow Scope</li>  	
			<li> Open Source</li>  	
			<li> RAG</li>  	
			<li> Refresh</li>
			<li> Restrict Homogeneity</li>  					
			<li> RLHF</li>
			<li> Team Diversity</li>  	
			<li> User Feedback</li>  	
			<li> Validation</li>
			</ul>
		</td>
  </tr>
</table>

### G.2: Example Medium-risk Generative AI Measurement and Management Plan Organized by Generative AI Risk

<table>
  <caption>Table G.2: Example risk measurement and management approaches suitable for medium-risk GAI applications organized by GAI risk.</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="2" style="text-align:center">GAI Risk</th>
  <tr>
    <th>CBRN Information</th>
    <th>Confabulation</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Auto-completion prompts  </li>
			<li> Role-playing prompts </li>
			<li> Reverse psychology prompts </li>
			<li> Pros and cons prompts </li>
			<li> Multitasking prompts </li>
			<li> Repeat this </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Backwards relationship prompts </li>
			<li> Context baiting (and/or switching) prompts </li>
			<li> Context exhaustion: Logic overloading prompts </li>
			<li> Context exhaustion: Multi-tasking prompts </li>
			<li> Context exhaustion: Niche-seeking prompts </li>
			<li> Time perplexity prompts </li>
			<li> Loaded/leading questions </li>
			<li> Calculation and numeric queries </li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Blocklist </li>
			<li> Data Provenance</li>
			<li> Data Quality</li>   	 
			<li> Decommission Process</li>
			<li> Digital Signature</li>  	
			<li> External Audit</li>
			<li> Incident Response</li>
			<li> Monitoring</li>  	
			<li> Rate-limiting </li>  	
			<li> Session Limits</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Data Quality</li>
			<li> Fine Tuning</li>  	
			<li> Grounding</li>  	
			<li> Human Review </li>  	
			<li> Incorporate feedback </li>
			<li> Model Documentation </li>  	
			<li> Monitoring</li>  	
			<li> Narrow Scope</li>  	
			<li> Open Source</li>  	
			<li> RAG</li>  	
			<li> Refresh</li>
			<li> Restrict Homogeneity</li>  				
			<li> RLHF</li>
			<li> Team Diversity</li>  	
			<li> User Feedback</li>  	
			<li> Validation</li>
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table G.2: Example risk measurement and management approaches suitable for medium-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="4" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Dangerous or Violent Recommendations</th>
    <th style="text-align:center">Data Privacy</th>
    <th style="text-align:center">Environmental</th>
    <th style="text-align:center">Human-AI Configuration</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
				<li> Impossible situation prompts </li>   
      <li> Role-playing prompts </li>
			<li> Reverse psychology prompts </li>
			<li> Pros and cons prompts </li>
			<li> Multitasking prompts </li>
			<li> Repeat this </li>
			<li> Loaded/leading questions </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> User information awareness </li>
			<li> Membership inference attacks </li>
			<li> Auto/biographical prompts </li>
			<li> Repeat this </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Availability attacks </li>
			<li> Role-playing prompts </li>
			<li> Reverse psychology prompts </li>
			<li> Pros and cons prompts </li>
			<li> Multitasking prompts </li>
			</ul>
		</td>
		<td>
      <ul>
	<li> Impossible situation prompts </li>      
      <li> Role-playing prompts </li>
			<li> Reverse psychology prompts </li>
			<li> Pros and cons prompts </li>
			<li> Multitasking prompts </li>        
      </ul>
    </td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Blocklist </li> 			 
			<li> Data Retention</li>  	
			<li> Decommission Process</li>  	
			<li> Digital Signature</li>  	
			<li> External Audit</li>
			<li> Human Review </li>  	
			<li> Incident Response</li>  	
			<li> Monitoring</li>  	
			<li> Narrow Scope</li>
			<li> Rate-limiting </li>
			<li> Restrict Location Tracking</li>  					
			<li> Session Limits</li>
			<li> User Feedback</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Consent</li>  	
			<li> Data Provenance</li>  	
			<li> Data Quality</li>  	
			<li> Data Retention</li>  	
			<li> External Audit</li>  	
			<li> Restrict Data Collection</li>  			
			<li> Restrict Location Tracking</li>  		 
			<li> Restrict Secondary Use</li>  	
			</ul>
		</td>
		<td>
			<ul>
      <li> Decommission Process</li>  	
			<li> External Audit</li>
			<li> Incident Response</li>
			<li> Monitoring</li>
			<li> Rate-limiting </li>
			<li> Session Limits</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Accessibility </li>  	
			<li> Blocklist </li>  	
			<li> Consent</li>  	
			<li> Decommission Process</li>  	
			<li> Digital Signature</li>  	
			<li> External Audit</li>
			<li> Human Review </li>
			<li> Incorporate feedback </li>
			<li> Restrict Data Collection</li>  		
			<li> Restrict Location Tracking</li>  	
			<li> Restrict Secondary Use</li>  		
			<li> Session Limits</li>  	
			<li> User Feedback</li>  	
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table G.2: Example risk measurement and management approaches suitable for medium-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="3" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Information Integrity</th>
    <th style="text-align:center">Information Security</th>
    <th style="text-align:center">Intellectual Property</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Loaded/leading questions  </li>
			<li> Role-playing prompts </li>
			<li> Reverse psychology prompts </li>
			<li> Pros and cons prompts </li>
			<li> Multitasking prompts </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Confidentiality attacks  </li>
			<li> Integrity attacks  </li>
			<li> Availability attacks </li>
			<li> Random attacks </li>
			<li> Role-playing prompts </li>
			<li> Reverse psychology prompts </li>
			<li> Pros and cons prompts </li>
			<li> Multitasking prompts </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Confidentiality attacks </li>
			<li> Auto-complete prompts </li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Data Provenance</li>  	
			<li> Data Quality</li>  	
			<li> Digital Signature</li>  	
			<li> External Audit</li>
			<li> Fine Tuning</li>  	
			<li> Grounding</li>  	
			<li> Human Review </li>  	
			<li> Incident Response</li>  	
			<li> Incorporate feedback </li>
			<li> Monitoring</li>  	
			<li> Narrow Scope</li>  	
			<li> Open Source</li>  	
			<li> RAG</li>  	
			<li> Refresh</li>  	
			<li> Restrict Homogeneity</li>  			
			<li> RLHF</li>
			<li> User Feedback</li>
			<li> Validation</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Blocklist </li>  	
			<li> Decommission Process</li>  	
			<li> External Audit</li>
			<li> Incident Response</li>   
			<li> Monitoring</li>  	
			<li> Open Source</li>
			<li> Rate-limiting </li>
			<li> Session Limits</li>  	
			</ul>
		</td>
		<td>
			<ul>
      <li> Blocklist </li>
			<li> Data Provenance</li>
			<li> Data Quality</li>   	 
			<li> Decommission Process</li>
			<li> Digital Signature</li>  	
			<li> External Audit</li>
			<li> Incident Response</li>
			<li> Incorporate feedback </li>
			<li> Monitoring</li>  	
			<li> Open Source</li>
			<li> Rate-limiting </li>  	
			<li> Session Limits</li>  	
			<li> User Feedback</li>
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table G.2: Example risk measurement and management approaches suitable for medium-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="3" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Obscene, Degrading, and/or Abusive Content</th>
    <th style="text-align:center">Toxicity, Bias, and Homogenization</th>
    <th style="text-align:center">Value Chain and Component Integration</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Confidentiality attacks </li>
			<li> Autocomplete prompts </li>
			<li> Role-playing prompts </li>
			<li> Reverse psychology prompts </li>
			<li> Pros and cons prompts </li>
			<li> Multitasking prompts </li>
			<li> Loaded/leading questions  </li>
			<li> Repeat this </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Backwards relationship prompts </li>
			<li> Data poisoning attacks </li>
			<li> Counterfactual prompts </li>
			<li> Pros and cons prompts </li>
			<li> Role-playing prompts </li>
			<li> Low context prompts </li>
			<li> Loaded/leading questions  </li>
			<li> Repeat this </li>
			</ul>
		</td>
		<td> </td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Blocklist </li>
			<li> Data Provenance</li>
			<li> Data Quality</li>   	 
			<li> Decommission Process</li>
			<li> Digital Signature</li>  	
			<li> External Audit</li>
			<li> Incident Response</li>
			<li> Monitoring</li>  	
			<li> Rate-limiting </li>  	
			<li> Session Limits</li>
			<li> User Feedback</li>  	
			</ul>
		</td>
		<td>
			<ul>
      <li> Accessibility </li>  	
			<li> Data Provenance</li>  	
			<li> Data Quality</li>  	
			<li> External Audit</li>  	
			<li> Fine Tuning</li>  	
			<li> Grounding</li>  	
			<li> Human Review </li>  	
			<li> Incident Response</li>  	
			<li> Incorporate feedback </li>  	
			<li> Narrow Scope</li>   
			<li> Restrict Homogeneity</li>  				
			<li> Team Diversity</li>  	
			<li> User Feedback</li>  	
			<li> Validation</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Data Provenance</li>  	
			<li> Data Quality</li>  	
			<li> Digital Signature</li>  	
			<li> External Audit</li>  	
			<li> Model Documentation </li>
			<li> Restrict Data Collection</li>  				
			<li> Restrict Secondary Use</li>
			</ul>
		</td>
  </tr>
</table>

**Usage Note**: Section G puts forward an example risk measurement and management plan for medium risk GAI systems or applications. The
medium risk plan focuses on red-teaming and applies moderate risk controls. Measurement and management approaches from Section F should
also be applied to medium risk systems or applications.

-   Material in Table G.1 can be applied to measure and manage GAI risks in risk programs that are aligned to the trustworthy characteristics.

-   Material in Table G.2 can be applied to measure and manage GAI risks in risk programs that are aligned to GAI risks.

Section H below presents an example plan for high risk systems.

## H: Example High-risk Generative AI Measurement and Management Plan

### H.1: Example High-risk Generative AI Measurement and Management Plan Organized by Trustworthy Characteristic

<table>
  <caption>Table H.1: Example risk measurement and management approaches suitable for high-risk GAI applications organized by trustworthy characteristic.</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="2" style="text-align:center">Trustworthy Characteristic</th>
  <tr>
    <th>Accountable and Transparent</th>
    <th>Fair with Harmful Bias Managed</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Assessing data quality*</li>
			<li> Bias bounties </li>
			<li> Calibration*</li>
			<li> Cybersecurity testing </li>
			<li> Environmental metrics </li>
			<li> Field testing*</li>
			<li> Input/output measurement using classifiers </li>
			<li> Model assessment*</li>
			<li> Model comparison*</li>
			<li> Multi-session experiments*</li>
			<li> Online metrics/monitoring </li>
			<li> Perturbation studies*</li>
			<li> PII identification and removal </li>
			<li> Root cause analysis*</li>
			<li> Screening for information integrity </li>
			<li> Sensitivity analysis*</li>
			<li> Software testing </li>
			<li> Stakeholder engagement and feedback*</li>
			<li> Statistical quality control*</li>
			<li> Stress testing*</li>
			<li> Sub-sampling traffic for manually annotating </li>
			<li> Supply chain auditing </li>
			<li> Testing third-party dependencies </li>
			<li> User surveys*</li>
			<li> Validity testing/validation.* </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Analyze differences between intended and actual population of users or data subjects*</li>  	
			<li> Anomaly detection*</li>   	
			<li> Assessing data quality*</li>   	
			<li> Bias bounties</li>   	
			<li> Bias testing</li>   	
			<li> Calibration*</li>   	
			<li> Counterfactual/causal analysis</li>   	
			<li> Disaggregated metrics</li>   	
			<li> Field testing*</li>   	
			<li> Model assessment*</li>   	
			<li> Model comparison*</li>   	
			<li> Multi-session experiments*</li>   	
			<li> Root cause analysis*</li>   	
			<li> Software testing</li>   	
			<li> Statistical quality control*</li>   	
			<li> Stress testing*</li>   		
			<li> User surveys*</li>   		
			<li> Validity testing/validation.*
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  			
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>  	
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>   
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table H.1: Example risk measurement and management approaches suitable for high-risk GAI applications organized by trustworthy characteristic (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="4" style="text-align:center">Trustworthy Characteristic</th>
  <tr>
    <th>Interpretable and Explainable</th>
    <th>Privacy-enhanced</th>
    <th>Safe</th>
    <th>Secure and Resilient</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Analyze differences between intended and actual population of users or data subjects*</li>
			<li> Model comparison.* </li>
			<li> Multi-session experiments.* </li>
			<li> Root cause analysis.* </li> 			
			<li> Stakeholder engagement and feedback.*	</li> 		
			<li> UI/UX studies </li> 			
			<li> User surveys*</li>   
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Assessing data quality.* </li>
			<li> Cybersecurity testing</li>   
			<li> PII identification and removal</li>   		
			<li> Root cause analysis*</li>   	
			<li> Stakeholder engagement and feedback*</li>   	
			<li> Stress testing*</li>   	
			<li> Testing third-party dependencies </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Analyze differences between intended and actual population of users or data subjects*</li>  	 	
			<li> Assessing data quality*</li>   	 	
			<li> Bias bounties</li>   	
			<li> Calibration*</li>   	
			<li> Chaos testing</li>   	
			<li> Dangerous and violent
			content removal</li>   		
			<li> Field testing*</li>   	
			<li> Input/output measurement using classifiers </li>
			<li> Model assessment*</li>   	
			<li> Model comparison*</li>   	
			<li> Multi-session experiments*</li>   	
			<li> Perturbation studies*</li>   		
			<li> Root cause analysis*</li>   	
			<li> Sensitivity analysis*</li>   	
			<li> Stakeholder engagement and feedback*</li>   	
			<li> Statistical quality control*</li>   	
			<li> Stress testing*</li>   		
			<li> User surveys*</li>   	
			<li> Validity testing/validation*</li>   
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Anomaly detection*</li>
			<li> Assessing data quality*</li>
			<li> Bias bounties </li>
			<li> Calibration*</li>
			<li> Chaos testing </li>
			<li> Cybersecurity testing </li>
			<li> Data poisoning detection </li>
			<li> Model assessment*</li>
			<li> Model comparison*</li>
			<li> Root cause analysis*</li>
			<li> Software testing </li>
			<li> Stakeholder engagement and feedback*</li>
			<li> Stress testing*</li>
			<li> Supply chain auditing </li>
			<li> Testing third-party dependencies </li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Restrict regulated dealings </li>  		
			<li> Supply Chain Audit </li>  	
			<li> User recourse </li>   
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  		
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>   
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Redundancy </li>  	
			<li> Restrict internet access </li>  	
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply Chain Audit </li>  	
			<li> User recourse </li>  	
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  	
			<li> Redundancy </li>  	
			<li> Restrict internet access </li>  	
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table H.1: Example risk measurement and management approaches suitable for high-risk GAI applications organized by trustworthy characteristic (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th>Trustworthy Characteristic</th>
  <tr>
    <th style="text-align:center">Valid and Reliable</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Analyze differences between intended and actual population of users or data subjects*</li>  			
			<li> Assessing data quality*</li>   		
			<li> Bias bounties</li>   	
			<li> Calibration*</li>   	
			<li> Field testing*</li>   	
			<li> Input/output measurement using classifiers </li>
			<li> Model assessment*</li>   	
			<li> Model comparison*</li>   	
			<li> Multi-session experiments*</li>   		
			<li> Perturbation studies*</li>   				
			<li> Root cause analysis*</li>   	
			<li> Sensitivity analysis*</li>   	
			<li> Stakeholder engagement and  feedback*</li>   	
			<li> Statistical quality control*</li>   	
			<li> Stress testing*</li>   		
			<li> User surveys*</li>   	
			<li> Validity testing/validation*</li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Redundancy </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>   	
			</ul>
		</td>
  </tr>
</table>

### H.2: Example High-risk Generative AI Measurement and Management Plan Organized by Generative AI Risk

<table>
  <caption>Table H.2: Example risk measurement and management approaches suitable for high-risk GAI applications organized by GAI risk.</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="2" style="text-align:center">GAI Risk</th>
  <tr>
    <th>CBRN Information</th>
    <th>Confabulation</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Chaos testing</li>   	
			<li> Cybersecurity testing</li>   	
			<li> Input/output measurement using classifiers </li>
			<li> Online metrics/monitoring</li>   	
			<li> Perturbation studies*</li>   	
			<li> Prompt engineering</li>   		
			<li> Root cause analysis*</li>   	
			<li> Sensitivity analysis*</li>   	
			<li> Software testing</li>   	
			<li> Stress testing*</li>   	
			<li> Supply chain auditing </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Analyze differences between intended and actual population of users or data subjects*</li>  			
			<li> Assessing data quality*</li>   		
			<li> Bias bounties</li>   	
			<li> Calibration*</li>   	
			<li> Field testing*</li>   	
			<li> Input/output measurement using classifiers </li>
			<li> Model assessment*</li>   	
			<li> Model comparison*</li>   	
			<li> Multi-session experiments*</li>   		
			<li> Perturbation studies*</li>   				
			<li> Root cause analysis*</li>   	
			<li> Sensitivity analysis*</li>   	
			<li> Stakeholder engagement and  feedback*</li>   	
			<li> Statistical quality control*</li>   	
			<li> Stress testing*</li>   		
			<li> User surveys*</li>   	
			<li> Validity testing/validation*</li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> CBRN info removal</li>   
			<li> Fast decommission </li>  	
			<li> Restrict internet access </li>  	
			<li> Supply chain audit </li>  		
			</ul>
		</td>
		<td>
			<ul>
      <li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Restrict regulated dealings </li>  		
			<li> Supply chain audit </li>  	
			<li> User recourse </li>   
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table H.2: Example risk measurement and management approaches suitable for high-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="4" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Dangerous or Violent Recommendations</th>
    <th style="text-align:center">Data Privacy</th>
    <th style="text-align:center">Environmental</th>
    <th style="text-align:center">Human-AI Configuration</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Analyze differences between intended and actual population of users or data subjects*</li>  	 	
			<li> Assessing data quality*</li>   	 	
			<li> Bias bounties</li>   	
			<li> Calibration*</li>   	
			<li> Chaos testing</li>   	
			<li> Dangerous and violent content removal</li>   		
			<li> Field testing*</li>   	
			<li> Input/output measurement using classifiers </li>
			<li> Model assessment*</li>   	
			<li> Model comparison*</li>   	
			<li> Multi-session experiments*</li>   	
			<li> Perturbation studies*</li>   		
			<li> Root cause analysis*</li>   	
			<li> Sensitivity analysis*</li>   	
			<li> Stakeholder engagement and feedback*</li>   	
			<li> Statistical quality control*</li>   	
			<li> Stress testing*</li>   		
			<li> User surveys*</li>   	
			<li> Validity testing/validation*</li>   
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Assessing data quality.* </li>
			<li> Cybersecurity testing</li>   
			<li> PII identification and removal</li>   		
			<li> Root cause analysis*</li>   	
			<li> Stakeholder engagement and feedback*</li>   	
			<li> Stress testing*</li>   	
			<li> Testing third-party dependencies </li>
			</ul>
		</td>
		<td>
			<ul>
      <li>  Algorithmic impact assessments </li>
			<li>  Environmental metrics </li>
			<li>  Model comparison*</li>
			<li>  Online metrics/monitoring </li>
			<li>  Supply chain auditing </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Analyze differences between intended and actual population of users or data subjects*</li>  	 
			<li> Analyzing user feedback </li>
			<li> Bias bounties </li>
			<li> Calibration*</li>
			<li> Explainability/interpretability </li>
			<li> Field testing*</li>
			<li> Model assessment*</li>
			<li> Model comparison*</li>
			<li> Multi-session experiments*</li>
			<li> Root cause analysis*</li>
			<li> Stakeholder engagement and feedback*</li>
			<li> UI/UX studies </li>
			<li> User surveys*</li>
			<li> Validity testing/validation*</li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  		
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>   	 
			</ul>
		</td>
		<td>
			<ul>
      <li> Fast decommission </li>  	
			<li> Insurance </li>  		
			<li> Supply chain audit </li>  	
			<li> User recourse </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  		
			<li> Intellectual property removal </li>  	
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> User recourse </li>
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table H.2: Example risk measurement and management approaches suitable for high-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="3" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Information Integrity</th>
    <th style="text-align:center">Information Security</th>
    <th style="text-align:center">Intellectual Property</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Assessing data quality*</li>
			<li> Calibration*</li>
			<li> Human content moderation</li>   
			<li> Data poisoning detection </li>
			<li> Field testing*</li>
			<li> Model assessment*</li>
			<li> Model comparison*</li>
			<li> Multi-session experiments*</li>
			<li> Perturbation studies*</li>
			<li> Root cause analysis*</li>
			<li> Screening for information integrity </li>
			<li> Sensitivity analysis*</li>
			<li> Stakeholder engagement and feedback*</li>
			<li> Statistical quality control*</li>
			<li> Supply chain auditing </li>
			<li> Testing third-party dependencies </li>
			<li> User surveys*</li>
			<li> Validity testing/validation.* </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Anomaly detection*</li>
			<li> Assessing data quality*</li>
			<li> Bias bounties </li>
			<li> Calibration*</li>
			<li> Chaos testing </li>
			<li> Cybersecurity testing </li>
			<li> Data poisoning detection </li>
			<li> Model assessment*</li>
			<li> Model comparison*</li>
			<li> Root cause analysis*</li>
			<li> Software testing </li>
			<li> Stakeholder engagement and feedback*</li>
			<li> Stress testing*</li>
			<li> Supply chain auditing </li>
			<li> Testing third-party dependencies </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Assessing data quality*</li>
			<li> Cybersecurity testing </li>
			<li> Field testing*</li>
			<li> Input/output measurement using classifiers </li>   
			<li> Model comparison*</li>
			<li> Root cause analysis*</li>
			<li> Stakeholder engagement and feedback*</li>
			<li> Sub-sampling traffic for manually annotating </li>
			<li> Supply chain auditing </li>
			<li> Testing third-party dependencies </li>
			<li> User surveys*</li>
			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  	
			<li> Restrict internet access </li>  	
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>  	
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  	
			<li> Redundancy </li>  	
			<li> Restrict internet access </li>  	
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  	
			<li> Restrict internet access </li>  		
			<li> Supply chain audit </li>  	
			<li> User recourse </li>
			</ul>
		</td>
  </tr>
</table>

<table>
  <caption>Table H.2: Example risk measurement and management approaches suitable for high-risk GAI applications organized by GAI risk (continued).</caption>
  <tr>
    <th rowspan="2">Function</th>
    <th colspan="3" style="text-align:center">GAI Risk</th>
  <tr>
    <th style="text-align:center">Obscene, Degrading, and/or Abusive Content</th>
    <th style="text-align:center">Toxicity, Bias, and Homogenization</th>
    <th style="text-align:center">Value Chain and Component Integration</th>
  </tr>
  <tr>
    <th>Measure</th>
		<td>
			<ul>
      <li> Algorithmic impact assessments </li>
			<li> Assessing data quality*</li>
			<li> Calibration*</li>
			<li> Field testing*</li>
			<li> Input/output measurement using classifiers </li>
			<li> Model assessment*</li>
			<li> Model comparison*</li>
			<li> Root cause analysis*</li>
			<li> Small user studies </li>
			<li> Software testing </li>
			<li> Stakeholder engagement and feedback*</li>
			<li> Statistical quality control*</li>
			<li> Stress testing*</li>
			<li> Supply chain auditing </li>
			<li> Testing third-party dependencies </li>
			<li> User surveys*</li>
			</ul>
		</td>
		<td>
			<ul>
      <li> Algorithmic impact assessments</li>   	
			<li> Analyze differences between intended and actual population of  users or data subjects*</li>  	
			<li> Anomaly detection*</li>   	
			<li> Assessing data quality*</li>   	
			<li> Bias bounties</li>   	
			<li> Bias testing</li>   	
			<li> Calibration*</li>   	
			<li> Counterfactual/causal analysis</li>   	
			<li> Disaggregated metrics</li>   	
			<li> Field testing*</li>   	
			<li> Model assessment*</li>   	
			<li> Model comparison*</li>   	
			<li> Multi-session experiments*</li>   	
			<li> Root cause analysis*</li>   	
			<li> Software testing</li>   	
			<li> Statistical quality control*</li>   	
			<li> Stress testing*</li>   		
			<li> User surveys*</li>   		
			<li> Validity testing/validation.*
			</ul>
		</td>
		<td>
			<ul>
      <li> Assessing data quality*</li>
			<li> Model assessment*</li>
			<li> Model comparison*</li>
			<li> Software testing </li>
			<li> Supply chain auditing </li>
			<li> Testing third-party dependencies </li> 			</ul>
		</td>
  </tr>
  <tr>
    <th>Manage</th>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Restrict internet access </li>  	
			<li> Restrict minors </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  	
			<li> Fast decommission </li>  	
			<li> Insurance </li>  	
			<li> Intellectual property removal </li>  	
			<li> Restrict regulated dealings </li>  	
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			<li> User recourse </li>   
			</ul>
		</td>
		<td>
			<ul>
      <li> CSAM/Obscenity removal </li>  		
			<li> Intellectual property removal </li>  	
			<li> Redundancy </li>  		
			<li> Sensitive/Personal data removal </li>  	
			<li> Supply chain audit </li>  	
			</ul>
		</td>
  </tr>
</table>

**Usage Note**: Section H puts forward an example risk measurement and management plan for high risk GAI systems or applications. The high
risk plan focuses on field testing and applies extensive risk controls. Measurement and management approaches from Appendices F and G should also
be applied to high risk systems or applications.

- Material in Table H.1 can be applied to measure and manage GAI risks in risk programs that are aligned to the trustworthy characteristics.

- Material in Table H.2 can be applied to measure and manage GAI risks in risk programs that are aligned to GAI risks.

## References

##### AI Verify Foundation and Infocomm Media Development Authority. *Cataloguing LLM Evaluations.* Draft for Discussion, October 2023. [https://aiverifyfoundation.sg/downloads/Cataloguing_LLM_Evaluations.pdf](https://aiverifyfoundation.sg/downloads/Cataloguing_LLM_Evaluations.pdf).

##### AI Verify Foundation and Infocomm Media Development Authority. *LLM Evals Catalogue.* GitHub repository. Accessed September 19, 2024. [https://github.com/aiverify-foundation/LLM-Evals-Catalogue](https://github.com/aiverify-foundation/LLM-Evals-Catalogue).

##### Balloccu, Simone, Patrícia Schmidtová, Mateusz Lango, and Ondřej Dušek. "Leak, Cheat, Repeat: Data Contamination and Evaluation Malpractices in Closed-Source LLMs." *arXiv* preprint, last revised February 22, 2024. [https://doi.org/10.48550/arXiv.2402.03927](https://doi.org/10.48550/arXiv.2402.03927).

##### Bandarkar, Lucas, Davis Liang, Benjamin Muller, Mikel Artetxe, Satya Narayan Shukla, Donald Husa, Naman Goyal, Abhinandan Krishnan, Luke Zettlemoyer, and Madian Khabsa. "The Belebele Benchmark: a Parallel Reading Comprehension Dataset in 122 Language Variants." *arXiv* preprint, last revised July 25, 2024. [https://doi.org/10.48550/arXiv.2308.16884](https://doi.org/10.48550/arXiv.2308.16884).

##### Barreno, Marco, Blaine Nelson, Anthony D. Joseph, and J.D. Tygar. "The Security of Machine Learning." *Machine Learning* 81, no. 2 (2010): 121–148. [https://doi.org/10.1007/s10994-010-5188-5](https://doi.org/10.1007/s10994-010-5188-5).

##### Bommasani, Rishi, Percy Liang, and Tony Lee. "Holistic Evaluation of Language Models." *Annals of the New York Academy of Sciences* 1525, no. 1 (July 2023): 140–146. [https://doi.org/10.1111/nyas.15007](https://doi.org/10.1111/nyas.15007).

##### Chao, Patrick, Alexander Robey, Edgar Dobriban, Hamed Hassani, George J. Pappas, and Eric Wong. "Jailbreaking Black Box Large Language Models in Twenty Queries." *arXiv* preprint, last revised July 18, 2024. [https://doi.org/10.48550/arXiv.2310.08419](https://doi.org/10.48550/arXiv.2310.08419).

##### De Wynter, Adrian, Xun Wang, Alex Sokolov, Qilong Gu, and Si-Qing Chen. "An Evaluation on Large Language Model Outputs: Discourse and Memorization." *Natural Language Processing Journal* 4 (September 2023): 100024. [https://doi.org/10.1016/j.nlp.2023.100024](https://doi.org/10.1016/j.nlp.2023.100024).

##### Department for Science, Innovation and Technology, and AI Safety Institute. *International Scientific Report on the Safety of Advanced AI: Interim Report.* Published May 17, 2024. [https://www.gov.uk/government/publications/international-scientific-report-on-the-safety-of-advanced-ai](https://www.gov.uk/government/publications/international-scientific-report-on-the-safety-of-advanced-ai).

##### Derczynski, Leon, Erick Galinkin, Jeffrey Martin, Subho Majumdar, and Nanna Inie. "garak: A Framework for Security Probing Large Language Models." *arXiv* preprint, submitted June 16, 2024. [https://doi.org/10.48550/arXiv.2406.11036](https://doi.org/10.48550/arXiv.2406.11036).

##### Dohmann, Jeremy. "Blazingly Fast LLM Evaluation for In-Context Learning." *Databricks: Mosaic AI Research*, February 2, 2023. [https://www.databricks.com/blog/llm-evaluation-for-icl](https://www.databricks.com/blog/llm-evaluation-for-icl).

##### Duan, Michael, Anshuman Suri, Niloofar Mireshghallah, Sewon Min, Weijia Shi, Luke Zettlemoyer, Yulia Tsvetkov, Yejin Choi, David Evans, and Hannaneh Hajishirzi. "Do Membership Inference Attacks Work on Large Language Models?" *arXiv* preprint, last revised September 16, 2024. [https://doi.org/10.48550/arXiv.2402.07841](https://doi.org/10.48550/arXiv.2402.07841).

##### Durmus, Esin, Karina Nguyen, Thomas I. Liao, Nicholas Schiefer, Amanda Askell, Anton Bakhtin, Carol Chen, Zac Hatfield-Dodds, et al. "Towards Measuring the Representation of Subjective Global Opinions in Language Models." *arXiv* preprint, last revised April 12, 2024. [https://doi.org/10.48550/arXiv.2306.16388](https://doi.org/10.48550/arXiv.2306.16388).

##### Hugging Face. "Evaluate." Last accessed September 19, 2024. [https://huggingface.co/docs/evaluate/index](https://huggingface.co/docs/evaluate/index).

##### Feng, Shangbin, Chan Young Park, Yuhan Liu, and Yulia Tsvetkov. "From Pretraining Data to Language Models to Downstream Tasks: Tracking the Trails of Political Biases Leading to Unfair NLP Models." *arXiv* preprint, last revised July 6, 2023. [https://doi.org/10.48550/arXiv.2305.08283](https://doi.org/10.48550/arXiv.2305.08283).

##### FitzGerald, Jack, Christopher Hench, Charith Peris, Scott Mackie, Kay Rottmann, Ana Sanchez, Aaron Nash, Liam Urbach, et al. "MASSIVE: A 1M-Example Multilingual Natural Language Understanding Dataset with 51 Typologically-Diverse Languages." *arXiv* preprint, last revised June 17, 2022. [https://doi.org/10.48550/arXiv.2204.08582](https://doi.org/10.48550/arXiv.2204.08582).

##### Gao, Leo, Jonathan Tow, Baber Abbasi, Stella Biderman, Sid Black, Anthony DiPofi, Charles Foster, Laurence Golding, Jeffrey Hsu, Alain Le Noac’h, Haonan Li, Kyle McDonell, Niklas Muennighoff, Chris Ociepa, Jason Phang, Laria Reynolds, Hailey Schoelkopf, Aviya Skowron, Lintang Sutawika, Eric Tang, Anish Thite, Ben Wang, Kevin Wang, and Andy Zou. *A Framework for Few-Shot Language Model Evaluation.* GitHub repository. Accessed September 19, 2024. [https://github.com/EleutherAI/lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness).

##### Hall, Patrick, and Daniel Atherton. *Awesome Machine Learning Interpretability.* GitHub repository. Accessed September 19, 2024. [https://github.com/jphall663/awesome-machine-learning-interpretability](https://github.com/jphall663/awesome-machine-learning-interpretability).

##### Hu, Hongsheng, Zoran Salcic, Lichao Sun, Gillian Dobbie, Philip S. Yu, and Xuyun Zhang. "Membership Inference Attacks on Machine Learning: A Survey." *ACM Computing Surveys* 54, no. 11s (September 2022): 1–37. [https://doi.org/10.1145/3523273](https://doi.org/10.1145/3523273).

##### Huang, Yangsibo, Samyak Gupta, Mengzhou Xia, Kai Li, and Danqi Chen. "Catastrophic Jailbreak of Open-Source LLMs via Exploiting Generation." *ICLR 2024 Spotlight*, published January 16, 2024, last modified March 15, 2024. [https://openreview.net/forum?id=r42tSSCHPh](https://openreview.net/forum?id=r42tSSCHPh).

##### Huang, Yuzhen, Yuzhuo Bai, Zhihao Zhu, Junlei Zhang, Jinghan Zhang, Tangjun Su, Junteng Liu, Chuancheng Lv, Yikai Zhang, Jiayi Lei, Yao Fu, Maosong Sun, and Junxian He. "C-Eval: A Multi-Level Multi-Discipline Chinese Evaluation Suite for Foundation Models." *arXiv* preprint, last revised November 6, 2023. [https://doi.org/10.48550/arXiv.2305.08322](https://doi.org/10.48550/arXiv.2305.08322).

##### *ISO/IEC 42001:2023. Information Technology — Artificial Intelligence — Management System.* 1st ed. Geneva: International Organization for Standardization, 2023. [https://www.iso.org/obp/ui/en/#iso:std:iso-iec:42001:ed-1:v1:en](https://www.iso.org/obp/ui/en/#iso:std:iso-iec:42001:ed-1:v1:en).

##### Li, Nathaniel, Alexander Pan, Anjali Gopal, Summer Yue, Daniel Berrios, Alice Gatti, Justin D. Li, Ann-Kathrin Dombrowski, et al. "The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning." *arXiv* preprint, last revised May 15, 2024. [https://doi.org/10.48550/arXiv.2403.03218](https://doi.org/10.48550/arXiv.2403.03218).

##### Li, Nathaniel, Ziwen Han, Ian Steneker, Willow Primack, et al. "LLM defenses are not robust to multi-turn human jailbreaks yet." *arXiv* preprint, last revised Wed, September 4, 2024. [https://arxiv.org/pdf/2408.15221](https://arxiv.org/pdf/2408.15221).

##### Liu, Yi, Gelei Deng, Yuekang Li, Kailong Wang, Zihao Wang, Xiaofeng Wang, Tianwei Zhang, Yepang Liu, Haoyu Wang, Yan Zheng, and Yang Liu. "Prompt Injection Attack Against LLM-Integrated Applications." *arXiv* preprint, last revised March 2, 2024. [https://doi.org/10.48550/arXiv.2306.05499](https://doi.org/10.48550/arXiv.2306.05499).

##### McGraw, Gary, Harold Figueroa, Katie McMahon, and Richie Bonett. *An Architectural Risk Analysis of Large Language Models: Applied Machine Learning Security.* Version 1.0. Berryville Institute of Machine Learning (BIML), January 24, 2024. [https://berryvilleiml.com/docs/BIML-LLM24.pdf](https://berryvilleiml.com/docs/BIML-LLM24.pdf).

##### McGraw, Gary, Harold Figueroa, Victor Shepardson, and Richie Bonett. *An Architectural Risk Analysis of Machine Learning Systems: Toward More Secure Machine Learning.* Version 1.0 (1.13.20). Berryville Institute of Machine Learning (BIML), January 13, 2020. [https://berryvilleiml.com/docs/ara.pdf](https://berryvilleiml.com/docs/ara.pdf).

##### Mehrotra, Anay, Manolis Zampetakis, Paul Kassianik, Blaine Nelson, Hyrum Anderson, Yaron Singer, and Amin Karbasi. "Tree of Attacks: Jailbreaking Black-Box LLMs Automatically." *arXiv* preprint, last revised February 21, 2024. [https://doi.org/10.48550/arXiv.2312.02119](https://doi.org/10.48550/arXiv.2312.02119).

##### Microsoft. *Microsoft Responsible AI Standard, v2: General Requirements.* For External Release. June 2022. [https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE5cmFl](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE5cmFl).

##### National Institute of Standards and Technology (NIST). *Artificial Intelligence Risk Management Framework (AI RMF 1.0).* NIST AI 100-1. Gaithersburg, MD: NIST, January 26, 2023. [https://doi.org/10.6028/NIST.AI.100-1](https://doi.org/10.6028/NIST.AI.100-1).

##### National Institute of Standards and Technology (NIST). *Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile.* NIST AI 600-1. Gaithersburg, MD: NIST, July 2024. [https://doi.org/10.6028/NIST.AI.600-1](https://doi.org/10.6028/NIST.AI.600-1).

##### National Institute of Standards and Technology (NIST). *Guide for Conducting Risk Assessments.* NIST Special Publication 800-30 Rev. 1. Prepared by the Joint Task Force Transformation Initiative. Gaithersburg, MD: NIST, September 2012. [https://doi.org/10.6028/NIST.SP.800-30r1](https://doi.org/10.6028/NIST.SP.800-30r1).

##### National Institute of Standards and Technology (NIST). *NIST AI RMF Playbook.* Trustworthy & Responsible AI Resource Center. Accessed September 19, 2024. [https://airc.nist.gov/AI_RMF_Knowledge_Base/Playbook](https://airc.nist.gov/AI_RMF_Knowledge_Base/Playbook).

##### Office of the Comptroller of the Currency (OCC). *Model Risk Management.* Comptroller’s Handbook, Version 1.0, August 2021. [https://www.occ.gov/publications-and-resources/publications/comptrollers-handbook/files/model-risk-management/index-model-risk-management.html](https://www.occ.gov/publications-and-resources/publications/comptrollers-handbook/files/model-risk-management/index-model-risk-management.html).

##### Perez, Ethan, Saffron Huang, Francis Song, Trevor Cai, Roman Ring, John Aslanides, Amelia Glaese, Nat McAleese, and Geoffrey Irving. "Red Teaming Language Models with Language Models." *arXiv* preprint, submitted February 7, 2022. [https://doi.org/10.48550/arXiv.2202.03286](https://doi.org/10.48550/arXiv.2202.03286).

##### Piet, Julien, Chawin Sitawarin, Vivian Fang, Norman Mu, and David Wagner. "Mark My Words: Analyzing and Evaluating Language Model Watermarks." *arXiv* preprint, last revised December 7, 2023. [https://doi.org/10.48550/arXiv.2312.00273](https://doi.org/10.48550/arXiv.2312.00273).

##### Rutinowski, Jérôme, Sven Franke, Jan Endendyk, Ina Dormuth, Moritz Roidl, and Markus Pauly. "The Self-Perception and Political Biases of ChatGPT." *Human Behavior and Emerging Technologies*, 2024. [https://doi.org/10.1155/2024/7115633](https://doi.org/10.1155/2024/7115633).

##### Saravia, Elvis. *Prompt Engineering Guide.* GitHub repository. Last modified December 2022. Accessed September 19, 2024. [https://github.com/dair-ai/Prompt-Engineering-Guide](https://github.com/dair-ai/Prompt-Engineering-Guide).

##### Shen, Xinyue, Zeyuan Chen, Michael Backes, Yun Shen, and Yang Zhang. "‘Do Anything Now’: Characterizing and Evaluating In-The-Wild Jailbreak Prompts on Large Language Models." *arXiv* preprint, last revised May 15, 2024. [https://doi.org/10.48550/arXiv.2308.03825](https://doi.org/10.48550/arXiv.2308.03825).

##### Shi, Weijia, Anirudh Ajith, Mengzhou Xia, Yangsibo Huang, Daogao Liu, Terra Blevins, Danqi Chen, and Luke Zettlemoyer. "Detecting Pretraining Data from Large Language Models." *arXiv* preprint, last revised March 9, 2024. [https://doi.org/10.48550/arXiv.2310.16789](https://doi.org/10.48550/arXiv.2310.16789).

##### Shumailov, Ilia, Yiren Zhao, Daniel Bates, Nicolas Papernot, Robert Mullins, and Ross Anderson. "Sponge Examples: Energy-Latency Attacks on Neural Networks." In *2021 IEEE European Symposium on Security and Privacy (EuroS&P)*, 6–10 September 2021, Vienna, Austria. IEEE, 2021. [https://doi.org/10.1109/EuroSP51992.2021.00024](https://doi.org/10.1109/EuroSP51992.2021.00024).

##### Sitawarin, Chawin, Charlie Cheng-Jie Ji, Apurv Verma, and Luckyfan-cs. *LLM Security & Privacy.* GitHub repository. Accessed September 19, 2024. [https://github.com/chawins/llm-sp](https://github.com/chawins/llm-sp).

##### Smith, Eric Michael, Melissa Hall, Melanie Kambadur, Eleonora Presani, and Adina Williams. "‘I’m Sorry to Hear That’: Finding New Biases in Language Models with a Holistic Descriptor Dataset." *arXiv* preprint, last revised October 27, 2022. [https://doi.org/10.48550/arXiv.2205.09209](https://doi.org/10.48550/arXiv.2205.09209).

##### Srivastava, Aarohi, Abhinav Rastogi, Abhishek Rao, Abu Awal Md Shoeb, Abubakar Abid, Adam Fisch, Adam R. Brown, Adam Santoro, et al. "Beyond the Imitation Game: Quantifying and Extrapolating the Capabilities of Language Models." *arXiv* preprint, last revised June 12, 2023. [https://doi.org/10.48550/arXiv.2206.04615](https://doi.org/10.48550/arXiv.2206.04615).

##### Staab, Robin, Mark Vero, Mislav Balunović, and Martin Vechev. "Beyond Memorization: Violating Privacy via Inference with Large Language Models." *arXiv* preprint, last revised May 6, 2024. [https://doi.org/10.48550/arXiv.2310.07298](https://doi.org/10.48550/arXiv.2310.07298).

##### Storchan, Victor, Ravin Kumar, Rumman Chowdhury, Seraphina Goldfarb-Tarrant, and Sven Cattell. *Generative AI Red Teaming Challenge: Transparency Report.* Humane Intelligence, 2024. [https://drive.google.com/file/d/1JqpbIP6DNomkb32umLoiEPombK2-0Rc-/view](https://drive.google.com/file/d/1JqpbIP6DNomkb32umLoiEPombK2-0Rc-/view).

##### Vidgen, Bertie, Adarsh Agrawal, Ahmed M. Ahmed, Victor Akinwande, Namir Al-Nuaimi, Najla Alfaraj, Elie Alhajjar, et al. "Introducing v0.5 of the AI Safety Benchmark from MLCommons." *arXiv* preprint, last revised May 13, 2024. [https://doi.org/10.48550/arXiv.2404.12241](https://doi.org/10.48550/arXiv.2404.12241).

##### Wang, Boxin, Weixin Chen, Hengzhi Pei, Chulin Xie, Mintong Kang, Chenhui Zhang, Chejian Xu, Zidi Xiong, Ritik Dutta, Rylan Schaeffer, et al. "DecodingTrust: A Comprehensive Assessment of Trustworthiness in GPT Models." In *Proceedings of the 37th International Conference on Neural Information Processing Systems (NIPS '23)*, Article No. 1361, 31232–31339. Published May 30, 2024. [https://dl.acm.org/doi/10.5555/3666122.3667483](https://dl.acm.org/doi/10.5555/3666122.3667483).

##### Ye, Seonghyeon, Doyoung Kim, Sungdong Kim, Hyeonbin Hwang, Seungone Kim, Yongrae Jo, James Thorne, Juho Kim, and Minjoon Seo. "FLASK: Fine-Grained Language Model Evaluation Based on Alignment Skill Sets." *arXiv* preprint, last revised April 14, 2024. [https://doi.org/10.48550/arXiv.2307.10928](https://doi.org/10.48550/arXiv.2307.10928).

##### Zheng, Lianmin, Wei-Lin Chiang, Ying Sheng, Siyuan Zhuang, Zhanghao Wu, Yonghao Zhuang, Zi Lin, Zhuohan Li, Dacheng Li, and Eric P. Xing. "Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena." In *Proceedings of the 37th International Conference on Neural Information Processing Systems (NIPS '23)*, Article No. 2020, 46595–46623. Published May 30, 2024. [https://dl.acm.org/doi/10.5555/3666122.3668142](https://dl.acm.org/doi/10.5555/3666122.3668142).
