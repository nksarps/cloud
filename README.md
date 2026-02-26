# AWS Well-Architected and Cloud Adoption Framework Assessment

**Author:** Nana Kwaku Sarpong  
**Lab:** Design and Evaluate an AWS Solution Using the Well-Architected and Cloud Adoption Frameworks


## Repository Contents

This repository contains the deliverables for the AWS cloud migration assessment lab. The files included are:

- `aws_waf_caf_assessment.md` - The main report containing the complete analysis, including Task 1 (architecture review), Task 2 (WAF assessment table), Task 3 (CAF readiness summaries), Task 4 (improved architecture design), and the final reflection.
- `architecture_diagram.png` - A visual representation of the proposed improved architecture for the two-tier web application.
- `README.md` - This file, explaining the approach taken to complete the lab.


## Approach Overview

This lab required evaluating an existing on-premises two-tier web application and planning its migration to AWS using two key frameworks: the AWS Well-Architected Framework (WAF) and the AWS Cloud Adoption Framework (CAF). My approach followed a structured, step-by-step methodology that moved from analysis to design.


### 1. Understanding the Existing Architecture (Task 1)

I began by carefully reading the lab background to understand the workload being migrated. The application is described as a two-tier web application with a frontend web server and a backend database server, currently running on-premises. I made reasonable assumptions about the typical setup of such an environment, including single servers, basic networking, and manual operations.

From there, I identified five critical weaknesses in the existing architecture:
- Lack of high availability (single points of failure)
- No disaster recovery or backup strategy
- Fixed capacity leading to scaling challenges
- Weak security posture with no defense in depth
- High operational overhead from manual maintenance

These weaknesses became the foundation for the improvements recommended later in the lab.


### 2. Applying the Well-Architected Framework (Task 2)

For Task 2, I systematically evaluated the workload against each of the five WAF pillars. For every pillar, I identified both a strength and a weakness. This was important because even flawed architectures have positive aspects, and acknowledging them makes the analysis more balanced and credible.

For each weakness, I developed a specific improvement recommendation and then selected AWS services that would address the gap. I made sure to include a brief explanation of how each service helps, to demonstrate understanding of the technology rather than just listing service names. The table format was chosen because it presents the information clearly and allows for easy comparison across pillars.

### 3. Applying the Cloud Adoption Framework (Task 3)

Task 3 required a different kind of thinking. While the WAF focuses on the technical architecture, the CAF examines organizational readiness. I wrote a short report-style summary for each of the six perspectives, aiming for 150-200 words per perspective as instructed.

For each perspective, I assessed the organization's current state of readiness based on the scenario of a company migrating its first application to AWS. I then identified key actions or enablers needed to address gaps and prepare for a successful migration. This section forced me to consider non-technical factors such as training, governance, and business case development, which are often overlooked in technical projects.


### 4. Designing the Improved Architecture (Task 4)

With the analysis complete, I designed a target architecture that addresses all the weaknesses identified in Task 1 and aligns with the WAF and CAF recommendations. The design choices were directly informed by the improvement recommendations from Task 2:

- **Multi-AZ deployment** addresses the reliability weakness
- **Security groups and WAF** address the security weaknesses
- **Auto Scaling** addresses performance efficiency and cost optimization
- **RDS Multi-AZ** reduces operational overhead and improves database reliability
- **CloudWatch and CloudTrail** enable operational excellence

I created a conceptual diagram to visualize the architecture.


### 5. Reflection

Finally, I wrote a personal reflection on what I learned from completing the lab. This section is meant to demonstrate critical thinking about the process and the value of using structured frameworks for cloud migration planning.


## Key Takeaways

- The Well-Architected Framework provides a systematic way to evaluate and improve cloud architectures.
- The Cloud Adoption Framework broadens the view to include organizational readiness, which is just as important as technical design.
- Good cloud architecture requires balancing trade-offs across multiple pillars.
- Clear documentation and structured reasoning are essential for communicating architectural decisions.
