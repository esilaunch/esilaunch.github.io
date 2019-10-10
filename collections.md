# Collections

Collections are used to group and display products on your website and pos.

## The collection object

```
{
 "id": "dfdd3929-5a24-4340-b9e1-eedfe25e8a63",
 "title": "Flowers",
 "type": "Manual",
 "content": "Collection of all flowers",
 "publishDate": "2018-05-18T04:10:38.833Z",
 "slug": "flowers",
  "featureImage":
  "https://images.commerce7.com/images/collection/flowers.png",
 "createdAt": "2018-05-18T16:53:47.913Z",
 "updatedAt": "2018-05-18T16:53:47.913Z",
 "seo": {
  "title": "Flowers",
  "description": "Collection of all flowers"
 }
}
```

## Create a collection

**POST: `/collection`**

```
{
 "title": "Gold Library Extracts",
 "content": "Library extracts reserved for gold club members",
 "type": "Manual"
}
```

**RESPONSE**: responds with a collection object.

## Retrieve a collection

**GET: `/collection/:id`**

**RESPONSE**: responds with a collection object.

## Update a collection

**PUT: `/collection/:id`**

```
{
 "title": "Gold Library Extracts",
 "content": "<p>Library extracts reserved for gold club members.</p>",
 "featureImage": "https://images.commerce7.com/images/collection/gold_library_extracts-1526928166546.png",
 "slug": "gold-library-extracts",
 "publishDate": "2018-05-21T18:41:00.000Z",
 "seo": {
  "title": "Gold Library Extracts",
  "description": "Library extracts reserved for gold club members."
 }
}
```

**RESPONSE**: responds with a collection object.

## Delete a collection

**DELETE: `/collection/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all collections

**GET: `/collection`**

**OPTIONS**: optional query parameters include: q and isPublished. Query params may look like collection?isPublished=Yes

**RESPONSE**: responds with an array of collection objects and a total count.

```
{
 "collections": [ {
 "id": "dfdd3929-5a24-4340-b9e1-eedfe25e8a63",
 "title": "Flowers",
 "type": "Manual",
 "content": "Collection of all flowers",
 "publishDate": "2018-05-18T04:10:38.833Z",
 "slug": "flowers",
  "featureImage":
  "https://images.commerce7.com/images/collection/flowers.png",
 "createdAt": "2018-05-18T16:53:47.913Z",
 "updatedAt": "2018-05-18T16:53:47.913Z",
 "seo": {
  "title": "Flowers",
  "description": "Collection of all flowers"
 }
}
}, {
 "id": "dfdd3929-5a24-4340-b9e1-eedfe25e8a63",
 "title": "Flowers",
 "type": "Manual",
 "content": "Collection of all flowers",
 "publishDate": "2018-05-18T04:10:38.833Z",
 "slug": "flowers",
  "featureImage":
  "https://images.commerce7.com/images/collection/flowers.png",
 "createdAt": "2018-05-18T16:53:47.913Z",
 "updatedAt": "2018-05-18T16:53:47.913Z",
 "seo": {
  "title": "Flowers",
  "description": "Collection of all flowers"
 }
}],
 "total": 2
}
```
