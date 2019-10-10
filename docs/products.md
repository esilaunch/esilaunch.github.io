# Products

Products must have one or more variants and the SKU must be unique.

## The product object

```
{
   "id":"89e4318b-9374-40f7-9da8-52769e046388",
   "title":"Caliva Afternoon Delight - Vape Cartridge",
   "subTitle":null,
   "image":"https://images.commerce7.com/hedony/images/original/img_1254-edit-edit-1547945621497.jpg",
   "type":"Cannabis",
   "departmentId":null,
   "vendorId":null,
   "teaser":"Afternoon Delight (Indica-Hybrid): Not quite quitting time, but almost. Sweet, earthy, satisfying and chill…like happy hour…with your shoes off.",
   "content":"<p>Find your session. These classy cartridges are the essence of cannabis refined with flavors so tasty you simply can't resist an extra pull. We&rsquo;ve crafted experiences catered to any and every moment with all-natural cold-pressed CO2 and cannabis-derived terpenes that pack a punch in potency.</p>\n<p>&nbsp;</p>",
   "webStatus":"Available",
   "adminStatus":"Available",
   "slug":"caliva-afternoon-delight---vape-cartridge",
   "metaData":{
      "review":"Really great!"
   },
   "productTemplateId":null,
   "createdAt":"2019-01-20T00:53:51.245Z",
   "updatedAt":"2019-09-16T20:12:58.442Z",
   "images":[
      {
         "id":"12238c43-b674-4ca0-9874-64345919a8b5",
         "src":"https://images.commerce7.com/hedony/images/original/img_1254-edit-edit-1547945621497.jpg",
         "sortOrder":0
      }
   ],
   "bundleItems":[

   ],
   "variants":[
      {
         "id":"b04291ec-b5b6-4478-8b1f-b4ae2881c334",
         "title":"300mg",
         "sku":"FI1KP8",
         "upcCode":null,
         "volumeInML":null,
         "costOfGood":2475,
         "price":3499,
         "comparePrice":null,
         "bottleDeposit":0,
         "sortOrder":1,
         "hasInventory":true,
         "inventoryPolicy":"Dont Sell",
         "hasShipping":true,
         "taxType":"Cannabis",
         "weight":0.3,
         "inventory":[
            {
               "reserveCount":0,
               "allocatedCount":0,
               "productVariantId":"b04291ec-b5b6-4478-8b1f-b4ae2881c334",
               "inventoryLocationId":"03e558df-494e-4920-8f23-08c67df70e11",
               "availableForSaleCount":0
            },
            {
               "reserveCount":1,
               "allocatedCount":13,
               "productVariantId":"b04291ec-b5b6-4478-8b1f-b4ae2881c334",
               "inventoryLocationId":"8cc83fcd-b5de-443f-9de4-ee1a539df475",
               "availableForSaleCount":5
            }
         ]
      }
   ],
   "tenantIds":[

   ],
   "collections":[
      {
         "id":"329e77f1-f583-4020-a31b-c73ce3709ef4",
         "title":"Vape",
         "content":"",
         "publishDate":"2018-12-26T21:48:00.000Z",
         "slug":"vape",
         "productTemplateId":"814be405-16cc-455d-bd9f-600c01b21a2e",
         "type":"Manual",
         "productCount":null,
         "appliesToCondition":null,
         "onlyShowProductsWithInventory":false,
         "createdAt":"2018-12-26T21:48:28.025Z",
         "updatedAt":"2019-01-30T14:37:42.239Z",
         "seo":{
            "title":"Vape",
            "description":null
         }
      },
      {
         "id":"94b5f18e-c53a-4b32-854c-d5f284ee24ef",
         "title":"Shop",
         "content":"",
         "publishDate":"2019-01-15T07:06:00.000Z",
         "slug":"shop",
         "productTemplateId":"814be405-16cc-455d-bd9f-600c01b21a2e",
         "type":"Manual",
         "productCount":null,
         "appliesToCondition":null,
         "onlyShowProductsWithInventory":false,
         "createdAt":"2019-01-15T07:06:31.329Z",
         "updatedAt":"2019-01-30T14:44:10.311Z",
         "seo":{
            "title":"Shop",
            "description":null
         }
      }
   ],
   "seo":{
      "title":"Caliva Afternoon Delight - Vape Cartridge",
      "description":"Find your session. These classy cartridges are the essence of cannabis refined with flavors so tasty you simply can't resist an extra pull. We&rsquo;ve..."
   },
   "security":{
      "availableTo":"Public"
   },
   "overrideOperatingRegions":{
      "isOverride":false,
      "operatingStateCodes":null,
      "operatingCountryCodes":null
   }
}
```

## Create a product

**POST: `/product`**

