# 📝 Practice Questions: 1. 🚀 Introduction & Cloud Fundamentals

[⬅️ Study guide: 1. 🚀 Introduction & Cloud Fundamentals](../README.md#1--introduction--cloud-fundamentals) · [📚 All topics](README.md) · [Next: 2. 🛡️ Getting Started & Account Security Baseline ➡️](02-account-security-baseline.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

Which TWO are perspectives of the AWS Cloud Adoption Framework (AWS CAF)?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> People</summary>

✅ **Correct.** People is a CAF perspective. It covers workforce transformation, cloud fluency, and culture.

</details>

<details><summary>☐ <b>B.</b> Reliability</summary>

❌ **Incorrect.** Reliability is a pillar of the AWS Well-Architected Framework, not a CAF perspective.

</details>

<details><summary>☐ <b>C.</b> Performance Efficiency</summary>

❌ **Incorrect.** Performance Efficiency is a Well-Architected pillar. The CAF perspectives are Business, People, Governance, Platform, Security, and Operations.

</details>

<details><summary>☐ <b>D.</b> Operations</summary>

✅ **Correct.** Operations is a CAF perspective. It covers observability, incident management, and patch management.

</details>

<details><summary>☐ <b>E.</b> Cost Optimization</summary>

❌ **Incorrect.** Cost Optimization is a Well-Architected pillar. In the CAF, cloud financial management sits under the Governance perspective.

</details>

📖 **Study:** [1.7 AWS Cloud Adoption Framework (AWS CAF)](../README.md#17-aws-cloud-adoption-framework-aws-caf)

---

### Question 2

A company keeps its customer database in its own data center and runs its web tier on AWS, connected through AWS Direct Connect. Which cloud deployment model is this?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Hybrid</summary>

✅ **Correct.** Hybrid cloud connects on-premises infrastructure with AWS resources, for example through AWS Direct Connect, Site-to-Site VPN, or AWS Outposts.

</details>

<details><summary>◯ <b>B.</b> Public cloud (cloud-native)</summary>

❌ **Incorrect.** A cloud-native deployment runs every component in the cloud. This company still runs its database on premises.

</details>

<details><summary>◯ <b>C.</b> Private cloud (on-premises)</summary>

❌ **Incorrect.** A private cloud keeps all infrastructure in the company's own data center. Part of this workload already runs on AWS.

</details>

<details><summary>◯ <b>D.</b> Multi-cloud</summary>

❌ **Incorrect.** Multi-cloud means using more than one cloud provider, such as AWS and Azure. This scenario combines on-premises and AWS only.

</details>

📖 **Study:** [1.5 Cloud Deployment Models](../README.md#15-cloud-deployment-models)

---

### Question 3

A company stops buying servers up front and instead pays only for the compute capacity it uses each month. Which benefit of the AWS Cloud does this describe?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Benefit from massive economies of scale</summary>

❌ **Incorrect.** This is about AWS passing on lower prices because it aggregates the usage of many customers. It does not describe how the company pays.

</details>

<details><summary>◯ <b>B.</b> Go global in minutes</summary>

❌ **Incorrect.** This is about deploying applications in several AWS Regions within minutes to reduce latency for users worldwide.

</details>

<details><summary>◯ <b>C.</b> Trade capital expense for variable expense</summary>

✅ **Correct.** Up-front capital expense (CapEx) is replaced by pay-as-you-go operating expense (OpEx). AWS also words this benefit as "trade fixed expense for variable expense".

</details>

<details><summary>◯ <b>D.</b> Stop guessing capacity</summary>

❌ **Incorrect.** This is about scaling resources up and down to match demand instead of sizing for peak load. It does not describe the payment model.

</details>

📖 **Study:** [1.3 The 6 Advantages of Cloud Computing](../README.md#13-the-6-advantages-of-cloud-computing)

---

### Question 4

A company wants to move its on-premises Linux servers to Amazon EC2 as quickly as possible without changing any application code. Which migration strategy should it choose?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Refactor / re-architect</summary>

❌ **Incorrect.** Refactoring redesigns the application, for example into microservices or serverless. It needs code changes and takes much longer.

</details>

<details><summary>◯ <b>B.</b> Replatform ("lift, tinker, and shift")</summary>

❌ **Incorrect.** Replatforming makes targeted optimizations, such as moving a self-managed database to Amazon RDS, so it goes beyond a pure lift and shift.

</details>

<details><summary>◯ <b>C.</b> Rehost ("lift and shift")</summary>

✅ **Correct.** Rehosting moves servers to EC2 as they are, with no code changes. AWS Application Migration Service (MGN), now branded AWS Transform MGN, automates it.

</details>

<details><summary>◯ <b>D.</b> Retire</summary>

❌ **Incorrect.** Retiring means decommissioning applications that are no longer needed. It does not move them.

</details>

📖 **Study:** [1.8 Cloud Migration Strategies: The 7 Rs & Migration Tools](../README.md#18-cloud-migration-strategies-the-7-rs--migration-tools)

---

### Question 5

A development team wants to upload its application code and let AWS manage the operating system, patching, and capacity provisioning behind it. Which cloud service model is this?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Platform as a Service (PaaS)</summary>

✅ **Correct.** The customer manages only the application and its data while AWS manages the platform underneath, for example with AWS Elastic Beanstalk.

</details>

<details><summary>◯ <b>B.</b> Infrastructure as a Service (IaaS)</summary>

❌ **Incorrect.** With IaaS, such as Amazon EC2, the customer still manages the guest operating system, patching, and runtime.

</details>

<details><summary>◯ <b>C.</b> Software as a Service (SaaS)</summary>

❌ **Incorrect.** SaaS delivers a finished application to end users. This team is deploying its own code, so it is not consuming SaaS.

</details>

<details><summary>◯ <b>D.</b> Hybrid cloud</summary>

❌ **Incorrect.** Hybrid is a deployment model that connects on-premises and cloud resources. It is not a service model.

</details>

📖 **Study:** [1.4 Types of Cloud Computing (Cloud Service Models)](../README.md#14-types-of-cloud-computing-cloud-service-models)

---

[⬅️ Study guide: 1. 🚀 Introduction & Cloud Fundamentals](../README.md#1--introduction--cloud-fundamentals) · [📚 All topics](README.md) · [Next: 2. 🛡️ Getting Started & Account Security Baseline ➡️](02-account-security-baseline.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
