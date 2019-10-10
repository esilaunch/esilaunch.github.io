# Web-hooks

Web-hooks are used to keep remote systems in-sync for customers, products, orders and web-hooks. You have the option to push new, updated and deleted records to a remote URL for consumption.

## The web-hook object

```
{
 "id": "28e547bb-baf4-433b-8c35-05b6e9b0ea04",
 "object": "Customer",
 "action": "Update",
 "url": "https://receivecustomerupdates.mymarketingengine.com",
 "createdAt": "2018-05-22T18:57:01.420Z",
 "updatedAt": "2018-05-22T19:13:08.231Z"
}
```

## Create a web-hook

**POST: `/web-hook`**

```
{
 "object": "Customer",
 "action": "Create",
 "url": "https://receivenewcustomer.mymarketingengine.com"
}
```

**RESPONSE**: responds with a web-hook object.

## Retrieve a web-hook

**GET: `/web-hook/:id`**

**RESPONSE**: responds with a web-hook object.

## Update a web-hook

**PUT: `/web-hook/:id`**

```
{
 "object": "Customer",
 "action": "Delete",
 "url": "https://receivedeletedcustomers.mymarketingengine.com"
}
```

**RESPONSE**: responds with a web-hook object.

## Delete a web-hook

**DELETE: `/web-hook/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all web-hooks

**GET: `/web-hook`**

**RESPONSE**: responds with an array of web-hook objects and a total count.

```
{
 "webHooks": [{
  "id": "28e547bb-baf4-433b-8c35-05b6e9b0ea04",
  "object": "Customer",
  "action": "Delete",
  "url": "https://receivedeletedcustomers.mymarketingengine.com",
  "createdAt": "2018-05-22T18:57:01.420Z",
  "updatedAt": "2018-05-22T19:14:57.640Z"
 }, {
  "id": "8335dc92-1d12-4a42-af6d-4cea607d1b1d",
  "object": "Customer",
  "action": "Create",
  "url": "https://receivecreatedcustomers.mymarketingengine.com",
  "createdAt": "2018-05-22T19:16:16.172Z",
  "updatedAt": "2018-05-22T19:16:16.172Z"
 }, {
  "id": "bd5f4986-a17c-4bfe-bba2-2fcc063c84bd",
  "object": "Customer",
  "action": "Update",
  "url": "https://receiveupdatedcustomers.mymarketingengine.com",
  "createdAt": "2018-05-22T19:16:29.285Z",
  "updatedAt": "2018-05-22T19:16:29.285Z"
 }],
 "total": 3
}
```


