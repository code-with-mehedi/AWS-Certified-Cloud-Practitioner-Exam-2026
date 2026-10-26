# 📝 Practice Questions: 8. 🗄️ Storage Services

[⬅️ Study guide: 8. 🗄️ Storage Services](../README.md#8-️-storage-services) · [📚 All topics](README.md) · [Next: 9. 📊 Database & Analytics Services ➡️](09-database-analytics.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

Which AWS storage option provides persistent block storage for Amazon EC2 instances and is tied to a single Availability Zone?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon EBS</summary>

✅ **Correct.** EBS volumes are network-attached persistent block storage. Their data persists independently of the instance and each volume lives in one AZ.

</details>

<details><summary>◯ <b>B.</b> Amazon EFS</summary>

❌ **Incorrect.** EFS is a shared file system that spans multiple AZs. It is not block storage.

</details>

<details><summary>◯ <b>C.</b> Amazon S3</summary>

❌ **Incorrect.** S3 is regional object storage, not block storage.

</details>

<details><summary>◯ <b>D.</b> EC2 instance store</summary>

❌ **Incorrect.** Instance store is temporary block storage on the host. Its data is lost when the instance stops or terminates.

</details>

📖 **Study:** [8.3 Amazon EBS vs. EC2 Instance Store](../README.md#83-amazon-ebs-vs-ec2-instance-store)

---

### Question 2

A company stores data with unknown or changing access patterns and wants storage costs optimized automatically, with no retrieval fees. Which Amazon S3 storage class should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> S3 Standard-IA</summary>

❌ **Incorrect.** Standard-IA charges a retrieval fee and has a 30-day minimum storage duration.

</details>

<details><summary>◯ <b>B.</b> S3 One Zone-IA</summary>

❌ **Incorrect.** One Zone-IA keeps data in a single Availability Zone and also charges for retrieval.

</details>

<details><summary>◯ <b>C.</b> S3 Intelligent-Tiering</summary>

✅ **Correct.** It moves objects between access tiers automatically as access patterns change, with no retrieval fees.

</details>

<details><summary>◯ <b>D.</b> S3 Glacier Flexible Retrieval</summary>

❌ **Incorrect.** It is an archive class with retrieval that takes minutes to hours, so it does not fit data that may be needed at any time.

</details>

📖 **Study:** [8.2 Amazon S3 Storage Classes & Lifecycle Management](../README.md#82-amazon-s3-storage-classes--lifecycle-management)

---

### Question 3

A company must keep compliance records for 10 years at the lowest possible storage cost. Retrieval within 12 to 48 hours is acceptable. Which Amazon S3 storage class should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> S3 Glacier Instant Retrieval</summary>

❌ **Incorrect.** It is meant for rarely accessed data that still needs millisecond retrieval, and it costs more than Deep Archive.

</details>

<details><summary>◯ <b>B.</b> S3 Standard-IA</summary>

❌ **Incorrect.** Standard-IA is for infrequently accessed data that needs fast access, and it costs much more than the archive classes.

</details>

<details><summary>◯ <b>C.</b> S3 Intelligent-Tiering</summary>

❌ **Incorrect.** Intelligent-Tiering suits unknown or changing access patterns. It is not the cheapest option for a known long-term archive.

</details>

<details><summary>◯ <b>D.</b> S3 Glacier Deep Archive</summary>

✅ **Correct.** Deep Archive is the lowest-cost storage class, designed for long-term retention with retrieval in 12 to 48 hours.

</details>

📖 **Study:** [8.2 Amazon S3 Storage Classes & Lifecycle Management](../README.md#82-amazon-s3-storage-classes--lifecycle-management)

---

### Question 4

Which TWO Amazon S3 features help protect objects from being accidentally deleted or overwritten?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> S3 Transfer Acceleration</summary>

❌ **Incorrect.** This speeds up long-distance uploads through CloudFront edge locations. It does not protect objects.

</details>

<details><summary>☐ <b>B.</b> S3 Intelligent-Tiering</summary>

❌ **Incorrect.** This is a storage class that optimizes cost. It does not protect against deletion.

</details>

<details><summary>☐ <b>C.</b> S3 Versioning</summary>

✅ **Correct.** Versioning keeps every version of an object, so you can restore a previous version after an overwrite or delete.

</details>

<details><summary>☐ <b>D.</b> S3 Event Notifications</summary>

❌ **Incorrect.** This sends a notification when events occur in a bucket. It does not prevent deletion or overwriting.

</details>

<details><summary>☐ <b>E.</b> S3 Object Lock</summary>

✅ **Correct.** Object Lock enforces a write-once-read-many (WORM) model, preventing an object version from being deleted or overwritten during a retention period or while a legal hold is in place.

</details>

📖 **Study:** [8.2 Amazon S3 Storage Classes & Lifecycle Management](../README.md#82-amazon-s3-storage-classes--lifecycle-management)

---

### Question 5

A company needs a shared file system that hundreds of Linux EC2 instances in multiple Availability Zones can access at the same time over NFS. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon EBS</summary>

❌ **Incorrect.** An EBS volume is block storage in a single AZ that is normally attached to one instance. It is not a shared NFS file system.

</details>

<details><summary>◯ <b>B.</b> Amazon EFS</summary>

✅ **Correct.** EFS is a managed POSIX/NFS file system for Linux that grows and shrinks automatically and can be mounted across AZs.

</details>

<details><summary>◯ <b>C.</b> Amazon FSx for Windows File Server</summary>

❌ **Incorrect.** It provides SMB file shares for Windows workloads, not NFS for Linux.

</details>

<details><summary>◯ <b>D.</b> EC2 instance store</summary>

❌ **Incorrect.** Instance store is temporary block storage on a single host. It cannot be shared across instances or AZs, and its data is lost when the instance stops or terminates.

</details>

📖 **Study:** [8.4 Amazon EFS vs. Amazon FSx](../README.md#84-amazon-efs-vs-amazon-fsx)

---

[⬅️ Study guide: 8. 🗄️ Storage Services](../README.md#8-️-storage-services) · [📚 All topics](README.md) · [Next: 9. 📊 Database & Analytics Services ➡️](09-database-analytics.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
