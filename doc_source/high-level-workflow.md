--------

Amazon DevOps Guru is in preview and available in the following AWS Regions: US West \(Oregon\), US East \(N\. Virginia\), US East \(Ohio\), Europe \(Ireland\), and Asia Pacific \(Tokyo\)\.

The preview is open to all AWS accounts\. You do not need to request access\. Features might be added or changed before General Availability is announced\. Contact us at [amazon\-devops\-guru\-feedback@amazon\.com](mailto:amazon-devops-guru-feedback@amazon.com) with feedback\.

--------

# High level DevOps Guru workflow<a name="high-level-workflow"></a>

The Amazon DevOps Guru workflow can be broken down into three high level steps\. First, you specify DevOps Guru coverage by telling it which AWS resources in your AWS account you want it to analyze\. Second, DevOps Guru starts analyzing Amazon CloudWatch metrics, AWS CloudTrail, and other operational data to identify problems that you can fix to improve your operations\. Third, DevOps Guru makes sure you know about insights and important information by sending you a notification for important DevOps Guru events\. You can also configure DevOps Guru to create an OpsItem in AWS Systems Manager OpsCenter to help you track your insights\. The following diagram shows this high\-level workflow\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/devops-guru/latest/userguide/)![\[Image NOT FOUND\]](http://docs.aws.amazon.com/devops-guru/latest/userguide/)

1. In the first step, you choose your coverage by specifying which AWS resources in your AWS account are analyzed\. DevOps Guru can cover, or analyze, all the resources in an AWS account, or you can use AWS CloudFormation stacks to specify a subset of the resources in your account to analyze\. Make sure that the resources you specify make up your business critical applications, workloads, and micro\-services\. For information about which AWS services are supported by DevOps Guru, see [Supported AWS services in DevOps Guru](quotas.md#services-devops-guru)\.

1. In the second step, DevOps Guru analyzes the resources to generate insights\. This is an ongoing process\. You can view the insights and see the recommendations and related information they contain in the DevOps Guru console\. DevOps Guru analyzes the following data to find issues and create insights\. 
   + Individual Amazon CloudWatch metrics emitted by your AWS resources\. When an issue is identified, DevOps Guru collects those metrics together\. 
   + DevOps Guru pulls enrichment data from AWS CloudTrail management logs to find events that are related to the collected metrics\. The events can be resource deployment events and configuration changes\. 
   + If you use AWS CodeDeploy, DevOps Guru analyzes deployment events to help generate insights\. Events for all types of CodeDeploy deployments \(on\-premises server, Amazon EC2 server, Lambda, or Amazon EC2\) are analyzed\. 
   + When DevOps Guru finds a specific pattern, it generates one or more recommendations to help mitigate or fix the identified issue\. The recommendations are collected in one insight\. The insight also contains a list of the metrics and events that are related to the issue\. You use the insight data to address and understand the identified problem\. 

1. In the third step, DevOps Guru integrates insight notification into your work flow to help you manage issues and quickly address them\. 
   + Insights generated in your AWS account are published to the Amazon Simple Notification Service \(Amazon SNS\) topic chosen during DevOps Guru setup\. This is how you are notified as soon as an insight is created\. For more information, see [Update your notifications in DevOps Guru](update-settings.md#update-notifications)\.
   + If you enabled AWS Systems Manager during DevOps Guru setup, each insight creates a corresponding OpsItem to help you track and manage the issues discovered\. For more information, see [Update AWS Systems Manager integration in DevOps Guru](update-settings.md#update-systems-manager-integration)\.