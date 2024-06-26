# Code examples for SaaS product integration<a name="saas-code-examples"></a>

The following code examples can help you integrate your software as a service \(SaaS\) product with the AWS Marketplace APIs that are required for publishing and maintaining your product\.

**Topics**
+ [`ResolveCustomer` code example](#saas-resolvecustomer-example)
+ [`GetEntitlement` code example](#saas-getentitlement-example)
+ [`BatchMeterUsage` code example](#saas-batchmeterusage-example)
+ [`BatchMeterUsage` with usage allocation tagging code example \(Optional\)](#saas-batchmeterusage-tagging)

## `ResolveCustomer` code example<a name="saas-resolvecustomer-example"></a>

The following code example is relevant for all pricing models\. The Python example exchanges a `x-amzn-marketplace-token` token for a `CustomerIdentifier`, `ProductCode`, and `CustomerAWSAccountId`\. The `CustomerAWSAccountId` is the AWS account Id associated with the subscription\. This code runs in an application on your registration website, when you are redirected there from the AWS Marketplace Management Portal\. The redirect is a POST request that includes the token\. 

For more information about `ResolveCustomer`, see [ResolveCustomer](https://docs.aws.amazon.com/marketplacemetering/latest/APIReference/API_ResolveCustomer.html) in the *AWS Marketplace Metering Service API Reference*\.

```
# Import AWS Python SDK and urllib.parse 
import boto3
import urllib.parse as urlparse 

# Resolving Customer Registration Token
formFields = urlparse.parse_qs(postBody)
regToken = formFields['x-amzn-marketplace-token']

# If regToken present in POST request, exchange for customerID
if (regToken):
    marketplaceClient = boto3.client('meteringmarketplace')
    customerData = marketplaceClient.resolve_customer(regToken)
    productCode = customerData['ProductCode']
    customerID = customerData['CustomerIdentifier']
    customerAWSAccountId = customerData['CustomerAWSAccountId']

    # TODO: Store customer information 
    # TODO: Validate no other accounts share the same customerID
```

### Example response<a name="saas-resolvecustomer-example-response"></a>

```
{
    'CustomerIdentifier': 'string',
    'CustomerAWSAccountId':'string',
    'ProductCode': 'string'
}
```

## `GetEntitlement` code example<a name="saas-getentitlement-example"></a>

The following code example is relevant for SaaS products with the contract and SaaS contract with consumption pricing model\. The Python example verifies that a customer has an active entitlement\.

For more information about `GetEntitlement`, see [GetEntitlement](https://docs.aws.amazon.com/marketplaceentitlement/latest/APIReference/API_GetEntitlements.html) in the *AWS Marketplace Entitlement Service API Reference*\.

```
# Import AWS Python SDK
import boto3

marketplaceClient = boto3.client('marketplace-entitlement')

# Filter entitlements for a specific customerID
#
# productCode is supplied after the AWS Marketplace Ops team has published 
# the product to limited
# 
# customerID is obtained from the ResolveCustomer response
entitlement = marketplaceClient.get_entitlements({
    'ProductCode': 'productCode',
    'Filter' : {
        'CUSTOMER_IDENTIFIER': [
            'customerID',
        ]
    },
    'NextToken' : 'string',
    'MaxResults': 123
})

# TODO: Verify the dimension a customer is subscribed to and the quantity, 
# if applicable
```

### Example response<a name="saas-getentitlement-example-response"></a>

The returned value corresponds to the dimensions created when you created the product in the AWS Marketplace Management Portal\.

```
{
   "Entitlements": [ 
      { 
         "CustomerIdentifier": "string",
         "Dimension": "string",
         "ExpirationDate": number,
         "ProductCode": "string",
         "Value": { 
            "BooleanValue": boolean,
            "DoubleValue": number,
            "IntegerValue": number,
            "StringValue": "string"
         }
      }
   ],
   "NextToken": "string"
}
```

## `BatchMeterUsage` code example<a name="saas-batchmeterusage-example"></a>

The following code example is relevant for SaaS subscription and contract with consumption pricing models, but not for SaaS contract products without consumption\. The Python example sends a metering record to AWS Marketplace to charge your customers for pay\-as\-you\-go fees\.

```
# NOTE: Your application will need to aggregate usage for the 
#       customer for the hour and set the quantity as seen below. 
#       AWS Marketplace can only accept records for up to an hour in the past. 
#
# productCode is supplied after the AWS Marketplace Ops team has 
# published the product to limited
#
# customerID is obtained from the ResolveCustomer response

# Import AWS Python SDK
import boto3

usageRecord = [
    {
        'Timestamp': datetime(2015, 1, 1),
        'CustomerIdentifier': 'customerID',
        'Dimension': 'string',
        'Quantity': 123
    }
]

marketplaceClient = boto3.client('meteringmarketplace')

response = marketplaceClient.batch_meter_usage(usageRecord, productCode)
```

For more information about `BatchMeterUsage`, see [BatchMeterUsage](https://docs.aws.amazon.com/marketplacemetering/latest/APIReference/API_BatchMeterUsage.html) in the *AWS Marketplace Metering Service API Reference*\.

### Example response<a name="saas-batchmeterusage-example-response"></a>

```
{
    'Results': [
        {
            'UsageRecord': {
                'Timestamp': datetime(2015, 1, 1),
                'CustomerIdentifier': 'string',
                'Dimension': 'string',
                'Quantity': 123
            },
            'MeteringRecordId': 'string',
            'Status': 'Success' | 'CustomerNotSubscribed' | 'DuplicateRecord'
        },
    ],
    'UnprocessedRecords': [
        {
            'Timestamp': datetime(2015, 1, 1),
            'CustomerIdentifier': 'string',
            'Dimension': 'string',
            'Quantity': 123
        }
    ]
}
```

## `BatchMeterUsage` with usage allocation tagging code example \(Optional\)<a name="saas-batchmeterusage-tagging"></a>

The following code example is relevant for a SaaS subscription and contract with consumption pricing models, but not for SaaS contract products without consumption\. The Python example sends a metering record with appropriate usage allocation tags to AWS Marketplace to charge your customers for pay\-as\-you\-go fees\.

```
# NOTE: Your application will need to aggregate usage for the 
#       customer for the hour and set the quantity as seen below. 
#       AWS Marketplace can only accept records for up to an hour in the past. 
#
# productCode is supplied after the AWS Marketplace Ops team has 
# published the product to limited
#
# customerID is obtained from the ResolveCustomer response

# Import AWS Python SDK
import boto3
import time

usageRecords = [
    {
        "Timestamp": int(time.time()),
        "CustomerIdentifier": "customerID",
        "Dimension": "Dimension1",
        "Quantity":3,
        "UsageAllocations": [ 
            { 
                "AllocatedUsageQuantity": 2, 
                "Tags": 
                    [ 
                        { "Key": "BusinessUnit", "Value": "IT" },
                        { "Key": "AccountId", "Value": "123456789" },
                    ]

            },
            { 
                "AllocatedUsageQuantity": 1, 
                "Tags": 
                    [ 
                        { "Key": "BusinessUnit", "Value": "Finance" },
                        { "Key": "AccountId", "Value": "987654321" },
                    ]

            },
         ]
     }    
]

marketplaceClient = boto3.client('meteringmarketplace')

response = marketplaceClient.batch_meter_usage(UsageRecords=usageRecords, ProductCode="testProduct")
```

For more information about `BatchMeterUsage`, see [BatchMeterUsage](https://docs.aws.amazon.com/marketplacemetering/latest/APIReference/API_BatchMeterUsage.html) in the *AWS Marketplace Metering Service API Reference*\.

### Example response<a name="saas-batchmeterusage-tagging-response"></a>

```
{
    "Results": [
        {
            "Timestamp": "1634691015",
            "CustomerIdentifier": "customerID",
            "Dimension": "Dimension1",
            "Quantity":3,
            "UsageAllocations": [ 
            { 
                "AllocatedUsageQuantity": 2, 
                "Tags": 
                    [ 
                        { "Key": "BusinessUnit", "Value": "IT" },
                        { "Key": "AccountId", "Value": "123456789" },
                    ]

            },
            { 
                "AllocatedUsageQuantity": 1, 
                "Tags": 
                    [ 
                        { "Key": "BusinessUnit", "Value": "Finance" },
                        { "Key": "AccountId", "Value": "987654321" },
                    ]

            },
         ]
            },
            "MeteringRecordId": "8fjef98ejf",
            "Status": "Success"
        },
    ],
    "UnprocessedRecords": [
        {
            "Timestamp": "1634691015",
            "CustomerIdentifier": "customerID",
            "Dimension": "Dimension1",
            "Quantity":3,
            "UsageAllocations": []
        }
    ]
}
```