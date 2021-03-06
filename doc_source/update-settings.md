--------

Amazon DevOps Guru is in preview and available in the following AWS Regions: US West \(Oregon\), US East \(N\. Virginia\), US East \(Ohio\), Europe \(Ireland\), and Asia Pacific \(Tokyo\)\.

The preview is open to all AWS accounts\. You do not need to request access\. Features might be added or changed before General Availability is announced\. Contact us at [amazon\-devops\-guru\-feedback@amazon\.com](mailto:amazon-devops-guru-feedback@amazon.com) with feedback\.

--------

# Update DevOps Guru settings<a name="update-settings"></a>

 You can update the following Amazon DevOps Guru settings\. 
+ Your DevOps Guru coverage\. This determines which resources in your account are analyzed\. 
+ Your notifications\. This determines which Amazon Simple Notification Service topics are used to notify you of important DevOps Guru events\. 
+ Your AWS Systems Manager integration\. This determines whether an OpsItem is created in Systems Manager OpsCenter for each new insight\. 

**Topics**
+ [Update your AWS analysis coverage in DevOps Guru](#update-coverage)
+ [Update your notifications in DevOps Guru](#update-notifications)
+ [Update AWS Systems Manager integration in DevOps Guru](#update-systems-manager-integration)

## Update your AWS analysis coverage in DevOps Guru<a name="update-coverage"></a>

 You can update which AWS resources in your account DevOps Guru analyzes\. The resources that are analyzed make up your DevOps Guru coverage boundary\. You have three boundary coverage options\. 
+ Choose to have DevOps Guru analyze all supported resources in your account\. 
+ Specify specific resources by choosing AWS CloudFormation stacks that define those resources\. If you do this, DevOps Guru analyzes every resource specified in the stacks you choose\. If a resource in your account is not defined by a stack you choose, it is not analyzed\. 
+ Specify to have no resources analyzed\. 

 DevOps Guru supports all resources that are associated with supported services\. For more information, see [Supported AWS services in DevOps Guru](quotas.md#services-devops-guru)\. 

**To manage your DevOps Guru analysis coverage**

1. Open the Amazon DevOps Guru console at [https://console\.aws\.amazon\.com/codeguru/devops\-guru/](https://console.aws.amazon.com/codeguru/devops-guru/)\. 

1. Choose **Settings** in the navigation pane\. 

1. In **DevOps Guru analysis coverage**, choose **Manage**\.

1. Choose one of the following coverage options\. 
   + Choose **Analyze all AWS resources in the current account** if you want DevOps Guru to analyze all supported resources in your AWS account\. If you choose this option, your account is your resource analysis coverage boundary\. 
   + Choose **Specify which resources in the current AWS account to analyze using CloudFormation stacks** if you want DevOps Guru to analyze the resources that are in stacks you choose\. 

     1. If you have not enabled any stacks, in **CloudFormation stacks**, choose **Manage analysis coverage**\. 

     1. Select up to 200 stacks that contain the resources that you want analyzed\. You can enter the name of a stack in **Find stacks** to quickly locate a specific stack\. 

     1. Choose **Save**\. 

     For more information, see [Working with AWS CloudFormation stacks in DevOps Guru](working-with-cfn-stacks.md)\.
   +  Choose **Don't analyze any resources** if you do not want DevOps Guru to analyze any resources\. 

1. Choose **Save**\. 

## Update your notifications in DevOps Guru<a name="update-notifications"></a>

Set up Amazon Simple Notification Service topics that are used to notify you about important Amazon DevOps Guru events\. You can choose from a list of topic names that already exist in your AWS account, enter the name for a new topic that DevOps Guru creates in your account, or enter the Amazon Resource Name \(ARN\) of an existing topic in any AWS account in your Region\. If you specify the ARN of a topic that is not in your account, you must grant permission for DevOps Guru to access that topic by adding an IAM policy to it\. For more information, see [Permissions for cross account Amazon SNS topics](sns-required-permissions.md)\. You can specify up to two topics\. 

 DevOps Guru sends notifications for the following events\. 
+  A new insight is created\. 
+  A new anomaly is added to an insight\. 
+  The severity of an insight is upgraded from `Low` or `Medium` to `High`\. 
+  The status of an insight changes from ongoing to resolved\. 
+  A recommendation for an insight is identified\. 

**To update your notifications**

1. Open the Amazon DevOps Guru console at [https://console\.aws\.amazon\.com/codeguru/devops\-guru/](https://console.aws.amazon.com/codeguru/devops-guru/)\. 

1.  Choose **Settings** in the navigation pane\. 

1.  In **SNS notifications**, choose **Set up notifications** if you have not set up any notifications\. Otherwise, choose **Edit**\. 

1.  To add an Amazon SNS topic, do one of the following\. 
   +  Choose **Chose an existing SNS topic in your AWS account**\. Then, from **Choose a topic in your AWS account**, choose the topic you want to use\. 
   +  Choose **Create a new SNS topic**\. Then, in **Create a new topic**, enter the name for your new topic\. 
   +  Choose **Use an SNS topic ARN to specify an existing account**\. Then, in **Enter an ARN for a topic**, enter the topic ARN\. The ARN is the topic's Amazon Resource Name\. You can specify a topic in a different account\. If you use a topic in another account, you must add a resource policy to the topic\. For more information, see [Permissions for cross account Amazon SNS topics](sns-required-permissions.md)\. 

1.  Choose **Add SNS topic** if you want to add a second topic\. 

1.  Choose **Save**\. 

1. To remove an Amazon SNS topic, choose **Remove** next to the topic you want to remove\. 

## Update AWS Systems Manager integration in DevOps Guru<a name="update-systems-manager-integration"></a>

You can enable the creation of an OpsItem for each new insight in AWS Systems Manager OpsCenter\. OpsCenter is a centralized system where you can view, investigate, and review operational work items \(OpsItems\)\. The OpsItems for your insights can help you manage work that addresses the anomalous behavior that triggered the creation of each insight\. For more information, see [AWS Systems Manager OpsCenter](https://docs.aws.amazon.com/systems-manager/latest/userguide/OpsCenter.html) and [Working with OpsItem](https://docs.aws.amazon.com/systems-manager/latest/userguide/OpsCenter-working-with-OpsItems.html) in the *AWS Systems Manager User Guide*\. 

**To manage your Systems Manager integration**

1. Open the Amazon DevOps Guru console at [https://console\.aws\.amazon\.com/codeguru/devops\-guru/](https://console.aws.amazon.com/codeguru/devops-guru/)\. 

1. Choose **Settings** in the navigation pane\. 

1. In **AWS Systems Manager integration**, select **Enable DevOps Guru to create an AWS OpstItem in OpsCenter for each insight** to have an OpsItem created for each new insight\. Deselect it to stop having an OpsItem created for each new insight\.

You are charged for OpsItems created in your account\. For more information, see [AWS Systems Manager pricing](http://aws.amazon.com/systems-manager/pricing/)\. 