# Coupons

## The coupon object

```
{
 "id": "84b0c0de-afce-4a93-bad0-8dcb2adc0849",
 "code": "50Off",
 "title": "50% Off",
 "actionMessage": null,
 "usageLimitType": "Unlimited",
 "usageLimit": null,
 "appliesTo": "Store",
 "appliesToObjectIds": null,
 "productDiscountType": "Percentage Off",
 "productDiscount": 50,
 "shippingDiscountType": "No Discount",
 "shippingDiscount": null,
 "startDate": "2018-05-18T04:10:38.835Z",
 "endDate": null,
 "status": "Enabled",
 "minimumCartAmount": null,
 "availableTo": "Everyone",
 "availableToObjectIds": null,
 "createdAt": "2018-05-18T16:53:46.157Z",
 "updatedAt": "2018-05-18T16:53:46.157Z",
 "promotionSets": []
}
```

## Create a coupon

**POST: `/coupon`**

```
{
 "title": "$10.00 Off",
 "actionMessage": "$10.00 off orders $50 and over until May 31st",
 "usageLimitType": "Unlimited",
 "appliesTo": "Store",
 "productDiscountType": "Dollar Off",
 "productDiscount": 1000,
 "shippingDiscountType": "No Discount",
 "status": "Enabled",
 "minimumCartAmount": 5000,
 "availableTo": "Everyone",
 "code": "10off",
 "startDate": "2018-05-22T07:00:00.000Z",
 "endDate": "2018-06-01T06:59:00.000Z"
}
```

**RESPONSE**: responds with a coupon object.

## Retrieve a coupon

**GET: `/coupon/:id`**

**RESPONSE**: responds with a coupon object.

## Update a coupon

**PUT: `/coupon/:id`**

```
{
 "title": "$10.00 Off",
 "actionMessage": "$10.00 off orders $50 and over until May 31st",
 "usageLimitType": "Unlimited",
 "usageLimit": null,
 "appliesTo": "Store",
 "appliesToObjectIds": null,
 "productDiscountType": "Dollar Off",
 "productDiscount": 1000,
 "shippingDiscountType": "No Discount",
 "shippingDiscount": null,
 "status": "Enabled",
 "minimumCartAmount": 5000,
 "availableTo": "Everyone",
 "availableToObjectIds": null,
 "promotionSets": [],
 "code": "10offmay",
 "startDate": "2018-05-22T07:00:00.000Z",
 "endDate": "2018-06-01T06:59:00.000Z"
}
```

**RESPONSE**: responds with a coupon object.

## Delete a coupon

**DELETE: `/coupon/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all coupons

**GET: `/coupon`**

**OPTIONS**: optional query parameters include: q.

**RESPONSE**: responds with an array of coupon objects and a total count.

```
{
 "coupons": [{
  "id": "d9e4d110-8c65-4f80-848a-538a4d8dbfd7",
  "code": "10offmay",
  "title": "$10.00 Off",
  "actionMessage": "$10.00 off orders $50 and over until May 31st",
  "usageLimitType": "Unlimited",
  "usageLimit": null,
  "appliesTo": "Store",
  "appliesToObjectIds": null,
  "productDiscountType": "Dollar Off",
  "productDiscount": 1000,
  "shippingDiscountType": "No Discount",
  "shippingDiscount": null,
  "startDate": "2018-05-22T07:00:00.000Z",
  "endDate": "2018-06-01T06:59:00.000Z",
  "status": "Enabled",
  "minimumCartAmount": 5000,
  "availableTo": "Everyone",
  "availableToObjectIds": null,
  "createdAt": "2018-05-22T15:56:29.192Z",
  "updatedAt": "2018-05-22T15:57:39.672Z",
  "promotionSets": []
 }, {
  "id": "84b0c0de-afce-4a93-bad0-8dcb2adc0849",
  "code": "50Off",
  "title": "50% Off",
  "actionMessage": null,
  "usageLimitType": "Unlimited",
  "usageLimit": null,
  "appliesTo": "Store",
  "appliesToObjectIds": null,
  "productDiscountType": "Percentage Off",
  "productDiscount": 50,
  "shippingDiscountType": "No Discount",
  "shippingDiscount": null,
  "startDate": "2018-05-18T04:10:38.835Z",
  "endDate": null,
  "status": "Enabled",
  "minimumCartAmount": null,
  "availableTo": "Everyone",
  "availableToObjectIds": null,
  "createdAt": "2018-05-18T16:53:46.157Z",
  "updatedAt": "2018-05-18T16:53:46.157Z",
  "promotionSets": []
 }],
 "total": 2
}
```
