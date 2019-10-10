# Customers

Customers can have one or more email addresses - but the email address must be unique. Email is a mandatory field on the customer object.

## The customer object

```
{
 "id": "91b4a9d1-2b0f-442d-a5b8-126ea50a1b18",
 "avatar": "http://graph.facebook.com/10156101208888136/picture?type=large",
 "firstName": "Nico",
 "lastName": "Viarnes",
 "birthDate": "1901-1-1",
 "city": "Oakland",
 "stateCode": "CA",
 "zipCode": "94609",
 "countryCode": "US",
 "emailMarketingStatus": "Subscribed",
 "lastActivityDate": "2018-05-11T15:35:45.123Z",
 "facebookId": "10156101208888136",
 "metaData": {
  "spouses-name": "Malene",
  "source": "Referal from Friend"
 },
 "createdAt": "2018-02-20T02:23:56.571Z",
 "updatedAt": "2018-05-14T18:09:17.445Z",
 "emails": [{
  "id": "e4a0342f-61c5-41e6-ab7c-86df4b6cb14e",
  "email": "nico@esilogistics.com"
 }, {
  "id": "f03e2191-ebf0-4f9d-bfba-1959c6f376c9",
  "email": "nico@viarn.es"
 }],
 "phones": [{
  "id": "b08aaf2d-734c-4b7f-9cff-7500b0096532",
  "phone": "+15555555555"
 }],
 "groups": [{
   "id": "560d385d-3322-4714-8455-501ddb558635",
   "title": "Employee",
   "type": "Manual",
   "createdAt": "2018-02-19T18:17:40.266Z",
   "updatedAt": "2018-02-19T18:17:40.266Z"
  }],
 "orderInformation": {
  "lastOrderId": "e5a694e0-3c01-43cd-8ef9-224b907214f0",
  "lastOrderDate": "2018-05-11T15:35:43.952Z",
  "orderCount": 65,
  "lifetimeValue": 590709,
  "currentClubTitle": "Spectra Club",
  "daysInCurrentClub": 28
 },
 "clubs": [{
  "clubId": "655eb7c3-ab0f-4c3f-997c-a77f1c5c4a2c",
  "clubTitle": "Spectra Club",
  "cancelDate": null,
  "signupDate": "2018-04-22T02:10:34.832Z",
  "clubMembershipId": "fefecc61-ef68-499b-8c1e-ee59e20b0053"
 }]
}
```

## Create a customer

**POST: `/customer`**

```
{
 "firstName": "Nico",
 "lastName": "Viarnes",
 "birthDate": "1901-1-1",
 "city": "Oakland",
 "stateCode": "CA",
 "zipCode": "94609",
 "countryCode": "US",
 "emailMarketingStatus": "Subscribed",
 "phones": [{
  "phone": "+15555555555"
 }],
 "emails": [{
  "email": "nico@esilogistics.com"
 }]
}
```

**RESPONSE**: responds with a customer object.

## Retrieve a customer

**GET: `/customer/:id`**

**RESPONSE**: responds with a customer object.

## Update a customer

**PUT: `/customer/:id`**

The request body only has to include the fields you wish to update. The below JSON example shows an update to the birthdate.

```
{
 "birthDate": "1973-11-15"
}
```

**RESPONSE**: responds with the updated customer object.

## Delete a customer

**DELETE: `/customer/:id`**

**RESPONSE**: responds with a blank object and a 204 status.

## List of all customers

**GET: `/customer`**

**Options**: optional query parameters include: q, groupId, lifetimeValue, orderCount, createdAt. Query params may look like ?q=nico&orderCount=gt:1 to find a customer with the name of Nico and order count greater than 1.

**RESPONSE**: responds with an array of customers objects and a total count.

