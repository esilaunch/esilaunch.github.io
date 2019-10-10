# Notes

Notes can be added to customers and orders.

## The note object

```
{
    "type": "Note",
    "content": "Test Note",
    "noteDate": "2018-06-07T18:03:56.067Z",
    "customerId": "e6418130-51f4-42f7-b295-c2874d156008"
}
```

## Create a note

**POST: `/note`**

```
{
    "type": "Note",
    "content": "Test Note",
    "noteDate": "2018-06-07T18:03:56.067Z",
    "customerId": "e6418130-51f4-42f7-b295-c2874d156008"
}
```

**RESPONSE**: responds with a note object.

## Retrieve a note

**GET: `/note/:id`**

**RESPONSE**: responds with a note object.

## Update a note

**PUT: `/note/:id`**

```
{
    "type": "Note",
    "content": "Test Note Update",
    "customerId": "e6418130-51f4-42f7-b295-c2874d156008"
}
```

**RESPONSE**: responds with a note object.

## Delete a note

**DELETE: `/note/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all notes

**GET: `/note`**

**OPTIONS**: optional query parameters include: q, customerId and orderId. Query params may look like note?customerId=e6418130-51f4-42f7-b295-c2874d156008

**RESPONSE**: responds with an array of note objects and a total count.

```
{
 "notes": [{
  "id": "edcc43c2-66c7-46a6-a8e0-48878fa72da1",
  "type": "Note",
  "noteDate": "2018-06-07T23:18:06.249Z",
  "content": "Note 2",
  "customerId": "e6418130-51f4-42f7-b295-c2874d156008",
  "createdAt": "2018-06-07T23:18:06.360Z",
  "updatedAt": "2018-06-07T23:18:06.360Z"
 }, {
  "id": "f70e92d8-ae86-4e89-b061-9f9c0f4fb99a",
  "type": "Note",
  "noteDate": "2018-06-07T23:18:03.090Z",
  "content": "Note 1",
  "customerId": "e6418130-51f4-42f7-b295-c2874d156008",
  "createdAt": "2018-06-07T23:18:03.210Z",
  "updatedAt": "2018-06-07T23:18:03.210Z"
 }],
 "total": 2
}
```


