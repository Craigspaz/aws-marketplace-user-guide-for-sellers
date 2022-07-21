# Product data feed<a name="data-feed-product"></a>

This data feed provides information about all products you've created as the seller of record and all products you're authorized to resell\.

Product data is mutable\. This means that when you change the value for one of the following fields, a new record is created in the data feed with a different value for `valid_from` field\. For more information about the data feed history columns, see [Historization of the data](data-feed-service.md#data-feed-historization)\.

The product data feed is refreshed every 24 hours, so new data is available daily\.

The following table explains the names and descriptions of the data feed's columns\. 


| Column name  | Description  | 
| --- | --- | 
| product\_id | The friendly identifier of the product\.Can used to join to the `product_id` fields of the `Account`, `Billing_Event`, and `Offer_Product` data feeds\. | 
| manufacturer\_account\_id | The identifier of the product owner\. This is a foreign key to the [Account](data-feed-account.md) data feed\.Can used to join to the `account_id` field of the `Account` data feed\. | 
| product\_code | The existing entitlement product code used to meter the product\. This value is also used to join data with a report, or to reference what is provided in AWS Marketplace Metering Service\. | 
| title | The title of the product\.  | 

## Example of product data feed<a name="data-feed-product-sample-data"></a>

The following shows an example of the offer target data feed\. For readability, the data history columns aren't shown\. For information about data history fields, see [Historization of the data](data-feed-service.md#data-feed-historization)\. 


| product\_id  | manufacturer\_account\_id  | product\_code | title | 
| --- | --- | --- | --- | 
| prod\-o4grxfafcxxxx | 555568000000 | product\_code\_1 | Product1 | 
| prod\-t3grxfafcxxxy | 444457000000 | product\_code\_2 | Product2 | 
| prod\-x8faxxfafcxxy | 666678000000 | product\_code\_3 | Product3 | 