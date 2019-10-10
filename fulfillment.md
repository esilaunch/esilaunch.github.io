# Fulfillment

Fulfillment is used to update an order shipping or pickup status.

## The fulfillment object

```
{
 "fulfillments": [{
  "id": "9a9a8a77-3bfc-4e4f-909b-c09325fddcfc",
  "type": "Shipped",
  "fulfillmentDate": "2018-07-03T07:00:00.000Z",
  "packageCount": 1,
  "items": [{
   "sku": "70010001-01",
   "quantityFulfilled": 1
  }],
  "shipped": {
   "trackingNumbers": ["Z1234231123523234"],
   "carrier": "UPS"
  }
 }]
}
```

## Create a fulfillment (Shipping)

**POST: `/order/:id/fulfillment`**

```
{
 "type": "Shipped",
 "packageCount": 1,
 "items": [{
  "sku": "70010001-01",
  "quantityFulfilled": 1
 }],
 "sendTransactionEmail": true,
 "fulfillmentDate": "2018-07-03T07:00:00.000Z",
 "shipped": {
  "trackingNumbers": ["Z1234231123523234"],
  "carrier": "UPS"
 }
}
```

**RESPONSE**: responds with an order object.

## Create a fulfillment (Pickup)

**POST: `/order/:id/fulfillment`**

```
{
 "type": "Picked Up",
 "packageCount": 1,
 "items": [{
  "sku": "70010001-01",
  "quantityFulfilled": 1
 }],
 "sendTransactionEmail": false,
 "fulfillmentDate": "2018-07-03T07:00:00.000Z",
 "pickedUp": {
  "pickedUpBy": "Jason Andres"
 }
}
```

**RESPONSE**: responds with an order object.

## Delete a fulfillment

**DELETE: `/order/:id/fulfillment/:id`**

**RESPONSE**: responds with a blank object and 204 status.