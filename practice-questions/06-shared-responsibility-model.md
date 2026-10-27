# Practice questions: 6. AWS Shared Responsibility Model

[Study guide: 6. AWS Shared Responsibility Model](../README.md#6--aws-shared-responsibility-model) · [All topics](README.md) · [Next: 7. Compute Services](07-compute-services.md)

> [!NOTE]
> Read the question and decide on your answer, then click an option to see whether it is right or wrong and why. A round marker (◯) means pick one answer. A square marker (☐) means pick every answer the question asks for, so click each option you think is correct.

### Question 1

Under the AWS Shared Responsibility Model, which task is the responsibility of AWS?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Managing IAM user permissions</summary>

❌ **Incorrect.** Controlling who can access which resources is the customer's responsibility.

</details>

<details><summary>◯ <b>B.</b> Maintaining the physical security of AWS data centers</summary>

✅ **Correct.** AWS is responsible for security of the cloud, including facilities, hardware, and the global infrastructure.

</details>

<details><summary>◯ <b>C.</b> Configuring security group rules</summary>

❌ **Incorrect.** Customers manage the network and firewall configuration of their own resources.

</details>

<details><summary>◯ <b>D.</b> Classifying customer data and choosing encryption settings</summary>

❌ **Incorrect.** Customers are responsible for their data and for how it is protected.

</details>

Study: [6.1 The Core Model: "OF" vs. "IN" the Cloud](../README.md#61-the-core-model-of-vs-in-the-cloud)

### Question 2

Which of the following is an example of a SHARED control in the AWS Shared Responsibility Model?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Physical and environmental security of data centers</summary>

❌ **Incorrect.** This is entirely AWS's responsibility, and customers inherit it.

</details>

<details><summary>◯ <b>B.</b> Destruction of retired storage devices</summary>

❌ **Incorrect.** AWS handles the decommissioning and destruction of storage media.

</details>

<details><summary>◯ <b>C.</b> Patch management</summary>

✅ **Correct.** AWS patches the physical hosts and infrastructure, while the customer patches the guest operating system and applications.

</details>

<details><summary>◯ <b>D.</b> Classifying customer data</summary>

❌ **Incorrect.** Data classification is the customer's responsibility.

</details>

Study: [6.3 Shared Controls Matrix](../README.md#63-shared-controls-matrix)

### Question 3

Which TWO are the customer's responsibility under the AWS Shared Responsibility Model?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> Managing IAM users, passwords, and MFA</summary>

✅ **Correct.** Identity and access management of the account is security in the cloud.

</details>

<details><summary>☐ <b>B.</b> Operating the AWS Regions, Availability Zones, and edge locations</summary>

❌ **Incorrect.** The global infrastructure is the responsibility of AWS.

</details>

<details><summary>☐ <b>C.</b> Classifying and protecting customer data</summary>

✅ **Correct.** Customers decide how their data is classified and encrypted.

</details>

<details><summary>☐ <b>D.</b> Replacing failed disks in AWS data centers</summary>

❌ **Incorrect.** AWS handles hardware maintenance in its own facilities.

</details>

<details><summary>☐ <b>E.</b> Patching the hypervisor</summary>

❌ **Incorrect.** AWS is responsible for the virtualization layer.

</details>

Study: [6.1 The Core Model: "OF" vs. "IN" the Cloud](../README.md#61-the-core-model-of-vs-in-the-cloud)

### Question 4

A company runs a custom web application on Amazon EC2 instances. Who is responsible for installing security patches on the guest operating system?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS</summary>

❌ **Incorrect.** AWS patches the hypervisor and the underlying hardware, but not the guest operating system of EC2 instances.

</details>

<details><summary>◯ <b>B.</b> Amazon Inspector</summary>

❌ **Incorrect.** Inspector scans for software vulnerabilities and reports findings but does not install patches.

</details>

<details><summary>◯ <b>C.</b> AWS Support, on any support plan</summary>

❌ **Incorrect.** AWS Support answers questions and helps troubleshoot. It does not patch customer instances.

</details>

<details><summary>◯ <b>D.</b> The customer</summary>

✅ **Correct.** With EC2, which is infrastructure as a service, the customer manages the guest OS, including patches.

</details>

Study: [6.2 Shared Responsibility Across Service Models](../README.md#62-shared-responsibility-across-service-models)

### Question 5

A company uses Amazon RDS for MySQL. Which task remains the customer's responsibility?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Patching the database engine software</summary>

❌ **Incorrect.** RDS is a managed service, so AWS provides and applies the engine patches during the maintenance window that you configure.

</details>

<details><summary>◯ <b>B.</b> Replacing failed physical storage hardware</summary>

❌ **Incorrect.** Hardware maintenance is part of the security of the cloud, which AWS handles.

</details>

<details><summary>◯ <b>C.</b> Configuring security groups and managing database user access</summary>

✅ **Correct.** AWS runs the managed database, but the customer controls network access and who can use the database.

</details>

<details><summary>◯ <b>D.</b> Maintaining the operating system of the underlying host</summary>

❌ **Incorrect.** With RDS, AWS manages the host operating system.

</details>

Study: [6.2 Shared Responsibility Across Service Models](../README.md#62-shared-responsibility-across-service-models)

[Study guide: 6. AWS Shared Responsibility Model](../README.md#6--aws-shared-responsibility-model) · [All topics](README.md) · [Next: 7. Compute Services](07-compute-services.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
