# 📝 Practice Questions: 9. 📊 Database & Analytics Services

[⬅️ Study guide: 9. 📊 Database & Analytics Services](../README.md#9--database--analytics-services) · [📚 All topics](README.md) · [Next: 10. 🔌 Networking & Content Delivery ➡️](10-networking-content-delivery.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

A mobile application needs a fully managed, schemaless NoSQL database that delivers single-digit millisecond latency at any scale. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon Redshift</summary>

❌ **Incorrect.** Redshift is a relational, columnar data warehouse for analytics and needs a defined schema.

</details>

<details><summary>◯ <b>B.</b> Amazon DynamoDB</summary>

✅ **Correct.** DynamoDB is a serverless NoSQL key-value and document database in which items can have different attributes.

</details>

<details><summary>◯ <b>C.</b> Amazon RDS for MySQL</summary>

❌ **Incorrect.** RDS runs relational databases with fixed schemas, so it is not a schemaless NoSQL service.

</details>

<details><summary>◯ <b>D.</b> Amazon Neptune</summary>

❌ **Incorrect.** Neptune is a graph database for highly connected data.

</details>

📖 **Study:** [9.3 NoSQL: Amazon DynamoDB (Schemaless, Global Tables, DAX)](../README.md#93-nosql-amazon-dynamodb-schemaless-global-tables-dax)

---

### Question 2

A company wants to run ad hoc standard SQL queries directly on data stored in Amazon S3, paying only for the queries it runs, without loading the data into a database and without setting up a data warehouse or cluster. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon Athena</summary>

✅ **Correct.** Athena is a serverless interactive query service that analyzes data in S3 with standard SQL, and you pay per query.

</details>

<details><summary>◯ <b>B.</b> Amazon Redshift</summary>

❌ **Incorrect.** Redshift is a data warehouse. Redshift Spectrum can query data in S3, but you still need a Redshift cluster or workgroup. Athena needs no warehouse.

</details>

<details><summary>◯ <b>C.</b> AWS Glue</summary>

❌ **Incorrect.** Glue is a serverless ETL and data catalog service. It prepares data, but it is not the SQL query engine.

</details>

<details><summary>◯ <b>D.</b> Amazon EMR</summary>

❌ **Incorrect.** EMR runs big data frameworks such as Apache Spark and Hadoop, usually on clusters that you size and configure. It is not a simple pay-per-query SQL service.

</details>

📖 **Study:** [9.5 Analytics & Big Data: Redshift, Athena, Glue, EMR, QuickSight](../README.md#95-analytics--big-data-redshift-athena-glue-emr-quicksight)

---

### Question 3

Which Amazon RDS feature provides high availability by synchronously replicating data to a standby instance in another Availability Zone, with automatic failover?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Read replicas</summary>

❌ **Incorrect.** Read replicas use asynchronous replication to scale read-heavy workloads. They are not the high-availability mechanism.

</details>

<details><summary>◯ <b>B.</b> Manual DB snapshots</summary>

❌ **Incorrect.** Snapshots are backups. Restoring one takes time and is not an automatic failover.

</details>

<details><summary>◯ <b>C.</b> Amazon ElastiCache</summary>

❌ **Incorrect.** ElastiCache caches data in memory. It is not an RDS feature.

</details>

<details><summary>◯ <b>D.</b> Multi-AZ deployment</summary>

✅ **Correct.** In a Multi-AZ DB instance deployment, the standby is kept in sync and takes over automatically during a failure. It does not serve read traffic.

</details>

📖 **Study:** [9.2 Relational: Amazon RDS & Amazon Aurora (Multi-AZ vs. Read Replicas)](../README.md#92-relational-amazon-rds--amazon-aurora-multi-az-vs-read-replicas)

---

### Question 4

Which TWO statements about Amazon Aurora are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> It is a NoSQL key-value database</summary>

❌ **Incorrect.** Key-value NoSQL is Amazon DynamoDB. Aurora is relational.

</details>

<details><summary>☐ <b>B.</b> It stores all of its data in a single Availability Zone</summary>

❌ **Incorrect.** Aurora storage spans three AZs.

</details>

<details><summary>☐ <b>C.</b> It is compatible with MySQL and PostgreSQL</summary>

✅ **Correct.** Aurora is a cloud-native relational database that works with MySQL and PostgreSQL applications.

</details>

<details><summary>☐ <b>D.</b> It replicates six copies of data across three Availability Zones</summary>

✅ **Correct.** This replication gives Aurora high durability and availability.

</details>

<details><summary>☐ <b>E.</b> It is a petabyte-scale data warehouse</summary>

❌ **Incorrect.** That describes Amazon Redshift. Aurora is a transactional relational database.

</details>

📖 **Study:** [9.2 Relational: Amazon RDS & Amazon Aurora (Multi-AZ vs. Read Replicas)](../README.md#92-relational-amazon-rds--amazon-aurora-multi-az-vs-read-replicas)

---

### Question 5

A company wants a caching layer in front of its relational database to deliver sub-millisecond responses for frequently read data. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon DynamoDB Accelerator (DAX)</summary>

❌ **Incorrect.** DAX is an in-memory cache built specifically for DynamoDB tables, not for relational databases.

</details>

<details><summary>◯ <b>B.</b> Amazon Redshift</summary>

❌ **Incorrect.** Redshift is a data warehouse, not a cache.

</details>

<details><summary>◯ <b>C.</b> Amazon ElastiCache</summary>

✅ **Correct.** ElastiCache is a managed in-memory cache (Redis OSS, Valkey, or Memcached) that can sit in front of a relational database.

</details>

<details><summary>◯ <b>D.</b> Amazon Neptune</summary>

❌ **Incorrect.** Neptune is a graph database, not a cache.

</details>

📖 **Study:** [9.4 In-Memory Caching: Amazon ElastiCache & MemoryDB](../README.md#94-in-memory-caching-amazon-elasticache--memorydb)

---

[⬅️ Study guide: 9. 📊 Database & Analytics Services](../README.md#9--database--analytics-services) · [📚 All topics](README.md) · [Next: 10. 🔌 Networking & Content Delivery ➡️](10-networking-content-delivery.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
