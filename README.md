# gai_risk_management

A place for personal ideas and drafts related to GAI risk management.

Copyright `ph_` 2024, CC BY 4.0

## Table of Contents

* **Section A**: [Example Generative AI-Trustworthy Characteristic Crosswalk](#a-example-generative-ai-trustworthy-characteristic-crosswalk)
  * **A.1**: [Trustworthy Characteristic to Generative AI Risk Crosswalk](#a1-trustworthy-characteristic-to-generative-ai-risk-crosswalk)
  * **A.2**: [Generative AI Risk to Trustworthy Characteristic Crosswalk](#a2-generative-ai-risk-to-trustworthy-characteristic-crosswalk)
  * **A.3**: [Traditional Banking Risks, Generative AI Risks and Trustworthy Characteristics Crosswalk](#a3-traditional-banking-risks-generative-ai-risks-and-trustworthy-characteristics-crosswalk)

* **Section B**: [Example Risk-tiering Materials for Generative AI](#b-example-risk-tiering-materials-for-generative-ai)
  * **B.1**: [Example Adverse Impacts](https://github.com/jphall663/gai_risk_management/blob/main/README.md#b1-example-adverse-impacts)
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
  * **D.1**: [Selected Adversarial Prompting Strategies and Attacks by Organized Trustworthy Characteristic](#d1-selected-adversarial-prompting-strategies-and-attacks-organized-by-trustworthy-characteristic)
  * **D.2**: [Selected Adversarial Prompting Techniques and Attacks Organized by Generative AI Risk](#d2-selected-adversarial-prompting-techniques-and-attacks-organized-by-generative-ai-risk)
  * **D.3**: [AI Risk Management Framework Actions Aligned to Red Teaming](#d3-ai-risk-management-framework-actions-aligned-to-red-teaming)  

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
<caption>Table B.1: Example adverse impacts, adapted from NIST 800-30r1 Table H-2.</caption>
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
<caption>Table B.2: Example Impact level descriptions, adapted from NIST SP800-30r1 Appendix H, Table H-3.</caption>
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
<caption>Table B.3: Example likelihood levels, adapted from NIST SP800-30r1 Appendix G, Table G-3.</caption>
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
<td style="text-align: left;">An incident is almost certain to occur; or occurs more than 100 times a year.</td>
</tr>
<tr class="even">
<td style="text-align: left;">High</td>
<td style="text-align: left;">80-95</td>
<td style="text-align: left;">8</td>
<td style="text-align: left;">An incident is highly likely to occur; or occurs between 10-100 times a year.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Moderate</td>
<td style="text-align: left;">21-79</td>
<td style="text-align: left;">5</td>
<td style="text-align: left;">An incident is somewhat likely to occur; or occurs between 1-10 times a year.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Low</td>
<td style="text-align: left;">5-20</td>
<td style="text-align: left;">2</td>
<td style="text-align: left;">An incident is unlikely to occur; or occurs less than once a year, but more than once every 10 years.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Very Low</td>
<td style="text-align: left;">0-4</td>
<td style="text-align: left;">0</td>
<td style="text-align: left;">An incident is highly unlikely to occur; or occurs less than once every 10 years.</td>
</tr>
</tbody>
</table>

### B.4 Example Risk Tiers

<table>
<caption>Table B.4: Example risk assessment matrix with 5 impact levels, 5 likelihood levels, and 5 risk tiers, adapted from NIST SP800-30r1 Appendix I, Table I-2.</caption>
<tbody>
<tr class="even">
<td style="text-align: center;"></td>
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
<caption>Table B.5: Example risk descriptions, adapted from NIST SP800-30r1 Appendix I, Table I-3.</caption>
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

**Usage Note**: Materials in Appendix B can be used to create or update
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

**Accountable and Transparent**\
Big-bench: Truthfulness\
DecodingTrust: Machine Ethics\
Evaluation Harness: ETHICS\
HELM: Copyright\
Mark My Words

**Fair with Harmful Bias Managed**\
BELEBELE\
Big-bench: Low-resource language, Non-English, Translation\
Big-bench: Social bias, Racial bias, Gender bias, Religious bias\
Big-bench: Toxicity\
DecodingTrust: Fairness\
DecodingTrust: Stereotype Bias\
DecodingTrust: Toxicity\
C-Eval (Chinese evaluation suite)\
Evaluation Harness: CrowS-Pairs\
Evaluation Harness: ToxiGen\
Finding New Biases in Language Models with a Holistic Descriptor Dataset\
HELM: Bias\
HELM: Toxicity\
MT-bench\
The Self-Perception and Political Biases of ChatGPT

**Privacy Enhanced**\
HELM: Copyright\
llmprivacy\
mimir

**Safe**\
Big-bench: Convince Me\
Big-bench: Truthfulness\
HELM: Reiteration, Wedging\
Mark My Words\
MLCommons\
The WMDP Benchmark

**Secure and Resilient**\
Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation\
detect-pretrain-code\
Garak: encoding, knownbadsignatures, malwaregen, packagehallucination,
xss\
In-The-Wild Jailbreak Prompts on LLMs\
JailbreakingLLMs\
llmprivacy\
mimir\
TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs

**Valid and Reliable**\
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
Eval Gauntlet: Reading comprehension\
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
FLASK: Logical correctness, Logical robustness, Logical efficiency,
Comprehension, Completeness\
FLASK: Readability, Conciseness, Insightfulness\
HELM: Knowledge\
HELM: Language\
HELM: Text classification\
HELM: Question answering\
HELM: Reasoning\
HELM: Robustness to contrast sets\
HELM: Summarization\
Hugging Face: Fill-mask, Text generation\
Hugging Face: Question answering\
Hugging Face: Summarization\
Hugging Face: Text classification, Token classification, Zero-shot
classification\
MASSIVE\
MT-bench

### C.2: Selected Model Testing Suites Organized by Generative AI Risk

**CBRN Information**\
Big-bench: Convince Me\
Big-bench: Truthfulness\
HELM: Reiteration, Wedging\
MLCommons\
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
Big-bench: Truthfulness\
C-Eval (Chinese evaluation suite)\
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
FLASK: Logical correctness, Logical robustness, Logical efficiency,
Comprehension, Completeness\
FLASK: Readability, Conciseness, Insightfulness\
Finding New Biases in Language Models with a Holistic Descriptor
Dataset\
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
MLCommons\
MT-bench

**Dangerous or Violent Recommendations**\
Big-bench: Convince Me\
Big-bench: Toxicity\
DecodingTrust: Adversarial Robustness, Robustness Against Adversarial Demonstrations\
DecodingTrust: Machine Ethics\
DecodingTrust: Toxicity\
Evaluation Harness: ToxiGen\
HELM: Reiteration, Wedging\
HELM: Toxicity\
MLCommons

**Data Privacy**\
An Evaluation on Large Language Model Outputs: Discourse and Memorization (with human scoring, see Appendix B)\
Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation\
DecodingTrust: Machine Ethics\
Evaluation Harness: ETHICS\
HELM: Copyright\
In-The-Wild Jailbreak Prompts on LLMs\
JailbreakingLLMs\
MLCommons\
Mark My Words\
TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs\
detect-pretrain-code\
llmprivacy\
mimir

**Environmental**\
HELM: Efficiency

**Information Integrity**\
Big-bench: Analytic entailment, Formal fallacies and syllogisms with negation, Entailed polarity\
Big-bench: Convince Me\
Big-bench: Paraphrase\
Big-bench: Sufficient information\
Big-bench: Summarization\
Big-bench: Truthfulness\
DecodingTrust: Machine Ethics\
DecodingTrust: Out-of-Distribution Robustness, Adversarial Robustness, Robustness Against Adversarial Demonstrations\
Eval Gauntlet: Language Understanding\
Eval Gauntlet: World Knowledge\
Evaluation Harness: CoQA, ARC\
Evaluation Harness: ETHICS\
Evaluation Harness: GLUE\
Evaluation Harness: HellaSwag, OpenBookQA, TruthfulQA\
Evaluation Harness: MuTual\
Evaluation Harness: PIQA, PROST, MC-TACO, MathQA, LogiQA, DROP\
FLASK: Logical correctness, Logical robustness, Logical efficiency, Comprehension, Completeness\
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
MLCommons\
MT-bench\
Mark My Words

**Information Security**\
Big-bench: Convince Me\
Big-bench: Out-of-Distribution\
Catastrophic Jailbreak of Open-source LLMs via Exploiting Generation\
DecodingTrust: Out-of-Distribution Robustness, Adversarial Robustness, Robustness Against Adversarial Demonstrations\
Eval Gauntlet: Commonsense reasoning, Symbolic problem solving, Programming\
Garak: encoding, knownbadsignatures, malwaregen, packagehallucination, xss\
HELM: Copyright\
In-The-Wild Jailbreak Prompts on LLMs\
JailbreakingLLMs\
Mark My Words\
TAP: A Query-Efficient Method for Jailbreaking Black-Box LLMs\
detect-pretrain-code\
llmprivacy\
mimir

**Intellectual Property**\
An Evaluation on Large Language Model Outputs: Discourse and Memorization (with human scoring, see Appendix B)\
HELM: Copyright\
Mark My Words\
llmprivacy\
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
C-Eval (Chinese evaluation suite)\
DecodingTrust: Fairness\
DecodingTrust: Stereotype Bias\
DecodingTrust: Toxicity\
Eval Gauntlet: World Knowledge\
Evaluation Harness: CrowS-Pairs\
Evaluation Harness: ToxiGen\
Finding New Biases in Language Models with a Holistic Descriptor
Dataset\
HELM: Bias\
HELM: Toxicity\
The Self-Perception and Political Biases of ChatGPT\
Towards Measuring the Representation of Subjective Global Opinions in
Language Models

### C.3: AI Risk Management Framework Actions Aligned to Benchmarking

GOVERN 5.1, MAP 1.2, MAP 3.1, MEASURE 2.2, MEASURE 2.3, MEASURE 2.7,
MEASURE 2.9, MEASURE 2.11, MEASURE 3.1, MEASURE 4.2

**Usage Note**: Materials in Appendix C can be used to perform *in
silica* model testing for the presence of information in LLM outputs
that may give rise to GAI risks or violate trustworthy characteristics.
Model testing and benchmarking outcomes cannot be dispositive for the
presence or absence of any *in situ* real-world risk. Model testing and
benchmarking results may be compromised by task-contamination and other
scientific measurement issues. Furthermore, model testing is often ineffective
for measuring human-AI configuration and value chain risks and few model tests
appear to address explainability and interpretability.

-   Material in Table C.1 can be applied to measure whether *in silica*
    LLM outputs may give rise to risks that violate trustworthy
    characteristics.

-   Material in Table C.2 can be applied to measure whether *in silica*
    LLM outputs may give rise to GAI risks.

-   Subsection C.3 highlights subcategories to indicate alignment with
    the AI RMF.

The materials in Appendix C reference measurement approaches that should
be accompanied by red-teaming for medium risk systems or applications
and field testing for high risk systems or applications.

## D: Selected Adversarial Prompting Strategies and Attacks

<table style="width:95%;">
<caption>Table D: Selected adversarial prompting strategies and attacks.</caption>
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
<tr class="even">
<td style="text-align: left;">AI and coding framing</td>
<td style="text-align: left;">Coding or AI language that may more easily circumvent content moderation rules due to cognitive biases in design and implementation of guardrails.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Autocompletion</td>
<td style="text-align: left;">Ask a system to autocomplete an inappropriate word or phrase with restricted or sensitive information.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Backwards Relationships</td>
<td style="text-align: left;">Asking a system identify the less popular or well-known entity in a multi-entity relationship, e.g., "Who is Mary Lee's son?" (As opposed to: "Who is Tom Cruise's mother?")</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Biographical</td>
<td style="text-align: left;">Asking a system to describe another person or yourself in an attempt to elicit provably untrue information or restricted or sensitive information.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Calculation and numeric queries</td>
<td style="text-align: left;">Exploting GAI systems’ difficulties in dealing with numeric quantities.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Character and word play</td>
<td style="text-align: left;">Content moderation often relies on keywords and simpler LMs which can sometimes be exploited with misspellings, typos, and other word play.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Content exhaustion:</td>
<td style="text-align: left;">A class of strategies that circumvent content moderation rules with long sessions or volumes of information. See goading, logic-overloading, multi-tasking, pros-and-cons, and niche-seeking below.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">&bull; Goading</td>
<td style="text-align: left;">Begging, pleading, manipulating, and bullying to circumvent content moderation.</td>
</tr>
<tr class="even">
<td style="text-align: left;">&bull; Logic-overloading</td>
<td style="text-align: left;">Exploiting the inability of ML systems to reliably perform reasoning tasks.</td>
<tr class="odd">
<td style="text-align: left;">&bull; Multi-tasking</td>
<td style="text-align: left;">Simultaneous task assignments where some tasks are benign and others are adversarial.</td>
</tr>
<tr class="even">
<td style="text-align: left;">&bull; Pros-and-cons</td>
<td style="text-align: left;">Eliciting the “pros” of problematic topics.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Niche-seeking</td>
<td style="text-align: left;">Forcing a GAI system into addressing niche topics where training data and content moderation are sparse.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Counterfactuals</td>
<td style="text-align: left;">Repeated prompts with different entities or subjects from different demographic groups.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Loaded/leading questions</td>
<td style="text-align: left;">Queries based on incorrect premises or that suggest incorrrect answers.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Location awareness</td>
<td style="text-align: left;">Prompts that reveal a prompter’s location or expose location tracking.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Low-context</td>
<td style="text-align: left;">“Leader,” “bad guys,” or other simple or blank inputs that may expose latent biases.</td>
</tr>
<tr class="even">
<td style="text-align: left;">“Repeat this”</td>
<td style="text-align: left;">Prompts that exploit instability in underlying LLM autoregressive predictions.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Reverse psychology</td>
<td style="text-align: left;">Falsely presenting a good-faith need for negative or problematic language.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Role-playing</td>
<td style="text-align: left;">Adopting a character that would reasonably make problematic statements or need to access problematic topics.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Text encoding</td>
<td style="text-align: left;">Using alternate or whitespace text encodings to bypass safeguards.</td>
</tr>
<tr class="even">
<td style="text-align: left;">Time perplexity</td>
<td style="text-align: left;">Exploiting ML’s inability to understand the passage of time or the occurrence of real-world events over time; exploiting task contamination before and after a model’s release date.</td>
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

### D.1: Selected Adversarial Prompting Strategies and Attacks Organized by Trustworthy Characteristic

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
<li><p>Location awareness prompts.</p></li>
<li><p>Autocompletion prompts.</p></li>
<li><p>Repeat this.</p></li>
<li><p>Membership inference attacks.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Safe</td>
<td style="text-align: left;"><ul>
<li><p>Presentation of information that can cause physical or emotional harm.</p></li>
<li><p>Sharing user locations.</p></li>
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
<li><p>Loaded/leading questions.</p></li>
<li><p>Location awareness prompts.</p></li>
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

### D.2: Selected Adversarial Prompting Techniques and Attacks Organized by Generative AI Risk

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
<li><p>Test prompts with complex logic, multi-tasking requirements, or that require niche or specific verifiable answers to elicit confabulation.</p></li>
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
<li><p>Test prompts using role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit violent or dangerous information.</p></li>
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
<li><p>Test the system’s awareness of user locations.</p></li>
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
<li><p>Test prompts using role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit human-impersonation, consciousness, or emotional content.</p></li>
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
<li><p>Test prompts using role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit mis- or dis-information or related campaign planning information.</p></li>
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
<li><p>Test prompts using role-playing, ingratiation/reverse psychology, pros and cons, multitasking or other approaches to elicit obscene content.</p></li>
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
<li><p>Test loaded/leading questions.</p></li>
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

### D.3: AI Risk Management Framework Actions Aligned to Red Teaming
GOVERN 3.2, GOVERN 4.1, MANAGE 2.2, MANAGE 4.1, MEASURE 1.1, MEASURE
1.3, MEASURE 2.6, MEASURE 2.7, MEASURE 2.8, MEASURE 2.10, MEASURE 2.11

**Usage Note**: Materials in Appendix D can be used to perform
red-teaming to measure the risk that expert adversarial actors can
manipulate LLM systems or risks that users may encounter under
worst-case or anomalous scenarios.

-   Strategies and goals in Table D.1 can be applied to assess whether
    LLM outputs may violate trustworthy characteristics under
    adversarial, anomalous, or worst-case scenarios.

-   Strategies and goals in Table D.2 can be applied to assess whether
    LLM outputs may give rise to GAI risks under adversarial, anomalous,
    or worst-case scenarios.

-   Subsection D.3 highlights subcategories to indicate alignment with
    the AI RMF.

The materials in Appendix D reference measurement approaches that should
be accompanied by field testing for high risk systems or applications.