```
{
 "id": "dd143573-263d-481d-a6c0-e4101e93a6c2",
 "title": "Gorilla Glue",
 "subTitle": null,
 "image": null,
 "type": "Wine",
 "departmentId": "5e253ffd-007c-435f-ad56-ff06649d06d5",
 "vendorId": null,
 "teaser": null,
 "content": null,
 "publishDate": "2018-12-05T06:05:00.000Z",
 "slug": "gorilla-glue",
 "productTemplateId": null,
 "createdAt": "2018-12-05T06:09:19.472Z",
 "updatedAt": "2018-12-05T06:09:19.472Z",
 "images": [],
 "variants": [{
  "id": "d7fc72a1-45f4-4c63-910c-37fc16edc809",
  "title": "3.5g",
  "sku": "83747572",
  "upcCode": null,
  "volumeInML": null,
  "costOfGood": 300,
  "price": 1000,
  "comparePrice": 1100,
  "bottleDeposit": 0,
  "sortOrder": 1,
  "hasInventory": true,
  "inventoryPolicy": "Back Order",
  "hasShipping": true,
  "taxType": "Cannabis",
  "weight": 3.5,
  "inventory": [{
   "id": "6106fc6a-d322-477a-b525-802b4eac0102",
   "tenantId": "hedony",
   "reserveCount": 0,
   "allocatedCount": 0,
   "productVariantId": "d7fc72a1-45f4-4c63-910c-37fc16edc809",
   "inventoryLocationId": "88145cdc-f5a6-11e8-a80a-06d2aa911ccc",
   "availableForSaleCount": 100
  }]
 }],
 "collections": [],
 "tenantIds": [],
 "seo": {
  "title": "Gorilla Glue 3.5g",
  "description": null
 },
 "security": {
  "availableTo": "Public"
 },
 "overrideOperatingRegions": {
  "isOverride": false,
  "operatingStateCodes": null,
  "operatingCountryCodes": null
 }
}
```

**RESPONSE**: responds with a product object.

## Retrieve a product

**GET: `/product/:id`**

**RESPONSE**: responds with a product object.

## Update a product

**PUT: `/product/:id`**

```
{
 "id": "dd610462-f307-4aa8-bf7b-e7e10843d496",
 "title": "White Widow 3.5g",
 "type": "Cannabis",
 "publishDate": "2018-05-20T07:36:00.000Z",
 "slug": "white-widow",
 "createdAt": "2018-05-20T07:37:44.230Z",
 "updatedAt": "2018-05-20T07:40:33.762Z",
 "variants": [{
  "id": "608c2695-7a53-4126-a5f3-64f9a650916e",
  "title": "3.5g",
  "sku": "2015-M",
  "volumeInML": null,
  "costOfGood": 500,
  "price": 4000,
  "comparePrice": 4500,
  "sortOrder": 1,
  "hasInventory": false,
  "inventoryPolicy": "Back Order",
  "hasShipping": true,
  "taxType": "Cannabis",
  "weight": 3.5,
  "weightUnits": "G"
 }],
 "seo": {
  "title": "White Widow 3.5g"
 }
}
```

**RESPONSE**: responds with a product object.

## Delete a products

