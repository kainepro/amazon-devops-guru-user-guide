--------

Amazon DevOps Guru is in preview and available in the following AWS Regions: US West \(Oregon\), US East \(N\. Virginia\), US East \(Ohio\), Europe \(Ireland\), and Asia Pacific \(Tokyo\)\.

The preview is open to all AWS accounts\. You do not need to request access\. Features might be added or changed before General Availability is announced\. Contact us at [amazon\-devops\-guru\-feedback@amazon\.com](mailto:amazon-devops-guru-feedback@amazon.com) with feedback\.

--------

# What is Amazon DevOps Guru?<a name="welcome"></a>

Welcome to the Amazon DevOps Guru user guide\.

DevOps Guru is a fully managed operations service that makes it easy for developers and operators to improve the performance and availability of their applications\. DevOps Guru lets you offload the administrative tasks associated with identifying operational issues so that you can quickly implement recommendations to improve your application\. DevOps Guru creates reactive insights you can use to improve your application now\. It also creates proactive insights to help you avoid operational issues that might affect your application in the future\. 

DevOps Guru applies machine learning to analyze your operational data and application metrics and events to identify behaviors that deviate from normal operating patterns\. You are notified when DevOps Guru detects an operational issue or risk\. For each issue, DevOps Guru presents intelligent recommendations to address current and predicted future operational issues\. 

To get started, see [How do I get started with DevOps Guru?](#how-do-i-get-started) 

## How does DevOps Guru work?<a name="how-it-works"></a>

The DevOps Guru workflow begins when you configure its coverage and notifications\. After you set up DevOps Guru, it starts to analyze your operational data\. When it detects anomalous behavior, it creates an insight that contains recommendations and lists of metrics and events that are related to the issue\. For each insight, DevOps Guru notifies you\. If you enabled AWS Systems Manager OpsCenter, an OpsItem is created so you can use Systems Manager OpsCenter to track and manage addressing your insights\. Each insight contains recommendations, metrics, and events related to anomalous behavior\. Use information in an insight to help you understand and address the anomalous behavior\.

See [High level DevOps Guru workflow](high-level-workflow.md) for more detail about the three high\-level workflow steps\. See [Detailed DevOps Guru workflow](detailed-workflow.md) to learn about the more detailed DevOps Guru workflow, including how it interacts with other AWS services\. 

**Topics**
+ [High level DevOps Guru workflow](high-level-workflow.md)
+ [Detailed DevOps Guru workflow](detailed-workflow.md)

## How do I get started with DevOps Guru?<a name="how-do-i-get-started"></a>

 We recommend that you complete the following steps: 

1. **Learn** more about DevOps Guru by reading the information in [ DevOps Guru concepts](concepts.md)\. 

1. **Set up** your AWS account, the AWS CLI, and an IAM user by following the steps in [Setting up Amazon DevOps Guru](setting-up.md)\. 

1. **Use** DevOps Guru, following the instructions in [Getting started with DevOps Guru](getting-started.md)\. 