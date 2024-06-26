# AWS Marketplace Seller Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in
connection with any product or service that is not Amazon's,
in any manner that is likely to cause confusion among customers,
or in any manner that disparages or discredits Amazon. All other
trademarks not owned by Amazon are the property of their respective
owners, who may or may not be affiliated with, connected to, or
sponsored by Amazon.

-----
## Contents
+ [What is AWS Marketplace?](what-is-marketplace.md)
+ [Getting started as a seller](user-guide-for-sellers.md)
   + [Seller registration process](seller-registration-process.md)
   + [Seller toolkit](additional-seller-tools.md)
      + [AWS MarketplaceCommerce Analytics Service](commerce-analytics-service.md)
      + [AWS Marketplace Field Demonstration Program](field-demonstration-program.md)
      + [Product Support Connection](product-support-connection.md)
      + [More resources in AWS Marketplace Management Portal](more-seller-resources.md)
+ [Preparing your product](product-preparation.md)
   + [Product pricing](pricing.md)
      + [Product refunds in AWS Marketplace](refunds.md)
   + [Regions and countries for your AWS Marketplace product](regions-and-countries.md)
   + [Private offers](private-offers-overview.md)
      + [Flexible payment scheduler](flexible-payment-scheduler.md)
      + [Consulting partner private offers](consulting-partner-offers.md)
         + [Creating a resell opportunity for a consulting partner as an ISV](consulting-partner-isv-info.md)
         + [Creating a private offer as a consulting partner](consulting-partner-info.md)
      + [Private offer upgrades and renewals](private-offers-upgrades-and-renewals.md)
   + [Standardized contracts in AWS Marketplace](standardized-license-terms.md)
   + [Categories and metadata](categories-and-metadata.md)
   + [AMI and container product usage instructions](ami-container-product-usage-instructions.md)
   + [Search engine optimization for products](search-engine-optimization.md)
+ [AWS Marketplace for Desktop Applications (AMDA)](amda.md)
+ [AMI-based products](ami-products.md)
   + [Understanding AMI-based products](ami-getting-started.md)
   + [Single-AMI products](ami-single-ami-products.md)
   + [AMI-based delivery using AWS CloudFormation](cloudformation.md)
      + [Adding serverless application components](cloudformation-serverless-application.md)
   + [Private images](private-images.md)
   + [Best practices for building AMIs](best-practices-for-building-your-amis.md)
   + [AMI product pricing](pricing-ami-products.md)
      + [Custom metering pricing for AMI products](custom-metering-pricing-ami-products.md)
      + [Contract pricing for AMI products](ami-contracts.md)
   + [AMI product billing, metering, and licensing integrations](ami-product-billing-metering-licensing-integrations.md)
      + [Custom metering for AMI products with AWS Marketplace Metering Service](custom-metering-with-mp-metering-service.md)
      + [Contract pricing for AMI products with AWS License Manager](ami-license-manager-integration.md)
   + [Amazon SNS notifications for AMI products](ami-notification.md)
   + [AMI product checklist](aws-marketplace-listing-checklist.md)
   + [AMI-based product requirements](product-and-ami-policies.md)
+ [Container-based products](container-based-products.md)
   + [Getting started with container products](container-product-getting-started.md)
   + [Container-based product requirements](container-product-policies.md)
   + [Container products pricing](pricing-container-products.md)
   + [Container product billing, metering, and licensing integrations](container-products-billing-integration.md)
      + [Hourly metering with AWS Marketplace Metering Service](container-metering-registerusage.md)
         + [Integrating your container product with the AWS Marketplace Metering Service using the AWS SDK for Java](java-integration-example-registerusage.md)
      + [Custom metering for container products with AWS Marketplace Metering Service](container-metering-meterusage.md)
         + [Integrating your container product with the AWS Marketplace Metering Service using the AWS SDK for Java](java-integration-example-meterusage.md)
      + [Contract pricing for Container products with AWS License Manager](container-license-manager-integration.md)
         + [Integrating an AWS Marketplace for Containers Anywhere product with License Manager](container-anywhere-license-manager-integration.md)
   + [Amazon SNS notifications for container products](container-notification.md)
+ [Machine learning products](machine-learning-products.md)
   + [Security and intellectual property](ml-security-and-intellectual-property.md)
   + [Machine learning product pricing](machine-learning-pricing.md)
   + [Prepare your product in SageMaker](ml-prepare-your-product-in-sagemaker.md)
      + [Packaging your code into images](ml-packaging-your-code-into-images.md)
         + [Model package images](ml-model-package-images.md)
         + [Algorithm images](ml-algorithm-images.md)
      + [Uploading your images](ml-uploading-your-images.md)
      + [Creating your Amazon SageMaker resource](ml-creating-your-amazon-sagemaker-resource.md)
   + [Publishing your product in AWS Marketplace](ml-publishing-your-product-in-aws-marketplace.md)
   + [Requirements and best practices for creating machine learning products](ml-listing-requirements-and-best-practices.md)
   + [Service restrictions and quotas](ml-service-restrictions-and-limits.md)
   + [Troubleshooting](ml-troubleshooting.md)
   + [Reporting](ml-reporting.md)