**DELETE: `/product/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all products

**GET: `/product`**

**OPTIONS**: ptional query parameters include: q, updatedAt, createdAt. Query params may look like ?q=white

**RESPONSE**: responds with an array of product objects and a total count.

```
{
 "products": [{
   "id":"89e4318b-9374-40f7-9da8-52769e046388",
   "title":"Caliva Afternoon Delight - Vape Cartridge",
   "subTitle":null,
   "image":"https://images.commerce7.com/hedony/images/original/img_1254-edit-edit-1547945621497.jpg",
   "type":"Cannabis",
   "departmentId":null,
   "vendorId":null,
   "teaser":"Afternoon Delight (Indica-Hybrid): Not quite quitting time, but almost. Sweet, earthy, satisfying and chill…like happy hour…with your shoes off.",
   "content":"<p>Find your session. These classy cartridges are the essence of cannabis refined with flavors so tasty you simply can't resist an extra pull. We&rsquo;ve crafted experiences catered to any and every moment with all-natural cold-pressed CO2 and cannabis-derived terpenes that pack a punch in potency.</p>\n<p>&nbsp;</p>",
   "webStatus":"Available",
   "adminStatus":"Available",
   "slug":"caliva-afternoon-delight---vape-cartridge",
   "metaData":{
      "review":"Really great!"
   },
   "productTemplateId":null,
   "createdAt":"2019-01-20T00:53:51.245Z",
   "updatedAt":"2019-09-16T20:12:58.442Z",
   "images":[
      {
         "id":"12238c43-b674-4ca0-9874-64345919a8b5",
         "src":"https://images.commerce7.com/hedony/images/original/img_1254-edit-edit-1547945621497.jpg",
         "sortOrder":0
      }
   ],
   "bundleItems":[

   ],
   "variants":[
      {
         "id":"b04291ec-b5b6-4478-8b1f-b4ae2881c334",
         "title":"300mg",
         "sku":"FI1KP8",
         "upcCode":null,
         "volumeInML":null,
         "costOfGood":2475,
         "price":3499,
         "comparePrice":null,
         "bottleDeposit":0,
         "sortOrder":1,
         "hasInventory":true,
         "inventoryPolicy":"Dont Sell",
         "hasShipping":true,
         "taxType":"Cannabis",
         "weight":0.3,
         "inventory":[
            {
               "reserveCount":0,
               "allocatedCount":0,
               "productVariantId":"b04291ec-b5b6-4478-8b1f-b4ae2881c334",
               "inventoryLocationId":"03e558df-494e-4920-8f23-08c67df70e11",
               "availableForSaleCount":0
            },
            {
               "reserveCount":1,
               "allocatedCount":13,
               "productVariantId":"b04291ec-b5b6-4478-8b1f-b4ae2881c334",
               "inventoryLocationId":"8cc83fcd-b5de-443f-9de4-ee1a539df475",
               "availableForSaleCount":5
            }
         ]
      }
   ],
   "tenantIds":[

   ],
   "collections":[
      {
         "id":"329e77f1-f583-4020-a31b-c73ce3709ef4",
         "title":"Vape",
         "content":"",
         "publishDate":"2018-12-26T21:48:00.000Z",
         "slug":"vape",
         "productTemplateId":"814be405-16cc-455d-bd9f-600c01b21a2e",
         "type":"Manual",
         "productCount":null,
         "appliesToCondition":null,
         "onlyShowProductsWithInventory":false,
         "createdAt":"2018-12-26T21:48:28.025Z",
         "updatedAt":"2019-01-30T14:37:42.239Z",
         "seo":{
            "title":"Vape",
            "description":null
         }
      },
      {
         "id":"94b5f18e-c53a-4b32-854c-d5f284ee24ef",
         "title":"Shop",
         "content":"",
         "publishDate":"2019-01-15T07:06:00.000Z",
         "slug":"shop",
         "productTemplateId":"814be405-16cc-455d-bd9f-600c01b21a2e",
         "type":"Manual",
         "productCount":null,
         "appliesToCondition":null,
         "onlyShowProductsWithInventory":false,
         "createdAt":"2019-01-15T07:06:31.329Z",
         "updatedAt":"2019-01-30T14:44:10.311Z",
         "seo":{
            "title":"Shop",
            "description":null
         }
      }
   ],
   "seo":{
      "title":"Caliva Afternoon Delight - Vape Cartridge",
      "description":"Find your session. These classy cartridges are the essence of cannabis refined with flavors so tasty you simply can't resist an extra pull. We&rsquo;ve..."
   },
   "security":{
      "availableTo":"Public"
   },
   "overrideOperatingRegions":{
      "isOverride":false,
      "operatingStateCodes":null,
      "operatingCountryCodes":null
   }
},
  {
   "id":"91299f0b-0664-45eb-9f0c-c1365b827375",
   "title":"CBD Vape Cartridge 1:1",
   "subTitle":null,
   "image":"https://images.commerce7.com/hedony/images/original/cbd-1-1561742292414.jpg",
   "type":"Cannabis",
   "departmentId":null,
   "vendorId":null,
   "teaser":"Good for nighttime use. The 1:1 is typically psychoactive and may cause sleepiness.",
   "content":"<p>Breath in fast-acting&nbsp;<span class=\"caps\">CBD</span>&nbsp;relief. Care By Design vape cartridges work with a standard vape pen and battery. Ideal for quick relief.</p>\n<p>&nbsp;</p>\n<p>Fast-acting, smoke free and easy to use relief. Ingredients: 100% Cannabis oil. Our cannabis oil is cleanly extracted using a supercritical CO2 method, and our products are lab tested to ensure the highest quality. We test for cannabinoid and terpene profiles, potency, and contamination. Our CBD-rich cannabis oil is extracted from local, sustainably grown cannabis.</p>",
   "webStatus":"Available",
   "adminStatus":"Available",
   "slug":"cbd-vape-cartridge-1-1",
   "metaData":null,
   "productTemplateId":null,
   "createdAt":"2019-06-28T17:18:52.110Z",
   "updatedAt":"2019-06-28T17:18:52.110Z",
   "images":[
      {
         "id":"60cd9171-2e2d-42e0-a5f3-d3bbf6c34d4f",
         "src":"https://images.commerce7.com/hedony/images/original/cbd-1-1561742292414.jpg",
         "sortOrder":0
      }
   ],
   "bundleItems":[

   ],
   "variants":[
      {
         "id":"97d30b6b-43fd-4709-90a6-47e9bf75e9ed",
         "title":"500mg",
         "sku":"canna34278274",
         "upcCode":null,
         "volumeInML":null,
         "costOfGood":1700,
         "price":3400,
         "comparePrice":null,
         "bottleDeposit":0,
         "sortOrder":1,
         "hasInventory":false,
         "inventoryPolicy":"Back Order",
         "hasShipping":false,
         "taxType":"Cannabis",
         "weight":0,
         "inventory":null
      }
   ],
   "tenantIds":[

   ],
   "collections":[

   ],
   "seo":{
      "title":"CBD Vape Cartridge 1:1",
      "description":"Breath in fast-acting CBD relief. Care By Design vape cartridges work with a standard vape pen and battery. Ideal for quick relief.\n \nFast-acting, smoke free..."
   },
   "security":{
      "availableTo":"Public"
   },
   "overrideOperatingRegions":{
      "isOverride":false,
      "operatingStateCodes":null,
      "operatingCountryCodes":null
   }
}
 ],
 "total": 2
}
```
