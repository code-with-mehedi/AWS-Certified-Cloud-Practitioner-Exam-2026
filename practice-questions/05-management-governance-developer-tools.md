# 📝 Practice Questions: 5. 🧰 Management, Governance & Developer Tools

[⬅️ Study guide: 5. 🧰 Management, Governance & Developer Tools](../README.md#5--management-governance--developer-tools) · [📚 All topics](README.md) · [Next: 6. 🤝 AWS Shared Responsibility Model ➡️](06-shared-responsibility-model.md)

> [!NOTE]
> **How to practice:** read the question, decide on your answer, then **click an option** to reveal whether it is ✅ right or ❌ wrong, and why. ◯ means choose **one** answer. ☐ means choose **all** the answers the question asks for, so click each option you think is correct.

---

### Question 1

A company needs to deploy the same AWS CloudFormation template to 40 AWS accounts across 3 Regions in a single operation. Which feature should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS Systems Manager</summary>

❌ **Incorrect.** Systems Manager manages and patches nodes. It does not provision infrastructure from templates.

</details>

<details><summary>◯ <b>B.</b> AWS CodeDeploy</summary>

❌ **Incorrect.** CodeDeploy rolls out application code to servers. It does not provision infrastructure.

</details>

<details><summary>◯ <b>C.</b> AWS CodePipeline</summary>

❌ **Incorrect.** CodePipeline automates a release workflow from source to deployment. It does not deploy one template to many accounts and Regions by itself.

</details>

<details><summary>◯ <b>D.</b> AWS CloudFormation StackSets</summary>

✅ **Correct.** StackSets deploy one template to multiple accounts and Regions in a single operation.

</details>

📖 **Study:** [5.3 Infrastructure as Code (IaC): CloudFormation & StackSets & CDK](../README.md#53-infrastructure-as-code-iac-cloudformation--stacksets--cdk)

---

### Question 2

Which access method typically authenticates requests with an access key ID and a secret access key?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Signing in to the AWS Management Console with an IAM user name and password</summary>

❌ **Incorrect.** Console sign-in uses a user name, a password, and optionally MFA, not access keys.

</details>

<details><summary>◯ <b>B.</b> The AWS CLI and AWS SDKs (programmatic access)</summary>

✅ **Correct.** Programmatic requests are signed with access keys. Prefer temporary credentials from IAM roles where possible.

</details>

<details><summary>◯ <b>C.</b> Opening AWS CloudShell from the console</summary>

❌ **Incorrect.** CloudShell reuses your console sign-in credentials, so no access keys are needed.

</details>

<details><summary>◯ <b>D.</b> Signing in to the console through IAM Identity Center</summary>

❌ **Incorrect.** Identity Center uses single sign-on with temporary credentials rather than long-term access keys.

</details>

📖 **Study:** [5.4 Developer Tools & Access Credentials](../README.md#54-developer-tools--access-credentials)

---

### Question 3

Which AWS service lets an administrator patch operating systems and run commands across a fleet of EC2 instances and on-premises servers without opening SSH ports?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS CloudFormation</summary>

❌ **Incorrect.** CloudFormation provisions infrastructure from templates. It does not patch or operate servers.

</details>

<details><summary>◯ <b>B.</b> AWS CodeDeploy</summary>

❌ **Incorrect.** CodeDeploy deploys application code. It is not a general fleet patching and command tool.

</details>

<details><summary>◯ <b>C.</b> AWS Systems Manager</summary>

✅ **Correct.** Patch Manager, Run Command, and Session Manager manage nodes at scale through the SSM Agent without inbound SSH.

</details>

<details><summary>◯ <b>D.</b> AWS Config</summary>

❌ **Incorrect.** Config records resource configuration changes and checks compliance. It does not run commands on servers.

</details>

📖 **Study:** [5.5 AWS Systems Manager (SSM)](../README.md#55-aws-systems-manager-ssm)

---

### Question 4

A developer wants to run AWS CLI commands from a web browser without installing anything locally, already signed in with their console credentials. Which service should they use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> AWS SDK for Python (Boto3)</summary>

❌ **Incorrect.** The SDK is a code library used inside applications. It is not a browser-based shell.

</details>

<details><summary>◯ <b>B.</b> AWS CloudFormation</summary>

❌ **Incorrect.** CloudFormation provisions infrastructure from templates. It does not provide a command-line environment.

</details>

<details><summary>◯ <b>C.</b> AWS Systems Manager Session Manager</summary>

❌ **Incorrect.** Session Manager opens a shell on managed instances. It is not an AWS CLI environment for your account.

</details>

<details><summary>◯ <b>D.</b> AWS CloudShell</summary>

✅ **Correct.** CloudShell is a browser-based shell that is pre-authenticated with your console credentials and comes with the AWS CLI preinstalled.

</details>

📖 **Study:** [5.1 Ways to Interact with AWS (Console, CLI, SDK, CloudShell)](../README.md#51-ways-to-interact-with-aws-console-cli-sdk-cloudshell)

---

### Question 5

Which TWO statements about the AWS Cloud Development Kit (AWS CDK) are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> It lets developers define cloud infrastructure in programming languages such as TypeScript and Python</summary>

✅ **Correct.** The CDK is an open-source framework for describing infrastructure in familiar languages.

</details>

<details><summary>☐ <b>B.</b> It deploys application code to on-premises servers</summary>

❌ **Incorrect.** That is the job of AWS CodeDeploy.

</details>

<details><summary>☐ <b>C.</b> It synthesizes the code into AWS CloudFormation templates</summary>

✅ **Correct.** Deployments still run through CloudFormation.

</details>

<details><summary>☐ <b>D.</b> It only supports YAML templates</summary>

❌ **Incorrect.** The CDK uses general-purpose programming languages. YAML and JSON are CloudFormation template formats.

</details>

<details><summary>☐ <b>E.</b> It replaces CloudFormation by provisioning resources directly</summary>

❌ **Incorrect.** The CDK generates CloudFormation templates and relies on CloudFormation to provision resources.

</details>

📖 **Study:** [5.3 Infrastructure as Code (IaC): CloudFormation & StackSets & CDK](../README.md#53-infrastructure-as-code-iac-cloudformation--stacksets--cdk)

---

[⬅️ Study guide: 5. 🧰 Management, Governance & Developer Tools](../README.md#5--management-governance--developer-tools) · [📚 All topics](README.md) · [Next: 6. 🤝 AWS Shared Responsibility Model ➡️](06-shared-responsibility-model.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
