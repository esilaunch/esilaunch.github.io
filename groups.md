# Groups

Groups are used to categorize customers. One customer can belong to one or more more groups. You can then have coupons and promotions assigned to groups. You can also search customers by group.

## The group object

```
{
 "id": "560d385d-3322-4714-8455-501ddb558635",
 "title": "Employee",
 "type": "Manual",
 "createdAt": "2018-02-19T18:17:40.266Z",
 "updatedAt": "2018-02-19T18:17:40.266Z"
}
```

## Create a group

**POST: `/group`**

```
{
 "title": "Employee",
 "type": "Manual"
}
```

**RESPONSE**: responds with a group object.

## Retrieve a group

**GET: `/group/:id`**

**RESPONSE**: responds with a group object.

## Update a group

**PUT: `/group/:id`**

```
{
 "title": "Employee"
}
```

**RESPONSE**: responds with a group object.

## Delete a group

**DELETE: `/group/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all groups

**GET: `/group`**

**RESPONSE**: responds with an array of group objects and a total count.

```
{
 "groups": [{
  "id": "b31b2501-9755-4d54-82fe-d13a835d079a",
  "title": "Employee",
  "type": "Manual",
  "createdAt": "2018-03-26T19:01:37.117Z",
  "updatedAt": "2018-03-26T19:01:37.117Z"
 }, {
  "id": "d49e9207-6ed9-4f78-9f88-bdfb25902ab1",
  "title": "Friends and Family",
  "type": "Manual",
  "createdAt": "2018-05-18T02:48:08.237Z",
  "updatedAt": "2018-05-18T02:48:08.237Z"
 }, {
  "id": "6d5c7948-8c0d-40d0-8c7c-c41fc5d0b9be",
  "title": "Gold Tier Customers",
  "type": "Manual",
  "createdAt": "2018-04-23T21:16:42.976Z",
  "updatedAt": "2018-05-18T02:48:01.142Z"
 }, {
  "id": "c3ec3c78-d6ec-40c4-b7b2-2e89b0004d42",
  "title": "Investor",
  "type": "Manual",
  "createdAt": "2018-03-26T19:01:37.118Z",
  "updatedAt": "2018-03-26T19:01:37.118Z"
 }],
 "total": 4
}
```


