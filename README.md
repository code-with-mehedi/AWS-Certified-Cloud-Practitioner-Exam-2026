# ☁️ AWS Certified Cloud Practitioner (CLF-C02) Complete Study Guide & Exam Notes

[![AWS Certified Cloud Practitioner](https://img.shields.io/badge/AWS-Certified%20Cloud%20Practitioner-FF9900?logo=amazon-aws&logoColor=white&style=for-the-badge)](https://aws.amazon.com/certification/certified-cloud-practitioner/)
[![Exam Code](https://img.shields.io/badge/Exam%20Code-CLF--C02-232F3E?style=for-the-badge&logo=amazon-aws)](https://aws.amazon.com/certification/certified-cloud-practitioner/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](https://github.com/)

A comprehensive, structured, and exam-focused revision guide for the **AWS Certified Cloud Practitioner (CLF-C02)** exam. This repository covers all exam domains, core concepts, AWS services, architectural principles, security models, billing mechanisms, **real exam question patterns, distractor trap analysis**, and high-yield comparison cheat sheets with direct video lecture timestamps from the renowned [freeCodeCamp 13+ Hour Full Course](https://www.youtube.com/watch?v=7HKot-brXFE).

> [!TIP]
> Free CLF-C02 mock tests are at [heymehedi.im/aws-cloud-practitioner](https://heymehedi.im/aws-cloud-practitioner). Every question has an explanation, and the full simulation is timed.
>
> This repository also has 5 practice questions for each topic in [practice-questions/](practice-questions/README.md). Click an option to see whether it is right or wrong.

---

## 🎯 Exam Overview & Blueprint

| Feature | Details |
| :--- | :--- |
| **Exam Code** | **CLF-C02** (Current Version) |
| **Duration** | 90 minutes (~1.3 minutes per question) |
| **Number of Questions** | 65 questions (Multiple choice or multiple response) |
| **Scoring Scale** | 100 – 1,000 |
| **Passing Score** | **700 / 1000** (~70%) |
| **Prerequisites** | None. Designed for candidates from technical and non-technical backgrounds |
| **Unscored Questions** | 15 unscored evaluation questions randomly distributed (50 scored questions) |

### Domain Weightings

```mermaid
pie title CLF-C02 Exam Domains Weighting
    "Domain 1: Cloud Concepts" : 24
    "Domain 2: Security and Compliance" : 30
    "Domain 3: Cloud Technology and Services" : 34
    "Domain 4: Billing, Pricing, and Support" : 12
```

---

## 🧠 Decoding the CLF-C02 Exam: Question Patterns & Trap Guide

> [!IMPORTANT]
> The AWS Certified Cloud Practitioner exam does not just test basic memorization — it tests **scenario pattern recognition** and deliberately includes tempting distractor choices. Understanding how questions are constructed is the key to passing with a high score.

### The 10 Most Common Exam Question Patterns

| Pattern # | Question Pattern Type | Example Exam Wording | How to Identify the Correct Answer | Typical Distractor / Trap |
| :---: | :--- | :--- | :--- | :--- |
| **1** | **Off-the-Shelf vs. Roll-Your-Own** | *"Which service provides a ready-made list of under-utilized EC2 instances without manual configuration?"* | Pick managed tools that provide automated recommendations out-of-the-box (**AWS Trusted Advisor**, **AWS Compute Optimizer**, or **Cost Explorer Rightsizing**). | **Amazon CloudWatch** (TRAP: CloudWatch only collects raw metrics; you must build alarms and dashboards yourself!). |
| **2** | **Reversed Wording Traps** | *"Which of the following is an advantage of the AWS Cloud?"* | Look for exact wording: **Trade Capital Expense for Variable Expense** (CapEx ➔ OpEx). | Distractors say *"Trade operational expense for capital expense"* or *"Trade variable expense for fixed expense"*. |
| **3** | **One-Word Responsibility Traps** | *"Under the Shared Responsibility Model, which is an AWS responsibility?"* | AWS is responsible for security **OF** the cloud. Customer is responsible for security **IN** the cloud. | Distractors say *"AWS is responsible for security IN the cloud"* or *"AWS is responsible for customer IAM policies"*. |
| **4** | **Timeline: Plan vs. Forecast vs. Alert** | *"A company wants to forecast future costs based on historical spending..."* vs. *"estimate costs before deploying..."* | - Forecast past spend ➔ **AWS Cost Explorer**<br/>- Estimate before building ➔ **AWS Pricing Calculator**<br/>- Set threshold alerts ➔ **AWS Budgets** | Mixing up Cost Explorer (historical + forecast) with Pricing Calculator (pre-launch modeling). |
| **5** | **App Code vs. Infrastructure** | *"Which service automates deploying application code to EC2 instances and on-premises servers?"* | - Application code deployment ➔ **AWS CodeDeploy**<br/>- Infrastructure provisioning ➔ **AWS CloudFormation**<br/>- Pipeline workflow ➔ **AWS CodePipeline** | Picking CloudFormation for application code rollout, or picking CodePipeline when only deployment is asked. |
| **6** | **APN Partner Paths** | *"A company needs an expert firm to design, migrate, and manage workloads on AWS..."* | - People/services to migrate & manage ➔ **Services Path (Consulting Partner)**<br/>- Commercial software/SaaS products ➔ **Software Path (Technology Partner)** | Picking Technology Partner for consulting services, or picking AWS Concierge (which is just enterprise billing support). |
| **7** | **Public vs. Personalized Health** | *"Which dashboard provides an RSS feed of all AWS service interruptions without logging in?"* | - Public status of all services in all regions ➔ **AWS Health Dashboard - Service Health**<br/>- Specific events affecting *your* active resources ➔ **AWS Health Dashboard - Your Account Health** | Picking "Your Account Health" for public RSS feeds, or picking Service Health when account-specific impact is asked. |
| **8** | **Default Encryption Nuances** | *"Which services have data encryption automatically enabled by default without user configuration?"* | - **Amazon S3** (SSE-S3 default on all new objects since Jan 2023)<br/>- **Amazon DynamoDB** (encrypted at rest by default)<br/>- **AWS Storage Gateway** (encrypted in-transit & at-rest) | Assuming Amazon EBS is encrypted by default (EBS is opt-in per volume unless the regional account setting is enabled!). |
| **9** | **Multi-Account & Multi-Region IaC** | *"Which feature provisions the same infrastructure across 40 accounts and 3 regions from one template?"* | **AWS CloudFormation StackSets** | Picking AWS Systems Manager (SSM manages OS nodes/patching, it does NOT provision infrastructure). |
| **10** | **Server Logs vs. Account API Logs** | *"Which service centralizes application and server logs from both EC2 and on-premises servers?"* | **Amazon CloudWatch Logs with the CloudWatch Agent** | Picking **AWS CloudTrail** (TRAP: CloudTrail records *AWS API calls*, not OS or application logs!). |

---

## 📑 Table of Contents

- [☁️ AWS Certified Cloud Practitioner (CLF-C02) Complete Study Guide & Exam Notes](#️-aws-certified-cloud-practitioner-clf-c02-complete-study-guide--exam-notes)
  - [🎯 Exam Overview & Blueprint](#-exam-overview--blueprint)
  - [🧠 Decoding the CLF-C02 Exam: Question Patterns & Trap Guide](#-decoding-the-clf-c02-exam-question-patterns--trap-guide)
  - [📑 Table of Contents](#-table-of-contents)
  - [1. 🚀 Introduction & Cloud Fundamentals](#1--introduction--cloud-fundamentals)
    - [1.1 Course Orientation & Exam Guide](#11-course-orientation--exam-guide)
    - [1.2 What is Cloud Computing?](#12-what-is-cloud-computing)
    - [1.3 The 6 Advantages of Cloud Computing](#13-the-6-advantages-of-cloud-computing)
    - [1.4 Types of Cloud Computing (Cloud Service Models)](#14-types-of-cloud-computing-cloud-service-models)
    - [1.5 Cloud Deployment Models](#15-cloud-deployment-models)
    - [1.6 Evolution of Hosting & Digital Transformation](#16-evolution-of-hosting--digital-transformation)
    - [1.7 AWS Cloud Adoption Framework (AWS CAF)](#17-aws-cloud-adoption-framework-aws-caf)
    - [1.8 Cloud Migration Strategies: The 7 Rs & Migration Tools](#18-cloud-migration-strategies-the-7-rs--migration-tools)
  - [2. 🛡️ Getting Started & Account Security Baseline](#2-️-getting-started--account-security-baseline)
    - [2.1 AWS Account Creation & Root User Rules](#21-aws-account-creation--root-user-rules)
    - [2.2 AWS Free Tier Types](#22-aws-free-tier-types)
    - [2.3 Budgets & Zero-Spend Billing Alarms](#23-budgets--zero-spend-billing-alarms)
  - [3. 🌐 AWS Global Infrastructure](#3--aws-global-infrastructure)
    - [3.1 AWS Regions & Availability Zones (AZs)](#31-aws-regions--availability-zones-azs)
    - [3.2 Edge Locations & Points of Presence (PoP)](#32-edge-locations--points-of-presence-pop)
    - [3.3 Edge & Hybrid Infrastructure Solutions](#33-edge--hybrid-infrastructure-solutions)
    - [3.4 Regional vs. Global AWS Services](#34-regional-vs-global-aws-services)
    - [3.5 Specialized AWS Regions & Sovereignty](#35-specialized-aws-regions--sovereignty)
  - [4. 📐 Cloud Architecture & Reliability](#4--cloud-architecture--reliability)
    - [4.1 Core Architecture Terminologies](#41-core-architecture-terminologies)
    - [4.2 Disaster Recovery (DR) Strategies & RTO / RPO](#42-disaster-recovery-dr-strategies--rto--rpo)
    - [4.3 High Availability Architecture Design](#43-high-availability-architecture-design)
  - [5. 🧰 Management, Governance & Developer Tools](#5--management-governance--developer-tools)
    - [5.1 Ways to Interact with AWS (Console, CLI, SDK, CloudShell)](#51-ways-to-interact-with-aws-console-cli-sdk-cloudshell)
    - [5.2 Amazon Resource Names (ARN)](#52-amazon-resource-names-arn)
    - [5.3 Infrastructure as Code (IaC): CloudFormation & StackSets & CDK](#53-infrastructure-as-code-iac-cloudformation--stacksets--cdk)
    - [5.4 Developer Tools & Access Credentials](#54-developer-tools--access-credentials)
    - [5.5 AWS Systems Manager (SSM)](#55-aws-systems-manager-ssm)
  - [6. 🤝 AWS Shared Responsibility Model](#6--aws-shared-responsibility-model)
    - [6.1 The Core Model: "OF" vs. "IN" the Cloud](#61-the-core-model-of-vs-in-the-cloud)
    - [6.2 Shared Responsibility Across Service Models](#62-shared-responsibility-across-service-models)
    - [6.3 Shared Controls Matrix](#63-shared-controls-matrix)
  - [7. 💻 Compute Services](#7--compute-services)
    - [7.1 Amazon Elastic Compute Cloud (EC2) Overview & Families](#71-amazon-elastic-compute-cloud-ec2-overview--families)
    - [7.2 EC2 Tenancy: Shared vs. Dedicated Instances vs. Dedicated Hosts](#72-ec2-tenancy-shared-vs-dedicated-instances-vs-dedicated-hosts)
    - [7.3 EC2 Pricing Models Matrix & Rules](#73-ec2-pricing-models-matrix--rules)
    - [7.4 Scaling & Load Balancing: ASG, ALB, NLB, GWLB](#74-scaling--load-balancing-asg-alb-nlb-gwlb)
    - [7.5 Containers on AWS: ECS, EKS, Fargate, ECR](#75-containers-on-aws-ecs-eks-fargate-ecr)
    - [7.6 Serverless Compute: AWS Lambda](#76-serverless-compute-aws-lambda)
    - [7.7 Lightsail, Batch, App Runner & HPC](#77-lightsail-batch-app-runner--hpc)
  - [8. 🗄️ Storage Services](#8-️-storage-services)
    - [8.1 Storage Types Comparison (Block vs. File vs. Object)](#81-storage-types-comparison-block-vs-file-vs-object)
    - [8.2 Amazon S3 Storage Classes & Lifecycle Management](#82-amazon-s3-storage-classes--lifecycle-management)
    - [8.3 Amazon EBS vs. EC2 Instance Store](#83-amazon-ebs-vs-ec2-instance-store)
    - [8.4 Amazon EFS vs. Amazon FSx](#84-amazon-efs-vs-amazon-fsx)
    - [8.5 AWS Snow Family & Hybrid Storage Gateway](#85-aws-snow-family--hybrid-storage-gateway)
  - [9. 📊 Database & Analytics Services](#9--database--analytics-services)
    - [9.1 Database Types: Relational vs. NoSQL vs. In-Memory vs. Warehouse](#91-database-types-relational-vs-nosql-vs-in-memory-vs-warehouse)
    - [9.2 Relational: Amazon RDS & Amazon Aurora (Multi-AZ vs. Read Replicas)](#92-relational-amazon-rds--amazon-aurora-multi-az-vs-read-replicas)
    - [9.3 NoSQL: Amazon DynamoDB (Schemaless, Global Tables, DAX)](#93-nosql-amazon-dynamodb-schemaless-global-tables-dax)
    - [9.4 In-Memory Caching: Amazon ElastiCache & MemoryDB](#94-in-memory-caching-amazon-elasticache--memorydb)
    - [9.5 Analytics & Big Data: Redshift, Athena, Glue, EMR, QuickSight](#95-analytics--big-data-redshift-athena-glue-emr-quicksight)
  - [10. 🔌 Networking & Content Delivery](#10--networking--content-delivery)
    - [10.1 Amazon Virtual Private Cloud (VPC), Subnets & Gateways](#101-amazon-virtual-private-cloud-vpc-subnets--gateways)
    - [10.2 Security Groups vs. Network ACLs (NACLs)](#102-security-groups-vs-network-acls-nacls)
    - [10.3 Hybrid Connectivity: Direct Connect, VPN & Transit Gateway](#103-hybrid-connectivity-direct-connect-vpn--transit-gateway)
    - [10.4 VPC Endpoints (Gateway vs. Interface / PrivateLink)](#104-vpc-endpoints-gateway-vs-interface--privatelink)
    - [10.5 Content Delivery & DNS: CloudFront & Route 53](#105-content-delivery--dns-cloudfront--route-53)
  - [11. 🔐 Security, Identity & Compliance](#11--security-identity--compliance)
    - [11.1 AWS Identity and Access Management (IAM) Entities & PoLP](#111-aws-identity-and-access-management-iam-entities--polp)
    - [11.2 AWS IAM Identity Center, Cognito & Directory Service](#112-aws-iam-identity-center-cognito--directory-service)
    - [11.3 Encryption & Secrets Management: KMS, CloudHSM, Secrets Manager, Parameter Store](#113-encryption--secrets-management-kms-cloudhsm-secrets-manager-parameter-store)
    - [11.4 Threat Detection & Boundary Security (Shield, WAF, GuardDuty, Inspector)](#114-threat-detection--boundary-security-shield-waf-guardduty-inspector)
    - [11.5 Governance & Compliance: AWS Artifact, Audit Manager, Macie, Security Hub](#115-governance--compliance-aws-artifact-audit-manager-macie-security-hub)
  - [12. 🔄 Application Integration & Messaging](#12--application-integration--messaging)
    - [12.1 SQS vs. SNS vs. EventBridge vs. Kinesis](#121-sqs-vs-sns-vs-eventbridge-vs-kinesis)
    - [12.2 Orchestration & CI/CD: Step Functions, API Gateway, CodeDeploy, CodePipeline](#122-orchestration--cicd-step-functions-api-gateway-codedeploy-codepipeline)
  - [13. 📋 Cloud Governance, Management & Monitoring](#13--cloud-governance-management--monitoring)
    - [13.1 AWS Organizations & Service Control Policies (SCPs)](#131-aws-organizations--service-control-policies-scps)
    - [13.2 AWS Config vs. AWS Control Tower](#132-aws-config-vs-aws-control-tower)
    - [13.3 Observability: Amazon CloudWatch vs. AWS CloudTrail](#133-observability-amazon-cloudwatch-vs-aws-cloudtrail)
  - [14. 🤖 Machine Learning, AI & High-Performance Compute](#14--machine-learning-ai--high-performance-compute)
    - [14.1 Generative AI & Turnkey AI Services (Bedrock, SageMaker, Q, etc.)](#141-generative-ai--turnkey-ai-services-bedrock-sagemaker-q-etc)
    - [14.2 Custom AI Silicon: Trainium, Inferentia, Graviton](#142-custom-ai-silicon-trainium-inferentia-graviton)
  - [15. 🏛️ AWS Well-Architected Framework](#15-️-aws-well-architected-framework)
    - [15.1 The 6 Pillars & Their Core Design Principles](#151-the-6-pillars--their-core-design-principles)
    - [15.2 AWS Well-Architected Tool](#152-aws-well-architected-tool)
  - [16. 💰 Billing, Pricing & Support Plans](#16--billing-pricing--support-plans)
    - [16.1 Cloud Economics: CapEx vs. OpEx & What is FREE in AWS](#161-cloud-economics-capex-vs-opex--what-is-free-in-aws)
    - [16.2 Cost Tools: Pricing Calculator vs. Cost Explorer vs. Budgets vs. CUR](#162-cost-tools-pricing-calculator-vs-cost-explorer-vs-budgets-vs-cur)
    - [16.3 AWS Support Plans Comparison (Detailed Matrix)](#163-aws-support-plans-comparison-detailed-matrix)
    - [16.4 AWS Trusted Advisor & Health Dashboard](#164-aws-trusted-advisor--health-dashboard)
    - [16.5 Partner Network (APN), Marketplace & Startup Programs](#165-partner-network-apn-marketplace--startup-programs)
  - [17. 🆚 High-Yield Exam "Cheat Sheet" & Service Disambiguation](#17--high-yield-exam-cheat-sheet--service-disambiguation)
    - [17.1 Commonly Confused Services Cheat Sheet](#171-commonly-confused-services-cheat-sheet)
    - [17.2 Essential Acronyms & Initialisms Reference](#172-essential-acronyms--initialisms-reference)
  - [18. 🎓 Exam Strategy & Last-Minute Checklist](#18--exam-strategy--last-minute-checklist)
  - [📝 Practice Questions (5 per topic)](practice-questions/README.md)

---

## 1. 🚀 Introduction & Cloud Fundamentals

### 1.1 Course Orientation & Exam Guide
- 🎥 **Video Sections**:
  - [1:07 - Introduction](https://www.youtube.com/watch?v=7HKot-brXFE&t=67s)
  - [1:07 - Is Certified Cloud Practitioner right for me?](https://www.youtube.com/watch?v=7HKot-brXFE&t=67s)
  - [6:10 - Exam Guide - Content Outline](https://www.youtube.com/watch?v=7HKot-brXFE&t=370s)

#### Detailed notes

The **AWS Certified Cloud Practitioner (CLF-C02)** exam tests broad knowledge of the AWS Cloud, independent of any job role. The target candidate has up to six months of exposure to AWS and may work alongside cloud teams in roles such as sales, marketing, or project management. The exam guide lists coding, designing cloud architecture, troubleshooting, implementation, and load and performance testing as job tasks that are out of scope.

The exam has 65 questions and lasts 90 minutes. Fifty questions count toward your score. The other fifteen are unscored items that AWS is trying out, and the exam does not identify them. Each question is **multiple choice** (one correct answer and three distractors) or **multiple response** (two or more correct answers out of five or more options). A wrong answer carries no penalty and an unanswered question counts as wrong, so answer every question.

AWS reports a scaled score from 100 to 1,000, and 700 is the minimum passing score. Scaling puts exam forms of slightly different difficulty on one scale. The scoring is **compensatory**, so you pass or fail on the whole exam and a strong domain can offset a weak one. You take the exam at a Pearson VUE testing center or online with a proctor, and the certification is valid for three years.

> [!NOTE]
> Update (2026): The exam guide is also published as web pages with a revision history ([exam guide](https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html)), and AWS releases each change about a month before it appears on the exam. The German and Italian versions of the exam retire after December 31, 2026 ([exam page](https://aws.amazon.com/certification/certified-cloud-practitioner/)).

#### In practice

Domains 2 and 3 hold 64 percent of the scored content, which is about 32 of the 50 scored questions, so they deserve the most study time. The counts in the table are approximate because AWS publishes percentages of scored content and no question counts.

| Domain | Weight | About how many of the 50 scored questions | Task statements in plain words |
| :--- | :---: | :---: | :--- |
| 1. Cloud Concepts | 24% | 12 | Benefits of the AWS Cloud, Well-Architected design principles, migration strategies and the CAF, cloud economics |
| 2. Security and Compliance | 30% | 15 | Shared responsibility, security and compliance concepts, access management, security components and resources |
| 3. Cloud Technology and Services | 34% | 17 | Deployment methods, global infrastructure, compute, databases, networking, storage, AI/ML and analytics, other service categories |
| 4. Billing, Pricing, and Support | 12% | 6 | Pricing models, billing and cost tools, support plans and technical resources |

The exam allows about 83 seconds per question (90 minutes for 65 questions). A first pass at 60 seconds per question takes 65 minutes and leaves 25 minutes for review. The exam screen has a Flag for Review button, and a review screen after the last question lists all, incomplete, or flagged questions. Flag the questions you are unsure about, fill in an answer for every unanswered one, and select End Review when you are done.

---

### 1.2 What is Cloud Computing?
- 🎥 **Video Sections**:
  - [8:51 - What is Cloud Computing?](https://www.youtube.com/watch?v=7HKot-brXFE&t=531s)
  - [14:03 - What is AWS?](https://www.youtube.com/watch?v=7HKot-brXFE&t=843s)
  - [29:47 - AWS Technology Overview](https://www.youtube.com/watch?v=7HKot-brXFE&t=1787s)

#### Detailed notes

**Cloud computing** is the on-demand delivery of IT resources over the internet with pay-as-you-go pricing, which is how AWS defines it. NIST defines it as a model for on-demand network access to a shared pool of configurable computing resources that can be provisioned and released quickly with little management effort. NIST names five characteristics: on-demand self-service, broad network access, resource pooling, rapid elasticity, and measured service.

**AWS** is Amazon's cloud platform. It began offering infrastructure services in 2006 with Amazon S3 for storage and Amazon EC2 for virtual servers. Instead of buying servers and building a data center, you use AWS services such as compute, storage, databases, networking, analytics, and machine learning. You reach them through the AWS Management Console, the AWS CLI, the SDKs, or the API. AWS builds and runs the data centers and hardware behind the services, and you choose the services and configure them.

> [!NOTE]
> Update (2026): The wording in the NIST note in this topic, "on-demand delivery of IT resources over the internet with pay-as-you-go pricing", is AWS's own definition ([What is cloud computing?](https://aws.amazon.com/what-is-cloud-computing/)). The NIST definition is the one in SP 800-145 ([NIST](https://csrc.nist.gov/pubs/sp/800/145/final)).

#### In practice

The first call below needs no ticket or purchase order, which is on-demand self-service, and it reaches AWS over the network like any API request (broad network access). AWS pools its hardware across customers and keeps each customer's resources isolated, so by default you do not choose the physical host (resource pooling). Raising `--count` from 3 to 30 is the same request with a bigger number, and the capacity arrives in minutes (rapid elasticity), up to your account's service quotas. AWS meters the time the instances run and bills for it (measured service). Terminating the instances returns the capacity to the pool.

```bash
# Request three small servers
aws ec2 run-instances --image-id AMI_ID --instance-type t3.micro --count 3 --region us-east-1

# List what is running
aws ec2 describe-instances --region us-east-1 --filters Name=instance-state-name,Values=running --query "Reservations[].Instances[].InstanceId" --output text

# Release the capacity when the work is done
aws ec2 terminate-instances --region us-east-1 --instance-ids INSTANCE_ID_1 INSTANCE_ID_2 INSTANCE_ID_3
```

> [!NOTE]
> **NIST Cloud Computing Definition**: The **on-demand delivery of IT resources** (compute, storage, databases, networking, software) over the internet with **pay-as-you-go pricing**.

#### Key Characteristics:
1. **On-Demand Self-Service**: Provision resources automatically without human interaction with AWS.
2. **Broad Network Access**: Services accessible over the network from anywhere via browser, CLI, or API.
3. **Resource Pooling**: Multi-tenant infrastructure pooled to serve many customers securely.
4. **Rapid Elasticity**: Resources scale outward and inward dynamically to match demand.
5. **Measured Service**: Pay strictly for what is consumed with transparent monitoring.

---

### 1.3 The 6 Advantages of Cloud Computing
- 🎥 **Video Sections**:
  - [1:23:23 - The Benefits of the Cloud](https://www.youtube.com/watch?v=7HKot-brXFE&t=5003s)
  - [1:25:16 - The Seven Advantages of the Cloud](https://www.youtube.com/watch?v=7HKot-brXFE&t=5116s)

#### Detailed notes

The **six advantages of cloud computing** are the benefits AWS lists for running IT in the cloud instead of in your own data center. Three concern cost: you trade fixed expense for variable expense, benefit from massive economies of scale, and stop spending money running and maintaining data centers. Two concern capacity and time: you stop guessing capacity, and you increase speed and agility. The sixth, go global in minutes, concerns reach.

Fixed expense, also called capital expense (CapEx), is money you commit before you know how much you will use, such as servers and data center space. Variable expense, the pay-as-you-go operating expense (OpEx), is paid only when you use computing resources and only for how much you use. Economies of scale come from AWS aggregating the usage of many customers, so AWS can charge lower pay-as-you-go prices than one company could get alone. Capacity scales up and down with a few minutes' notice, so you no longer size hardware for a peak that may never come. New resources are a click away, which cuts the time to give developers resources from weeks to minutes. With no data centers to run, staff work on projects that differentiate the business instead of racking and powering servers. Going global means deploying in several AWS Regions with a few clicks, which gives users in each area lower latency.

> [!NOTE]
> Update (2026): AWS's Overview of Amazon Web Services whitepaper currently words the first advantage "Trade fixed expense for variable expense" and the fifth "Stop spending money running and maintaining data centers" ([whitepaper](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)). The table in this topic says "capital expense" and uses a shorter fifth title. The exam guide's cloud economics task also compares fixed costs with variable costs ([exam guide](https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html)).

#### In practice

A seasonal shop shows fixed versus variable expense and capacity planning in numbers. The figures are an example, with one price per server-month for both options. The shop needs 2 servers from January to October and 10 servers in November and December.

| | On-premises, bought for the peak | Cloud, pay as you go |
| :--- | :---: | :---: |
| Servers available, January to October | 10 | 2 |
| Servers available, November and December | 10 | 10 |
| Server-months paid for in the year | 120 | 40 |
| Server-months sitting idle | 80 | 0 |

The on-premises shop commits to 10 servers for 12 months and pays for 120 server-months, 80 of them idle. The cloud shop pays for the 40 server-months it uses, which is variable expense, and it did not have to commit to the peak in advance. The cloud column assumes capacity follows demand exactly. If the holiday peak needs 15 servers instead of 10, the cloud shop adds 5 within minutes, while the on-premises shop waits for hardware to be ordered, delivered, and installed.

> [!IMPORTANT]
> **Must-Know Exam Trap**: Exam questions frequently reverse terms or swap single words!

| Advantage | Concept | Business Benefit | ⚠️ Exam Trap to Watch Out For |
| :--- | :--- | :--- | :--- |
| **1. Trade Capital Expense for Variable Expense** | Replace upfront hardware investment (**CapEx**) with pay-as-you-go operating expenses (**OpEx**). | Pay only for what you consume; zero upfront hardware depreciation. | **Trap**: Distractors say *"Trade operational expense for capital expense"* (REVERSED) or *"Trade variable expense for fixed expense"*. |
| **2. Benefit from Massive Economies of Scale** | Aggregated usage across hundreds of thousands of customers enables AWS to achieve lower costs. | AWS passes bulk purchase savings directly as lower pay-as-you-go prices. | **Trap**: Questions mentioning *"lower prices due to aggregated usage from many customers"* point to **Economies of Scale**, NOT "Go global in minutes". |
| **3. Stop Guessing Capacity** | Eliminate guesswork about peak server sizing. | Resources scale up or down automatically; no idle servers or under-provisioned crashes. | **Trap**: Do not confuse with "Elasticity" when the question asks about *financial/capacity planning benefit*. |
| **4. Increase Speed and Agility** | IT resources are accessible in a single click or API call. | Reduces time to make resources available to developers from **weeks to minutes**. | **Trap**: When a question highlights *"developers provisioning test environments in minutes"*, the answer is **Speed and Agility**. |
| **5. Stop Spending Money Running Data Centers** | Offload physical data center maintenance (power, cooling, cabling, racking). | Focus staff on business differentiators (apps, customers) instead of "undifferentiated heavy lifting". | **Trap**: Does not eliminate application code maintenance or customer security duties! |
| **6. Go Global in Minutes** | Deploy applications in multiple AWS Regions worldwide in a few clicks. | Delivers lower latency and a superior user experience worldwide. | **Trap**: "Go global in minutes" refers to **multi-region geographical deployment**, NOT economies of scale! |

---

### 1.4 Types of Cloud Computing (Cloud Service Models)
- 🎥 **Video Sections**:
  - [37:28 - Types of Cloud Computing](https://www.youtube.com/watch?v=7HKot-brXFE&t=2248s)

#### Detailed notes

A **cloud service model** describes how much of the technology stack the provider runs for you. AWS names three: **Infrastructure as a Service (IaaS)**, **Platform as a Service (PaaS)**, and **Software as a Service (SaaS)**. IaaS contains the basic building blocks of cloud IT: networking, computers (virtual or on dedicated hardware), and data storage. PaaS removes the need to manage the underlying infrastructure, so you focus on deploying and managing your applications. SaaS is a complete product that the provider runs and manages.

Each step from IaaS to SaaS moves more of the work, and some of the control, from you to the provider:

| Model | What you get | What you take on | AWS example |
| :--- | :--- | :--- | :--- |
| IaaS | The highest level of flexibility and control over networking, compute, and storage | The operating system, patching, runtime, application, and data | Amazon EC2 |
| PaaS | A ready platform where you deploy code and the provider runs the servers | Your application code, its data, and its configuration | AWS Elastic Beanstalk |
| SaaS | A finished application used over the web | User accounts, settings, and the content you put in | Amazon Connect |

Hybrid, private, and public describe where infrastructure runs. They are deployment models and answer a different question from the service model.

> [!NOTE]
> Update (2026): Amazon QuickSight, one of the SaaS examples in this topic, is now Amazon Quick Sight, a feature of Amazon Quick. Existing QuickSight APIs keep working ([What is Amazon Quick](https://docs.aws.amazon.com/quicksight/latest/user/welcome.html)).

#### In practice

Choose the model that matches how much of the stack your team wants to run. If you need a specific operating system or a custom software stack, choose IaaS and accept the patching and scaling work. If you have application code and want AWS to run the servers, choose PaaS: AWS Elastic Beanstalk takes source code, a Dockerfile, or a container image, provisions the servers, and configures load balancing, health monitoring, and auto scaling for it. For a working application with no code to write, buy SaaS. Software that you install on EC2 and run yourself is IaaS, even when users reach it through a browser, because SaaS means the vendor runs the application.

| Need | Model | AWS example |
| :--- | :--- | :--- |
| Run a legacy application that needs an older operating system version | IaaS | Amazon EC2 |
| Deploy a Python web application without managing servers or load balancers | PaaS | AWS Elastic Beanstalk |
| Give a support team a contact center without hosting any software | SaaS | Amazon Connect |

```mermaid
graph TD
    subgraph IaaS ["Infrastructure as a Service (IaaS)"]
        A1[Customer controls: OS, Middleware, Runtime, Apps, Data]
        A2[AWS controls: Physical Hardware, Datacenter, Hypervisor]
        A3[Example: Amazon EC2, EBS, VPC]
    end
    subgraph PaaS ["Platform as a Service (PaaS)"]
        B1[Customer controls: Application Code, Data]
        B2[AWS controls: OS, Hardware, Patches, Runtime Maintenance]
        B3[Example: AWS Elastic Beanstalk, Amazon RDS]
    end
    subgraph SaaS ["Software as a Service (SaaS)"]
        C1[Customer controls: Application Settings, End-user Data]
        C2[AWS controls: Everything under the hood]
        C3[Example: AWS QuickSight, WorkSpaces, Microsoft 365]
    end
```

- **IaaS**: Highest customer control over OS and networking. Example: **Amazon EC2**.
- **PaaS**: Customer uploads code/data; AWS manages OS, runtime, and patching. Example: **AWS Elastic Beanstalk**, **Amazon RDS**.
- **SaaS**: Complete software application delivered over the web; customer only manages user accounts and data. Example: **Amazon QuickSight**, **Amazon Connect**.

---

### 1.5 Cloud Deployment Models
- 🎥 **Video Sections**:
  - [39:16 - Cloud Computing Deployment Models](https://www.youtube.com/watch?v=7HKot-brXFE&t=2356s)

#### Detailed notes

A **cloud deployment model** describes where an application's infrastructure runs. AWS names three: cloud, on-premises (also called private cloud), and hybrid, and the exam guide's examples are the same three. What other sources call the public cloud is the cloud model in AWS's wording: every part of the application runs in the cloud, whether it was built there or migrated.

An on-premises deployment uses virtualization and resource management tools in your own facility. It provides dedicated resources but few of the benefits of cloud computing, and AWS describes it as mostly the same as legacy IT infrastructure. A **hybrid** deployment connects cloud resources with existing resources outside the cloud, most often your own data center, so that you can extend your infrastructure into the cloud. AWS Direct Connect and AWS Site-to-Site VPN provide the network link, AWS Outposts brings AWS infrastructure into your own site in a 42U rack or a 1U or 2U server, and AWS Storage Gateway connects on-premises applications to cloud storage. Multi-cloud means using more than one cloud provider, for example AWS together with Azure or Google Cloud.

| Model | Where the workload runs | Hardware owned by | Usual reason to choose it |
| :--- | :--- | :--- | :--- |
| Cloud | Fully in the cloud, for example on AWS | The provider | Cloud benefits from the start, or after a migration |
| On-premises (private cloud) | Your own data center | You | Dedicated resources |
| Hybrid | Split between your data center and the cloud | Both | Latency, data processing, or data residency needs |
| Multi-cloud | Two or more cloud providers | The providers | Avoiding dependence on one vendor |

#### In practice

A hybrid setup needs a network link between your data center and a VPC. A Site-to-Site VPN connection gives you two encrypted tunnels over the internet, between your customer gateway device and a virtual private gateway or transit gateway on the AWS side. AWS Direct Connect runs a fiber cable from your router to a Direct Connect location and bypasses internet service providers on the path. Plan the address ranges first: AWS recommends non-overlapping CIDR blocks when VPCs connect to a common on-premises network. In a typical layout the database stays on site and the web tier runs on AWS.

```text
Your data center                                AWS Region us-east-1
LAN 192.168.10.0/24                             VPC 10.0.0.0/16

+------------------------+                      +----------------------+
| Database, kept on site |                      | Web servers (EC2)    |
|                        |                      |                      |
| Customer gateway       |==== Site-to-Site ====| Virtual private      |
| device 203.0.113.12    |     VPN (internet)   | gateway              |
|                        |                      |                      |
| Router                 |==== Direct Connect ==|                      |
|                        |     (fiber)          |                      |
+------------------------+                      +----------------------+
```

1. **Public Cloud**: All application components run entirely in AWS infrastructure (cloud-native).
2. **Private Cloud (On-Premises)**: Infrastructure dedicated to a single company in their private data center (OpenStack, VMware).
3. **Hybrid Cloud**: Connects on-premises resources with AWS cloud infrastructure using **AWS Direct Connect**, **AWS Site-to-Site VPN**, **AWS Outposts**, or **AWS Storage Gateway**.
4. **Multi-Cloud**: Using AWS alongside another cloud provider (e.g., Azure or Google Cloud) to prevent vendor lock-in.

---

### 1.6 Evolution of Hosting & Digital Transformation
- 🎥 **Video Sections**:
  - [9:35 - Evolution of Cloud Hosting](https://www.youtube.com/watch?v=7HKot-brXFE&t=575s)
  - [32:18 - Evolution of Computing](https://www.youtube.com/watch?v=7HKot-brXFE&t=1938s)
  - [1:14:09 - Digital Transformation & Innovation Waves](https://www.youtube.com/watch?v=7HKot-brXFE&t=4449s)
  - [1:16:02 - Digital Transformation Checklist](https://www.youtube.com/watch?v=7HKot-brXFE&t=4562s)
  - [1:18:11 - Evolution of Computing Power](https://www.youtube.com/watch?v=7HKot-brXFE&t=4691s)

#### Detailed notes

**Hosting** is where and how an organization's applications run. Before cloud computing, organizations hosted applications on physical servers that they bought for on-premises data centers, or they hired physical or virtual servers from an off-site hosting provider. Cloud hosting adds another arrangement: you run applications on capacity rented on demand.

| Hosting model | What it is | Capacity and cost |
| :--- | :--- | :--- |
| On-premises data center | Physical servers you buy and keep in your own facility | New hardware and its infrastructure are a high upfront cost, and new capacity waits for setup |
| Dedicated hosting | One physical server rented for your exclusive use | High cost, and extra capacity means adding servers manually |
| Shared hosting | Many customers or websites on one server with one operating system | Resources are shared with the other customers on the server |
| VPS hosting | Many virtualized servers on one physical server | Typically a fixed amount of resources per virtual server |
| Cloud hosting | Applications run in the cloud on capacity rented on demand | Capacity on demand, with a range of architecture models |

**Digital transformation** is the process an organization applies to integrate and grow digital technologies in all areas of the business. Cloud computing supports it because new resources are a click away, so trying an idea costs less time and money. AWS began offering on-demand infrastructure services in 2006, with Amazon S3 in March and Amazon EC2 a few months later. The AWS Cloud Adoption Framework describes four transformation domains in a chain: technology transformation enables process transformation, which enables organizational transformation, which enables product transformation.

#### In practice

To place an initiative in a domain, ask what it changes: servers and data platforms, business operations, how teams are organized, or what the company sells. A hosting decision, such as moving from an on-premises data center to AWS, belongs to the technology domain and enables the process, organization, and product changes that follow. The retailer in the table is an invented example.

| Domain | Focus in the CAF | Example at the retailer |
| :--- | :--- | :--- |
| Technology | Migrate and modernize infrastructure, applications, and data and analytics platforms | Moves the web store and its database from its own servers to AWS |
| Process | Digitize, automate, and optimize business operations | Reorders stock automatically from sales data held in one analytics platform |
| Organization | Reimagine the operating model, with teams organized around products and value streams | Replaces separate IT and marketing queues with small teams that own store features end to end |
| Product | Reimagine the business model with new value propositions and revenue models | Launches a subscription service that the old systems could not bill |

---

### 1.7 AWS Cloud Adoption Framework (AWS CAF)
- 🎥 **Video Sections**:
  - [9:36:47 - Cloud Adoption Framework](https://www.youtube.com/watch?v=7HKot-brXFE&t=34607s)
  - [9:39:17 - Cloud Adoption Framework - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=34757s)

#### Detailed notes

The **AWS Cloud Adoption Framework (AWS CAF)** is AWS's guidance for planning and carrying out a move to the cloud. It groups the capabilities an organization needs into six **perspectives** and recommends four iterative phases of transformation. AWS says to use it to identify and prioritize transformation opportunities, evaluate and improve cloud readiness, and evolve a transformation roadmap over time. Its four business outcomes are reduced business risk, improved ESG performance, increased revenue, and increased operational efficiency.

Each perspective holds capabilities that a group of related stakeholders owns:

| Perspective | Common stakeholders | Example capabilities |
| :--- | :--- | :--- |
| Business | CEO, CFO, COO, CIO, CTO | Strategy management, portfolio management, innovation management, data monetization |
| People | CIO, COO, CTO, cloud director | Culture evolution, cloud fluency, workforce transformation, change acceleration |
| Governance | Chief transformation officer, CIO, CTO, CFO, CDO, CRO | Program and project management, benefits management, risk management, cloud financial management, data governance |
| Platform | CTO, technology leaders, architects, engineers | Platform architecture, data engineering, modern application development, CI/CD |
| Security | CISO, CCO, internal audit leaders, security engineers | Identity and access management, threat detection, vulnerability management, incident response |
| Operations | Infrastructure and operations leaders, site reliability engineers, IT service managers | Observability, event management, incident and problem management, patch management |

The four phases are iterative and incremental:

1. Envision: show how the cloud will accelerate business outcomes by identifying and prioritizing opportunities across the four transformation domains (technology, process, organization, product).
2. Align: identify capability gaps across the six perspectives, along with cross-organizational dependencies.
3. Launch: deliver pilot initiatives in production and demonstrate incremental business value.
4. Scale: expand the pilots to the desired scale and sustain the business benefits.

> [!NOTE]
> Update (2026): In the CAF 3.0 whitepaper, cloud financial management and benefits management are Governance capabilities. The Business perspective holds strategy management, portfolio management, innovation management, product management, strategic partnership, data monetization, business insights, and data science ([AWS CAF overview](https://docs.aws.amazon.com/whitepapers/latest/overview-aws-cloud-adoption-framework/business-perspective.html)).

#### In practice

AWS describes the Align phase as identifying capability gaps across the six perspectives and creating strategies to improve cloud readiness. It also says you may not need to tackle all the foundational capabilities at once, and you can build them up as the transformation progresses.

| The team asks | Perspective | Capability |
| :--- | :--- | :--- |
| Which cloud initiatives get priority? | Business | Portfolio management |
| How do we train staff on AWS? | People | Cloud fluency |
| Who checks that the promised benefits arrive? | Governance | Benefits management |
| How do new teams get compliant AWS accounts? | Platform | Platform engineering |
| Who responds to a security incident? | Security | Incident response |
| Who restores service when an application is down? | Operations | Incident and problem management |

Some names are easy to mix up. Security is both a CAF perspective and a Well-Architected pillar, and Operations (a perspective) resembles Operational Excellence (a pillar). Portfolio management (Business) prioritizes cloud initiatives, while application portfolio management (Governance) keeps the application inventory. The CAF phases (Envision, Align, Launch, Scale) also differ from the migration phases (Assess, Mobilize, Migrate and modernize).

> [!IMPORTANT]
> **Exam Question Pattern**: AWS frequently asks which perspective a specific capability belongs to, or asks for the 4 transformation phases!

#### The 6 Perspectives:
1. **Business Perspective**: Ensures cloud aligns with business goals (finance, strategy, value realization).
2. **People Perspective**: Bridges technology and people (**workforce transformation, cloud fluency, organizational change, culture evolution**).
3. **Governance Perspective**: Program management, benefits management, **risk management, cloud financial management, data governance**.
4. **Platform Perspective**: **Platform architecture, data engineering, modernizing workloads, continuous integration/continuous delivery (CI/CD)**.
5. **Security Perspective**: Confidentiality, integrity, availability, identity and access management, vulnerability management.
6. **Operations Perspective**: **Observability, event management, incident and problem management, patch management**.

#### The 4 Phases of Cloud Transformation Journey:
- **Envision** ➔ **Align** ➔ **Launch** ➔ **Scale**.
- *(Note: Do not confuse with migration lifecycle phases: Assess ➔ Mobilize ➔ Migrate & Modernize).*

#### 4 Key Business Outcomes of AWS CAF:
- Reduced business risk, improved ESG performance, increased revenue, and increased operational efficiency.

---

### 1.8 Cloud Migration Strategies: The 7 Rs & Migration Tools
- 🎥 **Video Sections**:
  - [11:44:52 - Migration Evaluator](https://www.youtube.com/watch?v=7HKot-brXFE&t=42292s)
  - [11:45:45 - VM Import Export](https://www.youtube.com/watch?v=7HKot-brXFE&t=42345s)
  - [11:47:58 - Database Migration Service (DMS)](https://www.youtube.com/watch?v=7HKot-brXFE&t=42478s)

#### Detailed notes

A **migration strategy** is the approach used to move a workload to the AWS Cloud. AWS names seven, known as the **7 Rs**, which differ in how much of the application changes:

| Strategy | What happens to the workload | AWS lists it for cases such as |
| :--- | :--- | :--- |
| Retire | Decommissioned | No business value, or average CPU and memory use under 5 percent |
| Retain | Stays where it is for now | Data residency rules, specialized hardware, a recent upgrade |
| Rehost | Moved as is (lift and shift) | Many servers to move with little disruption |
| Relocate | Moved to a cloud version of the same platform, with no new hardware or rewrite | VMware workloads, or an RDS instance moved to another VPC or account |
| Repurchase | Replaced by another product (drop and shop) | A SaaS version replaces a licensed application |
| Replatform | Moved with a few optimizations (lift, tinker, and shift) | Swapping a self-run database for a managed service |
| Refactor | Redesigned for cloud-native features | Business demand for scale and faster releases |

Common strategies for large migrations include rehost, replatform, relocate, and retire. AWS advises against refactor for large migrations because it modernizes the application during the move and is the most complex and costly strategy. It suggests migrating first and modernizing afterward. AWS splits a large migration into three phases. These are some of the tools that fit each one:

1. Assess: build the business case with Migration Evaluator and inventory servers and dependencies with AWS Application Discovery Service or AWS Transform.
2. Mobilize: choose a strategy for each application, build the landing zone, and prepare the team.
3. Migrate and modernize: move servers with AWS Transform MGN, databases with AWS DMS, and file data with AWS DataSync.

> [!NOTE]
> Update (2026): AWS Application Migration Service was renamed AWS Transform MGN in June 2026, and the exam guide still lists the old name ([announcement](https://aws.amazon.com/about-aws/whats-new/2026/06/aws-transform-mgn-rebrand/)). AWS Migration Hub (progress tracking) and AWS Application Discovery Service closed to new customers on November 7, 2025, and AWS recommends AWS Transform, an agentic AI service for discovery, wave planning, and migration, instead ([Migration Hub notice](https://docs.aws.amazon.com/migrationhub/latest/ug/whatishub.html), [Application Discovery Service notice](https://docs.aws.amazon.com/application-discovery/latest/userguide/application-discovery-service-availability-change.html)). AWS's VMware page now lists Amazon Elastic VMware Service (Amazon EVS) as the place to relocate VMware workloads ([AWS for VMware](https://aws.amazon.com/vmware/)).

#### In practice

With agent-based replication, you install the AWS Replication Agent on each source server, and the service copies its disks to AWS continuously while the source keeps running. You launch a test instance, check it, mark the server ready for cutover, and launch the cutover instance when you switch over. Rehost brings the application over without cloud optimizations, and AWS notes that applications are easier to optimize once they already run in the cloud. AWS DMS follows a similar pattern for databases: a task copies the existing data (full load), then replicates ongoing changes (change data capture) until you point the application at the new database. If the target engine differs from the source, convert the schema first with DMS Schema Conversion or the AWS Schema Conversion Tool.

```bash
aws mgn describe-source-servers --filters isArchived=false
aws mgn start-test --source-server-ids SOURCE_SERVER_ID
aws mgn change-server-life-cycle-state --source-server-id SOURCE_SERVER_ID --life-cycle state=READY_FOR_CUTOVER
aws mgn start-cutover --source-server-ids SOURCE_SERVER_ID
aws mgn finalize-cutover --source-server-id SOURCE_SERVER_ID
```

```bash
aws dms create-replication-task \
  --replication-task-identifier orders-to-aurora \
  --source-endpoint-arn SOURCE_ENDPOINT_ARN \
  --target-endpoint-arn TARGET_ENDPOINT_ARN \
  --replication-instance-arn REPLICATION_INSTANCE_ARN \
  --migration-type full-load-and-cdc \
  --table-mappings file://table-mappings.json
```

VM Import/Export brings a virtual machine image into Amazon EC2 as an AMI and can export it back, with no fee beyond the S3, EBS, and EC2 resources it uses. AWS Snowball Edge devices are available only to existing customers, and support for Snowball devices in commercial Regions ends on December 31, 2026. For offline transfers AWS points new customers to AWS Data Transfer Terminal and AWS Partner solutions.

| Strategy (The 7 Rs) | Definition & Exam Clue | Example |
| :--- | :--- | :--- |
| **Rehost ("Lift-and-Shift")** | Move servers as-is to EC2 without making code changes. | Moving VMs directly using **AWS Application Migration Service (MGN)**. |
| **Replatform ("Lift, Tinker, and Shift")** | Make targeted cloud optimizations without changing core application code. | Migrating self-managed MySQL on physical servers to **Amazon RDS**. |
| **Repurchase ("Drop and Shop")** | Abandon existing software and switch to a SaaS product. | Dropping custom on-premises CRM to purchase a SaaS CRM on AWS Marketplace. |
| **Refactor / Re-architect** | Redesign application architecture to cloud-native microservices or serverless. | Breaking a monolithic Java app into **AWS Lambda** functions and **DynamoDB**. |
| **Relocate** | Move virtual machines without purchasing new hardware or changing OS (hypervisor level). | Moving VMware vSphere workloads to **VMware Cloud on AWS**. |
| **Retain** | Keep applications on-premises because of legacy dependencies or near-term deprecation. | Retaining mainframes that are slated to be retired within 12 months. |
| **Retire** | Decommission applications that are no longer needed. | Shutting down unused staging and legacy reporting systems. |

#### Key Migration Services Comparison:
- **AWS Application Migration Service (AWS MGN)**: Primary tool for **automated lift-and-shift server replication** to EC2 with minimal downtime.
- **AWS Database Migration Service (AWS DMS)**: Migrates databases to AWS while source DB remains operational.
- **AWS Schema Conversion Tool (AWS SCT)**: Converts database schemas between different engines (**heterogeneous migration**, e.g., Oracle to Aurora PostgreSQL).
- **AWS Application Discovery Service**: Gathers on-premises server specifications, CPU/memory performance, and network dependencies to plan migration.
- **AWS Migration Hub**: Central single-pane-of-glass dashboard to track progress of migrations across multiple AWS and partner tools.
- **AWS Migration Evaluator** *(formerly TSO Logic)*: Builds a data-driven business case for migration by analyzing actual on-premises utilization and projecting AWS costs (replaces the retired TCO Calculator).
- **AWS DataSync**: Automated, high-speed online network data transfer between on-premises storage and S3, EFS, or FSx.

> Practice this section: [5 questions on Introduction & Cloud Fundamentals](practice-questions/01-cloud-fundamentals.md)

---

## 2. 🛡️ Getting Started & Account Security Baseline

### 2.1 AWS Account Creation & Root User Rules
- 🎥 **Video Sections**:
  - [44:25 - Create an AWS Account](https://www.youtube.com/watch?v=7HKot-brXFE&t=2665s)
  - [1:08:56 - Turning on MFA](https://www.youtube.com/watch?v=7HKot-brXFE&t=4136s)
  - [8:41:20 - AWS Account Root User](https://www.youtube.com/watch?v=7HKot-brXFE&t=31280s)

#### Detailed notes

The **root user** is the identity an AWS account starts with. You create it at sign-up and sign in to it with the email address and password you used to create the account. It has complete access to every service and resource, so use it only for the few tasks that need root credentials.

In a standalone account those tasks include changing the root email address, password, or access keys; closing or reopening the account; restoring IAM permissions when the only IAM administrator is locked out; activating IAM access to the Billing and Cost Management console; registering as a Reserved Instance Marketplace seller; configuring S3 MFA delete; editing or deleting an S3 bucket policy or SQS queue policy that denies every principal; and signing up for AWS GovCloud (US). Launching EC2 instances, creating buckets, and creating IAM users do not need root.

AWS enforces **MFA** on root users. You register it within 14 days of your first console sign-in attempt, with up to eight devices: passkeys and security keys, hardware TOTP tokens, or authenticator apps. AWS recommends against creating root access keys and suggests a group mailbox for the root email address.

| | Standalone account | Member account in AWS Organizations |
| :--- | :--- | :--- |
| Root credentials | Created at sign-up | None by default for accounts created in Organizations; centralized root access can remove them from existing members |
| Change root email, close the account | Root user | IAM principals in the management or delegated administrator account |

> [!NOTE]
> Update (2026): The current list of root-only tasks does not include changing the AWS Support plan, which IAM principals with Support Plans permissions can do, or an EC2 reverse DNS request, which you now set yourself on the Elastic IP address. Changing the account name does not need root either. See [Tasks that require root user credentials](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html).

#### In practice

Treat root as a break-glass account. A shared mailbox lets AWS reach someone when a person leaves, and splitting the password and the MFA device between two people means nobody can sign in alone. Do daily work as an administrative user in IAM Identity Center or through an IAM role. In AWS Organizations, you can remove root credentials from member accounts and let the management account run the few privileged tasks on them.

Any IAM identity with the iam:GetAccountSummary permission can check the two most common root mistakes, so you do not need to sign in as root to do it. A RootMFA of 1 means MFA is on, and a RootAccessKeys of 0 means root has no access keys.

```bash
aws iam get-account-summary \
  --query 'SummaryMap.{RootMFA:AccountMFAEnabled,RootAccessKeys:AccountAccessKeysPresent}'
```

Example output for a healthy account:

```json
{
    "RootMFA": 1,
    "RootAccessKeys": 0
}
```

> [!WARNING]
> **Definite Exam Question on Root User Privileges**:
> The exam specifically tests which actions **can ONLY be performed by the Root User**:
> 1. Changing the **AWS Support plan**.
> 2. **Closing the AWS account**.
> 3. Changing account settings (account name, root email address, root password).
> 4. Restoring IAM user permissions if administrative lock-out occurs.
> 5. Submitting a reverse DNS request for Amazon EC2.
>
> **Tasks that do NOT require Root**: Launching EC2, creating S3 buckets, creating IAM users, creating VPCs (these should ALWAYS be done via IAM administrator!).

#### Root User Security Best Practices:
- Enable **Multi-Factor Authentication (MFA)** immediately (passkey/FIDO2, virtual TOTP app, hardware token).
- **Never generate access keys** (Access Key ID and Secret Access Key) for the root user.
- **Never use root for daily administrative tasks** — create an IAM administrative user or use IAM Identity Center.

---

### 2.2 AWS Free Tier Types
- 🎥 **Video Sections**:
  - [1:01:27 - AWS Free Tier](https://www.youtube.com/watch?v=7HKot-brXFE&t=3687s)
  - [12:24:33 - AWS Free Tier Details](https://www.youtube.com/watch?v=7HKot-brXFE&t=44673s)

#### Detailed notes

The **AWS Free Tier** is the set of free usage limits and credits AWS gives new accounts, and the offers you get depend on when the account was created.

Accounts created on or after July 15, 2025 choose a **Free plan** or a **Paid plan** at sign-up. Both receive $100 in credits and can earn up to $100 more by completing activities, such as setting up a cost budget. The Free plan ends after six months or when the credits run out, whichever comes first. The account then closes, AWS keeps its content for 90 days, and you can upgrade to the Paid plan within that window. A Free plan cannot use services that could use up credits, such as Savings Plans and Reserved Instances, and it becomes a Paid plan automatically if you join AWS Organizations or set up a Control Tower landing zone. A Paid plan includes every service and charges pay-as-you-go prices beyond the credits.

**Always Free** offers cover more than 30 services with monthly limits that do not expire, and they work on both plans. **Short-term trials** need a Paid plan.

| Offer type | Free plan | Paid plan | Accounts created before July 15, 2025 |
| :--- | :--- | :--- | :--- |
| Always Free | Yes | Yes | Yes |
| Short-term trial | No | Yes | Yes |
| 12 months free | No | No | Yes |

> [!NOTE]
> Update (2026): The 12 months free offers exist only for accounts created before July 15, 2025. Newer accounts choose a Free or Paid plan instead. See [Choosing a plan](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/free-tier-plans.html) and the [Free Tier announcement](https://aws.amazon.com/blogs/aws/aws-free-tier-update-new-customers-can-get-started-and-explore-aws-with-up-to-200-in-credits/).

#### In practice

Plan for the end date from the first day. The Billing and Cost Management console home shows your credit balance, and AWS emails a Free Tier usage alert when you pass 85 percent of a service's monthly limit. A zero spend budget in AWS Budgets tells you when spending goes above the Free Tier limits. Credits left over after you upgrade apply to later bills until they expire.

You can read the same information from the CLI. `get-account-plan-state` returns the plan type, status, remaining credits, and expiration date, and `get-free-tier-usage` lists each offer with your usage against its limit.

```bash
aws freetier get-account-plan-state --region us-east-1

aws freetier get-free-tier-usage --region us-east-1 \
  --query 'freeTierUsages[].[service,freeTierType,actualUsageAmount,limit,unit]' \
  --output text
```

Example output of the first command for a Free plan account (invented values):

```json
{
    "accountId": "123456789012",
    "accountPlanType": "FREE",
    "accountPlanStatus": "ACTIVE",
    "accountPlanRemainingCredits": {
        "amount": 142.5,
        "unit": "USD"
    },
    "accountPlanExpirationDate": "2027-02-01T00:00:00+00:00"
}
```

1. **Always Free**: Never expires. (e.g., AWS Lambda: 1 million free invocations/month; DynamoDB: 25 GB storage).
2. **12 Months Free**: Valid for 12 months from initial sign-up date. (e.g., 750 hours/month of EC2 `t2.micro`/`t3.micro`, 5 GB S3 Standard storage).
3. **Short-Term Trials**: Free trial period starting upon service activation. (e.g., SageMaker 2-month trial, Inspector 15-day trial).

---

### 2.3 Budgets & Zero-Spend Billing Alarms
- 🎥 **Video Sections**:
  - [57:09 - AWS Budget](https://www.youtube.com/watch?v=7HKot-brXFE&t=3429s)
  - [1:04:14 - Billing Alarm](https://www.youtube.com/watch?v=7HKot-brXFE&t=3854s)
  - [12:30:49 - AWS Budgets Deep Dive](https://www.youtube.com/watch?v=7HKot-brXFE&t=45049s)
  - [12:34:57 - Billing Alarms with CloudWatch](https://www.youtube.com/watch?v=7HKot-brXFE&t=45297s)

#### Detailed notes

**AWS Budgets** tracks costs or usage against an amount you set and sends an alert when actual or forecasted spend crosses a threshold. The threshold can be a percentage of the budget or an absolute amount, and the alert goes to up to 10 email addresses, to an Amazon SNS topic, or to both. A budget can also run an action when it crosses a threshold: apply an IAM policy or a service control policy, or target specific EC2 or RDS instances, either automatically or after you approve. There are six budget types: cost, usage, RI utilization, RI coverage, Savings Plans utilization, and Savings Plans coverage. The console has templates, including the **zero spend budget**, which notifies you once spending goes above AWS Free Tier limits. Budget data refreshes up to three times a day, so alerts lag behind the spend.

A **CloudWatch billing alarm** watches the `EstimatedCharges` metric, the total estimated charges so far this month, and fires only when the current amount passes your threshold. It does not use a forecast. Billing metric data is stored in us-east-1 and covers worldwide charges, so you create the alarm in that Region after turning on Receive CloudWatch Billing Alerts in Billing preferences.

| | AWS Budgets | CloudWatch billing alarm |
| :--- | :--- | :--- |
| Measures | Cost, usage, and RI or Savings Plans utilization and coverage | Total estimated charges, in USD |
| Alerts on | Actual or forecasted values | Current charges only |
| Notifies | Email addresses, SNS topics | SNS topic |

> [!NOTE]
> Update (2026): On accounts created on or after July 15, 2025, setting up a cost budget is one of five activities that earn Free Tier credits, up to $100 in total. See [Earning additional credits](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/free-tier-plans-activities.html).

#### In practice

Create a zero spend budget on a new account, then add a monthly cost budget with an alert at 80 percent of actual spend and another at 100 percent of forecasted spend. AWS needs about 5 weeks of usage data to forecast, so the forecasted alert does not fire on a new account until then. Budget updates arrive about 8 to 12 hours apart, so a resource left running can pass the threshold before the email arrives. Email recipients must confirm their address before they get alerts. The first time you enable billing alerts, it takes about 15 minutes before billing data appears, and the alarm needs an SNS topic with a confirmed subscription.

In the example, budget-input.json holds a monthly budget of $10 (an example amount) with both alerts. The alarm threshold of 0.01 fires once estimated charges pass one cent.

```json
{
  "AccountId": "123456789012",
  "Budget": {
    "BudgetName": "monthly-10-usd",
    "BudgetType": "COST",
    "TimeUnit": "MONTHLY",
    "BudgetLimit": {"Amount": "10", "Unit": "USD"}
  },
  "NotificationsWithSubscribers": [
    {"Notification": {"NotificationType": "ACTUAL", "ComparisonOperator": "GREATER_THAN",
                      "Threshold": 80, "ThresholdType": "PERCENTAGE"},
     "Subscribers": [{"SubscriptionType": "EMAIL", "Address": "you@example.com"}]},
    {"Notification": {"NotificationType": "FORECASTED", "ComparisonOperator": "GREATER_THAN",
                      "Threshold": 100, "ThresholdType": "PERCENTAGE"},
     "Subscribers": [{"SubscriptionType": "EMAIL", "Address": "you@example.com"}]}
  ]
}
```

```bash
aws budgets create-budget --cli-input-json file://budget-input.json

aws cloudwatch put-metric-alarm --region us-east-1 \
  --alarm-name zero-spend-alarm \
  --namespace AWS/Billing --metric-name EstimatedCharges \
  --dimensions Name=Currency,Value=USD \
  --statistic Maximum --period 21600 --evaluation-periods 1 \
  --threshold 0.01 --comparison-operator GreaterThanThreshold \
  --alarm-actions arn:aws:sns:us-east-1:123456789012:billing-alerts
```

- **AWS Budgets**: Configures custom budgets to track costs and usage against thresholds. Alerts via email or SNS when **actual OR forecasted** spend crosses a threshold (e.g., 80% or 100%). Can trigger automated budget actions (e.g., apply an SCP or stop an instance).
- **CloudWatch Billing Alarms**: Monitored in the `us-east-1` region (where global billing metric data resides) to notify via Amazon SNS when total charges exceed a set dollar amount (e.g., $0.01 for a zero-spend alarm).

> Practice this section: [5 questions on Getting Started & Account Security Baseline](practice-questions/02-account-security-baseline.md)

---

## 3. 🌐 AWS Global Infrastructure

```mermaid
graph LR
    subgraph GlobalNetwork ["AWS Global Network"]
        subgraph Region1 ["AWS Region (e.g. us-east-1)"]
            AZ1["Availability Zone A<br/>(1+ Data Centers)"]
            AZ2["Availability Zone B<br/>(1+ Data Centers)"]
            AZ3["Availability Zone C<br/>(1+ Data Centers)"]
            AZ1 <-->|Low Latency Private Fiber| AZ2
            AZ2 <-->|Low Latency Private Fiber| AZ3
            AZ1 <-->|Low Latency Private Fiber| AZ3
        end
        PoP["Points of Presence (Edge Locations)<br/>CloudFront & Route 53"]
        LocalZone["AWS Local Zones<br/>Single-digit ms latency"]
        Outposts["AWS Outposts<br/>On-Premises Hybrid Racks"]
    end
```

### 3.1 AWS Regions & Availability Zones (AZs)
- 🎥 **Video Sections**:
  - [1:26:55 - AWS Global Infrastructure Overview](https://www.youtube.com/watch?v=7HKot-brXFE&t=5215s)
  - [1:31:16 - Regions](https://www.youtube.com/watch?v=7HKot-brXFE&t=5476s)
  - [1:35:31 - Availability Zones (AZs)](https://www.youtube.com/watch?v=7HKot-brXFE&t=5731s)
  - [1:39:13 - Selecting Regions and AZs - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=5953s)
  - [1:44:40 - Fault Tolerance](https://www.youtube.com/watch?v=7HKot-brXFE&t=6280s)

#### Detailed notes

An **AWS Region** is a separate geographic area where AWS runs data centers, and each Region is designed to be isolated from the others. Every Region has at least three **Availability Zones (AZs)**. An AZ is one or more discrete data centers with redundant power, networking, and connectivity, housed in separate facilities. AZs are many kilometers apart, so a fire, tornado, or flood affects only one AZ, yet all of them are within 100 km (60 miles) of each other and are linked by low-latency, high-bandwidth, redundant fiber.

A Region code looks like `us-east-2`, and an AZ name adds a letter, as in `us-east-2a`. Each AZ also has an **AZ ID**, such as `use2-az1`, that points to the same physical location in every account. Most AWS services create Regional resources: you pick a Region to see them, and AWS does not replicate them to another Region for you. Some resources, such as subnets and EC2 instances, are zonal and live in one AZ. Regions launched after March 20, 2019 stay disabled until you enable them.

| | Region | Availability Zone |
| :--- | :--- | :--- |
| What it is | A separate geographic area with at least three AZs | One or more data centers inside a Region |
| Example | `us-east-2` (US East (Ohio)) | `us-east-2a`, with AZ ID `use2-az1` |
| Resources tied to it | VPCs, S3 buckets | Subnets, EC2 instances, EBS volumes |
| Failure isolation | Isolated from other Regions | A failure in one AZ leaves the others running |

> [!NOTE]
> Update (2026): Accounts created from November 2025 all get the same AZ names for the same locations. In nine older Regions, including us-east-1, earlier accounts can still have names such as `us-east-1a` that point to different locations, so compare AZ IDs across accounts. Newer accounts can use only two AZs in US West (N. California). See [AZ IDs](https://docs.aws.amazon.com/global-infrastructure/latest/regions/az-ids.html).

#### In practice

Place an application in multiple AZs so that the loss of one AZ leaves it running. When you share a subnet with another account, match the AZ ID instead of the AZ name. AWS can also restrict zonal resources in a constrained AZ unless you already use it, so two accounts can see a different number of AZs in the same Region. A Region that is disabled by default needs `aws account enable-region` before you can use it. `describe-availability-zones` returns each AZ name with its AZ ID, and `get-region-opt-status` shows whether a Region is enabled:

```bash
aws ec2 describe-availability-zones --region us-east-2 \
  --filters Name=zone-type,Values=availability-zone \
  --query 'AvailabilityZones[].[ZoneName,ZoneId]' --output text

aws account get-region-opt-status --region-name af-south-1
```

Example output:

```text
us-east-2a    use2-az1
us-east-2b    use2-az2
us-east-2c    use2-az3
{
    "RegionName": "af-south-1",
    "RegionOptStatus": "DISABLED"
}
```

#### AWS Region:
- A physical geographical location containing **multiple Availability Zones** (minimum of 3 AZs per Region).
- Completely isolated from other regions.
- **4 Criteria for Selecting an AWS Region**:
  1. **Compliance & Data Sovereignty**: Legal regulations requiring data to stay within a country's borders.
  2. **Latency / Proximity to End Users**: Deploying close to users reduces round-trip network latency.
  3. **Service Availability**: Not all AWS services and new instance types are available in every region on day one.
  4. **Pricing**: Costs vary slightly between regions due to local taxes and operating expenses.

#### Availability Zone (AZ):
- One or more discrete physical data centers with independent power, cooling, and networking.
- Separated by meaningful physical distance (miles) to prevent shared disaster risk, but connected via ultra-low latency private fiber (<10 ms).
- Naming format: Region + letter (e.g., `us-east-1a`).

---

### 3.2 Edge Locations & Points of Presence (PoP)
- 🎥 **Video Sections**:
  - [1:48:11 - AWS Global Network](https://www.youtube.com/watch?v=7HKot-brXFE&t=6491s)
  - [1:49:59 - Points of Presence (PoP)](https://www.youtube.com/watch?v=7HKot-brXFE&t=6599s)
  - [6:47:36 - AWS CloudFront - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=24456s)

#### Detailed notes

A **point of presence (PoP)** is an AWS site, usually in a city near end users, that runs the edge services of the AWS global network. AWS operates the PoP network next to its Regions and AZs, and it hosts Amazon CloudFront, Amazon Route 53 public DNS, and AWS Global Accelerator. PoPs connect to the Regions over the AWS network backbone, and each PoP is isolated from the others, so a failure in one city does not affect the rest. The network includes **edge locations**, which serve viewers, and larger **Regional edge caches** behind them.

CloudFront sends each request to the edge location that can best serve it, typically the nearest one by latency. A cache hit returns the object at once. On a miss, the edge location typically asks the Regional edge cache, and only if that misses too does CloudFront fetch the object from the origin, such as an S3 bucket or an HTTP server. PUT, POST, PATCH, OPTIONS, and DELETE requests and dynamic requests go straight to the origin. Global Accelerator gives you two static anycast IPv4 addresses that bring traffic into the AWS network at the nearest edge location, then forwards it to endpoints such as Application Load Balancers, Network Load Balancers, EC2 instances, or Elastic IP addresses.

| | Edge location | Regional edge cache |
| :--- | :--- | :--- |
| Position | Closest to viewers | Between the edge locations and your origin |
| Serves viewers directly | Yes | No, it fills the edge locations that miss |
| Cache size | Smaller, so less popular objects are removed sooner | Larger, so objects stay cached longer |

#### In practice

The first request for an object is a miss and travels the full path to the origin. Later requests are answered from a cache until the object expires or you invalidate it. An invalidation removes the object from both the edge locations and the Regional edge caches, so the next request fetches a fresh copy from the origin. The two Global Accelerator addresses stay assigned to your accelerator for as long as it exists, even when it is disabled, and you lose them when you delete it.

A request that misses every cache travels to the origin and fills the caches on the way back:

```text
Viewer in Berlin
  |  DNS routes the request to the best edge location
  v
Edge location (Frankfurt) ...... hit: object returned
  |  miss
  v
Regional edge cache ............ hit: object returned and cached at the edge
  |  miss
  v
Origin (HTTP server) ........... object returned and cached at both layers
```

```bash
# Remove changed files from every cache before they expire
aws cloudfront create-invalidation \
  --distribution-id EDFDVBD6EXAMPLE \
  --paths "/index.html" "/images/*"
```

- **Point of Presence (PoP)**: Edge locations located in major cities worldwide.
- Used by:
  - **Amazon CloudFront**: Caches web content close to end users to reduce latency.
  - **Amazon Route 53**: Global authoritative DNS resolution.
  - **AWS Global Accelerator**: Ingests traffic at edge locations and routes over the AWS private fiber backbone.
  - **AWS Shield**: Edge-level DDoS mitigation.

---

### 3.3 Edge & Hybrid Infrastructure Solutions
- 🎥 **Video Sections**:
  - [1:52:58 - AWS Direct Connect](https://www.youtube.com/watch?v=7HKot-brXFE&t=6778s)
  - [1:54:21 - Direct Connect Locations](https://www.youtube.com/watch?v=7HKot-brXFE&t=6861s)
  - [1:54:51 - AWS Local Zones](https://www.youtube.com/watch?v=7HKot-brXFE&t=6891s)
  - [1:56:24 - Wavelength Zones](https://www.youtube.com/watch?v=7HKot-brXFE&t=6984s)
  - [2:08:17 - AWS Ground Station](https://www.youtube.com/watch?v=7HKot-brXFE&t=7697s)
  - [2:09:35 - AWS Outposts](https://www.youtube.com/watch?v=7HKot-brXFE&t=7775s)

#### Detailed notes

**Edge and hybrid infrastructure** services run AWS capacity outside the standard Regions, close to your users, devices, or data center, or connect your network to AWS without using the internet. **AWS Outposts**, **AWS Local Zones**, and **AWS Wavelength** extend a VPC from a Region to another location, so the resources there use the same APIs, tools, and subnets as in the Region.

An Outpost is a pool of AWS compute and storage at your site that AWS operates and manages as part of a Region, and it reaches the Region over a service link. It comes as 42U racks. AWS has discontinued sales of the 1U and 2U Outposts servers. **AWS Direct Connect** is a fiber connection from your router to a Direct Connect location. Virtual interfaces on it reach a VPC (private), public AWS services such as S3 (public), or a transit gateway (transit), and the traffic bypasses internet service providers. Dedicated connections run at 1, 10, 100, or 400 Gbps, and AWS Direct Connect Partners provision hosted connections from 50 Mbps to 25 Gbps. AWS Ground Station is a fully managed service for controlling satellite communications and processing the data.

| Service | Where it sits | How you start |
| :--- | :--- | :--- |
| Outposts | Your data center or other site | Order racks, which AWS installs; pick a contract term and a payment option |
| Local Zones | An AWS site in a metro area, tied to a parent Region | Opt in to the zone group, then create a subnet in the zone |
| Wavelength | A telecom carrier's 5G network | Extend a VPC to a Wavelength Zone and send traffic through a carrier gateway |
| Direct Connect | A Direct Connect location where you or a partner connect | Request a port, order a cross connect, create a virtual interface |
| Ground Station | AWS antenna sites | Pay for the antenna time you use; downlinked data goes to an EC2 instance or an S3 bucket in your account |

#### In practice

Local Zones are off until you opt in. Enabling one costs nothing extra, and its resources are priced differently from the parent Region. Outposts pricing depends on your order: the configuration, the contract term, and the payment option. A Direct Connect port takes time. AWS can take up to 72 business hours to review a request, and your network provider then orders the cross connect using the letter of authorization that AWS issues. You pay for port hours and outbound data transfer. MACsec encryption works on dedicated 10, 100, and 400 Gbps connections at selected locations, and hosted connections do not support it.

The first command lists the Local Zones of a parent Region, the second opts in to one zone group, and the third creates a subnet in it. You then launch resources into that subnet as you would in an AZ.

```bash
aws ec2 describe-availability-zones --region us-west-2 \
  --all-availability-zones \
  --filters Name=zone-type,Values=local-zone \
  --query 'AvailabilityZones[].[ZoneName,GroupName,OptInStatus]' --output text

aws ec2 modify-availability-zone-group --region us-west-2 \
  --group-name us-west-2-lax-1 --opt-in-status opted-in

aws ec2 create-subnet --region us-west-2 \
  --availability-zone us-west-2-lax-1a \
  --vpc-id vpc-0123456789abcdef0 --cidr-block 10.0.8.0/24
```

| Service | Primary Purpose | 🔑 Exam Trigger Keyword |
| :--- | :--- | :--- |
| **AWS Outposts** | Run native AWS compute and storage hardware directly inside your on-premises data center. | *"On-premises data center with AWS APIs and hardware"* |
| **AWS Local Zones** | Extend compute, storage, and database services to major population centers where no AWS Region exists. | *"Single-digit millisecond latency to metropolitan areas"* |
| **AWS Wavelength** | Embeds AWS services within 5G telecommunication networks. | *"Ultra-low latency for 5G mobile connected devices"* |
| **AWS Direct Connect** | Dedicated, private physical fiber link connecting on-premises to AWS. | *"Dedicated private connection, bypass public internet"* |
| **AWS Ground Station** | Managed satellite communication control and satellite data processing. | *"Control satellites, downlink satellite data"* |

---

### 3.4 Regional vs. Global AWS Services
- 🎥 **Video Sections**:
  - [1:33:41 - Regional vs Global Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=5621s)

#### Detailed notes

Most AWS services are **Regional services**: a resource exists in the Region where you create it, the console and CLI show only the resources of the Region you select, and AWS does not replicate them to other Regions for you. A few are **global services**, whose resources are not tied to one Region. A global service has one **control plane**, hosted in a single Region, and a data plane that runs worldwide. IAM and AWS Organizations have their control planes in us-east-1, and IAM answers requests from a data plane in every Region. Route 53 public DNS, CloudFront, and AWS WAF for CloudFront also have control planes in us-east-1, with data planes at points of presence. The Global Accelerator control plane is in us-west-2. If the Region that hosts a control plane has an outage, you may be unable to create or change that service's resources, although its data plane keeps working.

| Service | Scope | Detail |
| :--- | :--- | :--- |
| Amazon S3 | Regional | A bucket lives in one Region, but its name must be unique across all Regions in the partition |
| AWS WAF | Regional or global | A web ACL for CloudFront uses scope CLOUDFRONT and is managed in us-east-1 |
| AWS Certificate Manager | Regional | A certificate that CloudFront uses is managed in us-east-1 |
| IAM | Global | Users and roles work in every Region of the partition |

> [!NOTE]
> Update (2026): Since March 2026 you can also create S3 general purpose buckets in an account regional namespace, where the name ends with your account ID, the Region code, and -an, and no other account can ever use it. Buckets in the shared global namespace still need a name that is unique across the partition. See [Namespaces for general purpose buckets](https://docs.aws.amazon.com/AmazonS3/latest/userguide/gpbucketnamespaces.html).

#### In practice

When a resource seems to be missing, check the Region selector first, because Regional resources appear only in the Region where you created them. Some parts of global services still live in one Region: a web ACL for CloudFront is created through us-east-1, and so is a certificate that CloudFront uses. A service control policy that denies other Regions also blocks global services unless you exempt them with NotAction, for example iam:*, route53:*, cloudfront:*, and support:*.

```bash
# IAM is global: no Region choice, and the user works in every Region
aws iam create-user --user-name alice

# A web ACL for CloudFront is global in scope, but you call us-east-1
aws wafv2 list-web-acls --scope CLOUDFRONT --region us-east-1

# A web ACL for an Application Load Balancer is Regional
aws wafv2 list-web-acls --scope REGIONAL --region eu-west-1
```

Global services use one endpoint hostname, and Regional services use one per Region:

```text
Global endpoints             Regional endpoints
iam.amazonaws.com            ec2.us-east-2.amazonaws.com
route53.amazonaws.com        ec2.eu-west-1.amazonaws.com
cloudfront.amazonaws.com     s3.eu-west-1.amazonaws.com
```

| Scope | Services |
| :--- | :--- |
| **Global Services**<br/>*(Single global control plane; no region selector required)* | - **AWS IAM**<br/>- **Amazon Route 53**<br/>- **Amazon CloudFront**<br/>- **AWS WAF** (when attached to CloudFront)<br/>- **AWS Artifact**<br/>- **AWS Organizations** |
| **Regional Services**<br/>*(Resources exist within a specific chosen AWS Region)* | - **Amazon EC2**<br/>- **Amazon S3** (global bucket names, but stored in a specific Region)<br/>- **Amazon VPC**<br/>- **Amazon RDS / Aurora**<br/>- **Amazon DynamoDB**<br/>- **AWS Lambda**<br/>- **Amazon CloudWatch / CloudTrail** |

---

### 3.5 Specialized AWS Regions & Sovereignty
- 🎥 **Video Sections**:
  - [1:57:25 - Data Residency](https://www.youtube.com/watch?v=7HKot-brXFE&t=7045s)
  - [2:00:06 - AWS for Government](https://www.youtube.com/watch?v=7HKot-brXFE&t=7206s)
  - [2:00:52 - GovCloud](https://www.youtube.com/watch?v=7HKot-brXFE&t=7252s)
  - [2:02:21 - AWS in China](https://www.youtube.com/watch?v=7HKot-brXFE&t=7341s)
  - [2:05:11 - Sustainability](https://www.youtube.com/watch?v=7HKot-brXFE&t=7511s)

#### Detailed notes

**Specialized AWS Regions** are Regions built for particular legal or compliance needs, and each kind sits in a separate **partition**. A partition is a group of Regions, and every AWS account is scoped to one partition, so a standard AWS account cannot reach the GovCloud or China Regions.

**AWS GovCloud (US)** is two isolated Regions, US-East and US-West, for US government agencies and customers with sensitive workloads. It addresses requirements such as FedRAMP High, DoD SRG Impact Levels 4 and 5, and CJIS. Only AWS personnel who are US citizens administer it, which helps customers manage their ITAR and EAR export obligations. The **China Regions** are Beijing, operated by Sinnet, and Ningxia, operated by NWCD. They use account credentials separate from global AWS accounts, and data stored there stays in the Regions unless you move it.

The **AWS European Sovereign Cloud** launched in January 2026 with its first Region in Brandenburg, Germany. It is physically and logically separate from other AWS Regions, has its own IAM and billing, and is operated by EU residents located in the EU through German legal entities. In the standard Regions, AWS does not replicate your resources to another Region unless you set that up.

| Partition | Regions | Notes |
| :--- | :--- | :--- |
| `aws` | Standard Regions | Used by most accounts |
| `aws-us-gov` | AWS GovCloud (US-East), AWS GovCloud (US-West) | Administered only by AWS personnel who are US citizens |
| `aws-cn` | China (Beijing), China (Ningxia) | Separate account credentials |
| `aws-eusc` | AWS European Sovereign Cloud (`eusc-de-east-1`) | Own IAM and billing |

> [!NOTE]
> Update (2026): The Customer Carbon Footprint Tool was deprecated on June 30, 2026. Its replacement, the AWS Sustainability service, reports carbon emissions and water allocation and does not need Billing permissions. See [What is AWS Sustainability?](https://docs.aws.amazon.com/sustainability/latest/userguide/what-is-sustainability.html).

#### In practice

To keep workloads in approved Regions, deny API calls to every other Region with a service control policy that checks the aws:RequestedRegion condition. AWS Control Tower has a Region deny control for the same purpose. Global services such as IAM and Route 53 are not tied to your approved Regions, so a Region-restricting policy exempts them with NotAction. For in-country data residency and digital sovereignty needs, AWS Dedicated Local Zones are fully managed AWS infrastructure built exclusively for a customer and placed in a location the customer chooses.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "DenyAllOutsideEU",
      "Effect": "Deny",
      "NotAction": ["cloudfront:*", "iam:*", "route53:*", "support:*"],
      "Resource": "*",
      "Condition": {
        "StringNotEquals": {
          "aws:RequestedRegion": ["eu-central-1", "eu-west-1"]
        }
      }
    }
  ]
}
```

This policy denies every action requested in a Region other than eu-central-1 and eu-west-1, except actions of CloudFront, IAM, Route 53, and Support.

- **AWS GovCloud (US)**: Isolated regions allowing US government agencies and contractors to adhere to FedRAMP High, ITAR, and DoD Impact Levels.
- **AWS China Regions**: Physically isolated regions operated by local Chinese partners (Sinnet in Beijing, NWCD in Ningxia).
- **Customer Carbon Footprint Tool**: Measures and tracks carbon emissions associated with your AWS usage.

> Practice this section: [5 questions on AWS Global Infrastructure](practice-questions/03-global-infrastructure.md)

---

## 4. 📐 Cloud Architecture & Reliability

### 4.1 Core Architecture Terminologies
- 🎥 **Video Sections**:
  - [2:12:13 - Cloud Architecture Terminologies](https://www.youtube.com/watch?v=7HKot-brXFE&t=7933s)
  - [2:14:00 - High Availability](https://www.youtube.com/watch?v=7HKot-brXFE&t=8040s)
  - [2:15:02 - High Scalability](https://www.youtube.com/watch?v=7HKot-brXFE&t=8102s)
  - [2:15:43 - High Elasticity](https://www.youtube.com/watch?v=7HKot-brXFE&t=8143s)
  - [2:16:34 - Fault Tolerance](https://www.youtube.com/watch?v=7HKot-brXFE&t=8194s)
  - [2:17:20 - High Durability](https://www.youtube.com/watch?v=7HKot-brXFE&t=8240s)

#### Detailed notes

Five terms describe how a workload behaves under load and under failure. **High availability** means the workload keeps serving users when a component or a whole data center fails, which on AWS usually means running copies in at least two Availability Zones (AZs). **Scalability** is the ability to handle more load by adding capacity, either more instances (horizontal scaling, or scaling out) or a bigger instance (vertical scaling, or scaling up). **Elasticity** is scalability with automation: capacity grows when demand rises and shrinks when it falls, so you pay only for what the workload uses. **Fault tolerance** goes further than high availability. Spare components can take over all of the work, so a failure causes little or no interruption, and you pay for the duplicate capacity. **Durability** describes stored data: the likelihood that it survives without loss or corruption over time.

| | Horizontal scaling | Vertical scaling |
| :--- | :--- | :--- |
| What changes | The number of instances | The size of one instance |
| AWS example | Auto Scaling adds EC2 instances behind a load balancer | Change an instance from m5.large to m5.xlarge |
| Interruption | None, the other instances keep serving | Stop the instance, change its type, start it again |
| Limit | The application must run on several instances at once | The largest instance type available |

For EC2, elasticity is normally built with horizontal scaling, because resizing an instance means stopping it.

#### In practice

Availability is quoted as a percentage over a year, often shortened to "nines". AWS's Well-Architected guidance shows how little downtime each extra nine allows, and each extra nine costs more to build and test.

| Availability | Downtime allowed per year | Workloads AWS lists at this level |
| :--- | :--- | :--- |
| 99.9% | 8 hours 45 minutes | Internal tools such as knowledge management and project tracking |
| 99.95% | 4 hours 22 minutes | Online commerce, point of sale |
| 99.99% | 52 minutes | Video delivery, broadcast workloads |
| 99.999% | 5 minutes | ATM transactions, telecommunications |

Availability and durability are separate numbers. S3 Standard is designed for 99.999999999% durability (eleven nines) and 99.99% availability over a year, so objects are very unlikely to be lost even though the service can be unreachable for a short time.

- **High Availability (HA)**: System remains operational and accessible across component failures, achieved by multi-AZ redundancy.
- **Horizontal Scaling ("Scaling Out")**: Adding more instances of the same size (e.g., adding EC2 instances via Auto Scaling).
- **Vertical Scaling ("Scaling Up")**: Resizing an instance to a larger tier (e.g., changing `t3.medium` to `m5.2xlarge`).
- **Elasticity**: System automatically acquires resources when needed and releases them when not needed (matching demand dynamically).
- **Fault Tolerance**: The system continues operating without interruption even when components fail.
- **Durability**: Data is preserved against loss or corruption over time (S3 offers 11 9's durability: `99.999999999%`).

---

### 4.2 Disaster Recovery (DR) Strategies & RTO / RPO
- 🎥 **Video Sections**:
  - [2:17:58 - Business Continuity Plan](https://www.youtube.com/watch?v=7HKot-brXFE&t=8278s)
  - [2:19:07 - Disaster Recovery Options](https://www.youtube.com/watch?v=7HKot-brXFE&t=8347s)
  - [2:21:44 - RTO Visualized](https://www.youtube.com/watch?v=7HKot-brXFE&t=8504s)
  - [2:23:20 - RPO Visualized](https://www.youtube.com/watch?v=7HKot-brXFE&t=8600s)

#### Detailed notes

**Disaster recovery (DR)** is the plan for restoring a workload after a disaster such as the loss of a data center or a Region. It is one part of a business continuity plan, which also covers the parts of the business outside the workload. Two targets set how fast and how complete the recovery must be. The **Recovery Time Objective (RTO)** is the maximum acceptable delay between the interruption of service and its restoration. The **Recovery Point Objective (RPO)** is the maximum acceptable time since the last data recovery point, so it caps how much recent data you can lose. AWS describes four strategies for recovering in a second Region. They run from cheapest and slowest to most expensive and fastest.

| Strategy | RPO | RTO | In the recovery Region before a disaster |
| :--- | :--- | :--- | :--- |
| Backup and restore | Hours | 24 hours or less | Backups only |
| Pilot light | Minutes | Tens of minutes | Replicated data and databases running, application servers off |
| Warm standby | Seconds | Minutes | A scaled-down but fully working copy of the workload |
| Multi-site active/active | Near zero | Potentially zero | The full workload, serving traffic in every Region |

Tighter targets cost more, so AWS advises against a strategy that is more demanding than the business needs. Every strategy also needs point-in-time backups or versioning, because replication alone may not protect against data corruption or destruction.

> [!NOTE]
> Update (2026): The Well-Architected Reliability pillar lists RPO and RTO separately for each strategy, as in the table above. For backup and restore it gives an RPO in hours and an RTO of 24 hours or less. See [REL13-BP02](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/rel_planning_for_recovery_disaster_recovery.html).

#### In practice

Each target limits one span of the same timeline. RPO limits how old the last good copy of the data may be, and RTO limits how long users may wait for service to return.

```text
Hourly backups, one incident

14:00               14:40                  16:10
last backup         disaster               service restored
|<--- data lost --->|<----- downtime ----->|
      40 minutes            90 minutes
```

Hourly backups cap the data loss at about an hour, which fits an RPO of one hour. Without infrastructure as code such as CloudFormation, rebuilding the workload in the recovery Region takes longer and can exceed the RTO. For backup and restore, AWS Backup can schedule backups and copy them to another Region. AWS Elastic Disaster Recovery replicates servers continuously into a low-cost staging area in your account and follows the pilot light approach, with an RPO in seconds, an RTO in minutes, and support for non-disruptive recovery drills.

#### RTO vs. RPO:
- **RTO (Recovery Time Objective)**: The maximum acceptable **downtime** before service restoration.
- **RPO (Recovery Point Objective)**: The maximum acceptable **data loss** measured in time.

```mermaid
graph TD
    subgraph DRStrategies ["Disaster Recovery Spectrum (Cost vs. Recovery Speed)"]
        D1["1. Backup & Restore<br/>(Slowest recovery: Hours/Days RTO/RPO, Lowest Cost)"]
        D2["2. Pilot Light<br/>(Core data replicated, compute off until disaster)"]
        D3["3. Warm Standby<br/>(Scaled-down version always running 24/7)"]
        D4["4. Multi-Site Active/Active<br/>(Instant zero-downtime failover, Real-time sync, Highest Cost)"]
    end
    D1 --> D2 --> D3 --> D4
```

| Strategy | RTO / RPO | Cost | How it Works |
| :--- | :--- | :--- | :--- |
| **Backup & Restore** | High (Hours to Days) | $ (Lowest) | Regular data backups sent to S3/Glacier. Rebuild entire stack only after disaster. |
| **Pilot Light** | Moderate (Tens of minutes) | $$ | Core database is continuously replicated. Compute resources (EC2) are provisioned via AMIs only upon disaster. |
| **Warm Standby** | Low (Minutes) | $$$ | A scaled-down, fully functional mirror of production is running 24/7 in a secondary region. Scales up instantly on failover. |
| **Multi-Site Active/Active**| Near Zero (Seconds) | $$$$ (Highest) | Full production capacity running simultaneously in 2+ active AWS regions. |

---

### 4.3 High Availability Architecture Design
- 🎥 **Video Sections**:
  - [2:24:46 - Architectural diagram example](https://www.youtube.com/watch?v=7HKot-brXFE&t=8686s)
  - [2:31:56 - High Availability - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=9116s)

#### Detailed notes

A **highly available architecture** removes single points of failure by running every layer in at least two Availability Zones (AZs), so the loss of one AZ does not stop the application. The usual web design stacks four AWS services, and each reacts to a failed AZ in its own way.

| Layer | Service | How it spans AZs | When an AZ fails |
| :--- | :--- | :--- | :--- |
| DNS | Amazon Route 53 | Health checks watch each endpoint | Stops answering with the unhealthy endpoint |
| Load balancing | Application Load Balancer | At least two AZs enabled, one node in each | Sends requests only to healthy targets in the other AZs |
| Compute | EC2 Auto Scaling group | Subnets in several AZs, instances spread evenly | Launches replacement instances in the remaining AZs |
| Database | RDS Multi-AZ | Synchronous standby in a second AZ | Promotes the standby, typically in 60 to 120 seconds |

Cross-zone load balancing is always on at the load balancer level for an Application Load Balancer, so each of its nodes can send requests to registered targets in every enabled AZ. RDS has two Multi-AZ forms. A Multi-AZ DB instance deployment has one standby that serves no read traffic. A Multi-AZ DB cluster has a writer and two readable standbys in three AZs. Multiple AZs protect against events such as a fire or a major power outage that affect one AZ. Surviving the loss of a whole Region takes a DR strategy from topic 4.2.

#### In practice

Every layer has to be spread, or the design keeps a hidden single point of failure. An Application Load Balancer sends no traffic to targets in a zone you have not enabled, and an Auto Scaling group whose subnets sit in one AZ puts every instance in that AZ. Setting the group's health check type to ELB lets it replace instances that the load balancer reports as unhealthy. A health check grace period, which is 0 seconds by default in the CLI, gives new instances time to start before a failed check can replace them, so the command sets it to 300 seconds. Multi-AZ for RDS is a separate setting on the DB instance.

```bash
aws autoscaling create-auto-scaling-group \
  --auto-scaling-group-name web-asg \
  --launch-template LaunchTemplateName=web-template \
  --min-size 2 --max-size 6 \
  --vpc-zone-identifier "SUBNET_A_ID,SUBNET_B_ID" \
  --target-group-arns TARGET_GROUP_ARN \
  --health-check-type ELB \
  --health-check-grace-period 300

aws rds create-db-instance \
  --db-instance-identifier my-example-db \
  --engine postgres \
  --db-instance-class db.m6g.large \
  --allocated-storage 100 \
  --master-username dbadmin \
  --manage-master-user-password \
  --multi-az
```

With a minimum size of 2 and two subnets in different AZs, the group tries to keep one instance in each AZ.

A standard highly available AWS architecture deploys across multiple AZs:
1. **Route 53**: Global DNS with health checks.
2. **Application Load Balancer (ALB)**: Distributes incoming web traffic across multiple AZs.
3. **Auto Scaling Group (ASG)**: Maintains target EC2 instance count across multiple AZs.
4. **RDS Multi-AZ**: Replicates database synchronously to a standby instance in a second AZ with automatic failover.

> Practice this section: [5 questions on Cloud Architecture & Reliability](practice-questions/04-architecture-reliability.md)

---

## 5. 🧰 Management, Governance & Developer Tools

### 5.1 Ways to Interact with AWS (Console, CLI, SDK, CloudShell)
- 🎥 **Video Sections**:
  - [2:35:33 - AWS API](https://www.youtube.com/watch?v=7HKot-brXFE&t=9333s)
  - [2:41:51 - AWS Management Console](https://www.youtube.com/watch?v=7HKot-brXFE&t=9711s)
  - [2:55:00 - AWS Tools for PowerShell](https://www.youtube.com/watch?v=7HKot-brXFE&t=10500s)
  - [3:05:29 - AWS CLI](https://www.youtube.com/watch?v=7HKot-brXFE&t=11129s)
  - [3:19:42 - AWS SDK](https://www.youtube.com/watch?v=7HKot-brXFE&t=11982s)
  - [3:35:27 - AWS CloudShell](https://www.youtube.com/watch?v=7HKot-brXFE&t=12927s)

#### Detailed notes

You can work with AWS services in four main ways, and all of them send authenticated requests to the same **AWS API**. The **AWS Management Console** is the web interface for clicking through tasks. The **AWS CLI** runs the same actions as commands in a terminal, which makes them easy to script. **SDKs** are libraries for languages such as Python (Boto3), Java, JavaScript, Go, and .NET that let your application call AWS directly. **AWS CloudShell** is a shell in your browser that is already signed in with your console credentials and has the AWS CLI installed. PowerShell users can use AWS Tools for PowerShell in place of the CLI. The CLI and the SDKs sign each request with AWS Signature Version 4 for you.

| | Console | AWS CLI | SDK | CloudShell |
| :--- | :--- | :--- | :--- | :--- |
| Runs in | Your browser | A terminal on your computer | Your application | Your browser |
| Signs in with | Root user, IAM user, or a federated user | `aws login`, IAM Identity Center, roles, or access keys | A chain of sources checked in order, such as environment variables, config files, and IAM roles | The credentials you used for the console |
| Suits | Exploring and one-off tasks | Scripts and repeatable tasks | Code that calls AWS | A quick CLI session with nothing to install |

> [!NOTE]
> Update (2026): AWS CLI version 1 is in maintenance mode and reaches end of support on July 15, 2027, so install version 2. See the [AWS announcement](https://aws.amazon.com/blogs/developer/cli-v1-maintenance-mode-announcement).

#### In practice

CloudShell needs no installation and no credential setup. It gives you 1 GB of persistent storage per Region in your home directory, kept for 120 days after your last session, and a session ends after 20 to 30 minutes without keyboard or pointer input. You can run up to 10 shells at once in a Region. CloudShell has no additional charge, and you pay for the AWS resources you create with it. On your own machine, `aws login` signs the CLI in through your browser with your console credentials (CLI 2.32.0 or later).

```bash
aws login
aws sts get-caller-identity
aws s3api list-buckets --query "Buckets[].Name" --output text
```

The same request from Python uses Boto3, which finds credentials through its provider chain:

```python
import boto3

s3 = boto3.client("s3")
for bucket in s3.list_buckets()["Buckets"]:
    print(bucket["Name"])
```

- **AWS API**: Under the hood, **every action in AWS is an authenticated REST API call**.
- **AWS CLI**: Command-line tool to manage services via shell scripts.
- **AWS CloudShell**: Browser-based shell pre-authenticated with your console credentials, with the AWS CLI and developer tools preinstalled. Free to use within region limits.
- **AWS SDKs**: Software development kits for language-specific programmatic access (Python/Boto3, Java, JS, Go, C#).

---

### 5.2 Amazon Resource Names (ARN)
- 🎥 **Video Sections**:
  - [3:01:14 - Amazon Resource Names (ARN)](https://www.youtube.com/watch?v=7HKot-brXFE&t=10874s)
  - [3:03:10 - ARN - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=10990s)

#### Detailed notes

An **Amazon Resource Name (ARN)** uniquely identifies an AWS resource, and you need one wherever a resource must be named without ambiguity, such as in IAM policies, tags, and API calls. AWS does not consider ARNs secret, although it advises sharing them carefully. The general format is `arn:partition:service:region:account-id:resource`. The partition is the group of Regions the resource lives in: `aws` for standard Regions, `aws-cn` for China, and `aws-us-gov` for AWS GovCloud (US). Each AWS account belongs to one partition, and you cannot delegate access between accounts in different partitions. The resource part is a name, an ID, or a path, and it often takes the form `resource-type/resource-id` or `resource-type:resource-id`. Some ARNs leave the Region or the account ID empty. IAM resources are global, so their Region field is blank and the account ID stays. S3 bucket ARNs leave both fields blank.

| Resource | ARN | Empty fields |
| :--- | :--- | :--- |
| IAM user | `arn:aws:iam::123456789012:user/john` | Region |
| EC2 instance | `arn:aws:ec2:us-east-1:123456789012:instance/i-0123456789abcdef0` | None |
| Lambda function | `arn:aws:lambda:us-east-1:123456789012:function:my-function` | None |
| S3 bucket | `arn:aws:s3:::my-example-bucket` | Region and account ID |

> [!NOTE]
> Update (2026): AWS now has four partitions. The fourth, `aws-eusc`, is the AWS European Sovereign Cloud, so its ARNs start with `arn:aws-eusc:`. See the [S3 CreateBucket reference](https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html) and the [AWS Security Blog](https://aws.amazon.com/blogs/security/architecting-a-secure-landing-zone-in-the-aws-european-sovereign-cloud/).

#### In practice

ARNs matter most in IAM policies, where the `Resource` element names what a statement applies to. The `*` wildcard can stand in for part of the resource, so `arn:aws:s3:::my-example-bucket/reports/*` covers every object under the `reports/` prefix. Bucket actions and object actions need different ARNs: listing a bucket takes the bucket ARN, and reading or writing objects takes an ARN with a `/` and the object name after the bucket name. The exact format depends on the service, and the Service Authorization Reference lists the ARN pattern for each resource type. The command `aws sts get-caller-identity --query Arn --output text` prints the ARN of the identity you are using.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["s3:GetObject", "s3:PutObject"],
      "Resource": "arn:aws:s3:::my-example-bucket/reports/*"
    },
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::my-example-bucket"
    }
  ]
}
```

This policy allows reading and writing objects under `reports/` and listing the bucket.

Format:
```text
arn:partition:service:region:account-id:resource-type/resource-id
```
- Global resources (like S3 buckets or IAM roles) omit the `region` or `account-id` field (e.g., `arn:aws:s3:::my-bucket`).

---

### 5.3 Infrastructure as Code (IaC): CloudFormation & StackSets & CDK
- 🎥 **Video Sections**:
  - [3:36:40 - Infrastructure as Code (IaC)](https://www.youtube.com/watch?v=7HKot-brXFE&t=13000s)
  - [3:38:09 - CloudFormation](https://www.youtube.com/watch?v=7HKot-brXFE&t=13089s)
  - [3:48:26 - Cloud Development Kit (CDK)](https://www.youtube.com/watch?v=7HKot-brXFE&t=13706s)

#### Detailed notes

**Infrastructure as Code (IaC)** means you write a configuration file or a program that creates, updates, and deletes your cloud infrastructure for you. The file is a blueprint of the whole environment, so you can share it, keep it in version control, and rebuild the same setup whenever you need it.

AWS has two main ways to write IaC:

| | AWS CloudFormation | AWS CDK |
| :--- | :--- | :--- |
| Style | Declarative: you list the resources you want and CloudFormation works out the steps | Imperative code: you write a program and the CDK generates a CloudFormation template from it |
| You write | JSON or YAML | TypeScript, JavaScript, Python, Java, C#, or Go |
| Detail | Every resource and property is written out, so templates get long | Shorter, because constructs fill in defaults such as IAM roles |
| Deploys through | CloudFormation | CloudFormation |

A CloudFormation template creates a **stack**, a group of resources managed as one unit. Deleting the stack deletes the resources it created. You pay for the resources in a stack, not for CloudFormation itself. StackSets deploy one template to many accounts and Regions in a single operation.

#### In practice

CloudFormation templates are plain text, so they are easy to read, review, and compare in version control. They also grow long, and loops or conditions are clumsy next to a real programming language. People without a programming background often find CloudFormation the easier of the two to learn. The CDK produces CloudFormation templates, so you still need to read one when a CDK stack fails to deploy.

A small template that creates a versioned S3 bucket:

```yaml
AWSTemplateFormatVersion: "2010-09-09"
Description: One S3 bucket with versioning turned on
Resources:
  LogsBucket:
    Type: AWS::S3::Bucket
    Properties:
      VersioningConfiguration:
        Status: Enabled
Outputs:
  BucketName:
    Value: !Ref LogsBucket
```

The same bucket in the CDK (TypeScript) is one statement inside a stack class:

```typescript
new s3.Bucket(this, 'LogsBucket', { versioned: true });
```

Three CloudFormation features come up often. Change sets preview what an update will do before you apply it. Drift detection reports resources that someone edited outside the template. If a stack fails during creation, CloudFormation rolls back by default and removes what it had built.

> [!IMPORTANT]
> **Definite Exam Question on CloudFormation StackSets**:
> - **AWS CloudFormation**: Provisions resources declared in **JSON or YAML templates** as a single unit called a **Stack**. Free for AWS resources (you pay only for the resources created).
> - **AWS CloudFormation StackSets**: Lets you deploy a CloudFormation template across **MULTIPLE AWS ACCOUNTS and MULTIPLE AWS REGIONS in a single operation**.
>   - *Trap Alert*: Do NOT pick AWS Systems Manager when asked to deploy identical infrastructure templates across accounts!

- **AWS Cloud Development Kit (CDK)**: Open-source framework to define cloud infrastructure in modern programming languages (TypeScript, Python, Java) that synthesizes into CloudFormation templates.

---

### 5.4 Developer Tools & Access Credentials
- 🎥 **Video Sections**:
  - [3:50:39 - AWS Toolkit for VSCode](https://www.youtube.com/watch?v=7HKot-brXFE&t=13839s)
  - [3:51:48 - Access Key](https://www.youtube.com/watch?v=7HKot-brXFE&t=13908s)

#### Detailed notes

**Access keys** are long-term credentials for an IAM user or the account root user. Each one is a pair, an access key ID and a secret access key, that the AWS CLI and the SDKs use to sign programmatic requests. An IAM user can have up to two access keys, and AWS shows the secret access key only when you create it, so a lost secret means deleting the key and creating a new one. Temporary credentials from AWS STS add a session token to the pair, expire on their own, and have an ID that starts with ASIA. Long-term access key IDs start with AKIA. The AWS Toolkit for Visual Studio Code is an open-source extension that helps you develop, debug locally, and deploy serverless applications from your editor. It signs in with IAM Identity Center, an AWS Builder ID, or IAM credentials.

| | Long-term access keys | Temporary credentials |
| :--- | :--- | :--- |
| Belong to | An IAM user or the root user | A role session, an IAM Identity Center user, or a console login |
| ID prefix | AKIA | ASIA, plus a session token |
| Lifetime | Until you deactivate or delete them | Expire on their own, up to 12 hours with `aws login` |
| Where they live | Often in the shared credentials file, in plaintext | Cached by the CLI, or delivered to EC2 and Lambda through a role |
| AWS guidance | Only where roles or IAM Identity Center cannot be used | Preferred |

> [!NOTE]
> Update (2026): AWS's CLI guide now lists signing in with console credentials (`aws login`, CLI 2.32.0 or later) as the recommended option and marks IAM user long-term access keys as not recommended. See [Authentication and access credentials for the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-authentication.html).

#### In practice

Treat an access key like a password. Keep it out of source code and Git, and protect the shared credentials file, which stores keys in plaintext. Never create an access key for the root user. To rotate a key without downtime, create the second key, switch your applications to it, check when the old key was last used, deactivate the old key, and delete it once nothing breaks. Code that runs on EC2, Lambda, or ECS can use an IAM role instead, which delivers temporary credentials and keeps keys out of the code.

```ini
# ~/.aws/credentials
[default]
aws_access_key_id = AKIAIOSFODNN7EXAMPLE
aws_secret_access_key = wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
```

```bash
aws iam create-access-key --user-name alice
aws iam get-access-key-last-used --access-key-id OLD_ACCESS_KEY_ID
aws iam update-access-key --user-name alice --access-key-id OLD_ACCESS_KEY_ID --status Inactive
aws iam delete-access-key --user-name alice --access-key-id OLD_ACCESS_KEY_ID
```

- **Access Keys**: Pair of **Access Key ID** + **Secret Access Key** used to authenticate programmatic requests via the AWS CLI and AWS SDK.

---

### 5.5 AWS Systems Manager (SSM)
- 🎥 **Video Sections**:
  - [10:15:25 - AWS License Manager](https://www.youtube.com/watch?v=7HKot-brXFE&t=36925s)

#### Detailed notes

**AWS Systems Manager** lets you view, manage, and operate nodes at scale from one place: EC2 instances, on-premises servers, and machines in other clouds. A node becomes a managed node when the **SSM Agent** is installed on it and can reach the Systems Manager service, and when it has the IAM permissions to do so. Many AWS-provided AMIs already include the agent, among them Amazon Linux 2023 and recent Windows Server and Ubuntu Server images. Systems Manager groups its features into tools (older material calls them capabilities).

| Tool | What it does |
| :--- | :--- |
| Fleet Manager | One console view of node health and performance, plus file, registry, and user tasks |
| Patch Manager | Scans nodes for missing patches and installs approved ones, using patch baselines |
| Run Command | Runs commands or scripts on dozens or hundreds of nodes at once |
| Session Manager | Opens a shell in the browser or the CLI with no inbound ports, bastion hosts, or SSH keys |
| Parameter Store | Stores configuration values such as endpoints and AMI IDs, with a SecureString type that encrypts a value with a KMS key |

AWS recommends Secrets Manager for database credentials and API keys, and for encrypted data that needs automatic rotation, cross-account access, or fine-grained audit logging. AWS License Manager is a separate service that tracks vendor software licenses, such as Microsoft, SAP, Oracle, and IBM, and can set hard or soft limits on their use.

> [!NOTE]
> Update (2026): Run Command, Session Manager, and Patch Manager have no additional charge on EC2 instances. On hybrid and multicloud nodes, usage-based billing for Session Manager sessions and Run Command invocations applies from September 30, 2026. See [Systems Manager pricing](https://aws.amazon.com/systems-manager/pricing/).

#### In practice

Managed nodes need IAM permissions as well as the agent. Turning on Default Host Management Configuration gives Systems Manager access to every EC2 instance in the Region and account that uses IMDSv2 and runs SSM Agent 3.2.582.0 or later, without instance profiles. Otherwise attach an instance profile whose role has the AmazonSSMManagedInstanceCore policy to each instance. Session Manager API calls appear in CloudTrail, and session logs can go to Amazon S3 or CloudWatch Logs. Starting a session from the CLI needs the Session Manager plugin on your machine.

```bash
# List instances that are managed nodes
aws ssm describe-instance-information \
  --query "InstanceInformationList[].[InstanceId,PingStatus]" --output text

# Scan every instance tagged Environment=prod for missing patches
aws ssm send-command \
  --document-name "AWS-RunPatchBaseline" \
  --targets "Key=tag:Environment,Values=prod" \
  --parameters "Operation=Scan"

# Open a shell with no inbound port (needs the Session Manager plugin)
aws ssm start-session --target i-0123456789abcdef0

# Store an encrypted value and read it back
aws ssm put-parameter --name /myapp/prod/license-key --type SecureString --value EXAMPLE_LICENSE_KEY
aws ssm get-parameter --name /myapp/prod/license-key --with-decryption
```

> [!IMPORTANT]
> **Exam Question Pattern for Systems Manager**:
> - Look for keywords: *"Centrally view, manage, and operate nodes (EC2 instances and on-premises servers)"*, *"automate OS patching"*, *"run commands at scale"*, *"manage fleet"*.
> - **SSM Agent**: Must be installed on the EC2 or on-premises server for Systems Manager to manage it.
> - **Capabilities**:
>   - **Fleet Manager**: Centrally view server inventory and health.
>   - **Patch Manager**: Automate operating system patch deployments.
>   - **Run Command**: Execute scripts remotely across thousands of servers without SSH.
>   - **Session Manager**: Open a browser shell session into EC2 without opening inbound SSH ports (port 22) or managing bastion hosts.
>   - **Parameter Store**: Store configuration values and secrets (can encrypt with KMS).

> Practice this section: [5 questions on Management, Governance & Developer Tools](practice-questions/05-management-governance-developer-tools.md)

---

## 6. 🤝 AWS Shared Responsibility Model

- 🎥 **Video Sections**:
  - [4:01:33 - Introduction to Shared Responsibility Model](https://www.youtube.com/watch?v=7HKot-brXFE&t=14493s)
  - [4:02:33 - AWS Shared Responsibility Model](https://www.youtube.com/watch?v=7HKot-brXFE&t=14553s)
  - [4:06:04 - Types of Cloud Responsibilities](https://www.youtube.com/watch?v=7HKot-brXFE&t=14764s)
  - [4:08:22 - Shared Responsibility for Compute](https://www.youtube.com/watch?v=7HKot-brXFE&t=14902s)

### 6.1 The Core Model: "OF" vs. "IN" the Cloud

#### Detailed notes

The **AWS Shared Responsibility Model** divides security and compliance work between AWS and you. AWS is responsible for **security of the cloud**: protecting the hardware, software, networking, and facilities that run AWS services, from the host operating system and virtualization layer down to the physical security of the data centers. Third-party auditors regularly test and verify this side as part of the AWS compliance programs. You are responsible for **security in the cloud**, and how much that covers depends on the services you choose. On EC2 it includes the guest operating system and its patches, software you install, and the security group firewall. Even on the most managed services you still manage your data, including its encryption options, and the IAM permissions you grant.

| Situation | Responsible | Layer |
| :--- | :--- | :--- |
| A fire or power failure at a data center | AWS | Facilities |
| A flaw in the hypervisor under your instances | AWS | Virtualization layer |
| An unpatched guest operating system on an EC2 instance | You | Guest operating system |
| A security group that opens SSH to the whole internet | You | Firewall configuration |
| A bucket policy that makes private files public | You | Data and permissions |
| An access key posted in a public repository | You | IAM credentials |

#### In practice

AWS builds and runs S3, and by default new buckets, access points, and objects do not allow public access. Whatever you change after that is your configuration: a bucket policy can open a bucket to the world, and S3 Block Public Access settings can override such a policy. Requiring encrypted connections is another customer-side choice, made with a policy like this one.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "DenyRequestsWithoutTLS",
      "Effect": "Deny",
      "Principal": "*",
      "Action": "s3:*",
      "Resource": [
        "arn:aws:s3:::my-example-bucket",
        "arn:aws:s3:::my-example-bucket/*"
      ],
      "Condition": {
        "Bool": { "aws:SecureTransport": "false" }
      }
    }
  ]
}
```

This bucket policy denies every request to the bucket and its objects that does not use TLS.

> [!IMPORTANT]
> **Golden Rule**:
> - **AWS is responsible for security OF the cloud** (facilities, hardware, hypervisors, global infrastructure).
> - **Customer is responsible for security IN the cloud** (customer data, IAM users, passwords, guest OS, network configuration).

```mermaid
graph TB
    subgraph CustomerResponsibility ["Customer: Security IN the Cloud"]
        C1["Customer Data (Classification & Encryption)"]
        C2["Identity and Access Management (IAM Users, Passwords, MFA)"]
        C3["Guest Operating System Patches & Updates (EC2)"]
        C4["Network & Firewall Configuration (Security Groups, NACLs)"]
        C5["Application Code & Dependencies"]
    end
    subgraph AWSResponsibility ["AWS: Security OF the Cloud"]
        A1["Physical Security of Data Centers (Security guards, biometrics, cameras)"]
        A2["Hardware Infrastructure (Servers, disks, networking cables)"]
        A3["Virtualization Layer / Hypervisors (AWS Nitro, Xen)"]
        A4["Global Infrastructure (Regions, AZs, Edge Locations)"]
        A5["Decommissioning & Physical Destruction of Storage Drives"]
    end
```

---

### 6.2 Shared Responsibility Across Service Models

#### Detailed notes

The split of responsibility between AWS and you changes with the type of service, because AWS runs more of the stack for some services than for others. AWS describes three kinds of service. With **infrastructure services** such as Amazon EC2, AWS secures the underlying infrastructure, and you manage the guest operating system, its patches, the software you install, and the security group firewall. With **container services**, AWS also manages the operating system and the platform layer, and you manage your data and the firewall rules that control access to the service, such as the security groups on an RDS database. AWS's older security whitepaper gives Amazon RDS, Amazon EMR, and AWS Elastic Beanstalk as examples, and current AWS guidance gives Amazon ECS, Amazon EKS, and AWS Fargate. With **abstracted services** such as Amazon S3 and Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and the platform. You use the service endpoints and manage your data, its encryption options, your asset classification, and IAM permissions. Some AWS guidance calls this last group serverless services.

| Service | AWS runs | You run |
| :--- | :--- | :--- |
| Amazon EC2 | Facilities, hardware, virtualization | Guest OS and patches, installed software, security groups, data, IAM |
| Amazon ECS on AWS Fargate | The compute infrastructure, including its patching | Network configuration, container images, storage encryption, IAM |
| Amazon RDS | Hardware, operating system, and patch releases | Maintenance windows and applying updates, security groups, encryption, database users, data |
| AWS Lambda | Infrastructure and managed runtimes, patched automatically in Auto mode | Function code and dependencies, IAM, the runtime update mode |
| Amazon S3 and DynamoDB | Infrastructure, operating system, platform | Data, encryption options, asset classification, IAM |

> [!NOTE]
> Update (2026): AWS's current guidance splits patching for managed services by tenancy. For single-tenant services such as RDS, ElastiCache, and OpenSearch Service, AWS releases patches and you choose maintenance windows and apply the updates. For multi-tenant services such as DynamoDB and S3, AWS applies patches with no action from you. See the [Well-Architected Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/shared-responsibility.html).

#### In practice

The same chore, keeping software patched, falls to a different owner in each service. On EC2 you patch the guest operating system, for example with Systems Manager Patch Manager. On RDS, AWS releases the patches and you set the maintenance window. Operating system updates are either optional, which wait until you apply them, or mandatory, which RDS applies automatically in a maintenance window after their apply date. On Lambda, AWS patches managed runtimes automatically when the runtime update mode is Auto. A function packaged as a container image works differently: AWS publishes updated base images, and you rebuild and redeploy the function.

```bash
# EC2: you run the patching
aws ssm send-command \
  --document-name "AWS-RunPatchBaseline" \
  --targets "Key=tag:Environment,Values=prod" \
  --parameters "Operation=Install"

# RDS: AWS releases patches, you choose when they apply
aws rds modify-db-instance \
  --db-instance-identifier my-example-db \
  --preferred-maintenance-window "Sun:05:00-Sun:06:00"

# Lambda: AWS patches the managed runtime
aws lambda put-runtime-management-config \
  --function-name my-function \
  --update-runtime-on Auto
```

| Responsibility Area | Infrastructure as a Service (e.g., EC2) | Platform as a Service (e.g., Elastic Beanstalk, RDS) | Serverless / SaaS (e.g., Lambda, S3, DynamoDB) |
| :--- | :--- | :--- | :--- |
| **Physical Facilities & Data Centers** | **AWS** | **AWS** | **AWS** |
| **Hypervisor & Hardware Infrastructure** | **AWS** | **AWS** | **AWS** |
| **Guest OS Installation & Patching** | **Customer** | **AWS** | **AWS** |
| **Database Engine Patching** | **Customer** *(if DB is on EC2)* | **AWS** *(RDS automates patches during maintenance window)* | **AWS** |
| **Application Runtime (Python/Node)** | **Customer** | **AWS** | **AWS** |
| **Application Code** | **Customer** | **Customer** | **Customer** |
| **Firewall & Security Group Rules** | **Customer** | **Customer** | **Customer** |
| **IAM User Policies & Access Management** | **Customer** | **Customer** | **Customer** |
| **Customer Data Encryption** | **Customer** | **Customer** | **Customer** |

---

### 6.3 Shared Controls Matrix

#### Detailed notes

**Shared controls** apply to both the infrastructure layer that AWS runs and the layer you run, but in separate contexts. AWS provides the requirements for the infrastructure, and you provide your own implementation of the control within your use of AWS services. AWS describes two other control types. **Inherited controls** are ones you fully inherit from AWS, such as physical and environmental controls. **Customer specific controls** are solely yours and depend on the application you deploy, such as service and communications protection or zone security, which can require you to route or zone data within particular security environments. Patch management differs by service. On EC2 the guest operating system is yours to patch, while on managed services such as RDS, AWS releases patches and you decide when to apply them.

| Shared control | AWS | You |
| :--- | :--- | :--- |
| Patch management | Patches and fixes flaws within the infrastructure | Patch your guest operating system and applications |
| Configuration management | Maintains the configuration of its infrastructure devices | Configure your guest operating systems, databases, and applications |
| Awareness and training | Trains AWS employees | Train your own employees |

#### In practice

Sorting controls by type tells you what evidence to collect. Suppose a company hosts customer records on EC2 and S3 and an auditor asks how each control is met. For inherited controls, AWS Artifact provides on-demand downloads of AWS security and compliance reports, such as SOC and ISO reports, which you can hand to auditors as audit artifacts. AWS Artifact is free. Its documents describe AWS's side, and customers must develop or obtain their own documents that show the security and compliance of their company.

| Control the auditor asks about | Type | Evidence the company provides |
| :--- | :--- | :--- |
| Physical access to data centers | Inherited | AWS reports downloaded from AWS Artifact |
| Operating system patching on EC2 | Shared | Patch Manager compliance data for its instances, plus AWS reports for the infrastructure |
| Staff security training | Shared | The company's own training records |
| Routing customer data only through approved network zones | Customer specific | The company's VPC and subnet design documents |

- **Shared Controls**: Those that apply to both the infrastructure layer (AWS) and customer layer (Customer).
  1. **Patch Management**: AWS patches physical hosts; customer patches guest OS on EC2.
  2. **Configuration Management**: AWS configures physical network devices; customer configures security groups and virtual networks.
  3. **Awareness & Training**: AWS trains AWS employees; customer trains customer employees.

> Practice this section: [5 questions on AWS Shared Responsibility Model](practice-questions/06-shared-responsibility-model.md)

---

## 7. 💻 Compute Services

### 7.1 Amazon Elastic Compute Cloud (EC2) Overview & Families
- 🎥 **Video Sections**:
  - [4:20:29 - EC2 Overview](https://www.youtube.com/watch?v=7HKot-brXFE&t=15629s)
  - [6:50:21 - Introduction to EC2](https://www.youtube.com/watch?v=7HKot-brXFE&t=24621s)
  - [6:51:51 - EC2 Instance Families](https://www.youtube.com/watch?v=7HKot-brXFE&t=24711s)
  - [6:54:32 - EC2 Instance Types](https://www.youtube.com/watch?v=7HKot-brXFE&t=24872s)

#### Detailed notes

**Amazon Elastic Compute Cloud (EC2)** provides virtual servers, called instances, in the AWS Cloud. You launch an instance from an Amazon Machine Image (AMI), which holds the operating system and software, and you choose an **instance type**, which fixes the CPU, memory, storage, and network capacity. A security group acts as the instance's firewall, and a key pair gives you login access.

Instance types are grouped into **families** by the resource they favor. A name reads as series, generation, options, and size: in `m7g.2xlarge`, m is general purpose, 7 is the generation, g means AWS Graviton (Arm) processors, and 2xlarge is the size. T types are burstable: they earn CPU credits while CPU use stays under a baseline and spend them to burst above it. Instance store volumes live on the host and are erased when the instance stops, while EBS volumes survive a stop.

Pick the family by what limits the workload:

| Workload is limited by | Family | Example type |
| :--- | :--- | :--- |
| No single resource | General purpose (M, T) | m7g.large |
| CPU | Compute optimized (C) | c7i.large |
| Memory | Memory optimized (R, X, z, U) | r7g.large |
| Local storage speed | Storage optimized (I, D, H) | i4i.large |
| GPUs or ML chips | Accelerated computing (P, G, Trn, Inf) | g5.xlarge |
| Tightly coupled cluster jobs | HPC optimized (Hpc) | hpc7a.96xlarge |

#### In practice

Start with a general purpose type, watch how heavily it is used, and move to another family when one resource is the clear limit. AWS Compute Optimizer can recommend a type for an existing workload. To resize an EBS-backed instance, stop it, change the instance type, and start it again; the new type's rate applies from then on. A stopped instance has no usage charge, but its EBS volumes and any Elastic IP addresses keep billing, and terminating an instance deletes its root volume by default.

Four types with the same two vCPUs show how the families differ:

```bash
aws ec2 describe-instance-types \
  --instance-types t3.micro c7i.large m7g.large r7g.large \
  --query "InstanceTypes[].[InstanceType,VCpuInfo.DefaultVCpus,MemoryInfo.SizeInMiB]" \
  --output text | sort
```

```text
c7i.large    2     4096
m7g.large    2     8192
r7g.large    2    16384
t3.micro     2     1024
```

| Family Code | Instance Category | Best Use Case | Exam Clue |
| :--- | :--- | :--- | :--- |
| **T, M** | **General Purpose** | Web servers, dev environments, balanced compute/memory/networking. | *"Balanced compute, memory, and network resources"* |
| **C** | **Compute Optimized** | High-performance batch processing, gaming servers, scientific modeling. | *"Compute-intensive workloads requiring high CPU performance"* |
| **R, X, Z** | **Memory Optimized** | High-performance relational databases, in-memory caches, big data in RAM. | *"Memory-intensive workloads, in-memory databases"* |
| **I, D, H** | **Storage Optimized** | Sequential read/write to very large local datasets, data warehousing. | *"High sequential read/write IOPS to massive local storage"* |
| **P, G, Trn, Inf** | **Accelerated Computing** | Machine learning training and inference, graphics rendering, GPUs. | *"Workloads requiring hardware accelerators or GPUs"* |

> [!TIP]
> **EC2 Per-Second Billing Rule**: While EC2 instances can be billed per-second, there is a **60-second minimum charge**! If an instance runs for 30 seconds, it is billed for 60 seconds.

---

### 7.2 EC2 Tenancy: Shared vs. Dedicated Instances vs. Dedicated Hosts
- 🎥 **Video Sections**:
  - [6:56:19 - Dedicated Host vs Dedicated Instances](https://www.youtube.com/watch?v=7HKot-brXFE&t=24979s)
  - [6:58:26 - EC2 Tenancy](https://www.youtube.com/watch?v=7HKot-brXFE&t=25106s)

#### Detailed notes

**EC2 tenancy** controls whether other AWS accounts can run instances on the same physical server as yours. With shared tenancy, the default, several customers' instances run on one host and the hypervisor keeps them isolated. **Dedicated Instances** run on hardware that no other AWS account uses, even an account linked to the same payer, although that hardware can also run your own non-dedicated instances. **Dedicated Hosts** give you a whole physical server, with visibility into its sockets and cores and control over which instances land on it.

AWS states that Dedicated Instances and instances on Dedicated Hosts have no performance, security, or physical differences. The differences are visibility, control, and billing:

| | Shared (default) | Dedicated Instance | Dedicated Host |
| :--- | :--- | :--- | :--- |
| Other AWS accounts on the same server | Yes | No | Only accounts you share the host with |
| See sockets, cores, and host ID | No | No | Yes |
| Keep instances on the same server (affinity) | No | No | Yes |
| Billed per | Instance | Instance | Host |

Per-socket and per-core software licenses are the usual reason to choose a Dedicated Host, which supports them fully, including Windows Server, SQL Server, SUSE, and RHEL licenses, subject to the license terms. Dedicated Instances support licenses only in part, such as SQL Server licenses with License Mobility. You can pay for a Dedicated Host On-Demand, with a Dedicated Host Reservation (up to 70% off On-Demand host pricing), or through Savings Plans.

#### In practice

Choose shared tenancy unless a requirement says otherwise. A compliance rule that asks for hardware no other account uses points to Dedicated Instances. Licenses counted per socket or core, or a need to keep instances on one server over time, point to a Dedicated Host. You set tenancy per instance at launch, or for a whole VPC: a VPC with dedicated tenancy launches every instance as a Dedicated Instance. A Dedicated Host bills per second while it is allocated, whatever number of instances run on it, so release hosts you no longer use.

```bash
# Dedicated Instance: request dedicated tenancy at launch
aws ec2 run-instances --image-id ami-0abcdef1234567890 \
  --instance-type m5.4xlarge --placement Tenancy=dedicated

# Dedicated Host: allocate a server, then launch onto it
aws ec2 allocate-hosts --instance-type m5.4xlarge \
  --availability-zone us-east-1a --quantity 1
aws ec2 run-instances --image-id ami-0abcdef1234567890 \
  --instance-type m5.4xlarge \
  --placement Tenancy=host,HostId=h-0abcdef1234567890
```

A host allocated for one instance type has a fixed core count, which sets how many instances fit:

```text
Host allocated for m5.4xlarge: 48 physical cores
Each m5.4xlarge instance uses 8 cores
48 / 8 = up to 6 instances on the host
```

- **Shared (Default)**: Multiple customer VMs share the same physical server, securely isolated by the hypervisor.
- **Dedicated Instances**: Hardware is dedicated exclusively to your AWS account (no other customer VMs on that server).
- **Dedicated Hosts**: Physical server dedicated entirely to your account with full visibility into **physical sockets and cores**.
  - 🔑 **Exam Trigger**: Required when a question mentions **"Bring Your Own License (BYOL) for per-socket or per-core software licenses"** (e.g., Microsoft or Oracle licenses).

---

### 7.3 EC2 Pricing Models Matrix & Rules
- 🎥 **Video Sections**:
  - [7:42:00 - EC2 Pricing Models](https://www.youtube.com/watch?v=7HKot-brXFE&t=27720s)
  - [7:44:08 - On Demand](https://www.youtube.com/watch?v=7HKot-brXFE&t=27848s)
  - [7:45:43 - Reserved Instances (RI)](https://www.youtube.com/watch?v=7HKot-brXFE&t=27943s)
  - [7:53:28 - Standard vs Convertible RI](https://www.youtube.com/watch?v=7HKot-brXFE&t=28408s)
  - [7:55:54 - Spot Instances](https://www.youtube.com/watch?v=7HKot-brXFE&t=28554s)
  - [7:59:05 - Savings Plan](https://www.youtube.com/watch?v=7HKot-brXFE&t=28745s)

#### Detailed notes

**EC2 pricing models** trade commitment for a lower price. **On-Demand** has no commitment: you pay by the second for running instances. **Savings Plans** commit you to an amount of compute usage, in dollars per hour, for 1 or 3 years. **Reserved Instances** commit you to a specific instance configuration for the same terms; Standard ones can only be modified, while Convertible ones can be exchanged for another Convertible Reserved Instance. **Spot Instances** use spare EC2 capacity at up to 90% off On-Demand.

You pay the current Spot price, which EC2 sets and adjusts gradually with long-term supply and demand. When EC2 needs the capacity back, it interrupts the instance and sends a notice two minutes ahead on a best-effort basis. A hibernate interruption starts at once, with no two minutes of lead time, and a rebalance recommendation can arrive earlier than the notice.

A Savings Plan or Reserved Instance is a billing discount that applies to matching usage. It reserves no capacity, except a zonal Reserved Instance, which reserves capacity in one Availability Zone. Capacity is reserved with an On-Demand Capacity Reservation, which has no discount of its own and bills at the On-Demand rate whether or not instances run in it. Savings Plans and regional Reserved Instances can discount a Capacity Reservation.

| | Discount | Reserves capacity | Commitment | AWS can interrupt |
| :--- | :--- | :--- | :--- | :--- |
| On-Demand | None | No | None | No |
| Savings Plans | Yes | No | Dollars per hour, 1 or 3 years | No |
| Regional Reserved Instance | Yes | No | 1 or 3 years | No |
| Zonal Reserved Instance | Yes | Yes, in one AZ | 1 or 3 years | No |
| Spot | Up to 90% | No | None | Yes |
| On-Demand Capacity Reservation | None | Yes, in one AZ | None for immediate use | No |

> [!NOTE]
> Update (2026): AWS quotes Convertible Reserved Instances at up to 66% off On-Demand, with 54% as the average discount for a 3-year term, on its [pricing page](https://aws.amazon.com/ec2/pricing/reserved-instances/). Its [EC2 purchasing guide](https://docs.aws.amazon.com/decision-guides/latest/decision-guides/ec2-purchasing-options-aws-how-to-choose.html) calls Reserved Instances an older option, recommends replacing them with Savings Plans, and warns that newer instance families might not support them. The guide lists four Savings Plan types: Compute (up to 66%), EC2 Instance (up to 72%), SageMaker AI (up to 64%), and Database (up to 35%).

#### In practice

Cover the steady baseline with a Savings Plan, run the variable part On-Demand, and run work that can restart on Spot. A Savings Plan commits you to an hourly amount for the whole term, and an hour's unused commitment is not carried over, so set the commitment at or below your lowest steady usage. Savings Plans do not discount Spot usage. A Savings Plan bought by mistake can be returned if its hourly commitment is $100 or less, it was bought in the last 7 days, and the calendar month of the purchase has not ended. A return limit also applies.

Example with invented numbers, not AWS prices: an instance costs $0.10 per hour On-Demand, and a Savings Plan commitment of $0.06 per hour covers it. A year has 8,760 hours.

| Usage | Hours per year | On-Demand | Savings Plan |
| :--- | :--- | :--- | :--- |
| Runs 24 hours a day | 8,760 | $876.00 | $525.60 |
| Runs 12 hours a day | 4,380 | $438.00 | $525.60 |

The plan breaks even when the instance runs 60% of the hours, because $0.06 of commitment per hour is 60% of the $0.10 On-Demand rate.

| Pricing Model | Commitment | Discount | Best Exam Use Case | Risks / Limitations |
| :--- | :--- | :--- | :--- | :--- |
| **On-Demand** | None | 0% (Baseline) | Short-term, unpredictable workloads, testing, applications that cannot be interrupted. | Highest hourly cost. |
| **Savings Plans** | 1 or 3 Years ($/hr commitment) | Up to 72% | **Compute Savings Plans**: Most flexible across EC2 families, regions, OS, Fargate, and Lambda.<br/>**EC2 Instance Savings Plans**: Tied to instance family in a region. | Pay committed hourly rate regardless of whether resources are running. |
| **Standard Reserved Instances (RI)** | 1 or 3 Years | Up to 72% | Steady-state, predictable workloads with fixed capacity requirements. | Cannot change instance family or OS. |
| **Convertible Reserved Instances** | 1 or 3 Years | Up to 54% | Workloads requiring flexibility to change instance families, OS, or tenancy. | Slightly lower discount than Standard RI. |
| **Spot Instances** | None | **Up to 90%** | Fault-tolerant, stateless batch workloads, image rendering, background data processing. | AWS can terminate instances with a **2-minute warning** if capacity is needed back. |
| **Capacity Reservations** | Any duration | None (On-Demand rates) | Mission-critical workloads requiring a guarantee that EC2 capacity will be available in a specific AZ. | Charged whether you run instances into the reservation or not. |

---

### 7.4 Scaling & Load Balancing: ASG, ALB, NLB, GWLB
- 🎥 **Video Sections**:
  - [7:28:37 - Launch an ASG (Auto-Scaling Group)](https://www.youtube.com/watch?v=7HKot-brXFE&t=26917s)
  - [13:43:40 - ELB Variants](https://www.youtube.com/watch?v=7HKot-brXFE&t=49420s)

#### Detailed notes

**Elastic Load Balancing (ELB)** spreads incoming traffic across targets, such as EC2 instances, containers, and IP addresses, in one or more Availability Zones, and it sends requests only to healthy targets. An **Auto Scaling group (ASG)** keeps a set of EC2 instances between a minimum and a maximum size, replaces unhealthy instances, and adds or removes instances as demand changes. The two work together: instances the group launches register with the load balancer's target group, and instances it terminates are deregistered.

A group can be scaled manually, on a schedule, dynamically with a policy (target tracking, step, or simple), or ahead of demand with predictive scaling. It launches instances from a launch template. EC2 Auto Scaling has no additional charge; you pay for the instances and other resources it creates.

ELB has three current load balancer types: the **Application Load Balancer (ALB)**, the **Network Load Balancer (NLB)**, and the **Gateway Load Balancer (GWLB)**. The Classic Load Balancer is the previous generation, and AWS recommends migrating to a current type.

| | ALB | NLB | GWLB |
| :--- | :--- | :--- | :--- |
| OSI layer | 7, application | 4, transport | 3, network |
| Listens for | HTTP, HTTPS, gRPC | TCP, UDP, TLS | All IP packets |
| Routes on | URL path, host name, headers, query string, source IP | Protocol and port | Flows, each sent to one appliance |
| Addresses | DNS name | DNS name, plus one static IP per enabled AZ | Reached through Gateway Load Balancer endpoints |
| Typical use | Websites, APIs, containers | TCP or UDP services that need fixed IPs | Firewalls and inspection appliances |

> [!NOTE]
> Update (2026): A Network Load Balancer has one IP address per enabled Availability Zone, and an internet-facing one can use an Elastic IP address in each zone. Anycast static IP addresses belong to AWS Global Accelerator, not to the Network Load Balancer. See [Network Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/network-load-balancers.html).

#### In practice

A typical web tier puts an ALB in front of an ASG that spans at least two Availability Zones, so losing one zone leaves capacity running. With a target tracking policy you name a metric and a target value, and the group adds or removes instances to hold it. Set the group's health check type to ELB so that the group also replaces instances that fail the load balancer's health check; the EC2 status checks always stay on.

```text
Clients
   |
Application Load Balancer   (listener: HTTPS 443)
   |
Target group "web"          (health check: GET /health)
   |
+------------------ web-asg: min 2, desired 2, max 6 ------------------+
|  Availability Zone A                 Availability Zone B             |
|  [web instance]                      [web instance]                  |
+----------------------------------------------------------------------+
```

```bash
aws autoscaling create-auto-scaling-group \
  --auto-scaling-group-name web-asg \
  --launch-template LaunchTemplateName=web-template,Version='$Latest' \
  --min-size 2 --max-size 6 --desired-capacity 2 \
  --vpc-zone-identifier "subnet-0aaa1111,subnet-0bbb2222" \
  --target-group-arns TARGET_GROUP_ARN \
  --health-check-type ELB --health-check-grace-period 300

aws autoscaling put-scaling-policy \
  --auto-scaling-group-name web-asg \
  --policy-name keep-cpu-near-50 \
  --policy-type TargetTrackingScaling \
  --target-tracking-configuration '{"TargetValue": 50.0, "PredefinedMetricSpecification": {"PredefinedMetricType": "ASGAverageCPUUtilization"}}'
```

- **Auto Scaling Group (ASG)**: Automatically scales EC2 instances out or in based on demand metrics or schedules.
- **Application Load Balancer (ALB)**: Layer 7 (HTTP/HTTPS) traffic routing. Supports path-based (`/api`, `/images`) and host-based routing.
- **Network Load Balancer (NLB)**: Layer 4 (TCP/UDP) traffic routing. Ultra-low latency, handles **millions of requests per second**, supports static Anycast IPs. Ideal for gaming and financial applications.
- **Gateway Load Balancer (GWLB)**: Deploys and scales third-party virtual network appliances (firewalls, IDS/IPS).

---

### 7.5 Containers on AWS: ECS, EKS, Fargate, ECR
- 🎥 **Video Sections**:
  - [4:22:08 - VMs, Containers and Serverless](https://www.youtube.com/watch?v=7HKot-brXFE&t=15728s)
  - [9:03:02 - VMs vs Containers](https://www.youtube.com/watch?v=7HKot-brXFE&t=32582s)
  - [9:07:03 - Kubernetes](https://www.youtube.com/watch?v=7HKot-brXFE&t=32823s)
  - [9:11:06 - Container Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=33066s)

#### Detailed notes

A **container** packages an application with its libraries and settings so it runs the same way wherever it is started. Containers share the host's operating system kernel, whereas each virtual machine runs its own operating system, which makes containers smaller and quicker to start. A container image is the template, and a running copy of it is the container.

AWS splits container work into a registry, an orchestrator, and compute. **Amazon ECR** stores container images in private repositories controlled by IAM. **Amazon ECS** and **Amazon EKS** are orchestrators: they decide where containers run, restart failed ones, and scale them. **AWS Fargate** supplies serverless compute for both, so there are no EC2 instances to patch or scale. Costs follow the layers: ECR charges for stored data and transfer, EKS adds a per-cluster fee, and the compute (Fargate or EC2) is billed separately.

| | Amazon ECS | Amazon EKS |
| :--- | :--- | :--- |
| Orchestrator | AWS-native scheduler | Kubernetes, certified conformant |
| Workloads are described by | Task definitions, run as tasks and services | Kubernetes manifests, run as pods |
| Compute | Fargate, EC2 instances, ECS Managed Instances, on-premises with ECS Anywhere | Fargate, EC2 nodes, EKS Auto Mode, on-premises with Hybrid Nodes or EKS Anywhere |
| Choose it when | You want the simplest AWS-native option | You already run Kubernetes or want its ecosystem |

> [!NOTE]
> Update (2026): Amazon ECS Express Mode runs a container web application from an image and two IAM roles, and creates the Fargate service, load balancer, auto scaling, and networking for you. It has no extra charge beyond the resources it creates. See [Amazon ECS Express Mode](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/express-service-overview.html).

#### In practice

The usual path is to build an image, push it to ECR, describe it in a task definition, and run it as an ECS service on Fargate. Fargate tasks use the awsvpc network mode, so each task gets its own network interface, and CPU and memory must be a valid pair, such as 256 CPU units with 512 MiB. Fargate bills for the vCPU and memory a task requests, per second with a one-minute minimum for Linux. Fargate Spot runs interruption-tolerant tasks at a discount and gives a two-minute warning before stopping them.

```json
{
  "family": "my-app",
  "requiresCompatibilities": ["FARGATE"],
  "networkMode": "awsvpc",
  "cpu": "256",
  "memory": "512",
  "executionRoleArn": "arn:aws:iam::123456789012:role/ecsTaskExecutionRole",
  "containerDefinitions": [
    {
      "name": "web",
      "image": "123456789012.dkr.ecr.us-east-1.amazonaws.com/my-app:1.0",
      "essential": true,
      "portMappings": [{ "containerPort": 8080 }]
    }
  ]
}
```

```bash
aws ecr create-repository --repository-name my-app
aws ecr get-login-password --region us-east-1 | docker login \
  --username AWS --password-stdin 123456789012.dkr.ecr.us-east-1.amazonaws.com
docker build -t 123456789012.dkr.ecr.us-east-1.amazonaws.com/my-app:1.0 .
docker push 123456789012.dkr.ecr.us-east-1.amazonaws.com/my-app:1.0
# taskdef.json holds the task definition shown above
aws ecs register-task-definition --cli-input-json file://taskdef.json
aws ecs create-cluster --cluster-name my-cluster
aws ecs create-service --cluster my-cluster --service-name my-app \
  --task-definition my-app --desired-count 2 --launch-type FARGATE \
  --network-configuration "awsvpcConfiguration={subnets=[subnet-0aaa1111],securityGroups=[sg-0aaa1111],assignPublicIp=ENABLED}"
```

- **Amazon ECS**: AWS-native container orchestration service.
- **Amazon EKS**: Managed standard Kubernetes cluster control plane.
- **AWS Fargate**: **Serverless compute engine for containers**. Works with both ECS and EKS. Eliminates the need to provision, configure, or scale EC2 server instances.
- **Amazon ECR**: Fully managed Docker container registry to store and manage container images.

---

### 7.6 Serverless Compute: AWS Lambda
- 🎥 **Video Sections**:
  - [10:04:02 - Serverless Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=36242s)
  - [10:06:27 - What is Serverless?](https://www.youtube.com/watch?v=7HKot-brXFE&t=36387s)

#### Detailed notes

**AWS Lambda** is a serverless compute service that runs your code in response to events, with no servers for you to provision or manage. You upload a function as a zip file or a container image, choose a runtime and a memory size, and attach a trigger such as an S3 upload, an SQS message, an API Gateway request, or an EventBridge schedule. Lambda runs the function in an execution environment, adds environments as events arrive, and scales back to zero when they stop.

You pay for requests and for duration, which Lambda measures in milliseconds and weights by memory (GB-seconds). The monthly free tier is 1 million requests and 400,000 GB-seconds. New accounts can start with lower concurrency and memory quotas, which AWS raises automatically as you use Lambda. AWS documentation calls standard functions Event Functions; their limits are:

| Setting | Limit |
| :--- | :--- |
| Timeout | 900 seconds (15 minutes) |
| Memory | 128 MB to 10,240 MB; CPU scales with memory |
| Temporary storage (/tmp) | 512 MB to 10,240 MB |
| Package size | 50 MB zipped and 250 MB unzipped; container images up to 10 GB |
| Payload | 6 MB synchronous, 1 MB asynchronous |
| Concurrency | 1,000 per Region by default |

> [!NOTE]
> Update (2026): Since August 1, 2025, the duration Lambda bills includes the initialization (INIT) phase for all configurations, so cold-start setup time is billed ([AWS Compute Blog](https://aws.amazon.com/blogs/compute/aws-lambda-standardizes-billing-for-init-phase/)). Newer Lambda modes have other limits: Lambda Managed Instances allows up to 90 minutes for some invocations, and Lambda MicroVMs run up to 8 hours ([Lambda quotas](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html)).

#### In practice

Lambda suits short, stateless work that an event triggers, such as resizing an uploaded image or processing a queue message. Each invocation can land in a fresh execution environment, so keep state in S3 or DynamoDB, not in the function. Code outside the handler runs once per new environment, which makes it the place to create SDK clients. Memory is the tuning setting: 1,769 MB is about one vCPU, and a larger setting can shorten the run. A 512 MB function that runs for 200 ms uses 0.1 GB-seconds per call, so one million calls use 100,000 GB-seconds. A job that would run longer than 15 minutes in a standard function belongs on Fargate, Batch, or EC2.

```python
import urllib.parse

def lambda_handler(event, context):
    record = event["Records"][0]
    bucket = record["s3"]["bucket"]["name"]
    key = urllib.parse.unquote_plus(record["s3"]["object"]["key"])
    print(f"New object: s3://{bucket}/{key}")
```

S3 sends an event like this one (trimmed) when an object arrives, and the function above writes `New object: s3://my-example-bucket/photos/cat.jpg` to CloudWatch Logs:

```json
{"Records": [{"s3": {"bucket": {"name": "my-example-bucket"}, "object": {"key": "photos/cat.jpg"}}}]}
```

- Event-driven compute service running code in response to events without managing servers.
- **Key Exam Limits & Features**:
  - Maximum execution time: **15 minutes** per invocation.
  - Scales automatically from zero to thousands of parallel executions.
  - Billed strictly per request and execution duration in milliseconds.

---

### 7.7 Lightsail, Batch, App Runner & HPC
- 🎥 **Video Sections**:
  - [4:42:34 - High Performance Computing (HPC)](https://www.youtube.com/watch?v=7HKot-brXFE&t=16954s)

#### Detailed notes

**Amazon Lightsail** bundles virtual private servers, storage, managed databases, load balancers, and networking features for a low, predictable monthly price. You pick a blueprint (an operating system or an application such as WordPress) and a plan, and you can reach other AWS services through VPC peering. **AWS Batch** runs batch jobs: you define a job, submit it to a job queue, and Batch starts compute in a compute environment (EC2, Spot, or Fargate), runs the job, and scales the capacity back down. Batch has no charge of its own.

**AWS App Runner** deploys a container image or source code as a web app or API with no infrastructure to set up. **High performance computing (HPC)** means running jobs across many nodes that exchange data constantly, such as weather and fluid simulations. AWS offers HPC instance types, Elastic Fabric Adapter (EFA) networking for low-latency traffic between instances, cluster placement groups that pack instances close together in one Availability Zone, and Amazon FSx for Lustre for fast shared storage. Two services build and manage the clusters: AWS Parallel Computing Service (managed Slurm) and AWS ParallelCluster (open source).

| Service | Best for | You provide | Notes |
| :--- | :--- | :--- | :--- |
| Lightsail | Simple sites, blogs, small apps, test servers | A blueprint and a plan | Predictable monthly price |
| Batch | Many independent jobs, such as rendering | A job definition and a job queue | You pay for the compute it uses |
| App Runner | Container web apps and APIs | A container image or source repository | Closed to new customers since April 30, 2026 |
| Parallel Computing Service, ParallelCluster | Tightly coupled simulations | A cluster configuration | Slurm clusters; ParallelCluster is self-managed |

> [!NOTE]
> Update (2026): AWS App Runner stopped accepting new customers on April 30, 2026. Existing customers can keep using it, but AWS plans no new features and recommends Amazon ECS Express Mode for new container web apps. See [AWS App Runner availability change](https://docs.aws.amazon.com/apprunner/latest/dg/apprunner-availability-change.html).

#### In practice

Batch fits work that splits into many pieces. An array job submits one job definition with a size from 2 to 10,000, and each child job reads its index from AWS_BATCH_JOB_ARRAY_INDEX, which starts at 0, to pick its share. With 1,000 children that each render 100 frames, one submit call covers 100,000 frames. Spot capacity lowers the cost of jobs that can safely restart. For HPC, put the nodes of one job in a cluster placement group and use EFA-capable instances; neither has an extra charge. On Lightsail, the Bitnami-packaged WordPress, WordPress Multisite, LAMP, Nginx, and Node.js blueprints will be deprecated on November 19, 2026, after which you cannot pick them for new instances; choose the blueprints Lightsail packages itself. Existing instances keep running.

```bash
aws batch submit-job \
  --job-name render-frames \
  --job-queue my-queue \
  --job-definition render-job:1 \
  --array-properties size=1000
```

```python
import os

index = int(os.environ["AWS_BATCH_JOB_ARRAY_INDEX"])
first = index * 100
print(f"Rendering frames {first} to {first + 99}")
```

- **Amazon Lightsail**: Easiest way to launch a virtual private server (VPS) with bundled compute, storage, networking, and a predictable monthly price. Ideal for beginners, blogs, and simple websites.
- **AWS Batch**: Plans, schedules, and executes hundreds of thousands of batch computing jobs dynamically across EC2 and Spot instances.
- **AWS App Runner**: Fully managed service to deploy containerized web apps and APIs directly from source code or container images with zero infrastructure configuration.

> Practice this section: [5 questions on Compute Services](practice-questions/07-compute-services.md)

---

## 8. 🗄️ Storage Services

### 8.1 Storage Types Comparison (Block vs. File vs. Object)
- 🎥 **Video Sections**:
  - [5:12:18 - Types of Storage Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=18738s)

#### Detailed notes

AWS offers three storage types: **block storage**, a raw disk that you format and mount; **file storage**, a shared tree of folders and files; and **object storage**, a flat set of objects that you reach by key name through an API.

Block storage (Amazon EBS and the EC2 instance store) cuts data into fixed-size blocks. The operating system treats the volume as a local drive, so it can rewrite small pieces quickly, which suits boot volumes and database files. An EBS volume lives in a single Availability Zone.

File storage (Amazon EFS and Amazon FSx) keeps the folder structure on the storage side and shares it over NFS or SMB, so many servers see the same files at the same time.

Object storage (Amazon S3) stores each file as one object, with a key name and metadata, inside a bucket. S3 has no real folders: a key name such as reports/2026/q1.pdf is a single string, and the console groups keys that share a prefix into folders. A bucket has no size to provision, and you pay for the data you store.

| | Block | File | Object |
| :--- | :--- | :--- | :--- |
| Addressed by | Block on a volume | Path in a directory tree | Bucket and key name |
| Reached through | Attach, format, mount | Mount over NFS or SMB | HTTP API, SDK, or CLI |
| Shared by | One instance, except with EBS Multi-Attach | Many servers at once | Any number of clients |
| Changing data | Overwrite single blocks | Edit part of a file | Upload the whole object again |

> [!NOTE]
> Update (2026): [Amazon S3 Files](https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-files.html), generally available since April 7, 2026 and built on Amazon EFS, mounts an S3 general purpose bucket as an NFS file system on EC2, ECS, EKS, and Lambda. General purpose buckets can also be created in an [account regional namespace](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html), where the name ends in your account ID, the Region code, and -an.

#### In practice

The storage type decides how you attach it. A block volume is a device that you format and mount on one server. A file system is a network share that you mount on as many servers as need it. A bucket has no mount step: programs call the S3 API with a bucket name and a key name.

A web application can use all three. The operating system and database files sit on EBS, user uploads that every web server must see sit on EFS, and finished reports and backups sit in S3. A common mistake is using an EBS volume as the shared store for servers in different Availability Zones, because a volume attaches only to instances in its own zone. Another is putting a database that rewrites small pieces of data in S3, where every upload replaces a whole object.

```bash
# Block: format a new EBS volume and mount it as a local disk
sudo mkfs -t xfs /dev/nvme1n1
sudo mkdir /data
sudo mount /dev/nvme1n1 /data

# File: mount a shared EFS file system over NFS (needs the amazon-efs-utils package)
sudo mkdir /shared
sudo mount -t efs -o tls FILE_SYSTEM_ID:/ /shared

# Object: no mount, one API call per object
aws s3 cp q1.pdf s3://my-example-bucket/reports/2026/q1.pdf
```

| Storage Type | AWS Service | Access Protocol | Scope | Primary Use Case |
| :--- | :--- | :--- | :--- | :--- |
| **Block Storage** | **Amazon EBS** | Block protocol | Single AZ | OS boot drives, database data files |
| **File Storage** | **Amazon EFS** | POSIX / NFS | Multi-AZ | Linux shared file system for hundreds of EC2 instances |
| **File Storage (Windows)**| **Amazon FSx for Windows**| SMB protocol | Multi-AZ | Windows applications, Active Directory integration |
| **File Storage (HPC)** | **Amazon FSx for Lustre**| Lustre protocol | Subnet / AZ | High-throughput HPC, machine learning, S3 integration |
| **Object Storage** | **Amazon S3** | HTTP/HTTPS REST API | Regional (Globally unique names) | Static web assets, backups, big data lakes, raw media |

---

### 8.2 Amazon S3 Storage Classes & Lifecycle Management
- 🎥 **Video Sections**:
  - [5:14:55 - Introduction to S3](https://www.youtube.com/watch?v=7HKot-brXFE&t=18895s)
  - [5:16:47 - S3 Storage Classes](https://www.youtube.com/watch?v=7HKot-brXFE&t=19007s)
  - [5:24:38 - S3 - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=19478s)

#### Detailed notes

An **S3 storage class** sets how Amazon S3 stores an object, and it trades storage price against retrieval speed, retrieval fees, and resilience. S3 Standard is the default. Each class covered here is designed for 99.999999999% durability, but the two single-AZ classes, One Zone-IA and Express One Zone, do not survive the loss of their Availability Zone.

**S3 Intelligent-Tiering** moves each object between access tiers for you: to Infrequent Access after 30 days without access, to Archive Instant Access after 90 days, and back to Frequent Access when the object is accessed again. Objects under 128 KB are not monitored and stay in Frequent Access.

Objects in the Glacier Flexible Retrieval and Deep Archive classes are archived. A **restore** request creates a temporary copy that you can read once it is ready. All S3 Glacier classes live inside S3 and are separate from the older Amazon Glacier vault service.

**S3 Lifecycle** rules automate the moves. A rule selects objects by prefix, tag, or size and then transitions them to another class or expires them after a number of days. Transitions run one way, from Standard toward Deep Archive. Moving or deleting an object before its **minimum storage duration** still bills the rest of that period.

| Access pattern | Classes | Reads and fees |
| :--- | :--- | :--- |
| Frequent | S3 Standard, S3 Express One Zone | Millisecond reads. Express One Zone keeps data in one Availability Zone that you choose and answers in single-digit milliseconds. |
| Unknown or changing | S3 Intelligent-Tiering | Objects change tier on their own. No retrieval fee, and a small monitoring fee per object. |
| Infrequent, instant reads | S3 Standard-IA, S3 One Zone-IA, S3 Glacier Instant Retrieval | Millisecond reads, a per-GB retrieval fee, a 128 KB minimum billable size, and a minimum storage duration of 30 to 90 days. |
| Archive | S3 Glacier Flexible Retrieval, S3 Glacier Deep Archive | Restore first. Flexible Retrieval restores in about 1 minute to 12 hours depending on the tier, Deep Archive within 12 hours (Standard) or 48 hours (Bulk). |

> [!NOTE]
> Update (2026): [S3 Express One Zone](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html) stores objects in directory buckets in a single Availability Zone and is designed for 99.95% availability. [Lifecycle configurations](https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html) created or edited since September 2024 skip objects smaller than 128 KB by default; add an object size filter to include them.

#### In practice

A lifecycle configuration applies to existing and new objects that match its filter, and a typical rule moves logs or backups down the chain as they age. Each transition costs a request fee per object, so millions of tiny objects can cost more to move than they save, and objects under 128 KB stay put unless the rule has a size filter. An archived object stays archived after a restore: you pay for the archive and for the temporary copy until it expires.

```json
{
  "Rules": [
    {
      "ID": "age-out-logs",
      "Filter": { "Prefix": "logs/" },
      "Status": "Enabled",
      "Transitions": [
        { "Days": 30, "StorageClass": "STANDARD_IA" },
        { "Days": 90, "StorageClass": "GLACIER" },
        { "Days": 365, "StorageClass": "DEEP_ARCHIVE" }
      ],
      "Expiration": { "Days": 2555 }
    }
  ]
}
```

In this rule, objects under logs/ move to Standard-IA after 30 days, to Glacier Flexible Retrieval after 90 days, and to Deep Archive after 365 days. They are deleted after 2,555 days, about seven years.

```bash
aws s3api put-bucket-lifecycle-configuration \
  --bucket my-example-bucket \
  --lifecycle-configuration file://lifecycle.json

# Ask for a temporary copy of an archived object, kept for 7 days
aws s3api restore-object \
  --bucket my-example-bucket \
  --key logs/2026/01/app.log.gz \
  --restore-request '{"Days":7,"GlacierJobParameters":{"Tier":"Standard"}}'
```

> [!IMPORTANT]
> **Exam Question Pattern for S3 Storage Classes**:
> - *"Unknown or changing access patterns"* ➔ **S3 Intelligent-Tiering** (moves objects automatically, NO retrieval fee!).
> - *"Rarely accessed (once a quarter) medical records that require MILLISECOND retrieval"* ➔ **S3 Glacier Instant Retrieval**.
> - *"Archive where retrieval can take 3–5 hours"* ➔ **S3 Glacier Flexible Retrieval**.
> - *"Long-term archive (7–10 years for compliance) where 12–48 hour retrieval is acceptable, lowest cost"* ➔ **S3 Glacier Deep Archive**.
> - *"Secondary/reproducible backups where data loss during AZ destruction is acceptable to save 20% cost"* ➔ **S3 One Zone-IA**.

#### S3 Storage Classes Comparison Matrix:

| Storage Class | Availability | Durability | Min Duration | Retrieval Speed | Best Exam Use Case |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **S3 Standard** | 99.99% | 11 9's | None | Milliseconds | Frequently accessed web assets, active application data. |
| **S3 Intelligent-Tiering**| 99.9% | 11 9's | None | Milliseconds | Unknown or changing access patterns (no retrieval fee). |
| **S3 Standard-IA** | 99.9% | 11 9's | 30 days | Milliseconds | Long-term backups accessed infrequently but requiring rapid access. |
| **S3 One Zone-IA** | 99.5% | 11 9's (single AZ) | 30 days | Milliseconds | Reproducible secondary backups; saves 20% cost over Standard-IA. |
| **S3 Glacier Instant** | 99.9% | 11 9's | 90 days | **Milliseconds** | Archived data accessed quarterly that still requires immediate retrieval. |
| **S3 Glacier Flexible** | 99.99% | 11 9's | 90 days | 1–5 mins (expedited)<br/>3–5 hrs (standard) | Archives where immediate retrieval is not required. |
| **S3 Glacier Deep Archive**| 99.99% | 11 9's | 180 days | 12–48 hours | Lowest cost storage in AWS; 7–10 year regulatory compliance records. |

#### Key S3 Features:
- **S3 Default Encryption**: Since January 2023, all new objects uploaded to Amazon S3 are **automatically encrypted at rest with SSE-S3 by default** at no extra charge.
- **S3 Lifecycle Policies**: Automates transitioning objects to colder storage tiers (e.g., Standard ➔ Glacier after 90 days) or expiring (deleting) old versions.
- **S3 Versioning**: Preserves, retrieves, and restores every version of an object to protect against accidental overwrites or deletions.
- **S3 Object Lock**: Prevents objects from being deleted or overwritten for a fixed retention period (Write Once, Read Many / WORM compliance).
- **S3 Transfer Acceleration**: Speeds up long-distance uploads by routing data through Amazon CloudFront edge locations over the AWS private network.

---

### 8.3 Amazon EBS vs. EC2 Instance Store
- 🎥 **Video Sections**:
  - [5:40:09 - Elastic Block Store (EBS) - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=20409s)

#### Detailed notes

**Amazon EBS** (Elastic Block Store) provides network-attached block volumes for EC2 instances, and a volume keeps its data independently of any one instance. The **EC2 instance store** is temporary block storage on disks physically attached to the host server, so its data lasts only as long as the instance, and there is no extra charge for it.

EBS replicates a volume across several servers inside its Availability Zone, and the volume attaches only to instances in that zone. General Purpose SSD (gp3, gp2) and Provisioned IOPS SSD (io2 Block Express, io1) suit transactional work such as boot volumes and databases. Throughput Optimized HDD (st1) and Cold HDD (sc1) suit large sequential reads and writes and cannot be boot volumes. You can increase a volume's size and change its type and performance while it stays attached. A **snapshot** is an incremental backup that EBS stores in S3 and replicates across the Region's Availability Zones. AWS does not take snapshots for you.

Instance store volumes are fixed at launch and exist only on some instance types. They suit caches, buffers, scratch data, and data that you replicate across a fleet of instances.

| Event | EBS volume | Instance store volume |
| :--- | :--- | :--- |
| Instance is rebooted | Data stays | Data stays |
| Instance is stopped | Data stays | Data is lost |
| Instance is terminated | Root volume is deleted by default; other volumes stay by default | Data is lost |
| Underlying disk fails | Data is replicated inside the zone | Data on the failed disk is lost |

#### In practice

EBS bills for the size you provision whether or not the space is used, and a volume that outlives its instance keeps billing until you delete it. Because AWS does not back up volumes, schedule snapshots with Amazon Data Lifecycle Manager or AWS Backup. A snapshot also moves data between Availability Zones: restore it as a new volume in the target zone. Encrypting an existing unencrypted volume works the same way: snapshot it, then create a new encrypted volume from the snapshot. Use instance store only for data that you can recreate, since a stop, a termination, or a disk failure erases it.

```bash
# Create, attach, and back up a 100 GiB gp3 volume
aws ec2 create-volume --availability-zone us-east-1a --volume-type gp3 --size 100 --encrypted
aws ec2 attach-volume --volume-id VOLUME_ID --instance-id INSTANCE_ID --device /dev/sdf
aws ec2 create-snapshot --volume-id VOLUME_ID --description "before upgrade"

# Restore the snapshot as a new volume in another Availability Zone
aws ec2 create-volume --availability-zone us-east-1b --snapshot-id SNAPSHOT_ID --volume-type gp3
```

- **Amazon EBS**: Network-attached persistent block storage locked to a **single Availability Zone**. Data persists independently of the EC2 instance life. Point-in-time backups (**EBS Snapshots**) are stored redundantly on **Amazon S3**.
- **EC2 Instance Store**: Ephemeral (temporary) block storage physically attached to the host server. **Data is lost when the instance is stopped or terminated!** Used for buffers, scratch pads, and caching.

---

### 8.4 Amazon EFS vs. Amazon FSx
- 🎥 **Video Sections**:
  - [5:42:40 - Elastic File System (EFS) - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=20560s)

#### Detailed notes

**Amazon EFS** is a serverless, elastic file system that many Linux instances mount at once over NFS, and **Amazon FSx** is a family of managed file systems built on established file server software, each aimed at a different client or workload. EFS grows and shrinks as you add and remove files, so you never set a size. Regional file systems store data across multiple Availability Zones, and One Zone file systems use a single zone at lower resilience. EFS speaks NFS v4.1 and v4.0 and is not supported on Windows instances. Lifecycle management moves files that are rarely read to the Infrequent Access and Archive storage classes.

FSx offers four file systems. **FSx for Windows File Server** provides SMB shares and joins your Microsoft Active Directory. **FSx for Lustre** targets high-speed Linux workloads such as machine learning and high performance computing, and it can link to an S3 bucket. FSx for NetApp ONTAP and FSx for OpenZFS run NetApp ONTAP and OpenZFS as managed services, with snapshots and clones. For Windows File Server you set storage capacity, SSD IOPS, and throughput, and you can change them later.

| File system | Protocols | Clients | Typical use |
| :--- | :--- | :--- | :--- |
| EFS | NFS | Linux (Windows is not supported) | Shared content, home directories, web serving, containers |
| FSx for Windows File Server | SMB | Windows and Linux | Windows applications, Active Directory, home directories |
| FSx for Lustre | Lustre | Linux | Machine learning, HPC, media processing |
| FSx for NetApp ONTAP | NFS, SMB, iSCSI, NVMe | Linux, Windows, macOS | Moving NetApp file workloads, multi-protocol access |
| FSx for OpenZFS | NFS | Linux, Windows, macOS | Moving ZFS or Linux file servers |

#### In practice

EFS fits content that several Linux servers must read and write, such as uploads behind an Auto Scaling group, and it needs no capacity planning. You create the file system, add a mount target in each Availability Zone that has clients, allow NFS traffic from those clients in the mount target's security group, and mount it. A common mistake is trying to mount EFS on a Windows instance; use FSx for Windows File Server there. Data that already lives in S3 can also appear as files, either through an FSx for Lustre file system linked to the bucket or through Amazon S3 Files, which is built on EFS.

```bash
aws efs create-file-system \
  --performance-mode generalPurpose \
  --throughput-mode elastic \
  --encrypted \
  --tags Key=Name,Value=shared-content

aws efs create-mount-target \
  --file-system-id FILE_SYSTEM_ID \
  --subnet-id SUBNET_ID \
  --security-groups SECURITY_GROUP_ID

# Move files unread for 30 days to Infrequent Access, and back on first read
aws efs put-lifecycle-configuration \
  --file-system-id FILE_SYSTEM_ID \
  --lifecycle-policies TransitionToIA=AFTER_30_DAYS TransitionToPrimaryStorageClass=AFTER_1_ACCESS

# On each Linux client (needs the amazon-efs-utils package)
sudo mount -t efs -o tls FILE_SYSTEM_ID:/ /mnt/shared
```

- **Amazon EFS**: Fully managed POSIX NFS file system for Linux instances. Automatically grows/shrinks. Concurrently accessible across multiple AZs by thousands of EC2 instances.
- **Amazon FSx for Windows File Server**: Native Windows file storage built on Windows Server, fully compatible with SMB and Active Directory.
- **Amazon FSx for Lustre**: Ultra-high-performance file system designed for compute-heavy workloads (HPC, machine learning).

---

### 8.5 AWS Snow Family & Hybrid Storage Gateway
- 🎥 **Video Sections**:
  - [5:19:23 - AWS Snow Family](https://www.youtube.com/watch?v=7HKot-brXFE&t=19163s)

#### Detailed notes

The **AWS Snow Family** is a set of rugged devices that AWS ships to you to move large amounts of data to or from AWS offline, or to run compute at sites with little connectivity. Snowball Edge is the only Snow device left, and AWS is retiring it. It comes as a Storage Optimized model with 210 TB of usable NVMe storage and as a Compute Optimized model with 104 vCPUs and 28 TB of NVMe SSD for EC2-compatible instances. You order a job, AWS ships the device, you load or process data locally, and you ship it back.

**AWS Storage Gateway** solves a different problem. It connects on-premises applications to AWS storage through the protocols they already use (NFS, SMB, and iSCSI) and keeps a local cache for low latency. The gateway runs as a virtual machine on VMware ESXi, Hyper-V, KVM, or Nutanix AHV, or as an EC2 instance. AWS stopped offering the Storage Gateway Hardware Appliance on May 12, 2025.

| Gateway | Protocol | Where the data ends up | Typical use |
| :--- | :--- | :--- | :--- |
| S3 File Gateway | NFS, SMB | Objects in S3 | File shares for on-premises applications, with the objects readable from AWS |
| Volume Gateway | iSCSI | Cached: in S3, with hot data cached locally. Stored: on premises, with snapshots in S3 | Block volumes, backups, disaster recovery |
| Tape Gateway | iSCSI virtual tape library | Virtual tapes in S3, archived to Glacier Flexible Retrieval or Deep Archive | Replacing physical tape backups |
| FSx File Gateway | SMB | FSx for Windows File Server | Closed to new customers since October 28, 2024 |

> [!NOTE]
> Update (2026): AWS shut down Snowmobile on March 14, 2024 ([AWS services in full shutdown](https://docs.aws.amazon.com/general/latest/gr/full_shutdown_services.html)) and discontinued Snowcone and the older 80 TB Storage Optimized and 52 vCPU Compute Optimized Snowball Edge models on November 12, 2024. Snowball Edge has been closed to new customers since November 7, 2025, and AWS will end support for Snowball devices in all commercial Regions on December 31, 2026 ([AWS Snowball](https://aws.amazon.com/snowball/)). New customers are pointed to AWS DataSync for online transfers, AWS Data Transfer Terminal for physical transfers, and AWS Outposts for edge computing.

#### In practice

Start with arithmetic: divide the data size by the link speed that you can actually use. If the answer is weeks, move the data another way. AWS DataSync copies from NFS, SMB, HDFS, and object storage over the network, and it can run over a Direct Connect link. Data Transfer Terminal lets you upload from your own storage devices at an AWS site.

Storage Gateway suits the opposite case, where servers stay on premises and need cloud-backed storage with a local cache. A file share on S3 File Gateway turns each file into an S3 object, so lifecycle rules, replication, and other AWS services can use it. Size the cache disk for your working set, because reads of data that is not cached travel over the network.

```text
Example: copy 100 TB to AWS (round numbers)
100 TB = 8 x 10^14 bits

Link       Share of link used   Time
1 Gbps     100%                 about 9 days
1 Gbps      80%                 about 12 days
100 Mbps   100%                 about 93 days
```

```text
On premises                                       AWS Region
+-------------+   NFS or SMB   +------------+   HTTPS   +------------------+
| App servers | -------------> | S3 File    | --------> | S3 bucket        |
|             |                | Gateway VM |           | (one object per  |
+-------------+                | + cache    |           |  file)           |
                               +------------+           +------------------+
```

#### Snow Family (Physical Data Transfer Devices):
- **AWS Snowcone**: 8 TB usable storage; ruggedized, lightweight, can be battery-operated and air-dropped.
- **AWS Snowball Edge**: 80 TB Storage Optimized or 42 TB Compute Optimized with onboard EC2/Lambda computing for disconnected environments.
- **AWS Snowmobile**: 45-foot ruggedized shipping container truck for moving **up to 100 Petabytes (PB)** of data.

#### AWS Storage Gateway (Hybrid Storage):
- Seamlessly connects on-premises applications to AWS cloud storage.
- Types: File Gateway (NFS/SMB), Volume Gateway (iSCSI block storage), Tape Gateway (VTL for virtual tape backups).

> Practice this section: [5 questions on Storage Services](practice-questions/08-storage-services.md)

---

## 9. 📊 Database & Analytics Services

### 9.1 Database Types: Relational vs. NoSQL vs. In-Memory vs. Warehouse
- 🎥 **Video Sections**:
  - [5:52:46 - What is a database?](https://www.youtube.com/watch?v=7HKot-brXFE&t=21166s)
  - [5:54:16 - What is a data warehouse?](https://www.youtube.com/watch?v=7HKot-brXFE&t=21256s)
  - [5:55:47 - What is a key value store?](https://www.youtube.com/watch?v=7HKot-brXFE&t=21347s)
  - [5:57:30 - What is a document database?](https://www.youtube.com/watch?v=7HKot-brXFE&t=21450s)

#### Detailed notes

A **database** stores data in an organized form that applications can query, and the data model decides which AWS service fits. **Relational** databases keep rows in tables with a fixed schema, connect tables through keys, and answer SQL queries with joins and transactions, which suits orders and accounts (online transaction processing). **NoSQL** databases drop the fixed table layout and are built for a specific data shape, such as items looked up by ID, JSON documents, graphs, or time series. **In-memory** databases hold data in RAM and answer in microseconds, either as a cache in front of another database or as a durable primary store. A **data warehouse** stores tables by column so that analytic queries can scan a few columns across billions of rows (online analytical processing).

DynamoDB supports ACID transactions but has no JOIN operator, so you store data in the shape that the application reads it.

| Type | Data model | Typical workload | AWS services |
| :--- | :--- | :--- | :--- |
| Relational | Tables, fixed schema, SQL | Orders, accounts, inventory | RDS, Aurora |
| NoSQL | Key-value, document, wide-column, graph, time series | Carts, sessions, profiles, relationships | DynamoDB, DocumentDB, Keyspaces, Neptune, Timestream |
| In-memory | Key-value data in RAM | Caching, leaderboards, session stores | ElastiCache, MemoryDB |
| Data warehouse | Columnar tables, SQL | Reports and analytics over large datasets | Redshift |

> [!NOTE]
> Update (2026): Amazon QLDB, the ledger database, reached end of support on July 31, 2025 ([AWS services in full shutdown](https://docs.aws.amazon.com/general/latest/gr/full_shutdown_services.html)), and AWS published guides for moving ledgers to Aurora PostgreSQL ([AWS blog post](https://aws.amazon.com/jp/blogs/news/migration-from-amazon-qldb/), in Japanese). Amazon Timestream for LiveAnalytics has been closed to new customers since June 20, 2025, and AWS recommends that new customers evaluate [Timestream for InfluxDB](https://docs.aws.amazon.com/timestream/latest/developerguide/AmazonTimestreamForLiveAnalytics-availability-change.html).

#### In practice

The same order looks different in each model. A relational design splits customers and orders into two tables, and a query joins them when the page loads. A DynamoDB design stores the customer name and the line items inside the order item, so one read by order ID returns everything the page needs. A question that the item was not shaped for, such as total sales per product, needs a different design or another service.

Teams often combine models: a relational database as the system of record, ElastiCache in front of it for repeated reads, and Redshift for reporting so that heavy analytic queries do not slow the application. Running reports directly on the production relational database slows it down. Redshift is built for analytics, so it is a poor fit as the transactional database of an application.

```sql
SELECT c.name, o.order_id, o.total
FROM orders o
JOIN customers c ON c.customer_id = o.customer_id
WHERE o.order_id = 1001;
```

```json
{
  "order_id": 1001,
  "customer": { "customer_id": "C-17", "name": "Alex Example" },
  "items": [
    { "sku": "A-100", "qty": 2 },
    { "sku": "B-220", "qty": 1 }
  ],
  "total": 59.9
}
```

```mermaid
graph TD
    DB[AWS Database Portfolio]
    DB --> Relational["Relational (OLTP)<br/>Amazon RDS & Aurora<br/>Structured SQL"]
    DB --> NoSQL["NoSQL Key-Value / Document<br/>Amazon DynamoDB<br/>Schemaless, single-digit ms"]
    DB --> InMem["In-Memory Cache<br/>Amazon ElastiCache & MemoryDB<br/>Sub-millisecond"]
    DB --> Warehouse["Data Warehouse (OLAP)<br/>Amazon Redshift<br/>Petabyte columnar SQL"]
    DB --> Graph["Graph Database<br/>Amazon Neptune<br/>Highly connected data"]
```

---

### 9.2 Relational: Amazon RDS & Amazon Aurora (Multi-AZ vs. Read Replicas)
- 🎥 **Video Sections**:
  - [6:00:18 - Relational Database Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=21618s)
  - [6:10:53 - Relational Database Service (RDS) - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=22253s)

#### Detailed notes

**Amazon RDS** is a managed service that runs a relational database engine for you: MySQL, PostgreSQL, MariaDB, Oracle Database, Microsoft SQL Server, or IBM Db2. AWS installs and patches the database software and the operating system, takes backups, detects failures, and recovers, while you own the schema and the query tuning. **Amazon Aurora** is an AWS-built engine compatible with MySQL and PostgreSQL, managed through RDS. It keeps data in a shared cluster volume that grows automatically, with copies in three Availability Zones written synchronously to six storage nodes. A cluster can have up to 15 Aurora Replicas that share the volume and act as failover targets.

For the other RDS engines, availability and read scaling are separate features. A **Multi-AZ** DB instance deployment keeps a synchronous standby in a second Availability Zone and fails over to it automatically. The standby serves no queries, and failover typically takes 60 to 120 seconds. A Multi-AZ DB cluster deployment (MySQL and PostgreSQL) uses two readable standbys and typically fails over in under 35 seconds. A **read replica** is a read-only copy updated asynchronously. You create each one yourself, it can sit in another Region, and you can promote it to a standalone database. RDS for MySQL, MariaDB, and PostgreSQL allows up to 15 replicas per source.

| | Multi-AZ DB instance | Read replica |
| :--- | :--- | :--- |
| Purpose | Availability and automatic failover | Read scaling, reporting, disaster recovery |
| Replication | Synchronous | Asynchronous |
| Serves queries | No | Yes, read-only |
| Placement | Another Availability Zone in the same Region | Same Region or another Region |
| On failure | RDS fails over by itself | You promote the replica yourself |

> [!NOTE]
> Update (2026): The [Aurora user guide](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html) now says Aurora delivers up to 6x the throughput of stock MySQL and of stock PostgreSQL on similar hardware. Older material quotes 5x and 3x.

#### In practice

Use Multi-AZ for a production database that must survive the loss of an Availability Zone, and add read replicas when read queries or reports slow the primary. The two combine: a Multi-AZ primary with replicas for reporting. Replication to a replica is asynchronous, so it can return slightly stale data; watch the ReplicaLag metric. RDS does not add replicas on its own. Automated backups keep up to 35 days of history for point-in-time restore. The console defaults to 7 days, and the CLI defaults to 1. After a failover the endpoint name stays the same, but connections must be reopened.

With Aurora, adding a replica is quick because it attaches to the existing cluster volume, and failover to a replica typically completes in under 60 seconds. Aurora also comes as a serverless configuration that scales capacity with demand, and as Aurora DSQL, a serverless, PostgreSQL-compatible distributed database with active-active multi-Region clusters.

```bash
aws rds create-db-instance \
  --db-instance-identifier my-example-db \
  --engine postgres \
  --db-instance-class db.t3.micro \
  --allocated-storage 20 \
  --master-username dbadmin \
  --manage-master-user-password \
  --backup-retention-period 7 \
  --multi-az

aws rds create-db-instance-read-replica \
  --db-instance-identifier my-example-db-replica \
  --source-db-instance-identifier my-example-db

# Test a failover: reboot the primary and switch to the standby
aws rds reboot-db-instance \
  --db-instance-identifier my-example-db \
  --force-failover
```

```text
Application
  | reads and writes
  v
Primary (AZ a) --- async copy ---> Read replica (same Region or another Region)
  |                                  serves read-only queries, may lag
  | sync copy
  v
Standby (AZ b)
  serves no queries, takes over on failover
```

> [!IMPORTANT]
> **Definite Exam Question**: Multi-AZ vs. Read Replicas:
> - **RDS Multi-AZ**: High Availability & disaster recovery. Synchronously replicates data to a standby instance in a second AZ. Automatically fails over in <60 seconds. **Does NOT serve read traffic!**
> - **RDS Read Replicas**: Performance & scalability. Asynchronously replicates data to up to 15 read-only copies to offload read-heavy traffic.

- **Amazon Aurora**: Cloud-native relational database (MySQL & PostgreSQL compatible). 5x throughput of MySQL, 3x of PostgreSQL. Automatically replicates 6 copies of data across 3 AZs.

---

### 9.3 NoSQL: Amazon DynamoDB (Schemaless, Global Tables, DAX)
- 🎥 **Video Sections**:
  - [5:58:30 - NoSQL Database Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=21510s)

#### Detailed notes

**Amazon DynamoDB** is a serverless, fully managed NoSQL database that stores key-value and document data and responds in single-digit milliseconds at any scale. The only attributes you declare when you create a table are the primary key attributes: a partition key and, optionally, a sort key. Every other attribute is free-form, so two items in the same table can have different attributes. This is what **schemaless** means. DynamoDB encrypts all data at rest by default and keeps copies of each table in three Availability Zones.

Global tables and DAX each build on a plain table:

| | Table | Global table | DAX cluster |
| :--- | :--- | :--- | :--- |
| Adds | The data itself | Replicas of the table in several Regions | An in-memory cache in front of one table |
| Read latency | Single-digit milliseconds | Single-digit milliseconds in each Region | Microseconds on a cache hit |
| Writes | Handled in one Region | Accepted by any replica | Written to the table first, then to the cache |

**Global tables** are multi-active, so any replica serves reads and writes and there is no failover step between Regions. By default, changes replicate asynchronously, typically within a second. The availability SLA is 99.999%, against 99.99% for a single-Region table. **DynamoDB Accelerator (DAX)** is API-compatible with DynamoDB: you switch to the DAX client and point it at the cluster endpoint. DAX answers eventually consistent reads from memory, and strongly consistent reads pass through to the table.

> [!NOTE]
> Update (2026): Since June 2025 you can create a global table with multi-Region strong consistency instead of the default asynchronous replication. It uses exactly three Regions, and strongly consistent reads on any replica return the latest data. See the [AWS announcement](https://aws.amazon.com/about-aws/whats-new/2025/06/amazon-dynamo-db-global-tables-multi-region-strong-consistency-generally-available/).

#### In practice

DynamoDB suits workloads that look up items by key at high volume, such as shopping carts and game state. AWS recommends on-demand capacity mode for most workloads: it bills per request and scales with traffic. Provisioned mode, where you set reads and writes per second, fits steady workloads with predictable growth. You still design the table around your queries: there are no joins, and an item cannot exceed 400 KB. Ad hoc reporting across many tables fits Athena or Redshift better. A partition key with few distinct values, such as a country code, concentrates traffic on a few partitions, so choose a key with many values, such as a user ID.

The Players table below is created with only a key attribute. The two items then carry different attributes, and adding a replica in another Region is one more command.

```bash
aws dynamodb create-table \
  --table-name Players \
  --attribute-definitions AttributeName=PlayerId,AttributeType=S \
  --key-schema AttributeName=PlayerId,KeyType=HASH \
  --billing-mode PAY_PER_REQUEST
aws dynamodb wait table-exists --table-name Players

aws dynamodb put-item --table-name Players \
  --item '{"PlayerId": {"S": "p-1001"}, "Name": {"S": "Maya"}, "Level": {"N": "12"}}'
aws dynamodb put-item --table-name Players \
  --item '{"PlayerId": {"S": "p-1002"}, "Name": {"S": "Omar"}, "Guild": {"S": "Night Owls"}}'

aws dynamodb update-table --table-name Players \
  --replica-updates '[{"Create": {"RegionName": "eu-west-1"}}]'
```

> [!IMPORTANT]
> **Exam Question Pattern for Schemaless Data**:
> - When an exam question specifies: *"A mobile application requires a schemaless database where items can have different attributes..."* ➔ The correct answer is **Amazon DynamoDB**.
> - *Trap Alert*: Do NOT pick **Amazon Redshift**! Redshift is a relational columnar SQL data warehouse that requires strict schemas.

- **DynamoDB Key Features**:
  - Serverless NoSQL key-value and document database.
  - Consistent **single-digit millisecond latency**.
  - **Encrypted at rest by default**.
  - **DynamoDB Global Tables**: Multi-Region, multi-active (active-active) replication.
  - **DynamoDB Accelerator (DAX)**: Managed in-memory cache providing **microsecond** response times for read-heavy workloads.

---

### 9.4 In-Memory Caching: Amazon ElastiCache & MemoryDB
- 🎥 **Video Sections**:
  - [6:03:07 - Other Database Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=21787s)

#### Detailed notes

**In-memory caching** keeps frequently read data in RAM, so a read returns in microseconds instead of waiting on a database query. **Amazon ElastiCache** is the managed cache. It runs the Valkey, Redis OSS, or Memcached engine, either as a serverless cache that scales on its own or as a node-based cluster where you choose the node type and the number of nodes. The usual pattern puts ElastiCache in front of a database such as Amazon RDS: the application reads the cache first and queries the database only on a miss.

**Amazon MemoryDB** is a durable in-memory database that is compatible with Valkey and Redis OSS. It writes every change to a Multi-AZ transactional log, so it can be the primary data store with no separate database behind it. For DynamoDB, the matching cache is DAX, which fills its cache on reads, updates it on writes made through DAX, and expires entries after a time to live.

| | ElastiCache | MemoryDB |
| :--- | :--- | :--- |
| Role | Cache in front of another database | Primary database |
| Engines | Valkey, Redis OSS, Memcached | Valkey, Redis OSS |
| Durability | Data lives in memory, and the database behind it is the source of truth | Multi-AZ transactional log on every write |
| Latency | Microsecond reads and writes | Microsecond reads, single-digit millisecond writes |

> [!NOTE]
> Update (2026): AWS now calls the service Amazon MemoryDB, and it is compatible with Valkey as well as Redis OSS. On node-based clusters that run Valkey 9.0 or later with cluster mode enabled, ElastiCache can also persist writes to a Multi-AZ transactional log, a choice you make when you create the cluster. See the [MemoryDB overview](https://docs.aws.amazon.com/memorydb/latest/devguide/what-is-memorydb.html) and the [ElastiCache durability documentation](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/durability.html).

#### In practice

ElastiCache suits data that is read far more often than it changes and can be rebuilt from the source, such as session data and product catalog rows. In the cache-aside pattern, the application checks the cache, loads from the database on a miss, and stores the result with a time to live (TTL). The TTL caps how stale a value can get. The application owns this logic, so you write the invalidation rules yourself. A plain ElastiCache cache should not hold the only copy of your data. Choose MemoryDB when the data must survive node failures and you want in-memory speed for the primary store.

```python
import json
import redis  # the same client works with Valkey

cache = redis.Redis(host="my-cache.example.com", port=6379, ssl=True)

def get_product(product_id):
    key = f"product:{product_id}"
    cached = cache.get(key)
    if cached:
        return json.loads(cached)           # hit: no database call
    row = load_from_database(product_id)    # miss: slow path
    cache.setex(key, 300, json.dumps(row))  # keep for 300 seconds
    return row
```

- **Amazon ElastiCache**: Managed in-memory caching engine compatible with **Redis OSS, Valkey, and Memcached**. Placed in front of relational databases to cache frequent queries and deliver **sub-millisecond latency**.
- **Amazon MemoryDB for Redis**: Durable, in-memory primary database with multi-AZ transaction log persistence.

---

### 9.5 Analytics & Big Data: Redshift, Athena, Glue, EMR, QuickSight
- 🎥 **Video Sections**:
  - [6:21:42 - Redshift - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=22902s)
  - [10:36:23 - BigData and Analytics Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=38183s)
  - [10:40:44 - Amazon QuickSight](https://www.youtube.com/watch?v=7HKot-brXFE&t=38444s)
  - [11:08:22 - Introduction to Athena](https://www.youtube.com/watch?v=7HKot-brXFE&t=40102s)
  - [11:10:59 - Introduction to AWS Glue](https://www.youtube.com/watch?v=7HKot-brXFE&t=40259s)

#### Detailed notes

**AWS analytics services** are managed services that each handle one stage of turning raw data into reports. Amazon Kinesis covers streaming data: Kinesis Data Streams collects records in real time, Amazon Data Firehose delivers them to S3, Redshift, or OpenSearch Service without consumer code, and Amazon Managed Service for Apache Flink processes them with Java, Python, Scala, or SQL. **AWS Glue** is a serverless data integration service. Its crawlers infer the schema of your files and register it in the Data Catalog, and its ETL jobs clean and convert the data.

Three services then query or process the data. **Amazon Athena** runs SQL against files in S3 and bills for the queries you run. **Amazon Redshift** is a petabyte-scale data warehouse that stores data in columns and runs queries in parallel. **Amazon EMR** runs big data frameworks such as Spark and Hadoop on managed clusters. Amazon Quick Sight then draws dashboards from these sources.

| | Athena | Redshift | EMR |
| :--- | :--- | :--- | :--- |
| Data stays in | S3, queried in place | Redshift storage, plus S3 through Redshift Spectrum | S3 or the cluster's HDFS |
| Infrastructure | None, serverless | Serverless or provisioned clusters | EC2 clusters or EMR Serverless |
| You write | SQL | SQL | Spark, Hadoop, or other framework code |
| Fits | Ad hoc queries on files | Repeated BI queries that join large tables | Custom big data processing |

> [!NOTE]
> Update (2026): Amazon QuickSight evolved into Amazon Quick, an AI-powered service for automating tasks, analyzing data, building web applications, and conducting research. QuickSight continues as Amazon Quick Sight, a feature within Quick, and existing QuickSight APIs keep working. See the [Amazon Quick documentation](https://docs.aws.amazon.com/quicksight/latest/user/welcome.html).

#### In practice

By default, Athena SQL queries are billed by the amount of data they scan, so converting files to a columnar format such as Parquet, compressing them, and partitioning them by date all cut the cost. When many people run repeated dashboard queries that join large tables, loading the data into Redshift fits better. Use EMR when you need your own Spark or Hadoop code. Redshift is built for analytical queries over large data sets, so an application that updates single rows all day belongs on RDS, Aurora, or DynamoDB.

A clickstream pipeline might run in these steps:

| Step | Service | What happens |
| :--- | :--- | :--- |
| 1 | Kinesis Data Streams, then Amazon Data Firehose | Click events are collected and delivered to S3 as raw JSON files |
| 2 | Glue crawler | Registers the schema in the Data Catalog |
| 3 | Glue ETL job | Converts the JSON to partitioned Parquet files |
| 4 | Athena, Redshift, or EMR | Ad hoc SQL, repeated BI queries, or custom Spark jobs |
| 5 | Amazon Quick Sight | Dashboards on the results |

Once Glue has registered a table, Athena answers questions with plain SQL:

```sql
-- web_logs is a Glue Data Catalog table over Parquet files, partitioned by dt
SELECT status_code, COUNT(*) AS requests
FROM web_logs
WHERE dt = '2026-10-26'
GROUP BY status_code
ORDER BY requests DESC;
```

| Service | Category | 🔑 Exam Trigger Keyword |
| :--- | :--- | :--- |
| **Amazon Redshift** | Data Warehousing (OLAP) | *"Petabyte-scale, columnar storage, SQL analytics, BI reporting"* |
| **Amazon Athena** | Serverless SQL on S3 | *"Run interactive SQL queries directly against data in S3 without loading into a database"* |
| **AWS Glue** | Serverless ETL & Data Catalog | *"Discover data schemas with crawlers, transform and catalog data (ETL)"* |
| **Amazon EMR** | Big Data Processing Clusters | *"Managed Apache Spark, Hadoop, Presto big data clusters"* |
| **Amazon QuickSight** | Business Intelligence (BI) | *"Interactive dashboards, data visualizations, business reports, natural language query"* |
| **Amazon Kinesis** | Real-Time Streaming Data | *"Ingest and process real-time streaming clickstreams, IoT telemetry, video streams"* |

> Practice this section: [5 questions on Database & Analytics Services](practice-questions/09-database-analytics.md)

---

## 10. 🔌 Networking & Content Delivery

### 10.1 Amazon Virtual Private Cloud (VPC), Subnets & Gateways
- 🎥 **Video Sections**:
  - [6:28:32 - Networking Overview](https://www.youtube.com/watch?v=7HKot-brXFE&t=23312s)
  - [6:31:03 - Virtual Private Cloud (VPC) & Subnets](https://www.youtube.com/watch?v=7HKot-brXFE&t=23463s)

#### Detailed notes

**Amazon Virtual Private Cloud (VPC)** is a logically isolated virtual network in your AWS account where you launch resources such as EC2 instances. A VPC covers one Region and has an IPv4 address range written as a CIDR block, anywhere from /16 (65,536 addresses) to /28 (16 addresses). You divide that range into **subnets**, and each subnet sits in a single Availability Zone. AWS reserves five addresses in every subnet.

A subnet is public when its route table sends internet traffic (0.0.0.0/0) to an **internet gateway**, and private when it has no such route. An instance in a public subnet also needs a public IPv4 or IPv6 address before it can reach the internet. A **NAT gateway** lets instances in a private subnet start outbound connections while the internet cannot start connections to them. Every account has a default VPC in each Region.

| | Internet gateway | NAT gateway | Egress-only internet gateway |
| :--- | :--- | :--- | :--- |
| Direction | Two-way | Outbound only | Outbound only |
| Used for | Public subnets, IPv4 and IPv6 | IPv4 traffic from private subnets | IPv6 traffic from private subnets |
| Placed | Attached to the VPC | In a public subnet, with an Elastic IP address | Attached to the VPC |

> [!NOTE]
> Update (2026): Since November 2025 a NAT gateway can also be created in regional mode, which needs no public subnet and expands across Availability Zones as your workload grows. Zonal NAT gateways, the form in the table, still work. See the [regional NAT gateway documentation](https://docs.aws.amazon.com/vpc/latest/userguide/nat-gateways-regional.html).

#### In practice

A common layout has one public and one private subnet in each of two Availability Zones: load balancers and NAT gateways in the public subnets, application servers and databases in the private ones. Choose a CIDR block that does not overlap your other VPCs or your office network. VPC peering rejects overlapping ranges, and you cannot resize a CIDR block after you create it, although you can add secondary blocks. An instance in a private subnet cannot reach the internet even if it has a public IP address, because the subnet's route table has no route to the internet gateway. AWS charges an hourly rate for each public IPv4 address it assigns to you, in use or idle, and private addresses are free. A NAT gateway adds an hourly charge and a per-GB data processing charge.

| Subnet | Availability Zone | CIDR block | Route for 0.0.0.0/0 |
| :--- | :--- | :--- | :--- |
| public-a | us-east-1a | 10.0.0.0/24 | Internet gateway |
| public-b | us-east-1b | 10.0.1.0/24 | Internet gateway |
| private-a | us-east-1a | 10.0.10.0/24 | NAT gateway in public-a |
| private-b | us-east-1b | 10.0.11.0/24 | NAT gateway in public-b |

Every route table also has a local route for the VPC range, 10.0.0.0/16, so the subnets can reach each other. Each /24 subnet has 256 addresses, of which 251 are usable.

- **Amazon VPC**: Logically isolated virtual network dedicated to your AWS account.
- **Public Subnet**: Route table points to an **Internet Gateway (IGW)**. Resources have public IPs and can communicate bidirectionally with the internet.
- **Private Subnet**: No direct path to the internet.
- **NAT Gateway**: Placed in a **public subnet** to enable instances in private subnets to initiate outbound connections to the internet (for software/patch updates) while **blocking unsolicited inbound internet traffic**.

---

### 10.2 Security Groups vs. Network ACLs (NACLs)
- 🎥 **Video Sections**:
  - [6:32:42 - Security Groups vs NACLs](https://www.youtube.com/watch?v=7HKot-brXFE&t=23562s)
  - [6:33:59 - Security Groups vs NACLs - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=23639s)

#### Detailed notes

A **security group** is a stateful firewall attached to the network interface of a resource such as an EC2 instance. A **network ACL (NACL)** is a stateless firewall attached to a subnet. Stateful means that when a request is allowed in, the reply is allowed out automatically. With a stateless NACL, the reply needs a rule of its own.

Traffic that enters a subnet from outside passes the NACL first and then the security group of the instance it is going to. Security group rules only allow traffic, and when a resource has several groups their rules are combined. Each NACL rule has a number. AWS checks the rules from the lowest number up and stops at the first match, and a final rule shown as * denies anything that matched nothing else.

| | Security group | Network ACL |
| :--- | :--- | :--- |
| Attached to | Network interfaces, and a resource can have several groups | Subnets, and each subnet has exactly one NACL |
| Default one, created with the VPC | Allows traffic between members of the group and all outbound traffic | Allows all inbound and outbound traffic |
| New custom one | No inbound rules, so nothing gets in, and all outbound traffic allowed | Only the * rule, so it denies everything |
| Rule sources | A CIDR block, a prefix list, or another security group | A CIDR block only |

#### In practice

AWS recommends security groups as the main control and NACLs as a second layer, for example to deny one address or to act as a guard rail if an instance launches with the wrong security group. Because a NACL is stateless, an inbound HTTPS rule needs a matching outbound rule for the reply. The reply goes to a client-chosen (ephemeral) port, so allow a range such as 1024 to 65535. Number rules in steps of 10 or 100 so you can insert one later, and give a deny rule a lower number than the allow rule it must override. Do not open SSH (port 22) or RDP (port 3389) to 0.0.0.0/0. Allow your own address range instead.

This NACL serves HTTPS on a public subnet and blocks one abusive address:

| Direction | Rule | Protocol | Ports | Address | Action |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Inbound | 90 | All | All | 203.0.113.25/32 | DENY |
| Inbound | 100 | TCP | 443 | 0.0.0.0/0 | ALLOW |
| Outbound | 100 | TCP | 1024 to 65535 | 0.0.0.0/0 | ALLOW |
| Both | * | All | All | 0.0.0.0/0 | DENY |

Rule 90 is checked first, so 203.0.113.25 is refused even though rule 100 would allow it. The instance's security group needs one inbound rule, TCP 443 from 0.0.0.0/0, because replies leave automatically.

> [!IMPORTANT]
> **Definite Exam Question**: You WILL be asked how to block a specific IP address or compare statefulness!

| Feature | Security Group (SG) | Network Access Control List (NACL) |
| :--- | :--- | :--- |
| **Operating Level** | **Instance / ENI level** | **Subnet level** |
| **State Nature** | **Stateful**: Return traffic is automatically allowed. | **Stateless**: Return traffic must be explicitly allowed inbound and outbound. |
| **Rule Capabilities**| Supports **ALLOW rules only**. Implicit deny for everything else. | Supports both **ALLOW and DENY rules**. |
| **How to Block an IP**| **CANNOT explicitly deny an IP!** | **Can explicitly DENY a specific IP range.** |
| **Evaluation Order** | All rules evaluated before traffic is permitted. | Rules evaluated in **numerical order** (lowest number first). |

---

### 10.3 Hybrid Connectivity: Direct Connect, VPN & Transit Gateway
- 🎥 **Video Sections**:
  - [1:52:58 - AWS Direct Connect](https://www.youtube.com/watch?v=7HKot-brXFE&t=6778s)
  - [13:14:01 - AWS VPN](https://www.youtube.com/watch?v=7HKot-brXFE&t=47641s)

#### Detailed notes

**Hybrid connectivity** links your on-premises network to your VPCs. **AWS Site-to-Site VPN** builds IPsec-encrypted tunnels over the public internet, and each VPN connection has two tunnels. **AWS Direct Connect** is a dedicated fiber link between your network and an AWS Direct Connect location, so traffic bypasses the internet. You request a dedicated connection from AWS, and an AWS Direct Connect Partner provisions a hosted connection for you.

| | Site-to-Site VPN | Direct Connect |
| :--- | :--- | :--- |
| Path | Encrypted tunnels over the public internet | Dedicated private fiber |
| Speed | Up to 1.25 Gbps per tunnel, and up to 5 Gbps per large bandwidth tunnel on Transit Gateway or Cloud WAN | Dedicated ports of 1, 10, 100, or 400 Gbps, and hosted connections of 50 Mbps to 25 Gbps |
| Network behavior | Varies with the internet | More consistent than internet-based links |
| Encryption | IPsec on every connection | Off by default |
| Setup | Minutes | A port plus a physical cross connect at a Direct Connect location |

When more than two networks are involved, **AWS Transit Gateway** acts as a Regional hub. You attach VPCs, VPN connections, and Direct Connect gateways once, and the hub routes between all of them. By default one transit gateway supports 5,000 attachments. **VPC peering** connects two VPCs directly and is non-transitive: with A peered to B and B peered to C, traffic from A cannot reach C through B.

#### In practice

Start with a Site-to-Site VPN if you need connectivity quickly, since you can create one in minutes. Order Direct Connect when you need steady, high-volume throughput. Direct Connect bills for port hours plus outbound data transfer, and Transit Gateway bills per attachment per hour plus per GB processed. Give every VPC and your on-premises network non-overlapping CIDR blocks from the start: peering rejects overlaps, and VPCs on one Direct Connect gateway cannot overlap. Direct Connect does not encrypt traffic by default. To encrypt it, use MACsec on a 10, 100, or 400 Gbps dedicated connection, which protects the link to the Direct Connect location, or run an IPsec VPN over the connection.

```text
            Office or data center
              |               |
    Site-to-Site VPN     Direct Connect
    (encrypted tunnels)  (dedicated fiber)
              |               |
        +----------------------------+
        |      Transit Gateway       |
        +----------------------------+
           |          |          |
         VPC A      VPC B      VPC C
```

- **AWS Site-to-Site VPN**: IPsec encrypted tunnel established over the public internet between on-premises and AWS. Setup in minutes, cost-effective.
- **AWS Direct Connect (DX)**: Dedicated private physical fiber link bypassing the public internet. Consistent network throughput, lower egress fees, takes weeks to provision.
- **AWS Transit Gateway**: Central network transit hub connecting thousands of VPCs and on-premises networks (supports transitive routing).
- **VPC Peering**: Direct connection between two VPCs. **Non-transitive** (VPC A peering with B, and B with C does NOT allow A to communicate with C).

---

### 10.4 VPC Endpoints (Gateway vs. Interface / PrivateLink)
- 🎥 **Video Sections**:
  - [6:29:59 - Enterprise/Hybrid Networking Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=23399s)

#### Detailed notes

A **VPC endpoint** is a private connection from your VPC to an AWS service, or to a service hosted in another VPC, that needs no internet gateway, NAT device, or public IP address. Traffic stays on the AWS network. A **gateway endpoint** supports only Amazon S3 and Amazon DynamoDB. There is no charge for it, and it works through a route table entry that sends the service's prefix list to the endpoint.

An **interface endpoint**, powered by **AWS PrivateLink**, creates an elastic network interface with a private IP address in each subnet you choose. It reaches most AWS services, services offered by other AWS accounts, and AWS Partner SaaS products. It is billed per hour for each Availability Zone plus per GB of data processed. S3 and DynamoDB support both types, and you can use both in the same VPC.

| | Gateway endpoint | Interface endpoint |
| :--- | :--- | :--- |
| Services | S3 and DynamoDB | Most AWS services, other accounts' services, partner SaaS |
| Traffic reaches it through | A route table entry | A private IP address on a network interface in your subnet |
| Charge | None | Hourly per Availability Zone, plus per GB processed |
| Reachable from on premises | No | Yes, over Direct Connect or Site-to-Site VPN |
| Controlled by | Endpoint policy, plus the security groups and NACLs of your instances | Endpoint policy, plus a security group on the endpoint |

#### In practice

A gateway endpoint can lower your bill. A private subnet that reads S3 through a NAT gateway pays data processing charges for every gigabyte, and the same traffic through a gateway endpoint is free. A gateway endpoint works only in its own Region and only for the route tables you select, so subnets whose route tables you leave out keep using the public service endpoint. For services that support private DNS, an interface endpoint with private DNS enabled makes the normal service name resolve to the endpoint's private addresses, so application code does not change. Each Availability Zone you add to an interface endpoint adds an hourly charge. An endpoint policy limits what can be done through the endpoint, for example to a single bucket.

```bash
# Gateway endpoint for S3: free, adds a route to the chosen route table
aws ec2 create-vpc-endpoint \
  --vpc-id VPC_ID \
  --vpc-endpoint-type Gateway \
  --service-name com.amazonaws.us-east-1.s3 \
  --route-table-ids RTB_ID

# Interface endpoint for Secrets Manager: network interface in the subnet
aws ec2 create-vpc-endpoint \
  --vpc-id VPC_ID \
  --vpc-endpoint-type Interface \
  --service-name com.amazonaws.us-east-1.secretsmanager \
  --subnet-ids SUBNET_ID \
  --security-group-ids SG_ID \
  --private-dns-enabled
```

After the first command, the private subnet's route table looks like this. S3 requests match the prefix list route, which is more specific than 0.0.0.0/0, so they skip the NAT gateway.

```text
Destination    Target
10.0.0.0/16    local
0.0.0.0/0      nat-0abc1234567890def
pl-1a2b3c4d    vpce-0abc1234567890def   (S3 prefix list)
```

- Enables private connection from your VPC to supported AWS services without an Internet Gateway or NAT Gateway:
  - **Gateway Endpoint**: **Free**. Only supports **Amazon S3** and **Amazon DynamoDB**. Added as a route in your route table.
  - **Interface Endpoint (AWS PrivateLink)**: Hourly fee. Creates an Elastic Network Interface (ENI) with a private IP inside your subnet. Supports most AWS services and third-party SaaS.

---

### 10.5 Content Delivery & DNS: CloudFront & Route 53
- 🎥 **Video Sections**:
  - [6:47:36 - AWS CloudFront - Follow Along](https://www.youtube.com/watch?v=7HKot-brXFE&t=24456s)

#### Detailed notes

**Amazon CloudFront** is a content delivery network (CDN) that caches your content at edge locations around the world and serves each viewer from the location with the lowest latency. **Amazon Route 53** is the DNS service that points your domain name at your application. When a file is not in an edge cache, CloudFront fetches it from the origin you configured, such as an S3 bucket or a web server, and keeps a copy. By default a cached file expires after 24 hours.

Route 53 registers domain names, answers DNS queries, and checks the health of your resources. Each record has a routing policy, such as simple, weighted, latency, failover, or geolocation, that decides the answer. An **alias record** points a name at an AWS resource such as a CloudFront distribution or a load balancer. It works at the bare domain (example.com), where a CNAME cannot, and Route 53 does not charge for alias queries to AWS resources.

**AWS Global Accelerator** is a separate service that gives your application two static anycast IP addresses and sends traffic to the nearest healthy endpoint over the AWS network.

| | CloudFront | Global Accelerator | Route 53 |
| :--- | :--- | :--- | :--- |
| Job | Cache and deliver content from edge locations | Send traffic to the best healthy endpoint over the AWS network | Translate names to IP addresses |
| Entry point | A distribution domain name, or your own | Two static anycast IPv4 addresses | DNS records |
| Caches content | Yes | No | No |
| Protocols | HTTP and HTTPS | TCP and UDP | DNS |

> [!NOTE]
> Update (2026): CloudFront now has flat-rate pricing plans (Free, Pro, Business, and Premium) as an alternative to pay-as-you-go. Each plan has one monthly price per distribution and bundles the CDN with AWS WAF, DDoS protection, and Route 53 DNS. See [CloudFront pricing](https://aws.amazon.com/cloudfront/pricing/).

#### In practice

To serve a static site, keep the files in a private S3 bucket, put a CloudFront distribution in front of it, and use origin access control so that only CloudFront can read the bucket. Then create an alias record that points www.example.com at the distribution. CloudFront serves a cached copy until it expires, so after you change a file, either invalidate its path or give the new version a new file name. DNS answers are cached for the record's TTL as well, so lower the TTL before a planned cutover. Choose Global Accelerator when clients need fixed IP addresses or when the traffic is TCP or UDP. Route 53 answers weighted records in proportion to each record's weight divided by the sum of all the weights, and a weight of 0 stops traffic to that record.

To send 90 percent of queries for app.example.com to one address and 10 percent to another, create two weighted records in a change batch saved as weighted.json:

```json
{
  "Changes": [
    {
      "Action": "UPSERT",
      "ResourceRecordSet": {
        "Name": "app.example.com", "Type": "A", "SetIdentifier": "v1",
        "Weight": 90, "TTL": 60, "ResourceRecords": [{"Value": "203.0.113.10"}]
      }
    },
    {
      "Action": "UPSERT",
      "ResourceRecordSet": {
        "Name": "app.example.com", "Type": "A", "SetIdentifier": "v2",
        "Weight": 10, "TTL": 60, "ResourceRecords": [{"Value": "203.0.113.20"}]
      }
    }
  ]
}
```

```bash
aws route53 change-resource-record-sets \
  --hosted-zone-id ZONE_ID \
  --change-batch file://weighted.json
```

- **Amazon CloudFront**: Global Content Delivery Network (CDN) caching static and dynamic content at edge locations.
- **AWS Global Accelerator**: Uses 2 static Anycast IP addresses to route user traffic over the AWS global fiber backbone. Ideal for non-HTTP traffic (gaming, VoIP, TCP/UDP).
- **Amazon Route 53 Routing Policies**:
  - **Latency-Based**: Routes users to the AWS Region providing lowest network latency.
  - **Weighted**: Splits traffic by percentage (e.g., 90% to v1, 10% to v2).
  - **Geolocation**: Routes traffic based on the user's geographic location/country.
  - **Failover**: Active-passive automatic disaster recovery failover via health checks.

> Practice this section: [5 questions on Networking & Content Delivery](practice-questions/10-networking-content-delivery.md)

---

## 11. 🔐 Security, Identity & Compliance

### 11.1 AWS Identity and Access Management (IAM) Entities & PoLP
- 🎥 **Video Sections**:
  - [8:15:50 - AWS IAM](https://www.youtube.com/watch?v=7HKot-brXFE&t=29750s)
  - [8:17:13 - Anatomy of an IAM Policy](https://www.youtube.com/watch?v=7HKot-brXFE&t=29833s)
  - [8:39:05 - Principle-of-Least-Privilege (PoLP)](https://www.youtube.com/watch?v=7HKot-brXFE&t=31145s)

#### Detailed notes

**AWS Identity and Access Management (IAM)** is the free service that controls who can sign in to your AWS account and what each person or program is allowed to do. You create identities in IAM and give them permissions through policies.

| Entity | What it is | Credentials |
| :--- | :--- | :--- |
| **IAM user** | One person or one application | Long-term: a password and up to two access keys |
| **IAM group** | A set of users that share permissions | None of its own. A user can belong to several groups, and groups cannot be nested |
| **IAM role** | An identity that a user, an application, or an AWS service can assume | Temporary credentials from AWS STS, valid for one hour by default and up to 12 hours |

AWS recommends that people sign in through IAM Identity Center or another identity provider and that workloads use roles, which leaves IAM users and access keys for the few cases that need them.

A policy is a JSON document. Each statement has an effect (Allow or Deny), the actions and resources it covers, and optional conditions. Apart from the root user, every identity starts with no permissions: a request is denied unless a policy allows it, and an explicit Deny beats any Allow. The **principle of least privilege (PoLP)** means granting only the permissions a task needs and removing them once they are no longer used.

The credential report is a CSV file that lists every user with the status of their password, access keys, and MFA device. You can generate a new one every four hours. IAM Access Analyzer reports resources that are shared outside your account. Its unused access analyzer, which is billed, also reports roles, access keys, and permissions that nobody uses.

#### In practice

Attach policies to groups and roles, and give an EC2 instance or a Lambda function a role so that no access keys are stored on it. Start with no permissions and add what the task needs. This identity-based policy lets a reporting job read one folder of one bucket:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::my-example-bucket"
    },
    {
      "Effect": "Allow",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-example-bucket/reports/*"
    }
  ]
}
```

It allows listing the bucket and reading objects under reports/. Writes and deletes fall under the default deny. An identity-based policy has no Principal element because the identity it is attached to is the principal; resource-based policies such as bucket policies and role trust policies name one.

Common mistakes are attaching AdministratorAccess to get something working, sharing one user between several people, and leaving old access keys active. The credential report shows users without MFA and access keys that have not been used for months:

```bash
aws iam generate-credential-report
aws iam get-credential-report --query Content --output text | base64 --decode > credential-report.csv
```

- **IAM User**: Identity with long-term credentials (password, access keys).
- **IAM Group**: Collection of users. (Groups cannot be nested).
- **IAM Role**: Identity with **temporary credentials** assumed by users, applications, or AWS services (e.g., an EC2 instance role reading from S3 — no hardcoded access keys!).
- **IAM Credential Report**: Downloadable CSV report listing all account users and the exact status of their passwords, access keys, and MFA devices.
- **IAM Access Analyzer**: Identifies resources (S3 buckets, IAM roles) that are shared with external AWS accounts.
- **Principle of Least Privilege (PoLP)**: Grant only the bare minimum permissions necessary to complete the task.

---

### 11.2 AWS IAM Identity Center, Cognito & Directory Service
- 🎥 **Video Sections**:
  - [8:07:52 - Directory Service](https://www.youtube.com/watch?v=7HKot-brXFE&t=29272s)
  - [8:11:46 - Single-Sign-On (SSO)](https://www.youtube.com/watch?v=7HKot-brXFE&t=29506s)
  - [8:44:42 - AWS IAM Identity Center](https://www.youtube.com/watch?v=7HKot-brXFE&t=31482s)

#### Detailed notes

**AWS IAM Identity Center** (formerly AWS Single Sign-On) gives your workforce one sign-in for many AWS accounts and business applications, at no extra cost. People log in once, pick an account and a role, and receive temporary credentials, so you do not need an IAM user for each person in each account. Users and groups come from the built-in Identity Center directory, an Active Directory, or an external identity provider such as Okta or Microsoft Entra ID. You give them access to accounts through **permission sets**, which define the permissions for a job function and can be assigned across many accounts.

Customers of your own application and workloads that need Active Directory are covered by two other services.

| Service | Who it is for | What it does |
| :--- | :--- | :--- |
| **Amazon Cognito** | Customers of your web or mobile app | A user pool handles sign-up and sign-in, including social and SAML or OIDC sign-in, and issues tokens. An identity pool exchanges a token for temporary AWS credentials |
| **AWS Directory Service** | Windows and LDAP workloads | **AWS Managed Microsoft AD** runs a real Active Directory in AWS. AD Connector forwards sign-in requests to your on-premises directory |

> [!NOTE]
> Update (2026): [Simple AD](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/simple-ad-availability-change.html), the Samba-based directory in Directory Service, closed to new customers on July 30, 2026. Existing directories keep working.

#### In practice

An administrator turns on IAM Identity Center in the AWS Organizations management account, which creates an organization instance, the only kind that can manage access to AWS accounts. The administrator then picks an identity source and assigns a group to an account with a permission set. A developer in that group opens the AWS access portal, chooses the account and role, and gets temporary credentials for the console or the CLI:

```bash
aws configure sso                       # one-time setup: start URL, Region, account, permission set
aws sso login --profile dev-readonly    # opens a browser for the sign-in
aws s3 ls --profile dev-readonly        # runs with temporary credentials, no access keys stored
```

Cognito is for the customers of your application and Identity Center is for your employees. Directory Service fits when an application needs a real Active Directory, such as SharePoint, or when you want to join Windows instances to a domain. A common mistake is creating an IAM user with long-term access keys in every account when Identity Center can hand out temporary credentials.

- **AWS IAM Identity Center (formerly AWS SSO)**: Recommended service to manage centralized workforce single sign-on access to multiple AWS accounts and business applications.
- **Amazon Cognito**: Customer (consumer) identity management for web/mobile apps (user sign-up, sign-in, social login with Google/Facebook).
- **AWS Directory Service**: Managed Microsoft Active Directory in the cloud.

---

### 11.3 Encryption & Secrets Management: KMS, CloudHSM, Secrets Manager, Parameter Store
- 🎥 **Video Sections**:
  - [12:47:17 - Encryption](https://www.youtube.com/watch?v=7HKot-brXFE&t=46037s)
  - [13:22:03 - AWS Key Management Service (KMS)](https://www.youtube.com/watch?v=7HKot-brXFE&t=48123s)
  - [13:25:30 - CloudHSM](https://www.youtube.com/watch?v=7HKot-brXFE&t=48330s)

#### Detailed notes

**AWS Key Management Service (KMS)** creates and controls the encryption keys that protect your data, and you can audit the use of your keys in AWS CloudTrail. Keys never leave KMS unencrypted, and the hardware that holds them is validated to FIPS 140-3 Security Level 3. KMS has three kinds of keys: AWS owned keys that a service uses behind the scenes, AWS managed keys that a service creates in your account (for example aws/s3), and customer managed keys that you create and control. Three related services cover other jobs.

| Service | Holds | Who controls it | Rotation |
| :--- | :--- | :--- | :--- |
| KMS | Encryption keys | AWS operates the hardware, and your policies decide who can use customer managed keys | Every year for AWS managed keys, optional for customer managed keys |
| **AWS CloudHSM** | Keys in your own single-tenant hardware security module | You manage the keys and users, and AWS cannot see the keys | You manage it |
| **AWS Secrets Manager** | Database credentials, API keys, tokens | IAM policies, with encryption by KMS | Built in, on a schedule |
| **Systems Manager Parameter Store** | Configuration values, optionally encrypted as SecureString | IAM policies, with KMS for SecureString values | None |

> [!NOTE]
> Update (2026): AWS managed keys rotate every year; the schedule was every three years until May 2022. Automatic rotation is optional for customer managed keys, defaults to 365 days once you enable it, and can use a custom period. See [Rotate AWS KMS keys](https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html) for on-demand rotation.

#### In practice

Many AWS services call KMS for you when you choose KMS encryption, for example in S3 and EBS. Choose CloudHSM when a rule or contract requires a dedicated hardware module that only you control. AWS handles the hardware, but you manage the keys and users, which is more work than KMS. Secrets Manager suits credentials that must rotate; it runs a Lambda function on the schedule you set. Parameter Store suits plain configuration such as an endpoint, and its standard tier is free. For passwords and tokens, AWS recommends Secrets Manager over a SecureString parameter.

```bash
KEY_ID=$(aws kms create-key --description "Orders data key" --query KeyMetadata.KeyId --output text)
aws kms enable-key-rotation --key-id "$KEY_ID"
aws secretsmanager create-secret --name prod/orders/db --secret-string file://db-credentials.json
aws ssm put-parameter --name /orders/prod/endpoint --type String --value orders.example.com
```

| Service | Architecture | 🔑 Exam Trigger Keyword |
| :--- | :--- | :--- |
| **AWS KMS** | Multi-tenant, managed cryptographic keys integrated across AWS services. | *"Create and manage encryption keys, integrated with CloudTrail"* |
| **AWS CloudHSM** | Dedicated single-tenant hardware security module under customer sole cryptographic control. | *"Dedicated hardware security module, FIPS 140-3 Level 3, sole control"* |
| **AWS Secrets Manager** | Securely stores secrets with **automatic credential rotation** (native RDS integration). | *"Store database credentials with automatic rotation"* |
| **Systems Manager Parameter Store** | Hierarchical key-value configuration storage (plaintext or SecureString). | *"Store configuration values and license keys, no rotation"* |

---

### 11.4 Threat Detection & Boundary Security (Shield, WAF, GuardDuty, Inspector)
- 🎥 **Video Sections**:
  - [13:04:50 - AWS Inspector](https://www.youtube.com/watch?v=7HKot-brXFE&t=47090s)
  - [13:07:21 - AWS Shield](https://www.youtube.com/watch?v=7HKot-brXFE&t=47241s)
  - [13:09:52 - AWS GuardDuty](https://www.youtube.com/watch?v=7HKot-brXFE&t=47392s)
  - [13:15:12 - AWS WAF](https://www.youtube.com/watch?v=7HKot-brXFE&t=47712s)

#### Detailed notes

**Threat detection and boundary security** services defend the edge of your application and watch your account for suspicious activity. Shield and WAF act on traffic. GuardDuty and Inspector only report what they find, and you can send those findings to EventBridge to start an automatic response.

| Service | Looks at | Result |
| :--- | :--- | :--- |
| **AWS Shield** | Traffic to your AWS resources | Blocks DDoS attacks at layers 3 and 4 (Standard) and adds layer 7 protection for resources you choose (Advanced) |
| **AWS WAF** | HTTP and HTTPS requests | Rules that allow, block, count, or challenge each request |
| **Amazon GuardDuty** | CloudTrail management events, VPC Flow Logs, and DNS logs | Findings about suspicious activity, such as stolen credentials or cryptomining |
| **Amazon Inspector** | EC2 instances, ECR container images, and Lambda functions | Findings about software vulnerabilities and unintended network exposure |

Shield Standard is on for every customer at no charge. Shield Advanced is a paid subscription with a one-year commitment. It protects only the resources you add, includes the Shield Response Team (which needs a Business or Enterprise Support plan) and DDoS cost protection, and covers the standard AWS WAF fees for those resources.

WAF attaches a web ACL, which the newer console calls a protection pack, to CloudFront distributions, Application Load Balancers, API Gateway REST APIs, and other entry points. GuardDuty reads its three sources by itself, so you do not set up the logs first, and optional protection plans add S3, EKS, runtime, malware, RDS, and Lambda monitoring.

#### In practice

Put Shield and WAF in front of the application, and run GuardDuty and Inspector alongside it. Shield Advanced protects nothing until you add a resource, or until AWS Firewall Manager adds it for you. A new account gets a 30-day GuardDuty free trial in each Region, and sample findings show what a finding looks like before anything real happens. Amazon Detective helps you investigate a finding by showing the related activity as a graph.

A WAF rule is a JSON object. This one blocks any IP address that sends more than 1,000 requests within the evaluation window, which is five minutes by default. Save it as rules.json and pass it to `aws wafv2 create-web-acl` with `--rules file://rules.json`.

```json
[
  {
    "Name": "RateLimitPerIP",
    "Priority": 0,
    "Statement": {
      "RateBasedStatement": { "Limit": 1000, "AggregateKeyType": "IP" }
    },
    "Action": { "Block": {} },
    "VisibilityConfig": {
      "SampledRequestsEnabled": true,
      "CloudWatchMetricsEnabled": true,
      "MetricName": "RateLimitPerIP"
    }
  }
]
```

> [!IMPORTANT]
> **Exam Question Pattern**: What Amazon Inspector does NOT do:
> - **Amazon Inspector**: Scans EC2 instances, ECR container images, and Lambda functions for **software vulnerabilities (CVEs)** and unintended network exposure.
> - **Trap Alert**: Inspector does **NOT** track configuration changes over time (that is **AWS Config**!).

- **AWS Shield Standard**: Free, automatic DDoS protection against Layer 3 & Layer 4 attacks for all AWS customers.
- **AWS Shield Advanced**: Paid ($3,000/mo) DDoS protection with 24/7 Shield Response Team (SRT) access, financial cost spike protection, and bundled AWS WAF.
- **AWS WAF**: Layer 7 Web Application Firewall filtering malicious HTTP/HTTPS traffic (SQLi, XSS, rate limiting).
- **Amazon GuardDuty**: Intelligent threat detection using machine learning on **CloudTrail events, VPC Flow Logs, and DNS logs**.
- **Amazon Detective**: Analyzes and visualizes the root cause of security findings from GuardDuty.

---

### 11.5 Governance & Compliance: AWS Artifact, Audit Manager, Macie, Security Hub
- 🎥 **Video Sections**:
  - [13:01:12 - Pen Testing](https://www.youtube.com/watch?v=7HKot-brXFE&t=46872s)
  - [13:02:02 - AWS Artifact](https://www.youtube.com/watch?v=7HKot-brXFE&t=46922s)
  - [13:27:11 - AWS Security Hub](https://www.youtube.com/watch?v=7HKot-brXFE&t=48431s)
  - [13:28:02 - AWS Audit Manager](https://www.youtube.com/watch?v=7HKot-brXFE&t=48482s)

#### Detailed notes

**Governance and compliance** services help you show that AWS and your own workloads meet a standard, and find what puts that at risk.

| Service | Answers | Covers |
| :--- | :--- | :--- |
| **AWS Artifact** | What evidence does AWS give about its own controls? | Downloadable SOC, ISO, and PCI reports and agreements such as the HIPAA Business Associate Addendum (BAA), free of charge |
| **AWS Audit Manager** | How do I collect evidence for my own audits? | Continuous evidence from your accounts, mapped to frameworks such as SOC 2, PCI DSS, HIPAA, and GDPR |
| **Amazon Macie** | Where is sensitive data in S3? | Personal data and credentials inside objects, and buckets that are public or shared |
| **AWS Security Hub** | Which security issues matter most across my accounts? | Findings from GuardDuty, Inspector, Macie, and Security Hub CSPM, correlated into exposures |

Artifact documents cover AWS's infrastructure and services. Evidence about your own configuration comes from other tools. Audit Manager collects evidence from CloudTrail, AWS Config, Security Hub checks, and service API calls, and assembles it into assessment reports for an auditor. Macie uses managed data identifiers, custom data identifiers that you write, and an automated discovery mode that samples your buckets. A new account gets a 30-day Macie free trial.

> [!NOTE]
> Update (2026): The original Security Hub, which checks resources against standards such as CIS and PCI DSS, is now [AWS Security Hub CSPM](https://docs.aws.amazon.com/securityhub/latest/userguide/what-are-securityhub-services.html). On December 2, 2025 AWS Security Hub became a unified service that correlates GuardDuty, Inspector, Macie, and CSPM findings into exposures. AWS Audit Manager is in [maintenance mode](https://docs.aws.amazon.com/audit-manager/latest/userguide/audit-manager-availability-change.html) and cannot be set up in new accounts from April 30, 2026; AWS points to AWS Config conformance packs instead.

#### In practice

To give an auditor AWS's SOC 2 or ISO 27001 report, open AWS Artifact in the console, find the report, accept its terms, and download it. You can accept an agreement such as the BAA for one account or for every account in an organization. The CLI shows the report steps:

```bash
aws artifact list-reports --query 'reports[].[id,name]' --output text
aws artifact get-term-for-report --report-id REPORT_ID                  # returns the terms and a term token
aws artifact get-report --report-id REPORT_ID --term-token TERM_TOKEN   # returns a download URL
```

Turn on Macie in each Region that holds S3 data. Security Hub CSPM needs AWS Config recording because most of its controls run as AWS Config rules. If the unified Security Hub is also enabled, it creates a service-linked recorder for you. CSPM reports only findings that appear after you enable it.

You can run penetration tests against your own EC2 instances, RDS databases, CloudFront distributions, Lambda functions, and the other permitted services without asking AWS first. DoS and DDoS attacks, DNS zone walking, and port, protocol, or request flooding are prohibited.

- **AWS Artifact**: Free on-demand portal to download AWS compliance reports (SOC 1/2/3, ISO 27001, PCI-DSS) and accept legal agreements like the HIPAA Business Associate Addendum (BAA).
- **Amazon Macie**: Uses machine learning to discover, classify, and protect **sensitive personal data (PII)** stored in Amazon S3.
- **AWS Security Hub**: Centralized Cloud Security Posture Management (CSPM) aggregating findings from GuardDuty, Inspector, Macie, and Firewall Manager.
- **AWS Audit Manager**: Automates evidence collection for regulatory compliance assessments.
- **Penetration Testing**: Customers can perform penetration tests on permitted services (EC2, RDS, Aurora, API Gateway) **without prior approval**. Prohibited: DNS zone walking, DoS/DDoS simulation, port flooding.
- **AWS Abuse Team (Trust & Safety)**: Contact if you suspect AWS resources are used for abusive purposes (spam, malware, port scanning).

> Practice this section: [5 questions on Security, Identity & Compliance](practice-questions/11-security-identity-compliance.md)

---

## 12. 🔄 Application Integration & Messaging

### 12.1 SQS vs. SNS vs. EventBridge vs. Kinesis
- 🎥 **Video Sections**:
  - [8:46:45 - Queueing and SQS](https://www.youtube.com/watch?v=7HKot-brXFE&t=31605s)
  - [8:47:55 - Streaming and Kinesis](https://www.youtube.com/watch?v=7HKot-brXFE&t=31675s)
  - [8:49:10 - Pub-Sub and SNS](https://www.youtube.com/watch?v=7HKot-brXFE&t=31750s)
  - [8:53:33 - Event Bus and Amazon EventBridge](https://www.youtube.com/watch?v=7HKot-brXFE&t=32013s)

#### Detailed notes

**Messaging and event services** pass data between parts of an application so the parts need not call each other and can scale and fail independently.

| | SQS | SNS | EventBridge (rules) | Kinesis Data Streams |
| :--- | :--- | :--- | :--- | :--- |
| Each message goes to | One consumer | Every subscriber | Every target of each matching rule | Every application that reads the stream |
| Kept for | 4 days by default, up to 14, or until deleted | Not stored; failed deliveries are retried for a limited time | Not kept, unless you add an archive | 24 hours by default, up to 365 days |

**Amazon SQS** holds messages in a queue until a consumer deletes them, so a queue absorbs bursts and lets workers run at their own pace. Standard queues deliver at least once and order messages on a best-effort basis. FIFO queues keep order within a message group and process each message once.

**Amazon SNS** publishes to a topic and pushes a copy to every subscriber: SQS queues, Lambda functions, HTTPS endpoints, email, SMS, mobile push, and Firehose. **Amazon EventBridge** matches events against rules and sends them to targets. AWS services send events to the default event bus, and you can add your own applications, SaaS partners, and schedules.

**Amazon Kinesis Data Streams** stores an ordered stream of records, so several applications can read it and replay it. Amazon Data Firehose (formerly Kinesis Data Firehose) loads streams into S3, Redshift, and other destinations, and Amazon Managed Service for Apache Flink (formerly Kinesis Data Analytics) analyzes them.

> [!NOTE]
> Update (2026): SQS messages can now be up to 1 MiB (it was 256 KiB), and SNS topics can be raised to 1 MiB. In September 2026 EventBridge [added a Custom Event Bus](https://aws.amazon.com/about-aws/whats-new/2026/09/eventbridge-relaunches-custom-event-buses/) that retains events, delivers them in order, and uses subscribers instead of rules, and the rules-based custom bus is now called "Custom Event Bus - Classic".

#### In practice

An online shop publishes each new order to an SNS topic. Two SQS queues subscribe to it, so billing and shipping each get a copy and work through it at their own pace. If the shipping workers stop, orders wait in their queue. A worker has 30 seconds by default (the visibility timeout) to delete a message after receiving it, or the message becomes visible again, so workers must cope with seeing a message twice. A dead-letter queue collects messages that keep failing, and long polling of up to 20 seconds cuts empty responses.

```text
order placed --> SNS topic "orders" --+--> SQS "billing-queue"  --> billing workers poll
                                      +--> SQS "shipping-queue" --> shipping workers poll

page clicks --> Kinesis data stream "clicks" --> analytics app A reads the stream
                                             --> analytics app B reads the same stream

EC2 instance stopped --> default event bus --> rule on source "aws.ec2" --> SNS topic "ops-alerts"
```

An SNS subscriber that is offline can miss messages once SNS gives up on the delivery, which is why an SQS queue usually sits between SNS and a worker. EventBridge retries a failed delivery for 24 hours by default. Kinesis in provisioned mode needs you to choose the number of shards, and on-demand mode scales for you.

| Service | Architecture | Model | 🔑 Exam Trigger Keyword |
| :--- | :--- | :--- | :--- |
| **Amazon SQS** | Message Queue | **Pull (Polling)** | *"Decouple application components, asynchronous queue, worker pool"* |
| **Amazon SNS** | Pub/Sub Topic | **Push (Fanout)** | *"Instant push notifications to multiple subscribers, email, SMS, mobile"* |
| **Amazon EventBridge** | Serverless Event Bus | **Rules & Routing** | *"Event-driven architecture, third-party SaaS integrations, scheduled cron events"* |
| **Amazon Kinesis** | Real-Time Streaming | **Stream ingestion** | *"Real-time high-throughput streaming clickstreams, IoT telemetry"* |

---

### 12.2 Orchestration & CI/CD: Step Functions, API Gateway, CodeDeploy, CodePipeline
- 🎥 **Video Sections**:
  - [8:51:18 - API Gateway](https://www.youtube.com/watch?v=7HKot-brXFE&t=31878s)
  - [8:52:36 - State Machines and AWS Step Functions](https://www.youtube.com/watch?v=7HKot-brXFE&t=31956s)

#### Detailed notes

**Orchestration and CI/CD** services coordinate how an application runs and how new versions of it reach production. Step Functions and API Gateway are part of the running application. CodePipeline, CodeBuild, and CodeDeploy make up the release process.

| Service | What it does |
| :--- | :--- |
| **AWS Step Functions** | Runs a workflow as a state machine with branching, parallel steps, retries, and error handling. Standard workflows run up to a year, and Express workflows run up to five minutes at high volume |
| **Amazon API Gateway** | Front door for REST, HTTP, and WebSocket APIs, with authorization, throttling, and monitoring. REST APIs add API keys, caching, and AWS WAF, and HTTP APIs cost less |
| **AWS CodePipeline** | Models a release as stages such as source, build, test, approval, and deploy, and moves each change through them |
| AWS CodeBuild | Compiles source code, runs tests, and produces artifacts. You pay by the build minute |
| **AWS CodeDeploy** | Deploys a new revision to EC2 instances, on-premises servers, Lambda functions, or ECS services |

A pipeline starts from a source such as CodeCommit, GitHub, GitLab, Bitbucket, S3, or ECR. For servers, CodeDeploy does in-place deployments, which update the existing instances, plus blue/green deployments on EC2 instances, which install the new version on replacement instances and then move traffic to them. An agent on each instance follows the AppSpec file in the revision. Lambda and ECS deployments are always blue/green and shift traffic with canary, linear, or all-at-once settings.

> [!NOTE]
> Update (2026): AWS CodeCommit stopped accepting new customers on July 25, 2024 and became available to new customers again in November 2025, according to its [document history](https://docs.aws.amazon.com/codecommit/latest/userguide/history.html).

#### In practice

A typical release starts when someone pushes to the main branch. CodePipeline starts a run, CodeBuild builds and tests the code, and CodeDeploy installs the result. The CodeDeploy agent must be installed and running on each EC2 or on-premises instance; Lambda and ECS deployments need no agent. API Gateway commonly fronts Lambda functions, and a Cognito user pool or a Lambda authorizer can check each caller.

```text
Pipeline "orders-release"
  Source    CodeCommit repository, branch main
  Build     CodeBuild project: compile, run unit tests
  Approve   Manual approval action
  Deploy    CodeDeploy: blue/green deployment to the production Auto Scaling group
```

Step Functions suits work with several steps that must survive failures. Standard workflows fit long-running, auditable processes such as payment processing, and Express workflows fit high-volume event processing. This state machine charges a card and then ships the order. It retries a failed charge up to three times, starting with a five-second wait that doubles each time, and goes to a Fail state if the charge never succeeds. The OutputPath line passes only the function's result to the next step:

```json
{
  "Comment": "Charge the card, then ship the order",
  "StartAt": "ChargeCard",
  "States": {
    "ChargeCard": {
      "Type": "Task",
      "Resource": "arn:aws:states:::lambda:invoke",
      "Parameters": { "FunctionName": "charge-card", "Payload.$": "$" },
      "OutputPath": "$.Payload",
      "Retry": [ { "ErrorEquals": ["States.TaskFailed"], "IntervalSeconds": 5, "MaxAttempts": 3 } ],
      "Catch": [ { "ErrorEquals": ["States.ALL"], "Next": "PaymentFailed" } ],
      "Next": "ShipOrder"
    },
    "ShipOrder": {
      "Type": "Task",
      "Resource": "arn:aws:states:::lambda:invoke",
      "Parameters": { "FunctionName": "ship-order", "Payload.$": "$" },
      "End": true
    },
    "PaymentFailed": { "Type": "Fail", "Error": "PaymentFailed" }
  }
}
```

> [!IMPORTANT]
> **Exam Question Pattern: CodeDeploy vs. CodePipeline vs. CloudFormation**:
> - *"Which service installs and deploys new application code versions onto EC2 instances and on-premises servers?"* ➔ **AWS CodeDeploy** (runs agent, supports rolling/canary/blue-green).
> - *"Which service automates the end-to-end workflow from source to build to test to deploy?"* ➔ **AWS CodePipeline**.
> - *"Which service compiles source code and runs unit tests?"* ➔ **AWS CodeBuild**.
> - *Trap Alert*: CloudFormation provisions infrastructure resources from templates; it does NOT deploy application code updates to servers!

- **AWS Step Functions**: Serverless visual state machine orchestrating multiple AWS services (Lambda functions) into resilient workflows with error retries.
- **Amazon API Gateway**: Fully managed "front door" to publish, secure, and monitor REST, HTTP, and WebSocket APIs at scale.

> Practice this section: [5 questions on Application Integration & Messaging](practice-questions/12-application-integration-messaging.md)

---

## 13. 📋 Cloud Governance, Management & Monitoring

### 13.1 AWS Organizations & Service Control Policies (SCPs)
- 🎥 **Video Sections**:
  - [9:13:54 - Organizations and Accounts](https://www.youtube.com/watch?v=7HKot-brXFE&t=33234s)
  - [12:05:00 - Consolidated Billing](https://www.youtube.com/watch?v=7HKot-brXFE&t=43500s)

#### Detailed notes

**AWS Organizations** lets you create and manage many AWS accounts as one organization. You group accounts into **organizational units (OUs)** under a single root and attach policies to the root, to an OU, or to one account. Each account inherits the policies of every level above it.

One account, the **management account**, pays the charges of all member accounts. This is **consolidated billing**: you get one bill, usage across accounts is combined so volume discounts apply, and Reserved Instance and Savings Plans discounts are shared. Organizations itself has no additional charge.

A **service control policy (SCP)** is a guardrail that sets the maximum permissions for the IAM users and roles in member accounts. An SCP never grants anything: an action works only when an SCP allows it and an IAM policy grants it. SCPs also limit the root user of each member account. They do not apply to the management account or to service-linked roles, and they require an organization with all features enabled, so an organization limited to consolidated billing cannot use them.

| | IAM identity-based policy | Service control policy (SCP) |
| :--- | :--- | :--- |
| Attached to | IAM users, groups, and roles | The organization root, an OU, or a member account |
| What it does | Grants permissions | Sets the maximum, never grants |
| Can limit the root user of a member account | No | Yes |
| Applies to the management account | Yes | No |

> [!NOTE]
> Update (2026): Organizations has a second authorization policy type, resource control policies (RCPs), which set the maximum permissions on resources the way SCPs do for IAM users and roles ([policy types](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies.html)). An account on the AWS Free plan is upgraded to the Paid plan automatically when it joins AWS Organizations ([Free plan](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/free-tier-plans.html)).

#### In practice

Every root, OU, and account starts with the FullAWSAccess SCP attached, so a new organization allows everything and you add Deny statements. This is the deny list approach. Removing FullAWSAccess without a replacement blocks every action in member accounts. AWS recommends testing an SCP on a separate OU and moving accounts in a few at a time before you attach anything to the root. You can attach up to 10 SCPs directly to a root, OU, or account, an SCP can hold 10,240 characters, and OUs nest five levels deep.

A Region-restriction SCP looks like this. The NotAction list exempts IAM, Route 53, CloudFront, and Support from the Region check because requests to these global services are served from us-east-1. Add any other global services you use, such as organizations or waf.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "DenyAllOutsideEU",
      "Effect": "Deny",
      "NotAction": ["cloudfront:*", "iam:*", "route53:*", "support:*"],
      "Resource": "*",
      "Condition": {
        "StringNotEquals": {
          "aws:RequestedRegion": ["eu-central-1", "eu-west-1"]
        }
      }
    }
  ]
}
```

This SCP denies every action outside eu-central-1 and eu-west-1 to all principals in the affected accounts, including each account's root user, except actions of the four services in NotAction. Save the policy as scp.json, then create the policy in Organizations and attach it to an OU:

```bash
aws organizations create-policy --name approved-regions \
  --description "Deny actions outside approved Regions" \
  --type SERVICE_CONTROL_POLICY --content file://scp.json
aws organizations attach-policy --policy-id POLICY_ID --target-id OU_ID
```

- **AWS Organizations**: Centrally manage and govern multiple AWS accounts.
- **Service Control Policies (SCPs)**: Central policy guardrails applied at the OU or account level.
  - 🔑 **Critical Exam Rule**: SCPs set the maximum allowed permissions for member accounts. **Even the Root User of a member account cannot bypass an SCP deny rule!** (SCPs never grant permissions; they only restrict).
- **Consolidated Billing**: One single monthly bill for all accounts in the organization, combining usage for volume pricing discounts and sharing Reserved Instance / Savings Plans discounts across accounts.

---

### 13.2 AWS Config vs. AWS Control Tower
- 🎥 **Video Sections**:
  - [9:16:30 - AWS Control Tower](https://www.youtube.com/watch?v=7HKot-brXFE&t=33390s)
  - [9:18:35 - AWS Config](https://www.youtube.com/watch?v=7HKot-brXFE&t=33515s)

#### Detailed notes

**AWS Config** records the configuration of your AWS resources over time and checks it against rules, such as "S3 buckets must not allow public read access". Each resource is marked compliant or noncompliant, you can look back at how a resource was configured earlier, and a noncompliant resource can be fixed automatically with a Systems Manager Automation runbook. An aggregator collects results from several accounts and Regions into one view.

**AWS Control Tower** sets up and governs a multi-account environment. It orchestrates AWS Organizations, AWS Service Catalog, and AWS IAM Identity Center to build a **landing zone**, a multi-account environment based on best practices, and it provides Account Factory, a template for creating new accounts. **Controls** are the high-level rules that Control Tower applies to an OU, and every account in the OU receives them. Preventive controls stop an action, detective controls report noncompliance, and proactive controls check resources before CloudFormation provisions them.

| | AWS Config | AWS Control Tower |
| :--- | :--- | :--- |
| Purpose | Record resource configurations and evaluate them against rules | Set up and govern a multi-account environment |
| Scope | Resources in one account and Region; an aggregator combines several | OUs and the accounts in them |
| Rules | Config managed or custom rules | Controls, which use SCPs, RCPs, declarative policies, Config rules, and CloudFormation hooks |
| Blocks an action before it happens | No, it evaluates resources after a change | Yes, with preventive controls |
| Cost | Billed for configuration items recorded, rule evaluations, and conformance pack evaluations | No additional charge; you pay for the services it sets up |

> [!NOTE]
> Update (2026): AWS now calls guardrails controls and lists a third behavior, proactive controls, which use CloudFormation hooks. In landing zone version 4.0 and later, mandatory controls are no longer applied by default ([control behavior and guidance](https://docs.aws.amazon.com/controltower/latest/controlreference/control-behavior.html)). An account on the AWS Free plan is upgraded to the Paid plan automatically when you set up a landing zone ([Free plan](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/free-tier-plans.html)).

#### In practice

Turn on the configuration recorder in each Region you use, choose the resource types to record, and add rules. Config reports problems and can fix them afterwards, but it cannot block a change as it happens. Use an SCP or a preventive control for that. Control Tower suits companies that run more than a handful of accounts. You enable a control on an OU and every account in that OU receives it, except that preventive controls are not applied to the management account. Do not modify or delete resources that Control Tower creates, including the SCPs it attaches to an OU. Doing so can force you to update the landing zone or re-register the OU, and compliance reports can become inaccurate.

```bash
# AWS Config: check S3 buckets in this account and Region
aws configservice put-config-rule --config-rule '{
  "ConfigRuleName": "s3-no-public-read",
  "Source": {"Owner": "AWS", "SourceIdentifier": "S3_BUCKET_PUBLIC_READ_PROHIBITED"}
}'
aws configservice get-compliance-details-by-config-rule \
  --config-rule-name s3-no-public-read --compliance-types NON_COMPLIANT

# AWS Control Tower: turn on one control for every account in an OU
aws controltower enable-control \
  --control-identifier CONTROL_ARN --target-identifier OU_ARN
```

- **AWS Config**: Continuously records resource configuration changes over time and assesses compliance against predefined rules (e.g., alert if an S3 bucket is public or an EBS volume is unencrypted). Can trigger automated remediation via Systems Manager Automation.
- **AWS Control Tower**: Automates the setup of a secure, multi-account AWS environment using best-practice **Landing Zones** and preventive/detective guardrails.

---

### 13.3 Observability: Amazon CloudWatch vs. AWS CloudTrail
- 🎥 **Video Sections**:
  - [10:17:15 - Logging Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=37035s)
  - [10:18:39 - AWS CloudTrail](https://www.youtube.com/watch?v=7HKot-brXFE&t=37119s)
  - [10:20:16 - CloudWatch Alarm](https://www.youtube.com/watch?v=7HKot-brXFE&t=37216s)

#### Detailed notes

**Amazon CloudWatch** collects metrics and logs from your resources and applications, shows them on dashboards, and raises alarms, so it answers the question "how is it performing?" Many AWS services publish a default set of metrics at no charge. For EC2, basic monitoring publishes a data point every 5 minutes, and detailed monitoring, which has an extra charge, publishes one every 1 minute. Metrics from inside the operating system, such as memory and disk use, and application log files need the **CloudWatch agent**, which also runs on on-premises servers. A metric alarm watches one metric and, when its state changes, can notify an SNS topic, run an EC2 action, or start an EC2 Auto Scaling action.

**AWS CloudTrail** records who did what: each API call made through the console, the CLI, or an SDK, with the caller, the time, and the source IP address. Event history is on by default and shows the past 90 days of management events in a Region. To keep records longer or to capture data events, create a **trail** that delivers events to an S3 bucket. An organization trail does this for every account in an organization.

| | Amazon CloudWatch | AWS CloudTrail |
| :--- | :--- | :--- |
| Question it answers | How is the workload performing? | Who made which API call, and when? |
| What it records | Metrics, logs, and alarm states | API calls and other account activity, as events |
| Default look-back | 15 months for metrics, aggregated into coarser periods as they age | 90 days of management events in event history |
| Collects server log files | Yes, through the CloudWatch agent | No |

> [!NOTE]
> Update (2026): AWS CloudTrail Lake, a managed solution for storing and querying audit logs, has not accepted new customers since May 31, 2026, and AWS points to Amazon CloudWatch for similar capabilities. Trails and event history are not affected ([CloudTrail Lake availability change](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake-service-availability-change.html)).

#### In practice

Match the alarm period to the metric interval. A metric published every 5 minutes needs a period of at least 300 seconds, and with detailed monitoring the minimum is 60 seconds. An alarm sends its SNS notification when it changes state, so a metric that stays high does not send a message every period. Event history searches one Region at a time and accepts one attribute filter, so searching across Regions or accounts calls for a trail. CloudTrail keeps no copy of a server's log files; those go to CloudWatch Logs through the agent.

```bash
# CloudWatch: alarm when average CPU stays above 80 percent for two 5-minute periods
aws cloudwatch put-metric-alarm \
  --alarm-name web-cpu-high \
  --namespace AWS/EC2 --metric-name CPUUtilization \
  --dimensions Name=InstanceId,Value=i-0abc123def4567890 \
  --statistic Average --period 300 --evaluation-periods 2 \
  --threshold 80 --comparison-operator GreaterThanThreshold \
  --alarm-actions arn:aws:sns:us-east-1:123456789012:ops-alerts

# CloudTrail: who terminated instances recently (event history keeps 90 days)
aws cloudtrail lookup-events \
  --lookup-attributes AttributeKey=EventName,AttributeValue=TerminateInstances \
  --max-items 5
```

A shortened CloudTrail record of a terminated instance (values invented):

```json
{
  "eventTime": "2026-10-27T09:14:05Z",
  "eventSource": "ec2.amazonaws.com",
  "eventName": "TerminateInstances",
  "awsRegion": "us-east-1",
  "sourceIPAddress": "203.0.113.25",
  "userIdentity": {
    "type": "IAMUser",
    "userName": "alice"
  },
  "requestParameters": {
    "instancesSet": {"items": [{"instanceId": "i-0abc123def4567890"}]}
  }
}
```

> [!IMPORTANT]
> **Definite Exam Question: The Rule of Thumb**:
> - **Amazon CloudWatch** = **PERFORMANCE & APPLICATION LOGS** ("How is it performing? CPU, RAM, disk metrics, application logs, triggers alarms").
> - **AWS CloudTrail** = **GOVERNANCE & API AUDITING** ("Who made what API call, when, and from where?").

```mermaid
graph LR
    subgraph CloudWatchScope ["Amazon CloudWatch"]
        CW1["Metrics (CPU, Network, Disk)"]
        CW2["CloudWatch Logs + CloudWatch Agent (Server logs)"]
        CW3["Alarms (Trigger Auto Scaling, reboot EC2)"]
    end
    subgraph CloudTrailScope ["AWS CloudTrail"]
        CT1["API Call History (Console, CLI, SDK)"]
        CT2["Auditing & Compliance"]
        CT3["Organization Trail (Consolidate all accounts to S3)"]
    end
```

- **Collecting Server Logs**: To collect operating system and application log files from EC2 instances and on-premises servers into one central searchable place, install the **Amazon CloudWatch Agent** and stream to **CloudWatch Logs**. (CloudTrail CANNOT collect server log files!).

> Practice this section: [5 questions on Cloud Governance, Management & Monitoring](practice-questions/13-cloud-governance-management-monitoring.md)

---

## 14. 🤖 Machine Learning, AI & High-Performance Compute

### 14.1 Generative AI & Turnkey AI Services (Bedrock, SageMaker, Q, etc.)
- 🎥 **Video Sections**:
  - [10:31:09 - Introduction to ML and AI](https://www.youtube.com/watch?v=7HKot-brXFE&t=37869s)
  - [10:33:00 - AI and ML Services](https://www.youtube.com/watch?v=7HKot-brXFE&t=37980s)
  - [10:53:51 - Generative AI](https://www.youtube.com/watch?v=7HKot-brXFE&t=39231s)

#### Detailed notes

**Generative AI** is AI that creates new text, images, code, or audio from a prompt, using large pretrained **foundation models**. **Amazon Bedrock** is a fully managed service that gives you API access to foundation models from Amazon and other AI companies. Knowledge Bases ground answers in your own documents, Guardrails add safety filters, AgentCore builds AI agents, and you can customize a model with your data. **Amazon SageMaker AI** is a fully managed service for building, training, and deploying your own machine learning models. **Amazon Q** is a family of generative AI assistants: Amazon Q Developer helps with code and questions about AWS, and Amazon Q Business answers questions from company data.

Turnkey AI services each do one task behind an API and need no machine learning skills.

| Service | You send | You get back |
| :--- | :--- | :--- |
| Amazon Rekognition | An image or video | Objects, faces, text, and unsafe content |
| Amazon Textract | A scanned document | Text, handwriting, forms, and tables |
| Amazon Comprehend | Text | Sentiment and entities |
| Amazon Translate | Text in one language | The same text in another language |
| Amazon Transcribe | Audio | A text transcript |
| Amazon Polly | Text | Spoken audio |
| Amazon Lex | A user's message, typed or spoken | A reply from the chatbot you built |
| Amazon Personalize | User and item data | Personalized recommendations |
| Amazon Kendra (closed to new customers) | A question | Answers found in company documents |

> [!NOTE]
> Update (2026): Amazon SageMaker was renamed Amazon SageMaker AI on December 3, 2024; "Amazon SageMaker" now names a wider data, analytics, and AI platform ([AWS docs](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html)). Amazon Q Business and Amazon Kendra no longer accept new customers (AWS points to Amazon Quick and Bedrock knowledge bases), and Amazon Q Developer IDE plugins end support on April 30, 2027 (AWS points to Kiro) ([maintenance list](https://docs.aws.amazon.com/general/latest/gr/maintenance_services.html) and [sunset list](https://docs.aws.amazon.com/general/latest/gr/sunset_services.html)). Bedrock lists 100+ models from providers such as Anthropic, OpenAI, Meta, and Mistral AI; Amazon's own models there are the Nova family, and the Titan models still listed are embedding models ([model catalog](https://docs.aws.amazon.com/bedrock/latest/userguide/model-cards.html)).

#### In practice

Bedrock needs no servers or GPUs: you choose a model by its ID and call the API, and you can swap in another model without rewriting the application. Use Knowledge Bases when answers must come from your own documents, and Guardrails to filter unwanted content. SageMaker AI fits the case where you need a model trained on your own data and control over training and hosting. If a turnkey service already does the task, such as Textract reading forms and tables, it is less work than either. Models differ by Region, so check the model's page before you build. One question sent to Amazon Nova Lite through the Converse API:

```python
import boto3

client = boto3.client("bedrock-runtime", region_name="us-east-1")

response = client.converse(
    modelId="amazon.nova-lite-v1:0",
    messages=[
        {"role": "user", "content": [{"text": "Explain Amazon S3 in two sentences."}]}
    ],
    inferenceConfig={"maxTokens": 200},
)

print(response["output"]["message"]["content"][0]["text"])
```

- **Amazon Bedrock**: Serverless service providing API access to leading Foundation Models (Anthropic Claude, Meta Llama, Amazon Titan) for generative AI.
- **Amazon SageMaker**: End-to-end machine learning platform to build, train, tune, and deploy custom ML models.
- **Amazon Q**: Generative AI-powered assistant for enterprises (Q Business) and developers (Q Developer).
- **Turnkey AI Portfolio**:
  - **Amazon Rekognition**: Computer vision (identifies objects, faces, text, inappropriate content).
  - **Amazon Polly**: Text-to-Speech (turns text into lifelike speech).
  - **Amazon Transcribe**: Speech-to-Text (automatic speech recognition).
  - **Amazon Translate**: Language translation.
  - **Amazon Comprehend**: Natural Language Processing (NLP: sentiment analysis, entity extraction).
  - **Amazon Textract**: Extracts text, handwriting, forms, and tables from documents.
  - **Amazon Lex**: Voice and text conversational chatbots (powers Alexa).
  - **Amazon Kendra**: Intelligent enterprise search engine powered by ML.
  - **Amazon Personalize**: Real-time personalized recommendation engine.

---

### 14.2 Custom AI Silicon: Trainium, Inferentia, Graviton
- 🎥 **Video Sections**:
  - [11:02:15 - What is a GPU?](https://www.youtube.com/watch?v=7HKot-brXFE&t=39735s)
  - [11:04:05 - What is CUDA?](https://www.youtube.com/watch?v=7HKot-brXFE&t=39845s)

#### Detailed notes

**AWS custom silicon** is the family of processors that AWS designs itself for EC2. **AWS Trainium** is a machine learning chip built for training, which is processing large datasets to produce a model. **AWS Inferentia** is a machine learning chip built for inference, which is running a trained model each time it answers a request, at a low cost per inference. Both use the AWS Neuron SDK, which integrates with machine learning frameworks such as PyTorch and JAX. **AWS Graviton** is an Arm-based CPU for general cloud workloads, available in EC2 instance families such as M7g, M8g, and M9g. AWS states that Graviton-based instances deliver up to 40% better price performance than comparable x86-based instances for a wide variety of workloads.

| | Trainium | Inferentia | Graviton |
| :--- | :--- | :--- | :--- |
| Type | Machine learning accelerator | Machine learning accelerator | Arm-based CPU |
| Built for | Training (AWS also lists inference) | Inference | General compute workloads |
| EC2 instance names | Start with trn | Start with inf | A g after the generation number, such as m7g |
| Current generation | Trainium3, in Trn3 UltraServers | Inferentia2, in Inf2 instances | Graviton5, for example in M9g instances |
| Software | AWS Neuron SDK | AWS Neuron SDK | Software built for arm64 |

> [!NOTE]
> Update (2026): AWS now describes Trainium as designed for AI training and inference at scale ([Trainium](https://aws.amazon.com/ai/machine-learning/trainium/)), and Trainium3 UltraServers (Trn3) became generally available in December 2025 ([announcement](https://aws.amazon.com/about-aws/whats-new/2025/12/amazon-ec2-trn3-ultraservers/)). Graviton5, the fifth generation, has been available in M9g instances since June 2026 ([announcement](https://aws.amazon.com/about-aws/whats-new/2026/06/ec2-m9g-m9gd-instances-graviton5-processors-available/)).

#### In practice

Choose the chip by the job. Training a new model points to Trainium, serving predictions at a low cost per request points to Inferentia, and web or database servers point to Graviton. Models run on Trainium and Inferentia through the Neuron SDK. Moving to Graviton means running software built for the Arm architecture, so an application shipped only as an x86 binary must be rebuilt or stay on Intel or AMD instances. Treat "up to 40%" as a ceiling and measure your own workload before you migrate.

The CPU architecture is part of each instance type's description, and the "g" in m7g marks Graviton:

```bash
aws ec2 describe-instance-types --instance-types m7g.large m7i.large \
  --query "InstanceTypes[].[InstanceType,ProcessorInfo.SupportedArchitectures[0]]" \
  --output text
```

```text
m7g.large    arm64
m7i.large    x86_64
```

- **AWS Trainium**: Custom silicon chip purpose-built for deep learning **model training**.
- **AWS Inferentia**: Custom silicon chip purpose-built for deep learning **model inference** (predictions) at lowest cost.
- **AWS Graviton**: Custom ARM-based processor built by AWS delivering up to 40% better price-performance over comparable x86 processors.

> Practice this section: [5 questions on Machine Learning, AI & High-Performance Compute](practice-questions/14-ml-ai-hpc.md)

---

## 15. 🏛️ AWS Well-Architected Framework

- 🎥 **Video Sections**:
  - [11:12:40 - AWS Well-Architected Framework](https://www.youtube.com/watch?v=7HKot-brXFE&t=40360s)
  - [11:18:56 - General Design Principles](https://www.youtube.com/watch?v=7HKot-brXFE&t=40736s)

### 15.1 The 6 Pillars & Their Core Design Principles

#### Detailed notes

The **AWS Well-Architected Framework** is AWS's set of best practices for designing and running workloads in the cloud, organized into six pillars: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability. Each pillar has its own design principles and best practices. The Framework also lists six general design principles that apply across pillars: stop guessing your capacity needs, test systems at production scale, automate with architectural experimentation in mind, consider evolutionary architectures, drive architectures using data, and improve through game days.

The number of design principles differs by pillar: eight for Operational Excellence, seven for Security, six for Sustainability, and five each for Reliability, Performance Efficiency, and Cost Optimization. One principle, use managed services, appears under both Operational Excellence and Sustainability.

| Pillar | Design principles |
| :--- | :--- |
| Operational Excellence | Organize teams around business outcomes; implement observability for actionable insights; safely automate where possible; make frequent, small, reversible changes; refine operations procedures frequently; anticipate failure; learn from all operational events and metrics; use managed services |
| Security | Implement a strong identity foundation; maintain traceability; apply security at all layers; automate security best practices; protect data in transit and at rest; keep people away from data; prepare for security events |
| Reliability | Automatically recover from failure; test recovery procedures; scale horizontally to increase aggregate workload availability; stop guessing capacity; manage change through automation |
| Performance Efficiency | Democratize advanced technologies; go global in minutes; use serverless architectures; experiment more often; consider mechanical sympathy |
| Cost Optimization | Implement Cloud Financial Management; adopt a consumption model; measure overall efficiency; stop spending money on undifferentiated heavy lifting; analyze and attribute expenditure |
| Sustainability | Understand your impact; establish sustainability goals; maximize utilization; anticipate and adopt new, more efficient hardware and software offerings; use managed services; reduce the downstream impact of your cloud workloads |

> [!NOTE]
> Update (2026): The Framework now words some principles differently from older study material. Operational Excellence lists "safely automate where possible" where older material says "perform operations as code", Security lists "maintain traceability" where older material says "enable traceability", and Sustainability lists "understand your impact" where older material says "understand your environmental impact". The current lists also include "manage change through automation" (Reliability), "consider mechanical sympathy" (Performance Efficiency), and "establish sustainability goals" (Sustainability) ([Framework pillars](https://docs.aws.amazon.com/wellarchitected/latest/framework/the-pillars-of-the-framework.html)).

#### In practice

Use the principles as prompts in a design review. For each pillar, ask which principles the design follows and which it ignores, then record the risk. The AWS Well-Architected Tool turns the pillars into review questions for a workload. The pillars also pull against each other: a second Availability Zone raises Reliability and the bill, so you weigh each choice against the goals of the workload. Six decisions and the principle behind each (invented examples):

| Decision | Design principle | Pillar |
| :--- | :--- | :--- |
| A shop adds Auto Scaling so a sale does not overload the site | Stop guessing capacity | Reliability |
| A team ships many small changes a day and can roll each one back | Make frequent, small, reversible changes | Operational Excellence |
| A company centralizes identities and removes long-term access keys | Implement a strong identity foundation | Security |
| A game studio deploys in more Regions to cut latency for players | Go global in minutes | Performance Efficiency |
| A team stops its test environments outside working hours | Adopt a consumption model | Cost Optimization |
| A team right-sizes servers so each one runs at higher utilization | Maximize utilization | Sustainability |

> [!IMPORTANT]
> **Exam Question Pattern**: Match the design principle to the correct Well-Architected pillar!

| Well-Architected Pillar | Core Focus | Key Design Principles Tested on Exam |
| :--- | :--- | :--- |
| **1. Operational Excellence** | Running and monitoring systems that deliver business value, continually improving processes. | - Perform operations as code.<br/>- **Make frequent, small, reversible changes**.<br/>- Refine operations procedures frequently.<br/>- **Anticipate failure**.<br/>- Learn from all operational failures. |
| **2. Security** | Protecting information, systems, and assets while delivering business value. | - **Implement a strong identity foundation**.<br/>- Enable traceability.<br/>- **Apply security at all layers (defense in depth)**.<br/>- Automate security best practices.<br/>- Protect data in transit and at rest. |
| **3. Reliability** | Ensuring a workload performs correctly and consistently, recovering from failures. | - **Automatically recover from failure**.<br/>- Test recovery procedures.<br/>- **Scale horizontally to increase aggregate workload availability**.<br/>- Stop guessing capacity. |
| **4. Performance Efficiency** | Using computing resources efficiently to meet requirements as technologies evolve. | - Democratize advanced technologies.<br/>- **Go global in minutes**.<br/>- **Use serverless architectures**.<br/>- Experiment more often. |
| **5. Cost Optimization** | Running systems to deliver business value at the lowest price point. | - Implement Cloud Financial Management.<br/>- **Adopt a consumption model**.<br/>- **Measure overall efficiency**.<br/>- Stop spending money on undifferentiated heavy lifting.<br/>- Analyze and attribute expenditure. |
| **6. Sustainability** | Minimizing environmental impacts of running cloud workloads. | - **Understand your environmental impact**.<br/>- Maximize utilization.<br/>- Anticipate and adopt new efficient hardware.<br/>- Use managed services.<br/>- Reduce downstream impact. |

---

### 15.2 AWS Well-Architected Tool
- 🎥 **Video Sections**:
  - [11:28:41 - AWS Well-Architected-Tool](https://www.youtube.com/watch?v=7HKot-brXFE&t=41321s)

#### Detailed notes

The **AWS Well-Architected Tool** is a service in the AWS Management Console for reviewing a workload against the Well-Architected Framework. You define a **workload**, a set of components that delivers business value, such as a website or the backend of a mobile app. The Framework lens is applied automatically. A **lens** is a set of questions and best practices; AWS maintains a catalog of additional lenses, and you can write custom lenses.

You answer the questions for each pillar, and the Tool returns **high risk issues (HRIs)**, which are choices that might cause significant negative impact to the business, and medium risk issues (MRIs), which might cause less. It also produces an improvement plan that lists the issues in priority order. A **milestone** saves the state of a workload at a point in time, such as design, testing, go live, or production, so you can measure progress. You can share workloads with other AWS accounts, IAM users, AWS Organizations, and OUs. The Tool has no additional charge; you pay only for the AWS resources your workloads use.

> [!NOTE]
> Update (2026): AWS Well-Architected Agent entered preview on October 1, 2026. It is an AI-powered service that analyzes deployed resources and infrastructure as code templates and returns prioritized recommendations, and it is available to customers with an AWS Support plan. The Tool remains the manual, guided review of a workload against the Framework, and you can use both side by side ([announcement](https://aws.amazon.com/about-aws/whats-new/2026/10/aws-well-architected-agent/)).

#### In practice

AWS recommends a workload review at major milestones in your development cycle. Save a milestone each time, so the next review shows what changed. HRIs and MRIs are guidelines: if you decide not to fix one, AWS suggests recording the business approval and the reasons in the workload notes. Each workload carries an improvement status: not started, in progress, complete, or risk acknowledged. A workload can have up to 20 lenses and 100 milestones.

```bash
aws wellarchitected list-workloads \
  --query "WorkloadSummaries[].[WorkloadName,ImprovementStatus,RiskCounts.HIGH,RiskCounts.MEDIUM]" \
  --output text

aws wellarchitected create-milestone \
  --workload-id WORKLOAD_ID --milestone-name before-launch
```

Sample output of the first command for one workload with 4 high and 9 medium risks (invented numbers):

```text
shop-web    IN_PROGRESS    4    9
```

- **AWS Well-Architected Tool**: Free service in the management console that lets you review your workloads against the six pillars of the Well-Architected Framework and provides an action plan for improvement.

> Practice this section: [5 questions on AWS Well-Architected Framework](practice-questions/15-well-architected-framework.md)

---

## 16. 💰 Billing, Pricing & Support Plans

### 16.1 Cloud Economics: CapEx vs. OpEx & What is FREE in AWS
- 🎥 **Video Sections**:
  - [11:34:23 - Total Cost of Ownership (TCO)](https://www.youtube.com/watch?v=7HKot-brXFE&t=41663s)
  - [11:37:30 - CAPEX vs OPEX](https://www.youtube.com/watch?v=7HKot-brXFE&t=41850s)

#### Detailed notes

**Cloud economics** describes how the cost model changes when you rent IT instead of buying it. **Capital expenditure (CapEx)** is money spent up front on assets that last for years, such as servers and data center space. **Operating expenditure (OpEx)** is money spent on running costs as they occur, such as a monthly cloud bill. AWS turns infrastructure from CapEx into OpEx: you pay by the second or hour for what you run and stop paying when you stop, instead of buying hardware sized for your busiest day.

**Total cost of ownership (TCO)** compares the full cost of two options. On-premises TCO includes hardware, software licenses, space, power and cooling, networking, and staff. Migration Evaluator builds this business case from an inventory of your existing servers, and the AWS Pricing Calculator prices the AWS side.

Three things lower an AWS bill. You pay only for what you use. You pay less per hour when you commit to a one- or three-year term with Reserved Instances or Savings Plans (Compute, EC2 Instance, SageMaker AI, and Database; Database Savings Plans have only a one-year term). Tiered services such as Amazon S3 charge less per unit as volume grows.

IAM, AWS Organizations, and VPC creation cost nothing, but the resources you run inside a VPC are billed, and so is every public IPv4 address.

> [!NOTE]
> Update (2026): The first 100 GB of data transfer out to the internet each month is free, aggregated across all services and Regions (China and AWS GovCloud excluded). See [EC2 on-demand pricing](https://aws.amazon.com/ec2/pricing/on-demand/).

#### In practice

Cloud costs follow usage, so the bill rises and falls with what you run. That suits uneven demand and makes forgotten resources expensive. Charges begin when an EBS volume is created, attached or not, and a load balancer accrues charges as soon as it is configured. Trusted Advisor flags underutilized EBS volumes and unassociated Elastic IP addresses. Steady workloads that run around the clock gain less from pure pay-as-you-go pricing, so commitments such as Savings Plans fit them better.

Example with invented round numbers: a retailer needs 10 servers for a 2-month holiday peak and 4 servers for the other 10 months.

| | Buy servers (CapEx) | Rent on AWS (OpEx) |
| :--- | :--- | :--- |
| Payment at the start | $60,000 for 10 servers | $0 |
| Capacity | 10 servers all year | 4 servers for 10 months, 10 for 2 months |
| Yearly running cost | $15,000 for power, space, and staff | $30,000 of usage (60 server-months at $500) |
| Cost over 3 years | $105,000 | $90,000 |

> [!IMPORTANT]
> **Definite Exam Question: What is FREE in AWS?**
> - **FREE**:
>   - **Inbound data transfer** from the internet into AWS.
>   - **Data transfer between EC2 instances in the same Availability Zone** using private IP addresses.
>   - Management services: **IAM**, **AWS Organizations**, **Consolidated Billing**, **VPC creation**, **CloudFormation templates** (pay only for resources created), **AWS Artifact**.
> - **CHARGED**:
>   - **Outbound data transfer** to the internet.
>   - **Data transfer between different Availability Zones** or different AWS Regions.
>   - **All public IPv4 addresses** (including idle Elastic IPs).

---

### 16.2 Cost Tools: Pricing Calculator vs. Cost Explorer vs. Budgets vs. CUR
- 🎥 **Video Sections**:
  - [11:40:34 - AWS Pricing Calculator](https://www.youtube.com/watch?v=7HKot-brXFE&t=42034s)
  - [12:32:31 - AWS Budget Reports](https://www.youtube.com/watch?v=7HKot-brXFE&t=45151s)
  - [12:33:04 - AWS Cost and Usage Reports (CUR)](https://www.youtube.com/watch?v=7HKot-brXFE&t=45184s)
  - [12:34:09 - Cost Allocation Tags](https://www.youtube.com/watch?v=7HKot-brXFE&t=45249s)
  - [12:35:45 - AWS Cost Explorer](https://www.youtube.com/watch?v=7HKot-brXFE&t=45345s)

#### Detailed notes

**AWS cost management tools** estimate, analyze, limit, and report your AWS spending, each at a different point in a project. The AWS Pricing Calculator estimates what a design will cost before you build it. AWS Cost Explorer shows what you spent and forecasts what you will spend. AWS Budgets alerts you when cost or usage crosses a limit. AWS Cost and Usage Reports (**CUR**) deliver the line items behind your bill to S3.

| Tool | Works on | Data and timing | Output |
| :--- | :--- | :--- | :--- |
| Pricing Calculator | A design that you describe | Your inputs, before launch | Saved estimate, exportable to CSV or PDF |
| Cost Explorer | Your actual and forecast spend | Up to 13 months back, forecast up to 18 months ahead, multi-year data (up to 38 months) optional | Charts and reports, free in the console |
| Budgets | Cost or usage against a limit you set | Refreshed up to three times a day | Email or SNS alerts, optional actions |
| Cost and Usage Reports | Every line item on the bill | By the hour, day, or month, updated at least daily | Files in S3 for Athena, Redshift, or Amazon Quick |

**Cost allocation tags** group costs by project or team. A tag appears in Cost Explorer and in reports only after the management account (or a standalone account) activates it in the Billing and Cost Management console, and activation can take up to 24 hours. AWS Cost Anomaly Detection uses machine learning to flag unusual spend. The Pricing Calculator has two versions: the public website needs no AWS account, and the in-console version can model your own discounts and commitments.

> [!NOTE]
> Update (2026): AWS recommends CUR 2.0, created in AWS Data Exports, as the way to receive detailed cost and usage data. The original Cost and Usage Reports page now sits under Legacy Pages in the console, and the exam guide still uses the name AWS Cost and Usage Reports. See [AWS Data Exports](https://docs.aws.amazon.com/cur/latest/userguide/what-is-data-exports.html).

#### In practice

Use the Pricing Calculator while you design, a budget when you launch, and Cost Explorer when the bill surprises you. A cost budget can alert on actual spend and on forecasted spend, so the warning can arrive before the money is gone. A forecasted alert does not fire until the account has about five weeks of usage history. Alerts go to email or an SNS topic, and a budget action can apply an IAM or service control policy when a threshold is crossed. Budget data refreshes up to three times a day, so a notification can trail the charge. Cost Explorer often shows no forecast for an account with less than one full billing cycle of data.

```bash
# Spend by service last month (Cost Explorer)
aws ce get-cost-and-usage --time-period Start=2026-09-01,End=2026-10-01 --granularity MONTHLY --metrics UnblendedCost --group-by Type=DIMENSION,Key=SERVICE

# Forecast for the rest of October (Cost Explorer)
aws ce get-cost-forecast --time-period Start=2026-10-27,End=2026-11-01 --metric UNBLENDED_COST --granularity DAILY

# Create the budget defined in monthly-budget.json (Budgets)
aws budgets create-budget --cli-input-json file://monthly-budget.json
```

```json
{
  "AccountId": "123456789012",
  "Budget": {
    "BudgetName": "monthly-cost-budget",
    "BudgetLimit": { "Amount": "500", "Unit": "USD" },
    "TimeUnit": "MONTHLY",
    "BudgetType": "COST"
  },
  "NotificationsWithSubscribers": [
    {
      "Notification": {
        "NotificationType": "FORECASTED",
        "ComparisonOperator": "GREATER_THAN",
        "Threshold": 100,
        "ThresholdType": "PERCENTAGE"
      },
      "Subscribers": [{ "SubscriptionType": "EMAIL", "Address": "finance@example.com" }]
    }
  ]
}
```

This budget emails finance@example.com when the forecast shows the month passing $500.

> [!IMPORTANT]
> **Exam Question Pattern for Cost Tools**:
> - *"Estimate cost BEFORE launching resources"* ➔ **AWS Pricing Calculator**.
> - *"Visualize historical spend and FORECAST future costs"* ➔ **AWS Cost Explorer**.
> - *"Set spending thresholds and get ALERTED when actual or forecast spend crosses it"* ➔ **AWS Budgets**.
> - *"Most granular line-item billing breakdown delivered to S3"* ➔ **AWS Cost and Usage Report (CUR)**.
> - *"Detect unusual spending patterns using machine learning"* ➔ **AWS Cost Anomaly Detection**.
> - *"Track and categorize costs by department"* ➔ **Cost Allocation Tags** (must be activated in Billing console!).

---

### 16.3 AWS Support Plans Comparison (Detailed Matrix)
- 🎥 **Video Sections**:
  - [11:48:53 - AWS Support Plans](https://www.youtube.com/watch?v=7HKot-brXFE&t=42533s)
  - [11:53:37 - Technical Account Manager (TAM)](https://www.youtube.com/watch?v=7HKot-brXFE&t=42817s)

#### Detailed notes

**AWS Support plans** are tiers of help that you add to an AWS account. Basic Support is included for every customer: 24x7 customer service for account and billing questions, documentation, AWS re:Post, service health checks, and a limited set of Trusted Advisor checks. Technical support cases start with the paid plans.

**Business Support+** adds 24x7 phone, web, and chat access to Cloud Support Engineers, AI-assisted answers, and the Support API, with a response in under 30 minutes when a business-critical system is down. **Enterprise Support** adds a designated **Technical Account Manager (TAM)**, a response in under 15 minutes, and AWS Security Incident Response at no extra charge. **Unified Operations** adds a Domain Specialist Engineer, 24x7 monitoring, and a five-minute response for critical incidents.

Paid plans bill monthly with no long-term contract. The fee is the greater of a minimum or a percentage of your monthly AWS charges.

| | Basic | Business Support+ | Enterprise Support | Unified Operations |
| :--- | :--- | :--- | :--- | :--- |
| Suited to | Every account | Production workloads | Business-critical workloads | Mission-critical workloads |
| Technical cases | No | 24x7 phone, web, chat | 24x7 phone, web, chat | 24x7 phone, web, chat |
| Business-critical system down | None | Under 30 minutes | Under 15 minutes | Under 5 minutes |
| Designated TAM | No | No | Yes | Yes, plus a Domain Specialist Engineer |
| Trusted Advisor | Core checks | Full set | Full set plus Priority | Full set plus Priority |
| Monthly minimum | Included | $29 per account | $5,000 | $50,000 |

> [!NOTE]
> Update (2026): Developer Support, Business Support, and Enterprise On-Ramp end on January 1, 2027, and Enterprise On-Ramp accounts are moving to Enterprise Support during 2026. Existing customers can keep those plans until then, and all three stay available in AWS GovCloud (US). See [AWS Support plans](https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html).

#### In practice

Plans are set per account. Business Support+ is billed per account, but the management account of an organization with all features enabled can subscribe the whole organization, and accounts that join later are enrolled automatically. Enterprise Support and Unified Operations are billed on the combined monthly charges of every subscribed account. You change plans in the AWS Support Plans console with IAM permissions, and the root user is not required. Upgrading to Unified Operations goes through AWS sales, and downgrading Enterprise Support goes through your TAM. Paid plans carry a minimum commitment of 30 days, or 90 days for Unified Operations. You open and track cases in the AWS Support Center.

Fee example for Business Support+ with invented spend of $20,000 in monthly AWS charges, using the published rate tiers:

```text
Fee = greater of:
  $29 minimum per account
  9% of the first $10,000          = $900
  7% of the next $10,000           = $700   (this tier runs from $10,000 to $80,000)
  Total of the percentage tiers    = $1,600
Fee charged: $1,600
```

> [!IMPORTANT]
> **Guaranteed Exam Question**: Know who gets 24/7 technical support, who gets a TAM, and response times!

| Feature | Basic (Free) | Developer | Business | Enterprise On-Ramp | Enterprise |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Cost** | Free | Greater of $29/mo or 3% | Greater of $100/mo or % | Greater of $5,500/mo or 10% | Greater of $15,000/mo or % |
| **Technical Support Access** | None (Customer Service & Billing only) | Business hours email access to Cloud Support Associates | **24/7 phone, email, chat access** to Cloud Support Engineers | 24/7 phone, email, chat access to Senior Engineers | **24/7 phone, email, chat access** to Senior Engineers |
| **Authorized Contacts** | 1 primary user | 1 primary user | **Unlimited contacts** | Unlimited contacts | **Unlimited contacts** |
| **Production System Down Response Time** | N/A | N/A | **< 1 hour** | **< 1 hour** | **< 1 hour** |
| **Business-Critical System Down Response Time** | N/A | N/A | N/A | **< 30 minutes** | **< 15 minutes** |
| **Designated Technical Account Manager (TAM)** | None | None | None | Access to a pool of TAMs | **Designated TAM + Concierge Support Team** |
| **Trusted Advisor Checks** | Core checks (7 checks) | Core checks (7 checks) | **Full checks (All 5 pillars)** | **Full checks (All 5 pillars)** | **Full checks (All 5 pillars)** |
| **Infrastructure Event Management (IEM)** | None | None | Available for additional fee | Included | **Included** |

---

### 16.4 AWS Trusted Advisor & Health Dashboard
- 🎥 **Video Sections**:
  - [12:08:00 - AWS Trusted Advisor](https://www.youtube.com/watch?v=7HKot-brXFE&t=43680s)
  - [12:20:42 - Service Health Dashboard](https://www.youtube.com/watch?v=7HKot-brXFE&t=44442s)
  - [12:21:24 - AWS Personal Health Dashboard](https://www.youtube.com/watch?v=7HKot-brXFE&t=44484s)

#### Detailed notes

**AWS Trusted Advisor** checks your account against AWS best practices and reports findings in six categories: cost optimization, performance, security, fault tolerance, service limits, and operational excellence. Each check is red (action recommended), yellow (investigation recommended), or green (no problem detected). Every account sees all service limits checks and a few security and fault tolerance checks, such as S3 bucket permissions and MFA on the root account. The full set of checks, the API, and automatic weekly refreshes need Business Support+, Enterprise Support, or Unified Operations.

The **AWS Health Dashboard** reports events that affect AWS services or your resources. Service health is public, needs no sign-in, and has an RSS feed. Your account health needs sign-in and lists issues, scheduled changes, and notifications for your own resources, with a 90-day event log. Both views are free for all customers.

| | Trusted Advisor | Health: Service health | Health: Your account |
| :--- | :--- | :--- | :--- |
| Reports on | Your configuration against best practices | AWS service status in each Region | Events that affect your resources |
| Sign-in | Yes | No | Yes |
| Example | An unattached EBS volume | An EC2 operational issue in a Region | A scheduled instance retirement |
| Cost | Core checks free, full set needs a paid plan | Free | Free |

> [!NOTE]
> Update (2026): Trusted Advisor now has six check categories, with operational excellence added to the earlier five. Basic Support includes all service limits checks plus six selected security and fault tolerance checks, which replaces the older fixed set of seven core checks. See the [Trusted Advisor check reference](https://docs.aws.amazon.com/awssupport/latest/user/trusted-advisor-check-reference.html).

#### In practice

Health events reach you in three ways: the dashboard, Amazon EventBridge, and the AWS Health API. EventBridge delivery is free for all customers, so you can get alerts about scheduled changes on any plan. The Health API needs Business Support+, Enterprise Support, or Unified Operations (the classic Business and Enterprise plans also work), and a call without one of these plans returns a SubscriptionRequiredException error. Trusted Advisor sends a weekly email summary of check results to the contacts you choose.

This event pattern matches scheduled EC2 changes in your account, such as an instance retirement:

```json
{
  "source": ["aws.health"],
  "detail-type": ["AWS Health Event"],
  "detail": {
    "service": ["EC2"],
    "eventTypeCategory": ["scheduledChange"]
  }
}
```

```bash
aws events put-rule --name ec2-scheduled-changes --event-pattern file://health-pattern.json
aws events put-targets --rule ec2-scheduled-changes --targets "Id=1,Arn=arn:aws:sns:us-east-1:123456789012:ops-alerts"
```

The SNS topic needs an access policy that lets events.amazonaws.com publish to it.

#### AWS Trusted Advisor (5 Pillars of Checks):
1. **Cost Optimization**: Idle EC2 instances (daily CPU <10% and network <5 MB for 4 of 14 days), unattached EBS volumes, idle load balancers.
2. **Performance**: High EC2 usage, CloudFront optimizations.
3. **Security**: S3 public bucket permissions, MFA on root account, unrestricted security group ports.
4. **Fault Tolerance**: Missing EBS snapshots, non-Multi-AZ RDS, S3 versioning.
5. **Service Limits**: Usage approaching 80% of regional service quota.

#### AWS Health Dashboard:
- **Service Health (Public)**: Displays general status of all AWS services across all regions worldwide without requiring sign-in (provides RSS feeds).
- **Your Account Health (Personalized)**: Displays specific events, scheduled maintenance, and resource retirements directly affecting **your active AWS account's resources**.

---

### 16.5 Partner Network (APN), Marketplace & Startup Programs
- 🎥 **Video Sections**:
  - [12:02:48 - AWS Marketplace](https://www.youtube.com/watch?v=7HKot-brXFE&t=43368s)
  - [12:28:26 - AWS Partner Network (APN)](https://www.youtube.com/watch?v=7HKot-brXFE&t=44906s)

#### Detailed notes

The **AWS Partner Network (APN)** is the program for companies that build on AWS or help customers use it. Independent software vendors (ISVs) sell software and SaaS products. System integrators and other consulting partners design, migrate, and run workloads for customers. Partners get training and certification, events, and co-selling with AWS, and the exam guide also lists partner volume discounts.

**AWS Marketplace** is a curated digital catalog for finding, buying, and deploying third-party software, data, and services. Charges appear on your AWS bill, and AWS pays the seller. Pricing options include free trial, hourly, monthly, annual, multi-year, and bring your own license (BYOL), and a private offer carries custom pricing and terms. **AWS Activate** gives eligible startups credits and technical help, and **AWS re:Post** is a community question-and-answer site that replaced the AWS forums. The exam guide lists AWS Activate as out of scope.

| Need | Where to look |
| :--- | :--- |
| Software, SaaS, or data billed on your AWS invoice | AWS Marketplace |
| A firm to design, migrate, or run your workloads | An APN consulting partner or system integrator |
| AWS's own consultants for a migration or modernization project | AWS Professional Services |
| Architecture guidance from AWS staff | An AWS solutions architect |
| An answer to a technical question from the community | AWS re:Post |
| Credits and support for a startup | AWS Activate |

#### In practice

Marketplace spend is part of your AWS bill, so the usual cost controls apply. A cost budget includes AWS Marketplace charges, and the billing entity filter isolates them. Cost Anomaly Detection does not monitor third-party Marketplace products, except third-party foundation models on Amazon Bedrock, so a budget is the tool to use for the rest. Every software listing has passed AWS's curation process. The seller sets the price and the terms of use, and you accept them when you subscribe.

This budget tracks only AWS Marketplace spend and alerts when it passes 80 percent of a $1,000 monthly limit:

```json
{
  "AccountId": "123456789012",
  "Budget": {
    "BudgetName": "marketplace-monthly",
    "BudgetLimit": { "Amount": "1000", "Unit": "USD" },
    "TimeUnit": "MONTHLY",
    "BudgetType": "COST",
    "FilterExpression": {
      "Dimensions": { "Key": "BILLING_ENTITY", "Values": ["AWS Marketplace"] }
    },
    "Metrics": ["UnblendedCost"]
  },
  "NotificationsWithSubscribers": [
    {
      "Notification": {
        "NotificationType": "ACTUAL",
        "ComparisonOperator": "GREATER_THAN",
        "Threshold": 80,
        "ThresholdType": "PERCENTAGE"
      },
      "Subscribers": [{ "SubscriptionType": "EMAIL", "Address": "finance@example.com" }]
    }
  ]
}
```

```bash
aws budgets create-budget --cli-input-json file://marketplace-budget.json
```

> [!IMPORTANT]
> **Exam Question Pattern: Consulting vs. Technology Partners**:
> - **Services Path (formerly APN Consulting Partners)**: Professional service firms (system integrators, managed service providers) that help customers **design, architect, build, migrate, and manage** workloads on AWS.
> - **Software Path (formerly APN Technology Partners)**: Commercial software vendors that sell products hosted on or integrated with AWS (e.g., security firewalls, SaaS).

- **AWS Marketplace**: Digital catalog of third-party software, data, and services deployed on AWS with billing consolidated directly onto your AWS invoice.
- **AWS Activate**: Program providing eligible startups with free AWS credits, technical support, and resources.
- **AWS re:Post**: Community-driven Q&A service where customers get technical answers from the AWS community and experts (replaces AWS Forums).

> Practice this section: [5 questions on Billing, Pricing & Support Plans](practice-questions/16-billing-pricing-support.md)

---

## 17. 🆚 High-Yield Exam "Cheat Sheet" & Service Disambiguation

### 17.1 Commonly Confused Services Cheat Sheet
- 🎥 **Video Sections**:
  - [13:31:24 - Variation Study & Know Your Initialisms](https://www.youtube.com/watch?v=7HKot-brXFE&t=48684s)
  - [13:34:09 - AWS Config vs AWS AppConfig](https://www.youtube.com/watch?v=7HKot-brXFE&t=48849s)
  - [13:35:04 - SNS vs SQS](https://www.youtube.com/watch?v=7HKot-brXFE&t=48904s)
  - [13:36:42 - SNS vs SES vs PinPoint vs Workmail](https://www.youtube.com/watch?v=7HKot-brXFE&t=49002s)
  - [13:39:46 - Amazon Inspector vs AWS Trusted Advisor](https://www.youtube.com/watch?v=7HKot-brXFE&t=49186s)
  - [13:41:55 - Connect Named Services & Elastic Transcoder vs MediaConvert](https://www.youtube.com/watch?v=7HKot-brXFE&t=49315s)
  - [13:43:40 - AWS Artifact vs Amazon Inspector](https://www.youtube.com/watch?v=7HKot-brXFE&t=49420s)
  - [13:43:40 - ELB Variants (Elastic Load Balancer)](https://www.youtube.com/watch?v=7HKot-brXFE&t=49420s)

#### Detailed notes

**Service disambiguation** is choosing between AWS services whose names or jobs overlap. Three questions settle most cases. What does the service act on: API activity in your account, the configuration of a resource, or the data and traffic of your workload? When does it act: before an event, during it, or afterward? Do you operate it, or does AWS?

The verb in the question usually decides it. Block, filter, and deny point to a firewall such as a security group, a network ACL, or WAF. Detect points to a threat detection service such as GuardDuty, and investigate points to Detective. A single word often separates a pair: stateful or stateless, cache or no cache, workforce or customer, dedicated or over the internet.

| Pair | First service | Second service |
| :--- | :--- | :--- |
| Security group vs network ACL | Security group: stateful, applies to an instance's network interface, allow rules only | Network ACL: stateless, applies to a subnet, allow and deny rules |
| Shield vs WAF | Shield: DDoS protection; Standard is automatic at no extra charge, Advanced is a paid subscription | WAF: web ACL rules that filter HTTP and HTTPS requests, such as SQL injection or rate limits |
| GuardDuty vs Detective | GuardDuty: detects threats from CloudTrail events, VPC flow logs, and DNS logs and raises findings | Detective: investigates a finding to find its root cause |
| Direct Connect vs Site-to-Site VPN | Direct Connect: dedicated private connection that avoids the public internet | VPN: encrypted tunnels over the public internet |
| CloudFront vs Global Accelerator | CloudFront: caches content at edge locations | Global Accelerator: no caching, two static anycast IPs (an NLB has one static IP per Availability Zone) |
| IAM Identity Center vs Cognito | Identity Center: workforce sign-in to AWS accounts and business apps | Cognito: sign-up and sign-in for the customers of your own app |
| Elastic Beanstalk vs CloudFormation | Elastic Beanstalk: you upload code and it provisions and scales the environment | CloudFormation: you describe every resource in a template |
| AWS Backup vs Elastic Disaster Recovery | AWS Backup: centralized, policy-based backups that you define in backup plans | Elastic Disaster Recovery: ongoing server replication to a staging area, recovery within minutes |

> [!NOTE]
> Update (2026): Amazon Pinpoint support ends on October 30, 2026; email moves to Amazon SES, and SMS, voice, and push continue as AWS End User Messaging. Amazon Elastic Transcoder support ended on November 13, 2025, and AWS Elemental MediaConvert is the replacement. See [Pinpoint end of support](https://docs.aws.amazon.com/pinpoint/latest/userguide/migrate.html) and [Elastic Transcoder end of support](https://aws.amazon.com/blogs/media/support-for-amazon-elastic-transcoder-ending-soon/).

#### In practice

One resource can raise three different questions, and each has its own service. CloudTrail records API calls, so it shows who changed a security group. Config keeps configuration history and shows what the rules looked like before and after. CloudWatch collects metrics and logs, which tell you how busy the instance behind the group is. CloudTrail lookups cover the last 90 days of management events.

```bash
# Who changed the security group? (CloudTrail)
aws cloudtrail lookup-events --lookup-attributes AttributeKey=ResourceName,AttributeValue=sg-0123456789abcdef0 --max-items 5

# What did its rules look like before and after? (Config)
aws configservice get-resource-config-history --resource-type AWS::EC2::SecurityGroup --resource-id sg-0123456789abcdef0 --max-items 2

# How busy is the instance behind it? (CloudWatch)
aws cloudwatch get-metric-statistics --namespace AWS/EC2 --metric-name CPUUtilization --dimensions Name=InstanceId,Value=i-0123456789abcdef0 --start-time 2026-10-26T00:00:00Z --end-time 2026-10-27T00:00:00Z --period 3600 --statistics Average
```

| Confused Pair | Service A Focus | Service B Focus | Key Exam Differentiator |
| :--- | :--- | :--- | :--- |
| **Artifact vs. Inspector** | **AWS Artifact**: Self-service portal to download AWS compliance & audit reports (SOC 1/2/3, ISO, PCI-DSS) and sign BAA agreements. | **Amazon Inspector**: Automated security assessment service that scans *customer* EC2 instances, ECR container images, and Lambda functions for software vulnerabilities (CVEs). | Artifact is for *AWS audit/compliance documents*; Inspector is for *scanning workload software vulnerabilities*. |
| **Config vs. AppConfig** | **AWS Config**: Audits AWS resource configuration changes & compliance over time. | **AWS AppConfig**: Manages application feature flags and runtime configurations. | Config is for *infrastructure compliance*; AppConfig is for *app software feature toggles*. |
| **SNS vs. SQS** | **Amazon SNS**: Push notification pub/sub fanout. | **Amazon SQS**: Message queue where workers pull and process. | SNS *pushes to many*; SQS *stores messages for one worker to pull*. |
| **Messaging Services** | **Amazon SES**: Bulk/transactional inbound & outbound email. | **Amazon Pinpoint**: Multi-channel marketing campaigns (SMS, email, push). | SES is for *transactional emails*; Pinpoint is for *targeted user engagement campaigns*. |
| **Inspector vs. Trusted Advisor** | **Amazon Inspector**: Scans EC2, ECR, Lambda for software vulnerabilities (CVEs). | **AWS Trusted Advisor**: Recommends best practices across cost, security, fault tolerance, performance, limits. | Inspector scans *workload code & OS CVEs*; Trusted Advisor scans *account-level best practices*. |
| **Artifact vs. Macie** | **AWS Artifact**: Compliance documentation (SOC, ISO, BAA). | **Amazon Macie**: Discovers sensitive PII data stored in S3. | Artifact is for *AWS audit reports*; Macie is for *finding PII in S3*. |
| **KMS vs. CloudHSM** | **AWS KMS**: Managed multi-tenant cryptographic keys. | **AWS CloudHSM**: Dedicated single-tenant hardware HSM under customer sole control. | KMS is *managed and shared hardware*; CloudHSM is *dedicated physical hardware*. |
| **MediaConvert vs. Transcoder** | **AWS Elemental MediaConvert**: Modern broadcast-grade video transcoding. | **Amazon Elastic Transcoder**: Legacy cloud video transcoding. | MediaConvert has superseded Elastic Transcoder. |
| **CloudFormation vs. CodeDeploy** | **CloudFormation**: Provisions infrastructure stacks from templates. | **CodeDeploy**: Installs application code onto EC2 and on-premises servers. | CloudFormation creates *infrastructure*; CodeDeploy rolls out *software code*. |
| **Pricing Calculator vs. Cost Explorer** | **Pricing Calculator**: Estimates costs *before* deployment. | **Cost Explorer**: Analyzes past spend and *forecasts* future spend. | Calculator is *pre-build modeling*; Cost Explorer is *post-launch analytics & forecast*. |

---

#### 🔍 Deep Dive: AWS Artifact vs. Amazon Inspector
- **AWS Artifact**:
  - Think: **"AWS Compliance Documentation Locker"**.
  - Provides on-demand access to AWS security and compliance reports (e.g., SOC reports, PCI-DSS compliance packages, ISO certifications).
  - Used to review, accept, and manage agreements with AWS (such as the Business Associate Addendum / BAA for HIPAA compliance).
  - 🔑 **Exam Trigger**: *"Where can a compliance officer download AWS's ISO 27001 certification or SOC 2 report?"* ➔ **AWS Artifact**.
- **Amazon Inspector**:
  - Think: **"Vulnerability Scanner for Your Workloads"**.
  - Automatically assesses EC2 instances, ECR container images, and Lambda functions for software vulnerabilities (CVEs) and unintended network exposure.
  - 🔑 **Exam Trigger**: *"Which service automatically checks EC2 instances and container images for software vulnerabilities and CVEs?"* ➔ **Amazon Inspector**.

---

#### ⚖️ Deep Dive: Elastic Load Balancer (ELB) Variants

| ELB Variant | OSI Layer | Supported Protocols | Key Strengths & Features | 🔑 Exam Scenario Triggers |
| :--- | :---: | :--- | :--- | :--- |
| **Application Load Balancer (ALB)** | **Layer 7** (Application) | HTTP, HTTPS, gRPC, WebSockets | - Path-based routing (`/api`, `/static`)<br/>- Host-based routing (`app.domain.com`)<br/>- Query parameter & header routing<br/>- Native integration with **AWS WAF**<br/>- Redirects (HTTP to HTTPS) | *"Route HTTP/HTTPS traffic based on request URL path, host header, or microservices on ECS"* |
| **Network Load Balancer (NLB)** | **Layer 4** (Transport) | TCP, UDP, TLS | - Ultra-high performance (millions of requests/sec)<br/>- Ultra-low latency (sub-millisecond)<br/>- Provides **static Anycast IP addresses** or Elastic IPs per AZ<br/>- Preserves client source IP | *"Extreme performance, millions of requests per second, ultra-low latency, static IP addresses, gaming, VoIP"* |
| **Gateway Load Balancer (GWLB)** | **Layer 3 & 4** (Network & Transport) | IP packets (GENEVE protocol) | - Transparent network gateway & load balancer<br/>- Routes all traffic through a fleet of third-party virtual security appliances (firewalls, deep packet inspection, IDS/IPS)<br/>- Scales appliances horizontally | *"Deploy, scale, and manage a fleet of third-party virtual firewall appliances or deep packet inspection"* |
| **Classic Load Balancer (CLB)** | Layer 4 & 7 | HTTP, HTTPS, TCP, SSL | - Previous generation (legacy)<br/>- Basic load balancing across EC2 instances<br/>- Does not support advanced path routing or static IPs | *"Legacy EC2-Classic applications (rarely the correct answer for modern architectures)"* |

---

### 17.2 Essential Acronyms & Initialisms Reference

#### Detailed notes

**Acronyms** are shorthand for service names, concepts, and compliance programs, and exam questions often use them without spelling them out. AWS names are literal, so the words behind the letters usually describe the service. S3, SQS, SNS, and SES are all Simple services (Storage, Queue, Notification, Email). EC2, EBS, EFS, ECS, EKS, ECR, and ELB all start with Elastic. Encryption options follow a pattern too: SSE-S3, SSE-KMS, and SSE-C name who manages the keys, which is S3, KMS, or you. Compliance acronyms such as SOC and PCI DSS name audit reports and standards, and you download the reports from AWS Artifact.

Look-alike sets need a memory hook each. SNS pushes messages and SQS holds them in a queue. EBS is block storage for EC2 and EFS is a shared file system. ECS is AWS-native container orchestration and EKS is managed Kubernetes.

| Acronym | Full form | Meaning |
| :--- | :--- | :--- |
| ACM | AWS Certificate Manager | Issues and renews TLS certificates |
| ALB, NLB, GWLB | Application, Network, Gateway Load Balancer | ELB types for layer 7 web traffic, layer 4 traffic, and network appliances |
| AZ | Availability Zone | One or more data centers in a Region, isolated from other zones |
| BAA | Business Associate Addendum | HIPAA agreement that you accept in AWS Artifact |
| CVE | Common Vulnerabilities and Exposures | Public IDs of known software flaws, reported by Amazon Inspector |
| DNS | Domain Name System | Maps names to IP addresses (Route 53) |
| GDPR, HIPAA | General Data Protection Regulation, Health Insurance Portability and Accountability Act | EU privacy law and US health-data law |
| HSM | Hardware Security Module | Dedicated hardware that holds keys (CloudHSM) |
| IaaS, PaaS, SaaS | Infrastructure, Platform, Software as a Service | The three cloud service models |
| ISV | Independent software vendor | A company that sells software, often through AWS Marketplace |
| OU | Organizational unit | A container for accounts in AWS Organizations |
| PII | Personally identifiable information | Data that Amazon Macie looks for in S3 |
| RI | Reserved Instance | EC2 discount for a one- or three-year commitment |
| SLA | Service level agreement | AWS's availability commitment for a service |
| SNS, SQS, SES | Simple Notification, Queue, and Email Service | Pub/sub messaging, message queues, and email sending |
| SOC, PCI DSS | System and Organization Controls, Payment Card Industry Data Security Standard | Audit reports and a card-data standard, with the reports in AWS Artifact |
| SSE | Server-side encryption | The service encrypts data for you (SSE-S3, SSE-KMS, SSE-C) |
| SSM | AWS Systems Manager | Patching, commands, and parameters across a fleet |
| SSO | Single sign-on | One login for many apps (AWS IAM Identity Center) |
| TLS | Transport Layer Security | Encrypts data in transit |
| VPN | Virtual private network | Encrypted connection over the internet |

> [!NOTE]
> Update (2026): AWS Application Migration Service (MGN) was renamed AWS Transform MGN on June 8, 2026, and the MGN abbreviation stays. The exam guide still lists the older name. See the [AWS announcement](https://aws.amazon.com/about-aws/whats-new/2026/06/aws-transform-mgn-rebrand/).

#### In practice

Expand every acronym in a question before you read the options. A stem often packs several of them, and each one points at a different service family: a data type such as PII, a compliance document such as a SOC report or a BAA, a network component such as an ALB. Decode them one at a time, then pick the single service that covers all the pieces.

Example with an invented question stem:

```text
Stem: "A health app stores PII in RDS behind an ALB. Auditors ask for the
latest SOC report and a signed BAA. Where does the company get them?"

PII   personally identifiable information
RDS   Relational Database Service
ALB   Application Load Balancer (layer 7, HTTP and HTTPS)
SOC   System and Organization Controls (audit reports)
BAA   Business Associate Addendum (HIPAA agreement)

Answer: AWS Artifact holds the SOC reports and the BAA.
```

| Acronym | Full Form | Meaning / Function |
| :--- | :--- | :--- |
| **AMI** | Amazon Machine Image | Pre-configured template packaging OS, software, and settings to launch EC2 instances. |
| **ARN** | Amazon Resource Name | Uniquely identifies any AWS resource across all accounts worldwide. |
| **ASG** | Auto Scaling Group | Automatically scales EC2 instances out or in based on demand. |
| **BYOL** | Bring Your Own License | Licensing model letting customers reuse existing software licenses on AWS Dedicated Hosts. |
| **CAF** | Cloud Adoption Framework | 6 perspectives guiding organizational transition to the cloud. |
| **CDK** | Cloud Development Kit | Define cloud infrastructure using familiar modern programming languages. |
| **CDN** | Content Delivery Network | Globally distributed network of caching edge servers (CloudFront). |
| **CUR** | Cost and Usage Report | Most granular raw billing dataset in AWS delivered to S3. |
| **DDoS** | Distributed Denial of Service | Cyberattack attempting to disrupt availability by overwhelming network traffic. |
| **DMS** | Database Migration Service | Migrates databases to AWS while source database remains operational. |
| **EBS** | Elastic Block Store | Persistent, network-attached block storage for EC2 bound to a single AZ. |
| **EC2** | Elastic Compute Cloud | Resizable virtual machines in the cloud. |
| **ECR** | Elastic Container Registry | Managed Docker container image registry. |
| **ECS** | Elastic Container Service | AWS-native container orchestration service. |
| **EFS** | Elastic File System | Managed shared POSIX NFS file system across multiple AZs for Linux. |
| **EKS** | Elastic Kubernetes Service | Managed standard Kubernetes control plane on AWS. |
| **ELB** | Elastic Load Balancing | Automatically distributes incoming application traffic across healthy targets. |
| **IAM** | Identity and Access Management | Manages users, roles, groups, and permissions. |
| **IaC** | Infrastructure as Code | Managing and provisioning infrastructure through machine-readable code templates. |
| **IGW** | Internet Gateway | VPC component that enables communication between public subnets and the internet. |
| **KMS** | Key Management Service | Managed service for creating and controlling encryption keys. |
| **MFA** | Multi-Factor Authentication | Security mechanism requiring two or more verification factors. |
| **MGN** | Application Migration Service | Automated lift-and-shift server replication tool. |
| **NACL** | Network Access Control List | Stateless subnet-level firewall supporting allow and deny rules. |
| **NAT** | Network Address Translation | Enables private subnet instances to connect outbound to the internet. |
| **PoLP** | Principle of Least Privilege | Security rule: grant only minimal permissions necessary. |
| **PoP** | Point of Presence | AWS Edge Locations used by CloudFront and Route 53. |
| **RDS** | Relational Database Service | Managed relational database engine (MySQL, Postgres, Aurora, etc.). |
| **RPO** | Recovery Point Objective | Maximum acceptable data loss measured in time. |
| **RTO** | Recovery Time Objective | Maximum acceptable application downtime. |
| **S3** | Simple Storage Service | Scalable object storage in the cloud with 11 9's durability. |
| **SCP** | Service Control Policy | Policy guardrails for AWS Organizations accounts. |
| **SCT** | Schema Conversion Tool | Converts database schemas between different engines for heterogeneous migrations. |
| **SDK** | Software Development Kit | Code libraries for programming against AWS APIs in application code. |
| **TAM** | Technical Account Manager | Dedicated technical advisor for Enterprise Support customers. |
| **TCO** | Total Cost of Ownership | Financial estimate of direct and indirect costs of infrastructure. |
| **VPC** | Virtual Private Cloud | Logically isolated private network in the cloud. |
| **WAF** | Web Application Firewall | Layer 7 firewall protecting web applications from common web exploits. |

> Practice this section: [5 questions on High-Yield Exam "Cheat Sheet" & Service Disambiguation](practice-questions/17-service-disambiguation.md)

---

## 18. 🎓 Exam Strategy & Last-Minute Checklist

#### Detailed notes

**Exam strategy** is the plan for your last week and for the 90 minutes of the exam, built on how CLF-C02 is delivered and scored. The exam has 65 questions: 50 are scored and 15 are unscored questions that AWS is testing for future use and does not identify. A multiple choice question has one correct answer among four options, and a multiple response question has two or more correct answers among five or more options.

Results are a scaled score from 100 to 1,000, with a minimum passing score of 700. Scaling equates exam forms of slightly different difficulty, so the number of correct answers behind 700 can differ between forms. Scoring is compensatory: you pass on the overall score and need no minimum in any domain. An unanswered question counts as wrong and a wrong answer costs nothing extra, so answer every question.

Sixty-five questions in 90 minutes leaves about 83 seconds for each. You can move between questions, mark one with Flag for Review, and revisit all, incomplete, or flagged questions on a review screen at the end. A timer warning appears when 5 minutes remain.

| | Test center | Online proctored |
| :--- | :--- | :--- |
| Breaks | Unscheduled breaks allowed, and the clock keeps running | None, and you stay in view of the camera |
| Check-in | Store belongings as staff direct | Launch up to 30 minutes early; arriving over 15 minutes late or failing the system test forfeits the fee |
| ID | Two primary IDs, or one primary and one secondary | One primary ID |

> [!NOTE]
> Update (2026): The exam guide now names Business Support+, Enterprise Support, and Unified Operations as the Support plans to know, and AWS publishes guide changes about a month before they reach the exam. Check the in-scope and out-of-scope service lists in the [CLF-C02 exam guide](https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html) before test day.

#### In practice

Results are posted in your AWS Certification account under Exam History within five business days. If you fail, you wait 14 calendar days and can retry with no limit on attempts, paying the full fee each time. After a pass, the same exam cannot be retaken for two years. For practice, AWS Skill Builder has free Official Practice Question Sets (20 questions each, with feedback) and a free 2-hour Exam Prep course, and the full-length Official Practice Exam needs a subscription. Non-native English speakers testing in English can request a 30-minute extension once, before they register. The Italian and German versions of the exam retire after December 31, 2026.

In the last week, read the exam guide's service lists and sit one timed mock test. The day before, check that the names on your IDs match your AWS Certification account, and for an online exam run the system test. On each question, read the last sentence first, note constraint words such as lowest cost or least operational effort, and remove options that name the wrong kind of service.

Example pacing for 65 questions in 90 minutes:

```text
Minute  0   start
Minute 30   past question 25
Minute 60   past question 50
Minute 75   all 65 answered, 15 minutes left for flagged questions
```

### 🔑 Top Keyword Associations for the Exam:
- **"Ready-made list of under-utilized EC2 instances without manual alarms"** ➔ **AWS Trusted Advisor** or **AWS Compute Optimizer** *(NOT CloudWatch!)*.
- **"Deploy code to EC2 and on-premises servers"** ➔ **AWS CodeDeploy** *(NOT CloudFormation!)*.
- **"Forecast future spend based on past usage"** ➔ **AWS Cost Explorer** *(NOT Pricing Calculator!)*.
- **"Estimate costs before building anything"** ➔ **AWS Pricing Calculator**.
- **"Alert when forecasted or actual spend crosses a threshold"** ➔ **AWS Budgets**.
- **"Deploy the same template across 40 accounts and 3 regions"** ➔ **AWS CloudFormation StackSets**.
- **"Centrally view, patch, and manage a fleet of nodes"** ➔ **AWS Systems Manager (SSM Agent)**.
- **"Schemaless database with dynamic attributes"** ➔ **Amazon DynamoDB** *(NOT Redshift!)*.
- **"Lower prices from aggregated usage across many customers"** ➔ **Benefit from massive economies of scale**.
- **"Centralize server and application logs from EC2 and on-premises"** ➔ **Amazon CloudWatch Logs with the CloudWatch Agent** *(NOT CloudTrail!)*.
- **"Audit API calls: who deleted the database?"** ➔ **AWS CloudTrail**.
- **"Vulnerability scanning on EC2 and container images"** ➔ **Amazon Inspector** *(NOT AWS Config!)*.
- **"Intelligent threat detection using machine learning on logs"** ➔ **Amazon GuardDuty**.
- **"Download compliance reports and SOC documentation"** ➔ **AWS Artifact**.
- **"Dedicated hardware security module (FIPS 140-3 Level 3 single-tenant)"** ➔ **AWS CloudHSM**.
- **"Designated Technical Account Manager (TAM)"** ➔ **Enterprise Support Plan**.
- **"Central policy guardrails that even root cannot bypass"** ➔ **AWS Organizations Service Control Policies (SCPs)**.
- **"Public RSS feed for all AWS service outages without signing in"** ➔ **AWS Health Dashboard - Service Health**.
- **"Personalized notifications about scheduled maintenance or retirement of your specific EC2 instances"** ➔ **AWS Health Dashboard - Your Account Health**.
- **"Encrypted at rest by default without user configuration"** ➔ **Amazon S3** (SSE-S3 default) and **Amazon DynamoDB** *(EBS is opt-in!)*.
- **"Expert firm to design, migrate, and manage workloads"** ➔ **APN Services Path (Consulting Partner)** *(NOT Technology Partner!)*.
- **"Minimum charge for EC2 per-second billing"** ➔ **60 seconds minimum**.
- **"What is generally FREE in AWS?"** ➔ **Inbound data transfer from internet**, **data transfer between EC2 in same AZ via private IP**, **IAM**, **Organizations**, **VPC creation**, **CloudFormation templates**.

### 📝 Mock Tests & Practice Exams:
- The [free CLF-C02 mock tests](https://heymehedi.im/aws-cloud-practitioner) have practice sets for each domain and a timed, full-length simulation. Every question has an explanation.
- The simulation follows the real exam format: 65 questions in 90 minutes. Aim for 70% or higher, since the real passing score is 700 out of 1000.
- After a miss, read the explanation, then reread the matching section of this guide and the [Question Patterns & Trap Guide](#-decoding-the-clf-c02-exam-question-patterns--trap-guide).

> Practice this section: [5 questions on Exam Strategy & Last-Minute Checklist](practice-questions/18-exam-strategy.md)

---

<p align="center">
  <b>Good luck on your AWS Certified Cloud Practitioner exam! 🚀☁️</b>
  <br/>
  <i>Feel free to star ⭐ this repository and share it with fellow cloud learners!</i>
</p>