+ [Software as a service (SaaS)–based products](saas-products.md)
   + [Getting started with SaaS products](saas-getting-started.md)
      + [Creating a SaaS product](saas-create-product.md)
      + [Create an initial SaaS product page](saas-create-product-page.md)
      + [SaaS product settings](saas-product-settings.md)
      + [Integrate your SaaS subscription product](saas-integrate-subscription.md)
      + [Integrate your SaaS contract product](saas-integrate-contract.md)
      + [Integrate your SaaS contract with pay-as-you-go product](saas-integrate-contract-with-pay.md)
      + [Deploy a serverless SaaS integration solution](deploy-serverless-saas.md)
   + [Plan your SaaS product](saas-prepare.md)
   + [SaaS product guidelines](saas-guidelines.md)
   + [SaaS product pricing](saas-pricing-models.md)
      + [Pricing for SaaS subscriptions](saas-subscriptions.md)
      + [Pricing for SaaS contracts](saas-contracts.md)
   + [SaaS free trials](saas-free-trials.md)
   + [SaaS customer onboarding](saas-product-customer-setup.md)
   + [Amazon SNS notifications for SaaS products](saas-notification.md)
   + [Accessing the AWS Marketplace Metering and Entitlement Service APIs](saas-integration-metering-and-entitlement-apis.md)
      + [Metering for usage](metering-for-usage.md)
      + [Checking entitlements](checking-entitlements.md)
      + [SaaS product integration checklist](aws-marketplace-integration-checklist.md)
   + [Reporting](saas-reporting.md)
   + [Code examples for SaaS product integration](saas-code-examples.md)
   + [Using AWS PrivateLink with AWS Marketplace](privatelink.md)
+ [Professional services products](proserv-products.md)
   + [Getting started with professional services products](proserv-getting-started.md)
   + [Providing details for a professional services product](proserv-product-details.md)
   + [Requirements for professional services products](proserv-product-guidelines.md)
   + [Professional services product pricing](pricing-proserv-products.md)
+ [Data products](data-products.md)
+ [Submitting your product for publication](product-submission.md)
+ [Marketing your product](product-marketing.md)
+ [Notifications for AWS Marketplace events](notifications.md)
+ [Seller reports, data feeds, and dashboards](reports-and-data-feed.md)
   + [Seller Delivery Data Feeds Service](data-feed-service.md)
      + [Data feed tables overview](data-feed-joining.md)
      + [Data feed query examples](data-feed-full-examples.md)
      + [Data feeds](data-feeds.md)
         + [Account data feed](data-feed-account.md)
         + [Address data feed](data-feed-address.md)
         + [Billing event data feed](data-feed-billing-event.md)
         + [Legacy mapping data feed](data-feed-legacy-mapping.md)
         + [Offer data feed](data-feed-offer.md)
         + [Offer product data feed](data-feed-offer-product.md)
         + [Offer target data feed](data-feed-offer-target.md)
         + [Product data feed](data-feed-product.md)
         + [Tax item data feed](data-feed-tax-item.md)
   + [Seller reports](Reporting.md)
      + [Daily business report](daily-business-report.md)
      + [Daily customer subscriber report](daily-customer-subscriber-report.md)
      + [Disbursement report](monthly-disbursement-report.md)
      + [Monthly billed revenue report](monthly-billed-revenue-report.md)
      + [Sales compensation report](sales-compensation-report.md)
      + [US sales and use tax report](u.s.-sales-and-use-tax-report.md)
   + [Supplementary reports](supplementary-reports.md)
   + [Seller dashboards](dashboards.md)
      + [Billed revenue dashboard](billed-revenue-dashboard.md)
      + [Collections and disbursement dashboard](collections-disbursement-dashboard.md)
+ [AWS Marketplace Vendor Insights](vendor-insights.md)
   + [Understanding AWS Marketplace Vendor Insights](vendor-insights-understanding.md)
   + [Setting up AWS Marketplace Vendor Insights](vendor-insights-setting-up.md)
   + [Viewing your AWS Marketplace Vendor Insights profile](vendor-insights-profile.md)
   + [Managing snapshots in AWS Marketplace Vendor Insights](vendor-insights-snapshot.md)
   + [Controlling access in AWS Marketplace Vendor Insights](vendor-insights-seller-controlling-access.md)
+ [AWS Marketplace security](security.md)
   + [Controlling access to AWS Marketplace Management Portal](marketplace-management-portal-user-access.md)
   + [Policies and permissions for AWS Marketplace sellers](detailed-management-portal-permissions.md)
   + [AWS managed policies for AWS Marketplace sellers](security-iam-awsmanpol.md)
   + [AWS Marketplace Commerce Analytics Service account permissions](set-aws-iam-cas-permissions.md)
   + [AWS Marketplace Product Support Connection account permissions](set-aws-iam-psc-permissions.md)
   + [Amazon SQS permissions](set-aws-iam-sqs-permissions.md)
   + [AWS Marketplace metering and entitlement API permissions](iam-user-policy-for-aws-marketplace-actions.md)
   + [Logging AWS Marketplace API calls with AWS CloudTrail](logging-aws-marketplace-api-calls-with-aws-cloudtrail.md)
+ [Document history](document-history.md)
+ [AWS glossary](glossary.md)