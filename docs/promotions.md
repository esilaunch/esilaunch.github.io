# Promotions

## The promotion object

```
{
 "id": "8ac801c3-8bf9-4bd3-a65c-cd05dbdbaf15",
 "title": "$10 Off",
 "actionMessage": null,
 "usageLimitType": "Unlimited",
 "usageLimit": null,
 "appliesTo": "Store",
 "appliesToObjectIds": null,
 "productDiscountType": "Dollar Off",
 "productDiscount": 10,
 "shippingDiscountType": "No Discount",
 "shippingDiscount": null,
 "startDate": "2018-05-18T04:10:38.857Z",
 "endDate": null,
 "status": "Enabled",
 "minimumCartAmount": null,
 "availableTo": "Everyone",
 "availableToObjectIds": null,
 "createdAt": "2018-05-18T16:53:46.166Z",
 "updatedAt": "2018-05-18T16:53:46.166Z",
 "promotionSets": []
}
```

## Create a promotion

**POST: `/promotion`**

```
{
 "title": "Free Shipping",
 "actionMessage": "Free Shipping Until End of June on orders $100 and up.",
 "usageLimitType": "Unlimited",
 "appliesTo": "Product",
 "appliesToObjectIds": ["047d1599-9168-4a63-85d5-71b984984d53"],
 "productDiscountType": "No Discount",
 "shippingDiscountType": "Percentage Off",
 "shippingDiscount": 10000,
 "status": "Enabled",
 "minimumCartAmount": 10000,
 "availableTo": "Club",
 "availableToObjectIds": ["138cc09d-62d7-4298-8bfc-fd2fc3fddc79"],
 "startDate": "2018-05-22T07:00:00.000Z",
 "endDate": "2018-07-01T06:59:00.000Z"
}
```

**RESPONSE**: responds with a promotion object.

## Retrieve a promotion

**GET: `/promotion/:id`**

**RESPONSE**: responds with a promotion object.

## Update a promotion

**PUT: `/promotion/:id`**

```
{
 "title": "Free Shipping",
 "actionMessage": "Free Shipping Until End of June on orders $100 and up.",
 "usageLimitType": "Unlimited",
 "usageLimit": null,
 "appliesTo": "Product",
 "appliesToObjectIds": ["047d1599-9168-4a63-85d5-71b984984d53"],
 "productDiscountType": "No Discount",
 "productDiscount": null,
 "shippingDiscountType": "Percentage Off",
 "shippingDiscount": 10000,
 "status": "Enabled",
 "minimumCartAmount": 10000,
 "availableTo": "Club",
 "availableToObjectIds": ["138cc09d-62d7-4298-8bfc-fd2fc3fddc79"],
 "promotionSets": [{
  "id":"279c3a37-8b06-49d4-a588-9911bda7f917"
 }],
 "startDate": "2018-05-22T07:00:00.000Z",
 "endDate": "2018-07-01T06:59:00.000Z"
}
```

**RESPONSE**: responds with a promotion object.

## Delete a promotion

**DELETE: `/promotion/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all promotions

**GET: `/promotion`**

**OPTIONS**: optional query parameters include: q.

**RESPONSE**: responds with an array of promotion objects and a total count.

```
{
 "promotions": [{
  "id": "8ac801c3-8bf9-4bd3-a65c-cd05dbdbaf15",
  "title": "$10 Off",
  "actionMessage": null,
  "usageLimitType": "Unlimited",
  "usageLimit": null,
  "appliesTo": "Store",
  "appliesToObjectIds": null,
  "productDiscountType": "Dollar Off",
  "productDiscount": 10,
  "shippingDiscountType": "No Discount",
  "shippingDiscount": null,
  "startDate": "2018-05-18T04:10:38.857Z",
  "endDate": null,
  "status": "Enabled",
  "minimumCartAmount": null,
  "availableTo": "Everyone",
  "availableToObjectIds": null,
  "createdAt": "2018-05-18T16:53:46.166Z",
  "updatedAt": "2018-05-18T16:53:46.166Z",
  "promotionSets": []
 }, {
  "id": "b6fc94a6-3e6b-4118-9c53-e0818b19e17a",
  "title": "15% Off",
  "actionMessage": null,
  "usageLimitType": "Unlimited",
  "usageLimit": null,
  "appliesTo": "Store",
  "appliesToObjectIds": null,
  "productDiscountType": "Percentage Off",
  "productDiscount": 15,
  "shippingDiscountType": "No Discount",
  "shippingDiscount": null,
  "startDate": "2018-05-18T04:10:38.857Z",
  "endDate": null,
  "status": "Enabled",
  "minimumCartAmount": null,
  "availableTo": "Everyone",
  "availableToObjectIds": null,
  "createdAt": "2018-05-18T16:53:46.165Z",
  "updatedAt": "2018-05-18T16:53:46.165Z",
  "promotionSets": []
 }],
 "total": 2
}
```
