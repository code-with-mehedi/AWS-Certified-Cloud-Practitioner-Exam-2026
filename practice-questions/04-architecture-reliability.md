# 📝 Practice Questions: 4. 📐 Cloud Architecture & Reliability

[⬅️ Study guide: 4. 📐 Cloud Architecture & Reliability](../README.md#4--cloud-architecture--reliability) · [📚 All topics](README.md) · [Next: 5. 🧰 Management, Governance & Developer Tools ➡️](05-management-governance-developer-tools.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

Which THREE design choices improve the availability of a web application on AWS?

*☐ Choose THREE.*

<details><summary>☐ <b>A.</b> Run EC2 instances in multiple Availability Zones behind an Elastic Load Balancer</summary>

✅ **Correct.** If one AZ fails, the load balancer keeps sending traffic to healthy instances in the others.

</details>

<details><summary>☐ <b>B.</b> Run the entire application on one large EC2 instance</summary>

❌ **Incorrect.** A single instance is a single point of failure.

</details>

<details><summary>☐ <b>C.</b> Use an Amazon RDS Multi-AZ deployment for the database</summary>

✅ **Correct.** RDS keeps a synchronous standby in a second AZ and fails over automatically.

</details>

<details><summary>☐ <b>D.</b> Use Amazon Route 53 health checks with failover routing</summary>

✅ **Correct.** Route 53 detects an unhealthy endpoint and automatically routes users to a healthy standby.

</details>

<details><summary>☐ <b>E.</b> Keep all application data on EC2 instance store volumes</summary>

❌ **Incorrect.** Instance store data is lost when the instance stops or terminates.

</details>

<details><summary>☐ <b>F.</b> Place every resource in one Availability Zone to reduce latency</summary>

❌ **Incorrect.** An outage in that AZ would take down the whole application.

</details>

📖 **Study:** [4.3 High Availability Architecture Design](../README.md#43-high-availability-architecture-design)

---

### Question 2

A company changes an Amazon EC2 instance from a t3.medium to an m5.2xlarge to handle more load. What type of scaling is this?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Horizontal scaling (scaling out)</summary>

❌ **Incorrect.** Horizontal scaling adds more instances of the same size, for example through an Auto Scaling group.

</details>

<details><summary>◯ <b>B.</b> Vertical scaling (scaling up)</summary>

✅ **Correct.** Vertical scaling makes one instance larger or smaller by changing its size.

</details>

<details><summary>◯ <b>C.</b> Cross-Region replication</summary>

❌ **Incorrect.** This copies S3 objects between Regions. It is not a way to scale compute.

</details>

<details><summary>◯ <b>D.</b> Elastic Load Balancing</summary>

❌ **Incorrect.** A load balancer distributes traffic across targets. It does not change the size of an instance.

</details>

📖 **Study:** [4.1 Core Architecture Terminologies](../README.md#41-core-architecture-terminologies)

---

### Question 3

A company states that after a failure it can tolerate losing, at most, the last 15 minutes of data. Which metric does this describe?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Recovery Time Objective (RTO)</summary>

❌ **Incorrect.** RTO is the maximum acceptable downtime before service is restored, not the amount of data lost.

</details>

<details><summary>◯ <b>B.</b> Total Cost of Ownership (TCO)</summary>

❌ **Incorrect.** TCO estimates the direct and indirect costs of running infrastructure.

</details>

<details><summary>◯ <b>C.</b> Service Level Agreement (SLA)</summary>

❌ **Incorrect.** An SLA is a commitment about service availability. It does not define acceptable data loss.

</details>

<details><summary>◯ <b>D.</b> Recovery Point Objective (RPO)</summary>

✅ **Correct.** RPO is the maximum acceptable amount of data loss, measured in time.

</details>

📖 **Study:** [4.2 Disaster Recovery (DR) Strategies & RTO / RPO](../README.md#42-disaster-recovery-dr-strategies--rto--rpo)

---

### Question 4

A company wants a disaster recovery strategy in which a scaled-down but fully functional copy of its production environment runs continuously in another Region and is scaled up after a failure. Which strategy is this?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Backup and restore</summary>

❌ **Incorrect.** Data is backed up and the stack is rebuilt only after a disaster. It is the cheapest strategy but has the slowest recovery.

</details>

<details><summary>◯ <b>B.</b> Pilot light</summary>

❌ **Incorrect.** Only core components such as the replicated database run. Compute is started only when a disaster happens.

</details>

<details><summary>◯ <b>C.</b> Warm standby</summary>

✅ **Correct.** A smaller always-on copy of production can be scaled up quickly, giving a low recovery time at moderate cost.

</details>

<details><summary>◯ <b>D.</b> Multi-site active/active</summary>

❌ **Incorrect.** Full production capacity runs in two or more Regions at the same time, which is the fastest but most expensive option.

</details>

📖 **Study:** [4.2 Disaster Recovery (DR) Strategies & RTO / RPO](../README.md#42-disaster-recovery-dr-strategies--rto--rpo)

---

### Question 5

Amazon S3 Standard is designed for 99.999999999% (11 nines) of what?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Durability</summary>

✅ **Correct.** Durability is the likelihood that stored data is not lost or corrupted over time. S3 offers 11 nines of durability.

</details>

<details><summary>◯ <b>B.</b> Availability</summary>

❌ **Incorrect.** S3 Standard is designed for 99.99% availability. The 11 nines figure refers to durability.

</details>

<details><summary>◯ <b>C.</b> Fault tolerance</summary>

❌ **Incorrect.** Fault tolerance describes a system that keeps working through component failures. It is not measured in nines of object loss.

</details>

<details><summary>◯ <b>D.</b> Elasticity</summary>

❌ **Incorrect.** Elasticity describes automatically adding and removing resources to match demand.

</details>

📖 **Study:** [4.1 Core Architecture Terminologies](../README.md#41-core-architecture-terminologies)

---

[⬅️ Study guide: 4. 📐 Cloud Architecture & Reliability](../README.md#4--cloud-architecture--reliability) · [📚 All topics](README.md) · [Next: 5. 🧰 Management, Governance & Developer Tools ➡️](05-management-governance-developer-tools.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
