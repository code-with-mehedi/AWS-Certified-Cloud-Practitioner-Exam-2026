# Practice questions: 12. Application Integration & Messaging

[Study guide: 12. Application Integration & Messaging](../README.md#12--application-integration--messaging) · [All topics](README.md) · [Next: 13. Cloud Governance, Management & Monitoring](13-cloud-governance-management-monitoring.md)

> [!NOTE]
> Read the question and decide on your answer, then click an option to see whether it is right or wrong and why. A round marker (◯) means pick one answer. A square marker (☐) means pick every answer the question asks for, so click each option you think is correct.

### Question 1

A company wants a fully managed front door to publish, secure, and monitor REST APIs that invoke its backend AWS Lambda functions. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon CloudFront</summary>

❌ **Incorrect.** CloudFront is a content delivery network that caches content and is not an API management service.

</details>

<details><summary>◯ <b>B.</b> AWS Step Functions</summary>

❌ **Incorrect.** Step Functions coordinates workflows. It does not publish APIs to clients.

</details>

<details><summary>◯ <b>C.</b> Amazon SNS</summary>

❌ **Incorrect.** SNS sends notifications to subscribers and does not expose REST APIs.

</details>

<details><summary>◯ <b>D.</b> Amazon API Gateway</summary>

✅ **Correct.** API Gateway creates, publishes, secures, and monitors REST, HTTP, and WebSocket APIs at scale.

</details>

Study: [12.2 Orchestration & CI/CD: Step Functions, API Gateway, CodeDeploy, CodePipeline](../README.md#122-orchestration--cicd-step-functions-api-gateway-codedeploy-codepipeline)

### Question 2

A company needs to send a notification to many subscribers at once, including email addresses, SMS numbers, and AWS Lambda functions. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon SNS</summary>

✅ **Correct.** SNS is a pub/sub service that pushes (fans out) a message to all subscribers of a topic.

</details>

<details><summary>◯ <b>B.</b> Amazon SQS</summary>

❌ **Incorrect.** SQS stores messages for consumers to pull and does not push to email or SMS.

</details>

<details><summary>◯ <b>C.</b> AWS Step Functions</summary>

❌ **Incorrect.** Step Functions orchestrates workflows, which is a different job from sending notifications.

</details>

<details><summary>◯ <b>D.</b> Amazon API Gateway</summary>

❌ **Incorrect.** API Gateway publishes and secures APIs. It does not send notifications to subscribers.

</details>

Study: [12.1 SQS vs. SNS vs. EventBridge vs. Kinesis](../README.md#121-sqs-vs-sns-vs-eventbridge-vs-kinesis)

### Question 3

A company wants to decouple its order-processing components so that messages wait in a queue until worker instances poll for them. Which service should it use?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon SQS</summary>

✅ **Correct.** SQS is a managed message queue where consumers pull messages at their own pace, which decouples the components.

</details>

<details><summary>◯ <b>B.</b> Amazon SNS</summary>

❌ **Incorrect.** SNS pushes messages to many subscribers at once and does not hold them for workers to poll.

</details>

<details><summary>◯ <b>C.</b> Amazon EventBridge</summary>

❌ **Incorrect.** EventBridge routes events to targets based on rules. It is not a polling queue.

</details>

<details><summary>◯ <b>D.</b> Amazon Kinesis Data Streams</summary>

❌ **Incorrect.** Kinesis ingests and processes real-time streaming data such as clickstreams, and it does not act as a simple work queue.

</details>

Study: [12.1 SQS vs. SNS vs. EventBridge vs. Kinesis](../README.md#121-sqs-vs-sns-vs-eventbridge-vs-kinesis)

### Question 4

Which service lets a company orchestrate several AWS Lambda functions into a visual workflow with built-in error handling and retries?

*◯ Choose ONE.*

<details><summary>◯ <b>A.</b> Amazon SQS</summary>

❌ **Incorrect.** SQS passes messages between components. It does not model a workflow with steps.

</details>

<details><summary>◯ <b>B.</b> Amazon EventBridge</summary>

❌ **Incorrect.** EventBridge routes events to targets but cannot define multi-step workflows with retries.

</details>

<details><summary>◯ <b>C.</b> AWS Step Functions</summary>

✅ **Correct.** Step Functions runs serverless state machines that coordinate services and handle errors and retries.

</details>

<details><summary>◯ <b>D.</b> AWS CodePipeline</summary>

❌ **Incorrect.** CodePipeline automates software release workflows and does not run workflows between Lambda functions at runtime.

</details>

Study: [12.2 Orchestration & CI/CD: Step Functions, API Gateway, CodeDeploy, CodePipeline](../README.md#122-orchestration--cicd-step-functions-api-gateway-codedeploy-codepipeline)

### Question 5

Which TWO statements about AWS developer tools are correct?

*☐ Choose TWO.*

<details><summary>☐ <b>A.</b> AWS CloudFormation deploys new application code versions to running servers</summary>

❌ **Incorrect.** CloudFormation provisions infrastructure from templates. CodeDeploy runs application rollouts.

</details>

<details><summary>☐ <b>B.</b> AWS CodePipeline compiles source code itself</summary>

❌ **Incorrect.** CodePipeline orchestrates the source, build, test, and deploy stages. CodeBuild handles the compiling.

</details>

<details><summary>☐ <b>C.</b> AWS CodeDeploy automates deploying application code to Amazon EC2 instances and on-premises servers</summary>

✅ **Correct.** CodeDeploy supports in-place and blue/green deployments.

</details>

<details><summary>☐ <b>D.</b> AWS CodeBuild provisions infrastructure from JSON or YAML templates</summary>

❌ **Incorrect.** Template-based provisioning belongs to CloudFormation.

</details>

<details><summary>☐ <b>E.</b> AWS CodeBuild compiles source code and runs tests</summary>

✅ **Correct.** CodeBuild is a fully managed build service.

</details>

Study: [12.2 Orchestration & CI/CD: Step Functions, API Gateway, CodeDeploy, CodePipeline](../README.md#122-orchestration--cicd-step-functions-api-gateway-codedeploy-codepipeline)

[Study guide: 12. Application Integration & Messaging](../README.md#12--application-integration--messaging) · [All topics](README.md) · [Next: 13. Cloud Governance, Management & Monitoring](13-cloud-governance-management-monitoring.md)

*Original exam-style practice questions written for this study guide. They are not actual AWS exam questions, and this project is not affiliated with or endorsed by AWS.*