```
{
 "customers": [{
 "id": "91b4a9d1-2b0f-442d-a5b8-126ea50a1b18",
 "avatar": "http://graph.facebook.com/10156101208888136/picture?type=large",
 "firstName": "Nico",
 "lastName": "Viarnes",
 "birthDate": "1901-1-1",
 "city": "Oakland",
 "stateCode": "CA",
 "zipCode": "94609",
 "countryCode": "US",
 "emailMarketingStatus": "Subscribed",
 "lastActivityDate": "2018-05-11T15:35:45.123Z",
 "facebookId": "10156101208888136",
 "metaData": {
  "spouses-name": "Malene",
  "source": "Referal from Friend"
 },
 "createdAt": "2018-02-20T02:23:56.571Z",
 "updatedAt": "2018-05-14T18:09:17.445Z",
 "emails": [{
  "id": "e4a0342f-61c5-41e6-ab7c-86df4b6cb14e",
  "email": "nico@esilogistics.com"
 }, {
  "id": "f03e2191-ebf0-4f9d-bfba-1959c6f376c9",
  "email": "nico@viarn.es"
 }],
 "phones": [{
  "id": "b08aaf2d-734c-4b7f-9cff-7500b0096532",
  "phone": "+15555555555"
 }],
 "groups": [{
   "id": "560d385d-3322-4714-8455-501ddb558635",
   "title": "Employee",
   "type": "Manual",
   "createdAt": "2018-02-19T18:17:40.266Z",
   "updatedAt": "2018-02-19T18:17:40.266Z"
  }],
 "orderInformation": {
  "lastOrderId": "e5a694e0-3c01-43cd-8ef9-224b907214f0",
  "lastOrderDate": "2018-05-11T15:35:43.952Z",
  "orderCount": 65,
  "lifetimeValue": 590709,
  "currentClubTitle": "Spectra Club",
  "daysInCurrentClub": 28
 },
 "clubs": [{
  "clubId": "655eb7c3-ab0f-4c3f-997c-a77f1c5c4a2c",
  "clubTitle": "Spectra Club",
  "cancelDate": null,
  "signupDate": "2018-04-22T02:10:34.832Z",
  "clubMembershipId": "fefecc61-ef68-499b-8c1e-ee59e20b0053"
 }]
}, {
  "id": "2d298efa-0ccf-4dbd-9a6a-0f726accaafc",
  "avatar": "https://s3.amazonaws.com/uifaces/faces/twitter/edgarchris99/128.jpg",
  "firstName": "Erik",
  "lastName": "Christiansen",
  "birthDate": null,
  "city": "Lake Joliemouth",
  "stateCode": "MD",
  "zipCode": "20601",
  "countryCode": "US",
  "emailMarketingStatus": "Subscribed",
  "lastActivityDate": "2018-05-07T23:47:32.983Z",
  "facebookId": null,
  "metaData": {
   "spouses-name": "Gena",
   "source": "Facebook Ad"
  },
  "createdAt": "2018-02-19T18:17:43.231Z",
  "updatedAt": "2018-05-14T18:09:16.022Z",
  "emails": [{
   "id": "e668e52c-c9b7-44aa-a627-8e64d5648187",
   "email": "erik.christiansen@gmail.com"
  }],
  "phones": [],
  "groups": [{
   "id": "560d385d-3322-4714-8455-501ddb558635",
   "title": "Employee",
   "type": "Manual",
   "createdAt": "2018-02-19T18:17:40.266Z",
   "updatedAt": "2018-02-19T18:17:40.266Z"
  }],
  "orderInformation": {
   "lastOrderId": "c758c7ac-85e5-4ffa-a728-5255213c26fd",
   "lastOrderDate": "2018-05-07T23:47:32.740Z",
   "orderCount": 7,
   "lifetimeValue": 342958,
   "currentClubTitle": null,
   "daysInCurrentClub": null
  },
  "clubs": [{
   "clubId": "655eb7c3-ab0f-4c3f-997c-a77f1c5c4a2c",
   "clubTitle": "Spectra Club",
   "cancelDate": "2018-05-16T06:59:00.000Z",
   "signupDate": "2017-06-23T07:00:00.000Z",
   "clubMembershipId": "dc9abd39-159a-46dd-a2d2-2d464bcf4abf"
  }]
 }],
 "total": 2
}
```
