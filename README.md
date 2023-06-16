# wix-connector
Repository for the Wix connector

The .authconfig file needs an "api_key" property

# TODO last modified

## Collections

TODO

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
    "$based_on_properties": TODO
```

## Inventory

TODO


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
    "$based_on_properties": TODO
```

## Siteproperties

TODO

## Transactions

TODO