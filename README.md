# wix-connector
Repository for the Wix connector

The .authconfig file needs an "api_key" property

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

## Products
Insert:

Minimal object:
```
{
  "_id": "2",
  "$origin": "a",
  "product": {
    "name": "Test product 5",
    "priceData": {
      "price": 6
    },
    "productType": "physical"
  }
}
```