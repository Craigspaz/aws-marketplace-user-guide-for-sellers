# Getting started as a seller<a name="user-guide-for-sellers"></a>

 If you want to sell your software in AWS Marketplace, review the requirements and then follow the steps to register as a seller\. There are different registration requirements based on where you reside and what type of products you're selling\. To register as a seller in AWS Marketplace, you can use an existing AWS account or create a new account\. All AWS Marketplace interactions are tied to the account that you choose\. 

**Notes**  
Registering as an AWS Marketplace seller is a prerequisite to listing data products on AWS Data Exchange and making them available on AWS Marketplace\. For more information about these requirements, see [Providing Data Products on AWS Data Exchange](https://docs.aws.amazon.com/data-exchange/latest/userguide/providing-data-sets.html) in the *AWS Data Exchange User Guide*\.
For information about the permissions that AWS Marketplace sellers need, see [Policies and permissions for AWS Marketplace sellers](detailed-management-portal-permissions.md)\.
For more information about product listing fees, registered sellers can view the [AWS Marketplace Seller Terms](https://aws.amazon.com/marketplace/management/seller-settings/terms) in the AWS Marketplace Management Portal\.

## Seller requirements for publishing free software products<a name="seller-requirements-for-publishing-free-products"></a>

 Regardless of whether you charge for your product when you offer it in AWS Marketplace, you're selling that product\. The cost to the customer is $0\.00, but you and the customer agree to a mutual contract for use of the product\. If you offer only free products, you don't have to provide banking information to AWS Marketplace\. To create and offer free products in AWS Marketplace, you must: 
+  Sell publicly available, full\-feature production\-ready software\. 
+  Have a defined customer support process and support organization\. 
+  Provide a means to keep software regularly updated and free of vulnerabilities\. 
+  Follow best practices and guidelines when marketing your product in AWS Marketplace\. 
+  Be an AWS customer in good standing and meet the requirements in the terms and conditions for AWS Marketplace sellers\. 

## Additional seller requirements for paid products<a name="additional-seller-requirements-for-paid-products"></a>

If you charge for your products or offer Bring Your Own License model \(BYOL\) products, you must also meet the following requirements and provide this additional information:
+ You must be a permanent resident or citizen in an [eligible jurisdiction](#eligible-jurisdictions), or a business entity organized or incorporated in one of those areas\.
+  You must provide tax and bank account information\. For US\-based entities, a W\-9 form and a banking account from a US\-based bank are required\. 
+ Non\-US sellers are required to provide a \(i\) W\-8 form, value\-added tax \(VAT\) or goods and services tax \(GST\) registration number, and \(ii\) US bank information\. If you don't have a US bank account, you can register for a virtual US bank account from [Hyperwallet](https://wssellers.hyperwallet.com/)\. 
+ To provide data products, you must also request on\-boarding through the [Create case](https://console.aws.amazon.com/support/cases?#/create?issueType=customer-service) wizard for AWS Support\.
+ To sell products to customers whose AWS accounts are based in countries and territories in Europe, the Middle East, and Africa \(EMEA\) \(excluding Turkey and South Africa\) through Amazon Web Services EMEA SARL, you must [complete the **Know Your Customer** process](seller-registration-process.md#completing-the-know-your-customer-process)\. In addition:
  + You receive up to two disbursements \(for transactions through AWS Inc\. and Amazon Web Services EMEA SARL\)\.
  + You may be taxed on the listing fee for certain transactions, depending on location\. For more information about taxes, see the [AWS Marketplace Sellers Tax](https://aws.amazon.com/tax-help/marketplace/) help page\. If value\-added tax \(VAT\) on your listing fee is assessed, AWS Marketplace will provide a tax\-compliant invoice\.
  + For more information about Amazon Web Services EMEA SARL, see *AWS EMEA Marketplace \- Sellers* on the [Amazon Web Services Europe FAQs](https://aws.amazon.com/legal/aws-emea/) website\.

 To sell into the AWS GovCloud \(US\) Region, sellers must have an [AWS GovCloud \(US\) account](https://aws.amazon.com/govcloud-us/getting-started/)\. For details on ITAR requirements, see the *[AWS GovCloud \(US\) User Guide](https://docs.aws.amazon.com/govcloud-us/latest/UserGuide/getting-started-sign-up.html)*\. 

 For questions about AWS Marketplace seller requirements or the registration process, contact the [AWS Marketplace Seller Operations](https://aws.amazon.com/marketplace/management/contact-us/) team\.

### Eligible jurisdictions for paid products<a name="eligible-jurisdictions"></a>

To sell paid software in AWS Marketplace, you must be a permanent resident or citizen in one of the following countries or SARs, or a business entity organized or incorporated therein: 
+ Australia¹
+ Bahrain¹ ²
+ European Union \(EU\) member state¹
+ Hong Kong SAR
+ Israel¹ ²
+ Japan² ³
+ New Zealand¹
+ Norway¹ ²
+ Qatar
+ Switzerland¹ ²
+ United Arab Emirates \(UAE\)¹ ²
+ United Kingdom \(UK\)¹
+ United States \(US\)

¹ Sellers of paid products in these countries must provide VAT registration information in country of establishment\. 

² If you as a seller are located in the same country as the buyer, you may be responsible for tax invoicing, collections, and remittances\. Please consult with your tax advisor\.

³ Sellers based in Japan have an obligation to self\-account for the Japanese Consumption Tax \(JCT\) on the listing fee charges\. Sellers based in other jurisdictions may have similar obligations\. Please consult with your tax advisor\.

For more information about VAT, invoicing, and your tax obligations as a seller, see [AWS Marketplace Sellers](https://aws.amazon.com/tax-help/marketplace/) on [Amazon Web Service Tax Help](https://aws.amazon.com/tax-help/)\.

## AWS Marketplace Management Portal<a name="management-portal"></a>

 The [AWS Marketplace Management Portal](https://aws.amazon.com/marketplace/management/tour) is the tool that you use to register as an AWS Marketplace seller\. Then, you can use the portal to manage the products that you sell in AWS Marketplace\. You can complete the following tasks on the portal:
+  Register as an AWS Marketplace seller\. 
+  Use the **Products** page to submit new software products and update existing software products\. 
+  Monitor the status of your requests\. 
+  Upload files needed to create and manage your new software products\. 
+  Manage your software products into incremental channel revenue by taking advantage of the go\-to\-market activities\. 
+  Measure the results of your marketing efforts within hours of launch, including the usage and revenue driven by your campaigns\. 
+ Enable customer service representatives to retrieve customer data in real time\.
+  Initiate an automatic Amazon Machine Image \(AMI\) scan to detect vulnerabilities\. 

**Note**  
Data products are published and managed from the AWS Data Exchange console\. AWS Data Exchange providers can use the AWS Marketplace Management Portal to register as a seller, request AWS Data Exchange on\-boarding, access seller reports, and submit refund requests\.

 All registered sellers can access the AWS Marketplace Management Portal using their AWS credentials for the account that they used to create their products\. The account that you use is defined as the seller of record when a customer subscribes to your product\. If you need help determining the specific account that is the seller of record for your products, contact the [AWS Marketplace Seller Operations](https://aws.amazon.com/marketplace/management/contact-us/) team\. 

 AWS Marketplace strongly recommends using AWS Identity and Access Management \(IAM\) roles to sign in to the AWS Marketplace Management Portal rather than using your root account credentials\. For more information, see [AWS Marketplace security](https://docs.aws.amazon.com/en_us/marketplace/latest/userguide/security.html)\. 