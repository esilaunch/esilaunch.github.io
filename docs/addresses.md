# Addresses

## The address object

```
{
 "id": "5057e055-2ca6-4421-bf63-6c2a164e21ae",
 "customerId": "9d30102b-afdf-42ca-9919-1500c730cac8",
 "birthDate": "1972-10-03",
 "firstName": "Jason",
 "lastName": "Andres",
 "company": "ESI Launch",
 "phone": "+17783477874",
 "address": "33925 Araki Court",
 "address2": "Unit #9",
 "city": "Mission",
 "stateCode": "BC",
 "zipCode": "V2V7R4",
 "countryCode": "CA",
 "isDefault": true,
 "createdAt": "2018-05-22T17:51:08.878Z",
 "updatedAt": "2018-05-22T17:51:08.878Z"
}
```

## Create an address

**POST: `/customer/:customerId/address`**

```
{
 "firstName": "Jason",
 "lastName": "Andres",
 "company": "Commerce7",
 "address": "33925 Araki Ct",
 "address2": "Unit #9",
 "city": "Mission",
 "stateCode": "BC",
 "zipCode": "V2V7R4",
 "phone": "+17783477874",
 "countryCode": "CA",
 "isDefault": false,
 "birthDate": "1972-10-03"
}
```

**RESPONSE**: responds with an address object.

## Retrieve an address

**GET: `/customer/:customerId/address/:id`**

**RESPONSE**: responds with an address object.

## Update an address

**PUT: `/customer/:customerId/address/:id`**

```
{
 "firstName": "Jason",
 "lastName": "Andres",
 "company": "ESI Launch",
 "address": "33925 Araki Court",
 "address2": "House #9",
 "city": "Mission",
 "stateCode": "BC",
 "zipCode": "V2V7R4",
 "phone": "+17783477874",
 "countryCode": "CA",
 "isDefault": false,
 "birthDate": "1972-10-03"
}
```

**RESPONSE**: responds with an address object.

## Delete an address

**DELETE: `/customer/:customerId/address/:id`**

**RESPONSE**: responds with a blank object and 204 status.

## List all addresses for a customer

**GET: `/customer/:customer/address`**

**OPTIONS**: optional parameters include: searchText

**RESPONSE**: responds with an array of address objects and a total count.

```
{
 "customerAddresses": [{
  "id": "4a87ac0b-8b97-46ea-af15-bb579e5f4bcd",
  "customerId": "9d30102b-afdf-42ca-9919-1500c730cac8",
  "birthDate": "1972-10-03",
  "firstName": "Jason",
  "lastName": "Andres",
  "company": "ESI Launch",
  "phone": "+17783477874",
  "address": "289 Alexander Street",
  "address2": "Unit #624",
  "city": "Vancouver",
  "stateCode": "BC",
  "zipCode": "V6A1C2",
  "countryCode": "CA",
  "isDefault": false,
  "createdAt": "2018-05-22T18:27:35.998Z",
  "updatedAt": "2018-05-22T18:31:31.487Z"
 }, {
  "id": "5057e055-2ca6-4421-bf63-6c2a164e21ae",
  "customerId": "9d30102b-afdf-42ca-9919-1500c730cac8",
  "birthDate": "1972-10-03",
  "firstName": "Jason",
  "lastName": "Andres",
  "company": "ESI Launch",
  "phone": "+17783477874",
  "address": "33925 Araki Court",
  "address2": "Unit #9",
  "city": "Mission",
  "stateCode": "BC",
  "zipCode": "V2V7R4",
  "countryCode": "CA",
  "isDefault": true,
  "createdAt": "2018-05-22T17:51:08.878Z",
  "updatedAt": "2018-05-22T17:51:08.878Z"
 }],
 "total": 2
}
```
