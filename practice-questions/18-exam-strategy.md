# Practice questions: 18. Exam Strategy & Last-Minute Checklist

[Study guide: 18. Exam Strategy & Last-Minute Checklist](../README.md#18--exam-strategy--last-minute-checklist) · [All topics](README.md)

> [!NOTE]
> Read the question and decide on your answer, then click an option to see whether it is right or wrong and why. A round marker (◯) means pick one answer. A square marker (☐) means pick every answer the question asks for, so click each option you think is correct.

### Question 1

AWS can offer lower pay-as-you-go prices because it aggregates the usage of hundreds of thousands of customers. Which benefit of the AWS Cloud does this describe?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Go global in minutes</summary>

❌ **Incorrect.** This is about deploying applications in multiple Regions quickly.

</details>

<details><summary>◯ <b>B.</b> Stop guessing capacity</summary>

❌ **Incorrect.** This is about matching resources to demand instead of sizing for peak load.

</details>

<details><summary>◯ <b>C.</b> Benefit from massive economies of scale</summary>

✅ **Correct.** Aggregated usage lets AWS achieve lower costs and pass the savings to customers as lower prices.

</details>

<details><summary>◯ <b>D.</b> Increase speed and agility</summary>

❌ **Incorrect.** This is about getting resources in minutes instead of weeks.

</details>

Study: [1.3 The 6 Advantages of Cloud Computing](../README.md#13-the-6-advantages-of-cloud-computing)

### Question 2

Which TWO statements about AWS Support plans are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> Business Support+ includes a designated Technical Account Manager</summary>

❌ **Incorrect.** A designated TAM comes with Enterprise Support, not with Business Support+.

</details>

<details><summary>☐ <b>B.</b> Basic Support is included for all AWS customers at no additional charge</summary>

✅ **Correct.** Basic provides help with account and billing questions, plus documentation, support forums, and service health checks.

</details>

<details><summary>☐ <b>C.</b> Basic Support includes 24/7 technical support by phone</summary>

❌ **Incorrect.** Basic has no technical support. It covers account and billing questions.

</details>

<details><summary>☐ <b>D.</b> Only Enterprise Support includes the full set of Trusted Advisor checks</summary>

❌ **Incorrect.** Business Support+ and the higher plans also include the full set of checks.

</details>

<details><summary>☐ <b>E.</b> Enterprise Support includes a designated Technical Account Manager (TAM)</summary>

✅ **Correct.** A designated TAM is a feature of Enterprise Support.

</details>

Study: [16.3 AWS Support Plans Comparison (Detailed Matrix)](../README.md#163-aws-support-plans-comparison-detailed-matrix)

### Question 3

An Amazon Linux EC2 instance runs for 30 seconds and is then terminated. For how many seconds is the company billed?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> 30 seconds</summary>

❌ **Incorrect.** The minimum charge is 60 seconds, so a shorter run is still billed for 60 seconds.

</details>

<details><summary>◯ <b>B.</b> 600 seconds (10 minutes)</summary>

❌ **Incorrect.** EC2's minimum charge is 60 seconds, not 10 minutes.

</details>

<details><summary>◯ <b>C.</b> 60 seconds</summary>

✅ **Correct.** EC2 is billed per second with a 60-second minimum charge.

</details>

<details><summary>◯ <b>D.</b> 3,600 seconds (1 hour)</summary>

❌ **Incorrect.** Per-second billing replaced the hourly minimum for these instances.

</details>

Study: [7.1 Amazon Elastic Compute Cloud (EC2) Overview & Families](../README.md#71-amazon-elastic-compute-cloud-ec2-overview--families)

### Question 4

Which of the following does NOT encrypt data at rest by default unless the customer turns encryption on?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon S3</summary>

❌ **Incorrect.** Since January 2023, new objects are encrypted automatically with SSE-S3.

</details>

<details><summary>◯ <b>B.</b> Amazon EBS volumes</summary>

✅ **Correct.** EBS encryption is opt-in per volume, unless the account-level default encryption setting is enabled for the Region.

</details>

<details><summary>◯ <b>C.</b> Amazon DynamoDB</summary>

❌ **Incorrect.** DynamoDB encrypts all tables at rest by default.

</details>

<details><summary>◯ <b>D.</b> AWS Storage Gateway</summary>

❌ **Incorrect.** Data handled by Storage Gateway is encrypted in transit and at rest by default.

</details>

Study: [8.3 Amazon EBS vs. EC2 Instance Store](../README.md#83-amazon-ebs-vs-ec2-instance-store)

### Question 5

A company wants to centralize operating system and application log files from its EC2 instances and on-premises servers in one searchable place. What should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS CloudTrail</summary>

❌ **Incorrect.** CloudTrail records AWS API calls, not operating system or application logs.

</details>

<details><summary>◯ <b>B.</b> Amazon CloudWatch Logs with the CloudWatch agent</summary>

✅ **Correct.** The agent streams operating system and application logs from servers to CloudWatch Logs.

</details>

<details><summary>◯ <b>C.</b> AWS Config</summary>

❌ **Incorrect.** Config records resource configuration changes, not server log files.

</details>

<details><summary>◯ <b>D.</b> Amazon Inspector</summary>

❌ **Incorrect.** Inspector scans for software vulnerabilities and does not collect logs.

</details>

Study: [13.3 Observability: Amazon CloudWatch vs. AWS CloudTrail](../README.md#133-observability-amazon-cloudwatch-vs-aws-cloudtrail)

[Study guide: 18. Exam Strategy & Last-Minute Checklist](../README.md#18--exam-strategy--last-minute-checklist) · [All topics](README.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
