# 📝 Practice Questions: 17. 🆚 High-Yield Exam "Cheat Sheet" & Service Disambiguation

[⬅️ Study guide: 17. 🆚 High-Yield Exam "Cheat Sheet" & Service Disambiguation](../README.md#17--high-yield-exam-cheat-sheet--service-disambiguation) · [📚 All topics](README.md) · [Next: 18. 🎓 Exam Strategy & Last-Minute Checklist ➡️](18-exam-strategy.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

Which service automatically scans Amazon EC2 instances, container images in Amazon ECR, and AWS Lambda functions for software vulnerabilities?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Artifact</summary>

❌ **Incorrect.** Artifact provides AWS's own compliance reports and agreements. It does not scan your workloads.

</details>

<details><summary>◯ <b>B.</b> AWS Trusted Advisor</summary>

❌ **Incorrect.** Trusted Advisor checks account-level best practices across areas such as cost, security, fault tolerance, performance, and service limits, not software vulnerabilities in your workloads.

</details>

<details><summary>◯ <b>C.</b> Amazon Macie</summary>

❌ **Incorrect.** Macie finds sensitive data such as PII in Amazon S3.

</details>

<details><summary>◯ <b>D.</b> Amazon Inspector</summary>

✅ **Correct.** Inspector is a vulnerability management service that scans these workloads for software vulnerabilities (CVEs) and unintended network exposure.

</details>

📖 **Study:** [17.1 Commonly Confused Services Cheat Sheet](../README.md#171-commonly-confused-services-cheat-sheet)

---

### Question 2

Which AWS service shows scheduled maintenance and resource retirements that specifically affect the company's own EC2 instances?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Health Dashboard - Service Health</summary>

❌ **Incorrect.** It shows the public status of AWS services in all Regions and is not personalized to your account.

</details>

<details><summary>◯ <b>B.</b> AWS Trusted Advisor</summary>

❌ **Incorrect.** Trusted Advisor gives best-practice recommendations. It does not report scheduled maintenance events.

</details>

<details><summary>◯ <b>C.</b> Amazon CloudWatch</summary>

❌ **Incorrect.** CloudWatch collects metrics and logs about your resources. It does not announce AWS maintenance events.

</details>

<details><summary>◯ <b>D.</b> AWS Health Dashboard - Your Account Health</summary>

✅ **Correct.** It shows events that affect the resources in your own account, such as scheduled maintenance and retirements.

</details>

📖 **Study:** [16.4 AWS Trusted Advisor & Health Dashboard](../README.md#164-aws-trusted-advisor--health-dashboard)

---

### Question 3

Which TWO statements about Elastic Load Balancing types are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> A Gateway Load Balancer routes HTTP requests by URL path</summary>

❌ **Incorrect.** A Gateway Load Balancer deploys and scales third-party virtual appliances such as firewalls.

</details>

<details><summary>☐ <b>B.</b> An Application Load Balancer is the right choice for UDP traffic</summary>

❌ **Incorrect.** An ALB supports HTTP, HTTPS, and gRPC. For UDP, use a Network Load Balancer.

</details>

<details><summary>☐ <b>C.</b> An Application Load Balancer operates at Layer 7 and supports path-based routing</summary>

✅ **Correct.** An ALB can route HTTP and HTTPS requests by URL path or host header.

</details>

<details><summary>☐ <b>D.</b> A Network Load Balancer operates at Layer 4 and supports static IP addresses</summary>

✅ **Correct.** An NLB handles TCP, UDP, and TLS traffic at very high performance, with a static IP address per Availability Zone.

</details>

<details><summary>☐ <b>E.</b> A Network Load Balancer supports host-based and path-based routing</summary>

❌ **Incorrect.** That is a layer 7 feature of the Application Load Balancer.

</details>

📖 **Study:** [17.1 Commonly Confused Services Cheat Sheet](../README.md#171-commonly-confused-services-cheat-sheet)

---

### Question 4

A company requires a dedicated, single-tenant hardware security module (HSM) that only the company controls. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Key Management Service (AWS KMS)</summary>

❌ **Incorrect.** KMS is a managed service that uses multi-tenant, AWS-managed hardware to create and control keys.

</details>

<details><summary>◯ <b>B.</b> AWS CloudHSM</summary>

✅ **Correct.** CloudHSM provides dedicated single-tenant HSMs that are under the customer's sole control.

</details>

<details><summary>◯ <b>C.</b> AWS Secrets Manager</summary>

❌ **Incorrect.** Secrets Manager stores and automatically rotates secrets such as database credentials.

</details>

<details><summary>◯ <b>D.</b> AWS Certificate Manager</summary>

❌ **Incorrect.** Certificate Manager provisions and manages TLS certificates.

</details>

📖 **Study:** [17.1 Commonly Confused Services Cheat Sheet](../README.md#171-commonly-confused-services-cheat-sheet)

---

### Question 5

A company wants a ready-made list of under-utilized EC2 instances without building any alarms or dashboards itself. Which service provides this?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon CloudWatch</summary>

❌ **Incorrect.** CloudWatch collects the raw metrics. You would still have to build the alarms and dashboards yourself.

</details>

<details><summary>◯ <b>B.</b> AWS CloudTrail</summary>

❌ **Incorrect.** CloudTrail records API calls, not resource utilization.

</details>

<details><summary>◯ <b>C.</b> AWS Config</summary>

❌ **Incorrect.** Config records configuration changes and compliance, not utilization.

</details>

<details><summary>◯ <b>D.</b> AWS Trusted Advisor</summary>

✅ **Correct.** Trusted Advisor runs checks, such as idle or low-utilization EC2 instances, and gives recommendations out of the box. The cost optimization checks need a Business-level or higher Support plan.

</details>

📖 **Study:** [17.1 Commonly Confused Services Cheat Sheet](../README.md#171-commonly-confused-services-cheat-sheet)

---

[⬅️ Study guide: 17. 🆚 High-Yield Exam "Cheat Sheet" & Service Disambiguation](../README.md#17--high-yield-exam-cheat-sheet--service-disambiguation) · [📚 All topics](README.md) · [Next: 18. 🎓 Exam Strategy & Last-Minute Checklist ➡️](18-exam-strategy.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
