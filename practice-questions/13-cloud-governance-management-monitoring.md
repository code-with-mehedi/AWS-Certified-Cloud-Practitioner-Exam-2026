# Practice questions: 13. Cloud Governance, Management & Monitoring

[Study guide: 13. Cloud Governance, Management & Monitoring](../README.md#13--cloud-governance-management--monitoring) · [All topics](README.md) · [Next: 14. Machine Learning, AI & High-Performance Compute](14-ml-ai-hpc.md)

> [!NOTE]
> Read the question and decide on your answer, then click an option to see whether it is right or wrong and why. A round marker (◯) means pick one answer. A square marker (☐) means pick every answer the question asks for, so click each option you think is correct.

### Question 1

A security team needs to find out who deleted an Amazon S3 bucket, when it happened, and from which IP address. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon CloudWatch</summary>

❌ **Incorrect.** CloudWatch collects metrics, logs, and alarms about performance and does not provide an audit trail of API calls.

</details>

<details><summary>◯ <b>B.</b> AWS CloudTrail</summary>

✅ **Correct.** CloudTrail records AWS API calls, including who made the call, when, and from where.

</details>

<details><summary>◯ <b>C.</b> AWS Config</summary>

❌ **Incorrect.** Config records how resource configurations change and evaluates compliance. CloudTrail is the service that records who made the API call.

</details>

<details><summary>◯ <b>D.</b> AWS Trusted Advisor</summary>

❌ **Incorrect.** Trusted Advisor gives best-practice recommendations. Auditing API activity is outside its scope.

</details>

Study: [13.3 Observability: Amazon CloudWatch vs. AWS CloudTrail](../README.md#133-observability-amazon-cloudwatch-vs-aws-cloudtrail)

### Question 2

A company wants to set up a new multi-account AWS environment that follows best practices, with preventive and detective guardrails, and with minimal manual effort. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Control Tower</summary>

✅ **Correct.** Control Tower automates the setup of a secure multi-account landing zone and applies preventive and detective guardrails.

</details>

<details><summary>◯ <b>B.</b> AWS Organizations</summary>

❌ **Incorrect.** Organizations is the foundation for managing accounts, consolidated billing, and SCPs, but it does not build a best-practice landing zone with guardrails by itself.

</details>

<details><summary>◯ <b>C.</b> AWS Config</summary>

❌ **Incorrect.** Config records resource configuration changes and checks compliance. Setting up an account structure is not part of its job.

</details>

<details><summary>◯ <b>D.</b> AWS CloudFormation</summary>

❌ **Incorrect.** CloudFormation provisions resources from templates. The company would still have to design the multi-account governance itself.

</details>

Study: [13.2 AWS Config vs. AWS Control Tower](../README.md#132-aws-config-vs-aws-control-tower)

### Question 3

Which statement about Service Control Policies (SCPs) in AWS Organizations is correct?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> SCPs set the maximum permissions available in member accounts, even for the root user of those accounts</summary>

✅ **Correct.** Even a member account's root user cannot bypass an SCP deny. SCPs restrict permissions and never grant them.

</details>

<details><summary>◯ <b>B.</b> SCPs grant permissions directly to IAM users</summary>

❌ **Incorrect.** SCPs only limit what can be allowed. IAM policies still have to grant the permissions.

</details>

<details><summary>◯ <b>C.</b> The root user of a member account can bypass an SCP</summary>

❌ **Incorrect.** Root users of member accounts are restricted by SCPs.

</details>

<details><summary>◯ <b>D.</b> SCPs apply only to the Organizations management account</summary>

❌ **Incorrect.** SCPs apply to member accounts and have no effect on the management account.

</details>

Study: [13.1 AWS Organizations & Service Control Policies (SCPs)](../README.md#131-aws-organizations--service-control-policies-scps)

### Question 4

A company wants to continuously check whether its Amazon S3 buckets and Amazon EBS volumes comply with internal configuration rules and keep a history of configuration changes. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon Inspector</summary>

❌ **Incorrect.** Inspector scans for software vulnerabilities and network exposure, but it does not track configuration compliance over time.

</details>

<details><summary>◯ <b>B.</b> AWS CloudTrail</summary>

❌ **Incorrect.** CloudTrail records API calls. Evaluating resource configuration against rules is a different job.

</details>

<details><summary>◯ <b>C.</b> Amazon GuardDuty</summary>

❌ **Incorrect.** GuardDuty detects threats and does not check configuration compliance.

</details>

<details><summary>◯ <b>D.</b> AWS Config</summary>

✅ **Correct.** Config records resource configuration changes over time and evaluates them against rules, for example flagging public buckets or unencrypted volumes.

</details>

Study: [13.2 AWS Config vs. AWS Control Tower](../README.md#132-aws-config-vs-aws-control-tower)

### Question 5

Which TWO tasks can Amazon CloudWatch perform?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> Record a history of AWS API calls made in the account</summary>

❌ **Incorrect.** That is AWS CloudTrail.

</details>

<details><summary>☐ <b>B.</b> Scan EC2 instances for software vulnerabilities</summary>

❌ **Incorrect.** That is Amazon Inspector.

</details>

<details><summary>☐ <b>C.</b> Collect and track performance metrics such as EC2 CPU utilization</summary>

✅ **Correct.** CloudWatch monitoring is built on metrics.

</details>

<details><summary>☐ <b>D.</b> Trigger alarms that send Amazon SNS notifications or start Auto Scaling actions</summary>

✅ **Correct.** Alarms watch a metric and react when a threshold is crossed.

</details>

<details><summary>☐ <b>E.</b> Provide AWS compliance reports for download</summary>

❌ **Incorrect.** That is AWS Artifact.

</details>

Study: [13.3 Observability: Amazon CloudWatch vs. AWS CloudTrail](../README.md#133-observability-amazon-cloudwatch-vs-aws-cloudtrail)

[Study guide: 13. Cloud Governance, Management & Monitoring](../README.md#13--cloud-governance-management--monitoring) · [All topics](README.md) · [Next: 14. Machine Learning, AI & High-Performance Compute](14-ml-ai-hpc.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
