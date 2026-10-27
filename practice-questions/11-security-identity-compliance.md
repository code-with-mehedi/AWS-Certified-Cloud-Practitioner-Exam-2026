# Practice questions: 11. Security, Identity & Compliance

[Study guide: 11. Security, Identity & Compliance](../README.md#11--security-identity--compliance) · [All topics](README.md) · [Next: 12. Application Integration & Messaging](12-application-integration-messaging.md)

> [!NOTE]
> Read the question and decide on your answer, then click an option to see whether it is right or wrong and why. A round marker (◯) means pick one answer. A square marker (☐) means pick every answer the question asks for, so click each option you think is correct.

### Question 1

Which service uses machine learning to analyze AWS CloudTrail events, VPC Flow Logs, and DNS logs to detect threats such as compromised instances?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon Inspector</summary>

❌ **Incorrect.** Inspector scans workloads for software vulnerabilities and unintended network exposure. It is not a threat detection service.

</details>

<details><summary>◯ <b>B.</b> Amazon Macie</summary>

❌ **Incorrect.** Macie discovers and protects sensitive data such as PII in Amazon S3.

</details>

<details><summary>◯ <b>C.</b> Amazon GuardDuty</summary>

✅ **Correct.** GuardDuty is an intelligent threat detection service that continuously analyzes these data sources.

</details>

<details><summary>◯ <b>D.</b> AWS WAF</summary>

❌ **Incorrect.** WAF filters malicious web requests and does not analyze logs for threats.

</details>

Study: [11.4 Threat Detection & Boundary Security (Shield, WAF, GuardDuty, Inspector)](../README.md#114-threat-detection--boundary-security-shield-waf-guardduty-inspector)

### Question 2

Which TWO AWS services help protect web applications from common exploits and DDoS attacks?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> Amazon Macie</summary>

❌ **Incorrect.** Macie discovers sensitive data in S3. It does not protect web applications.

</details>

<details><summary>☐ <b>B.</b> AWS KMS</summary>

❌ **Incorrect.** KMS creates and manages encryption keys and has no part in filtering web traffic.

</details>

<details><summary>☐ <b>C.</b> AWS WAF</summary>

✅ **Correct.** WAF filters HTTP and HTTPS requests at layer 7 to block threats such as SQL injection and cross-site scripting.

</details>

<details><summary>☐ <b>D.</b> AWS Shield</summary>

✅ **Correct.** Shield protects against DDoS attacks. Shield Standard is automatic and free, and Shield Advanced adds extra protection and support.

</details>

<details><summary>☐ <b>E.</b> AWS Artifact</summary>

❌ **Incorrect.** Artifact provides compliance documents. It does not filter web traffic.

</details>

Study: [11.4 Threat Detection & Boundary Security (Shield, WAF, GuardDuty, Inspector)](../README.md#114-threat-detection--boundary-security-shield-waf-guardduty-inspector)

### Question 3

Where can a compliance officer download AWS's SOC reports and ISO certifications on demand?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Artifact</summary>

✅ **Correct.** Artifact is a free portal for AWS compliance reports and agreements such as the HIPAA Business Associate Addendum.

</details>

<details><summary>◯ <b>B.</b> Amazon Inspector</summary>

❌ **Incorrect.** Inspector scans your workloads for vulnerabilities. It does not provide AWS audit reports.

</details>

<details><summary>◯ <b>C.</b> AWS Config</summary>

❌ **Incorrect.** Config tracks the configuration of your resources over time, and AWS audit reports are not among its outputs.

</details>

<details><summary>◯ <b>D.</b> AWS Security Hub</summary>

❌ **Incorrect.** Security Hub aggregates security findings and posture checks for your accounts and does not include AWS's own compliance reports.

</details>

Study: [11.5 Governance & Compliance: AWS Artifact, Audit Manager, Macie, Security Hub](../README.md#115-governance--compliance-aws-artifact-audit-manager-macie-security-hub)

### Question 4

An application on an EC2 instance needs to read objects from an Amazon S3 bucket. How should the company grant access securely?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Store an IAM user's access keys in the application code</summary>

❌ **Incorrect.** Hard-coded long-term keys can leak and are hard to rotate.

</details>

<details><summary>◯ <b>B.</b> Create access keys for the root user and use them in the application</summary>

❌ **Incorrect.** Root access keys are never recommended because they allow unrestricted access to the whole account.

</details>

<details><summary>◯ <b>C.</b> Make the S3 bucket public</summary>

❌ **Incorrect.** A public bucket exposes the data to everyone, well beyond the one application that needs it.

</details>

<details><summary>◯ <b>D.</b> Attach an IAM role to the EC2 instance</summary>

✅ **Correct.** A role provides temporary credentials automatically, so no access keys are stored on the instance.

</details>

Study: [11.1 AWS Identity and Access Management (IAM) Entities & PoLP](../README.md#111-aws-identity-and-access-management-iam-entities--polp)

### Question 5

A company is building a mobile app and wants its customers to sign up and sign in with accounts such as Google or Facebook. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS IAM Identity Center</summary>

❌ **Incorrect.** Identity Center provides single sign-on for a company's workforce to AWS accounts and business applications, so it does not cover app customers.

</details>

<details><summary>◯ <b>B.</b> AWS Directory Service</summary>

❌ **Incorrect.** Directory Service provides managed Microsoft Active Directory in the cloud.

</details>

<details><summary>◯ <b>C.</b> Amazon Cognito</summary>

✅ **Correct.** Cognito provides sign-up, sign-in, and social identity federation for the customers of web and mobile apps.

</details>

<details><summary>◯ <b>D.</b> IAM users</summary>

❌ **Incorrect.** Creating an IAM user for every app customer does not scale and is not meant for application end users.

</details>

Study: [11.2 AWS IAM Identity Center, Cognito & Directory Service](../README.md#112-aws-iam-identity-center-cognito--directory-service)

[Study guide: 11. Security, Identity & Compliance](../README.md#11--security-identity--compliance) · [All topics](README.md) · [Next: 12. Application Integration & Messaging](12-application-integration-messaging.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
