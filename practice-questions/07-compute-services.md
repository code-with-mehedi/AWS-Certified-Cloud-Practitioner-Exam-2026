# 📝 Practice Questions: 7. 💻 Compute Services

[⬅️ Study guide: 7. 💻 Compute Services](../README.md#7--compute-services) · [📚 All topics](README.md) · [Next: 8. 🗄️ Storage Services ➡️](08-storage-services.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

A company wants to run containers on Amazon ECS or Amazon EKS without provisioning or managing the underlying EC2 instances. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon Elastic Container Registry (Amazon ECR)</summary>

❌ **Incorrect.** ECR stores and manages container images. It does not run containers.

</details>

<details><summary>◯ <b>B.</b> Amazon EC2 Dedicated Hosts</summary>

❌ **Incorrect.** Dedicated Hosts are physical servers that you would have to manage yourself.

</details>

<details><summary>◯ <b>C.</b> Amazon Lightsail</summary>

❌ **Incorrect.** Lightsail provides simple virtual private servers with bundled resources and a predictable price. It is not a compute engine for ECS or EKS.

</details>

<details><summary>◯ <b>D.</b> AWS Fargate</summary>

✅ **Correct.** Fargate is a serverless compute engine for containers that works with both ECS and EKS.

</details>

📖 **Study:** [7.5 Containers on AWS: ECS, EKS, Fargate, ECR](../README.md#75-containers-on-aws-ecs-eks-fargate-ecr)

---

### Question 2

Which Amazon EC2 instance family category is best suited for memory-intensive workloads such as high-performance in-memory databases?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Compute optimized (C)</summary>

❌ **Incorrect.** Compute optimized instances suit CPU-bound work such as batch processing and scientific modeling.

</details>

<details><summary>◯ <b>B.</b> Storage optimized (I, D, H)</summary>

❌ **Incorrect.** Storage optimized instances target high sequential read and write access to large local datasets.

</details>

<details><summary>◯ <b>C.</b> Memory optimized (R, X, Z)</summary>

✅ **Correct.** Memory optimized instances deliver fast performance for workloads that process large datasets in memory.

</details>

<details><summary>◯ <b>D.</b> General purpose (T, M)</summary>

❌ **Incorrect.** General purpose instances balance compute, memory, and networking for typical workloads.

</details>

📖 **Study:** [7.1 Amazon Elastic Compute Cloud (EC2) Overview & Families](../README.md#71-amazon-elastic-compute-cloud-ec2-overview--families)

---

### Question 3

Which TWO statements about AWS Lambda are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> It runs code in response to events without provisioning or managing servers</summary>

✅ **Correct.** Lambda is event-driven, serverless compute.

</details>

<details><summary>☐ <b>B.</b> A single invocation can run for up to 24 hours</summary>

❌ **Incorrect.** A standard Lambda invocation can run for at most 15 minutes, so 24 hours is not possible.

</details>

<details><summary>☐ <b>C.</b> Customers must patch the operating system that runs their functions</summary>

❌ **Incorrect.** AWS manages the underlying servers and operating system.

</details>

<details><summary>☐ <b>D.</b> It is billed for the number of requests and the duration of execution</summary>

✅ **Correct.** You pay per request and per millisecond of execution time, and nothing when the code is not running.

</details>

<details><summary>☐ <b>E.</b> Customers must provision and scale a fleet of servers to run their functions</summary>

❌ **Incorrect.** Lambda manages the servers for you and scales automatically, so there is no fleet to provision or scale.

</details>

📖 **Study:** [7.6 Serverless Compute: AWS Lambda](../README.md#76-serverless-compute-aws-lambda)

---

### Question 4

A company runs a fault-tolerant image-rendering batch job that can be interrupted and restarted. Which EC2 purchasing option provides the LOWEST cost?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> On-Demand Instances</summary>

❌ **Incorrect.** On-Demand has no commitment but it is the baseline price, so it costs far more than Spot.

</details>

<details><summary>◯ <b>B.</b> Standard Reserved Instances</summary>

❌ **Incorrect.** Reserved Instances discount steady-state workloads in exchange for a 1-year or 3-year commitment. They are not the cheapest choice for interruptible jobs.

</details>

<details><summary>◯ <b>C.</b> Spot Instances</summary>

✅ **Correct.** Spot Instances offer up to a 90% discount. AWS can reclaim them with a 2-minute warning, which this fault-tolerant job can handle.

</details>

<details><summary>◯ <b>D.</b> Dedicated Hosts</summary>

❌ **Incorrect.** Dedicated Hosts are physical servers for your exclusive use and are among the most expensive options.

</details>

📖 **Study:** [7.3 EC2 Pricing Models Matrix & Rules](../README.md#73-ec2-pricing-models-matrix--rules)

---

### Question 5

A company wants to reuse its existing per-socket and per-core server software licenses on AWS and needs visibility into the physical sockets and cores. What should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon EC2 Dedicated Instances</summary>

❌ **Incorrect.** Dedicated Instances run on hardware reserved for your account but do not give you visibility into sockets and cores.

</details>

<details><summary>◯ <b>B.</b> Amazon EC2 Spot Instances</summary>

❌ **Incorrect.** Spot is a pricing model for spare capacity. It does not provide physical server visibility.

</details>

<details><summary>◯ <b>C.</b> Amazon EC2 On-Demand Capacity Reservations</summary>

❌ **Incorrect.** A Capacity Reservation guarantees capacity in an Availability Zone. It does not provide physical server visibility.

</details>

<details><summary>◯ <b>D.</b> Amazon EC2 Dedicated Hosts</summary>

✅ **Correct.** A Dedicated Host is a physical server dedicated to your account, with visibility into sockets and cores to support bring-your-own-license (BYOL).

</details>

📖 **Study:** [7.2 EC2 Tenancy: Shared vs. Dedicated Instances vs. Dedicated Hosts](../README.md#72-ec2-tenancy-shared-vs-dedicated-instances-vs-dedicated-hosts)

---

[⬅️ Study guide: 7. 💻 Compute Services](../README.md#7--compute-services) · [📚 All topics](README.md) · [Next: 8. 🗄️ Storage Services ➡️](08-storage-services.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
