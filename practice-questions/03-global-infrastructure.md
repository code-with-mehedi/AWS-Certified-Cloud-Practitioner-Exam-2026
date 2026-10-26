# 📝 Practice Questions: 3. 🌐 AWS Global Infrastructure

[⬅️ Study guide: 3. 🌐 AWS Global Infrastructure](../README.md#3--aws-global-infrastructure) · [📚 All topics](README.md) · [Next: 4. 📐 Cloud Architecture & Reliability ➡️](04-architecture-reliability.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

A company must keep its customer data inside one specific country because of legal requirements. Which factor should drive its choice of AWS Region?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Lowest latency to end users</summary>

❌ **Incorrect.** Latency matters, but it is secondary when the law restricts where the data may be stored.

</details>

<details><summary>◯ <b>B.</b> Lowest price</summary>

❌ **Incorrect.** Prices vary by Region, but cost cannot override a legal data residency requirement.

</details>

<details><summary>◯ <b>C.</b> Compliance and data sovereignty</summary>

✅ **Correct.** When regulations require data to stay within a country, that requirement decides which Regions are allowed.

</details>

<details><summary>◯ <b>D.</b> Availability of the newest AWS services</summary>

❌ **Incorrect.** New services launch in some Regions first, but a legal requirement comes before service availability.

</details>

📖 **Study:** [3.1 AWS Regions & Availability Zones (AZs)](../README.md#31-aws-regions--availability-zones-azs)

---

### Question 2

Which statement correctly describes an AWS Availability Zone (AZ)?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> One or more discrete data centers with redundant power, networking, and connectivity inside an AWS Region</summary>

✅ **Correct.** Each Region has multiple AZs, which are isolated from each other but connected by low-latency private networking.

</details>

<details><summary>◯ <b>B.</b> A geographic area that contains several AWS Regions</summary>

❌ **Incorrect.** It is the other way around: a Region contains multiple Availability Zones.

</details>

<details><summary>◯ <b>C.</b> A location used by Amazon CloudFront to cache content close to users</summary>

❌ **Incorrect.** That describes an edge location (Point of Presence), not an Availability Zone.

</details>

<details><summary>◯ <b>D.</b> A single rack of servers that hosts Amazon EC2 instances</summary>

❌ **Incorrect.** An AZ is made of one or more full data centers, far larger than a rack.

</details>

📖 **Study:** [3.1 AWS Regions & Availability Zones (AZs)](../README.md#31-aws-regions--availability-zones-azs)

---

### Question 3

Which TWO statements about AWS Regions and Availability Zones are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> An Availability Zone is made up of several AWS Regions</summary>

❌ **Incorrect.** A Region is made up of several Availability Zones, not the other way around.

</details>

<details><summary>☐ <b>B.</b> Every AWS service is available in every Region on the day it launches</summary>

❌ **Incorrect.** New services and instance types often launch in a subset of Regions first.

</details>

<details><summary>☐ <b>C.</b> Each AWS Region consists of multiple isolated Availability Zones</summary>

✅ **Correct.** AZs are physically separate so that a failure in one is unlikely to affect the others.

</details>

<details><summary>☐ <b>D.</b> Data stored in one Region is automatically copied to all other Regions</summary>

❌ **Incorrect.** Data stays in the Region where you store it unless you choose to replicate it.

</details>

<details><summary>☐ <b>E.</b> Availability Zones in a Region are connected by low-latency, high-throughput private networking</summary>

✅ **Correct.** This makes synchronous replication between AZs, such as RDS Multi-AZ, practical.

</details>

📖 **Study:** [3.1 AWS Regions & Availability Zones (AZs)](../README.md#31-aws-regions--availability-zones-azs)

---

### Question 4

Which of the following is a global AWS service that is not tied to a single Region?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Identity and Access Management (IAM)</summary>

✅ **Correct.** IAM users, groups, roles, and policies apply across all Regions. Other global services include Route 53 and CloudFront.

</details>

<details><summary>◯ <b>B.</b> Amazon EC2</summary>

❌ **Incorrect.** EC2 instances run in a specific Region and Availability Zone.

</details>

<details><summary>◯ <b>C.</b> Amazon RDS</summary>

❌ **Incorrect.** RDS databases are created in a specific Region.

</details>

<details><summary>◯ <b>D.</b> AWS Lambda</summary>

❌ **Incorrect.** Lambda functions are created and run in a specific Region.

</details>

📖 **Study:** [3.4 Regional vs. Global AWS Services](../README.md#34-regional-vs-global-aws-services)

---

### Question 5

A company needs single-digit millisecond latency for end users in a large metropolitan area where no AWS Region is nearby. Which AWS infrastructure offering should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Outposts</summary>

❌ **Incorrect.** Outposts racks run in the company's own data center, not in a nearby AWS facility.

</details>

<details><summary>◯ <b>B.</b> AWS Local Zones</summary>

✅ **Correct.** Local Zones place compute, storage, and database services close to large population centers.

</details>

<details><summary>◯ <b>C.</b> AWS Wavelength</summary>

❌ **Incorrect.** Wavelength embeds AWS services inside 5G carrier networks for mobile-connected devices.

</details>

<details><summary>◯ <b>D.</b> AWS Ground Station</summary>

❌ **Incorrect.** Ground Station controls satellites and downlinks satellite data.

</details>

📖 **Study:** [3.3 Edge & Hybrid Infrastructure Solutions](../README.md#33-edge--hybrid-infrastructure-solutions)

---

[⬅️ Study guide: 3. 🌐 AWS Global Infrastructure](../README.md#3--aws-global-infrastructure) · [📚 All topics](README.md) · [Next: 4. 📐 Cloud Architecture & Reliability ➡️](04-architecture-reliability.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
