# Understanding AWS Marketplace Vendor Insights<a name="vendor-insights-understanding"></a>

AWS Marketplace Vendor Insights gathers compliance artifacts and security control information for your product and presents it in a dashboard\. The dashboard takes data from the product owner's self\-assessment, evidence from audit reports, and live evidence from AWS accounts\. This data feeds into the security controls, and then to the dashboard for buyers to review\. 

The dashboard presents the evidence\-based information gathered by AWS Marketplace Vendor Insights from multiple security control categories\. This provides buyers with a near real\-time view of the security profile and reduces discussions between the buyer and seller\. Buyers can validate a vendor’s information completing assessments within a few hours\. AWS Marketplace Vendor Insights provides a mechanism for vendors to keep security and compliance posture information up\-to\-date automatically\. They can share it with buyers on\-demand which eliminates the need to respond to questionnaires on a random basis\.



AWS Marketplace Vendor Insights gathers the evidence\-based information from three sources: 
+ **Your production accounts** – Of the multiple controls, 30 controls support live evidence gathering from your production accounts\. Live evidence for each control is generated by evaluating the configuration settings of your AWS resources using one or more AWS Config rules\. AWS Audit Manager captures the evidence and delivers it to the AWS Marketplace Vendor Insights dashboard\. The onboarding AWS CloudFormation template automates the prerequisite steps required for enabling live evidence gathering, such as: 
  + Turning on AWS Config and the AWS Audit Manager service\.
  + Creating AWS Config rules and the AWS Audit Manager self\-assessment\.
  + Provisioning the AWS Identity and Access Management \(IAM\) role so that AWS Marketplace Vendor Insights can pull assessment results\.
+ **Your ISO 27001 and SOC2 Type II report** – The control categories are mapped to controls in the International Organization for Standardization \(ISO\) and System and Organization Controls \(SOC2\) reports\. When you share these reports with AWS Marketplace Vendor Insights, it can extract relevant evidence from these reports and present it on the dashboard\.
+ **Your vendor self\-assessment** – The CloudFormation template sets up an AWS Marketplace Vendor Insights self\-assessment in AWS Audit Manager\. You can complete this assessment to provide information for all 140 control categories\. You can upload supporting documents for each control using AWS Audit Manager\. 
**Note**  
If you enable automated evidence gathering from the production environments and share your ISO and SOC2 reports, you are only required to answer 29 of the more than 140 controls\. You can identify these 29 controls by the control name that contains "requires manual attestation"\. 

For more information about sharing artifacts with AWS Marketplace, refer to [How to upload artifacts on AWS Marketplace](vendor-insights-onboarding.md#upload-artifacts)\. 