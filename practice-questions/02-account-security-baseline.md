# 📝 Practice Questions: 2. 🛡️ Getting Started & Account Security Baseline

[⬅️ Study guide: 2. 🛡️ Getting Started & Account Security Baseline](../README.md#2-️-getting-started--account-security-baseline) · [📚 All topics](README.md) · [Next: 3. 🌐 AWS Global Infrastructure ➡️](03-global-infrastructure.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

A finance team wants an email alert when the company's actual or forecasted monthly AWS spend crosses 80% of a set amount. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Cost Explorer</summary>

❌ **Incorrect.** Cost Explorer visualizes past spend and forecasts future spend, but it does not send threshold alerts.

</details>

<details><summary>◯ <b>B.</b> AWS Pricing Calculator</summary>

❌ **Incorrect.** The Pricing Calculator estimates the cost of a planned architecture before it is deployed.

</details>

<details><summary>◯ <b>C.</b> AWS Budgets</summary>

✅ **Correct.** AWS Budgets sends email or Amazon SNS alerts when actual or forecasted cost or usage crosses a threshold. It can also trigger budget actions.

</details>

<details><summary>◯ <b>D.</b> AWS Cost and Usage Reports</summary>

❌ **Incorrect.** The Cost and Usage Report delivers the most detailed billing data to Amazon S3. It does not send alerts.

</details>

📖 **Study:** [2.3 Budgets & Zero-Spend Billing Alarms](../README.md#23-budgets--zero-spend-billing-alarms)

---

### Question 2

A company wants a zero-spend safeguard for a new learning account: an Amazon CloudWatch billing alarm that notifies it through Amazon SNS when total estimated charges exceed $1. In which Region must the billing alarm be created?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> US East (N. Virginia), <code>us-east-1</code></summary>

✅ **Correct.** Billing metric data for the whole account is stored in us-east-1, so billing alarms must be created there.

</details>

<details><summary>◯ <b>B.</b> The Region where most of the company's resources run</summary>

❌ **Incorrect.** Billing metrics are not stored in each workload Region, so an alarm there cannot see the total estimated charges.

</details>

<details><summary>◯ <b>C.</b> Europe (Frankfurt), <code>eu-central-1</code></summary>

❌ **Incorrect.** This is a valid AWS Region, but account billing metric data is not stored there.

</details>

<details><summary>◯ <b>D.</b> Any Region, because billing metrics are replicated to every Region</summary>

❌ **Incorrect.** Billing metrics are not replicated. They exist only in us-east-1.

</details>

📖 **Study:** [2.3 Budgets & Zero-Spend Billing Alarms](../README.md#23-budgets--zero-spend-billing-alarms)

---

### Question 3

A startup uses AWS Lambda and stays within the 1 million free requests per month that never expire. Which type of AWS Free Tier offer is this?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> 12 months free</summary>

❌ **Incorrect.** These offers are free only for a limited period after sign-up (for example, the first 12 months on legacy Free Tier accounts) and are billed at standard rates afterward.

</details>

<details><summary>◯ <b>B.</b> Always Free</summary>

✅ **Correct.** Always Free offers, such as the monthly Lambda request allowance, do not expire.

</details>

<details><summary>◯ <b>C.</b> Short-term free trial</summary>

❌ **Incorrect.** A trial starts when you first activate a service and ends after a fixed period, so the benefit eventually runs out.

</details>

<details><summary>◯ <b>D.</b> Savings Plans</summary>

❌ **Incorrect.** Savings Plans trade a 1-year or 3-year spend commitment for a discount. They are not a Free Tier offer.

</details>

📖 **Study:** [2.2 AWS Free Tier Types](../README.md#22-aws-free-tier-types)

---

### Question 4

In a standalone AWS account (one that is not part of AWS Organizations), which of the following tasks can ONLY be performed by the root user?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Closing the AWS account</summary>

✅ **Correct.** In a standalone account, closing the account and changing the root email address or password require root credentials. In AWS Organizations, authorized principals in the management account can close member accounts.

</details>

<details><summary>◯ <b>B.</b> Launching an Amazon EC2 instance</summary>

❌ **Incorrect.** This is a routine task. An IAM user or role with the right permissions can do it.

</details>

<details><summary>◯ <b>C.</b> Creating an IAM user</summary>

❌ **Incorrect.** An IAM administrator can create users, so the root user is not needed for this.

</details>

<details><summary>◯ <b>D.</b> Creating an Amazon S3 bucket</summary>

❌ **Incorrect.** Any identity with the right S3 permissions can create a bucket.

</details>

📖 **Study:** [2.1 AWS Account Creation & Root User Rules](../README.md#21-aws-account-creation--root-user-rules)

---

### Question 5

Which TWO actions follow security best practices for the AWS account root user?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> Use the root user for everyday administrative tasks</summary>

❌ **Incorrect.** Daily work should use an IAM administrator or IAM Identity Center. Keep the root user for the few tasks that require it.

</details>

<details><summary>☐ <b>B.</b> Share the root user password with all administrators</summary>

❌ **Incorrect.** Shared root credentials remove accountability and widen the attack surface.

</details>

<details><summary>☐ <b>C.</b> Enable multi-factor authentication (MFA) on the root user</summary>

✅ **Correct.** MFA adds a second factor to protect the most powerful identity in the account.

</details>

<details><summary>☐ <b>D.</b> Create root access keys and embed them in applications</summary>

❌ **Incorrect.** Hard-coded root keys are a severe risk. Applications should use IAM roles with temporary credentials.

</details>

<details><summary>☐ <b>E.</b> Do not create access keys for the root user</summary>

✅ **Correct.** Root access keys give unrestricted programmatic access to the whole account. Use IAM roles or users instead.

</details>

📖 **Study:** [2.1 AWS Account Creation & Root User Rules](../README.md#21-aws-account-creation--root-user-rules)

---

[⬅️ Study guide: 2. 🛡️ Getting Started & Account Security Baseline](../README.md#2-️-getting-started--account-security-baseline) · [📚 All topics](README.md) · [Next: 3. 🌐 AWS Global Infrastructure ➡️](03-global-infrastructure.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
