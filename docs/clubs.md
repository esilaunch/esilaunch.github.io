# Clubs

## The club object

```
{
 "id": "138cc09d-62d7-4298-8bfc-fd2fc3fddc79",
 "title": "Red Club",
 "content": null,
 "publishDate": "2018-05-18T17:00:00.000Z",
 "slug": "red-club",
 "createdAt": "2018-05-18T17:00:38.114Z",
 "updatedAt": "2018-05-18T17:00:38.114Z",
 "addOns": [],
 "seo": {
  "title": "Red Club",
  "description": null
 }
}
```

## Create a club

**POST: `/club`**

```
{
 "title": "Mixed Club",
 "slug": "mixed-club",
 "publishDate": "2018-05-22T16:21:00.000Z",
 "seo": {
  "title": "Mixed Club"
 },
 "addOns": [{
  "productVariantId": "52491ea6-4335-447c-816f-c060362d0ad3",
  "price": 3500
 }]
}
```

**RESPONSE**: responds with a club object.

## Retrieve a club

**GET: `/club/:id`**

**RESPONSE**: responds with a club object.

## Update a club

**PUT: `/club/:id`**

```
{
 "title": "Mixed Club",
 "content": "<p>Mixed wine club.</p>",
 "slug": "mixed-club",
 "publishDate": "2018-05-22T16:21:00.000Z",
 "seo": {
  "title": "Mixed Club",
  "description": "Mixed wine club."
 },
 "addOns": []
}
```

**RESPONSE**: responds with a club object.

## Delete a club

**DELETE: `/club/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all clubs

**GET: `/club`**

**RESPONSE**: responds with an array of club objects and a total count.

```
{
 "clubs": [{
  "id": "138cc09d-62d7-4298-8bfc-fd2fc3fddc79",
  "title": "Red Club",
  "content": null,
  "publishDate": "2018-05-18T17:00:00.000Z",
  "slug": "red-club",
  "createdAt": "2018-05-18T17:00:38.114Z",
  "updatedAt": "2018-05-18T17:00:38.114Z",
  "addOns": [],
  "seo": {
   "title": "Red Club",
   "description": null
  }
 }, {
  "id": "194cc50a-e324-4f21-8e52-98500a4b751c",
  "title": "White Club",
  "content": null,
  "publishDate": "2018-05-18T17:00:00.000Z",
  "slug": "white-club",
  "createdAt": "2018-05-18T17:00:45.726Z",
  "updatedAt": "2018-05-18T17:00:45.726Z",
  "addOns": [],
  "seo": {
   "title": "White Club",
   "description": null
  }
 }],
 "total": 2
}
```


