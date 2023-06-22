# wix-connector
Repository for the Wix connector

The .authconfig file needs an "api_key" property. In addition, you need to add these env-vars manually (for now):

```
  "wix-site-id": "<wix site id here>"
```

For convenience, you can put this into a "test-env.json" file locally, but make sure you don't include it in any 
subsequent `git add` or `git commit` command!

## Contacts
Insert:

Minimal object:
```
{
  "_id": "1",
  "$origin": "1",
  "info": {
    "name": {
      "first": "Bob"
    }
  }
}
```

Updated:
```
    "$based_on_properties": [
        "createdDate",
        "updatedDate",
        "id",
        "info.*"             # for example "info.name.last"
    ]
```

## Inventory
Insert: cannot be inserted directly, but inserting a new product will create a new inventory

Updated:
```
    "$based_on_properties": [
        "externalId",
        "id",
        "lastUpdated",
        "numericId",
        "productId",
        "trackQuantity"
    ]
```

## Members
Insert:



Updated:
```
    "$based_on_properties": [
        "activityStatus",
        "contactId",
        "createdDate",
        "id",
        "privacyStatus",
        "status",
        "updatedDate"
    ]
```

## Orders
Insert:

Minimal object:
```
{
  "_id:" "foo",
  "$origin": "faf",
  "channelInfo": {
    "type": "WEB"
  },
  "lineItems": [
    {
      "name": "some product",
      "priceData": {
        "price": "5"
      },
      "quantity": 1
    }
  ],
  "paymentStatus": "PAID",
  "shippingInfo": {
    "shipmentDetails": {
      "address": {
        "email": "hans@example.com"
      }
    }
  },
  "totals": {
    "subtotal": "10",
    "total": "10"
  }
}
```

Updated:

There are several endpoints related to updating an order, but not a "general" endpoint that lets you update several 
fields at once, see https://dev.wix.com/api/rest/wix-stores/orders. We have 

PUT   `stores/v2/orders/{orderId}/fulfillments/{fulfillmentId}`

PATCH `stores/v2/orders/{orderId}/updateEmail`

PUT   `stores/v2/orders/{orderId}/updateShippingAddress`

## Products
Insert:

Minimal object:
```
{
  "_id": "2",
  "$origin": "a",
  "name": "Test product 5",
  "priceData": {
    "price": 6
  },
  "productType": "physical"
}
```

Updated:
```
    "$based_on_properties": [
        "name",
        "description",
        "collectionIds",
        "createdDate",
        "exportProductId",
        "id",
        "inventoryItemId",
        "lastUpdated",
        "manageVariants",
        "numericId",
        "productType",
        "slug",
        "visible",
        "weight"
    ]
```

## Currencies (currency converter)

Currencies are only available as a collection, there's no insert, get, delete or update APIs.

