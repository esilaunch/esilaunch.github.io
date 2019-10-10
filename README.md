# Getting Started With ESI Launch

This page will help you get started with ESI Launch. You'll be up and running in a jiffy!

## Base URL

https://api.commerce7.com/v1

## Authentication

You connect to ESI Launch Rest APIs using basic auth. To obtain a username and password, you need to request a current admin to send you an invite, please request that the admin set the role on your account to "Data" see below for details. The username is required to be an email address and you configure the password when you receive the invite email.

\*\*Note a specific permission "Data role" is required to enable API access to migrate historical data to Commerce7 and retain the existing primary key, createdAt and updatedAt fields, for Customers, Customer Addresses, Customer Credit Card Tokens, Clubs, Club Memberships, Notes, Orders and Products. The admin that sends the invite can set this Data role to be enabled for your API user. If you are unable to push your own UUIDs then this role is not set on your API user.

## Requests

The tenant is required to be sent with every API request as a header field. You can obtain the tenant from logging into the Commerce7 Admin using your API credentials at the following link https://platform.esilaunch.com.

The tenant is the first part of the URL when you are logged into the admin interface.

Example:
https:// **hedony**.admin.platform.esilaunch.com

`Header Value`  
`tenant` `hedony`

All requests that send JSON to the API endpoint require sending the Content-Type to "application/json"

`Header Value`  
`Content-Type` `application/json`

## Pagination

All get requests for lists have a limit of 50 records per page, you can add a query param
?limit=n where n is between 1 and 50 to retrieve less records per page if you choose. The response is an object with an array of the objects your listing and a total, which is the total record count.

To request the next page pass in a query param ?page=n

**Example:**

```
Request:
https://api.commerce7.com/v1/customer?page=1&limit=10

Response:
{
    "customers": [
        { .... customer objects .... }
    ],
    "total": 79318
}

Total requests you need to make to retrieve all data: 79318 / 10 = 7932
```

## Data formats

All currency amounts are stored in ESI Launch in cents. eg. If you pass in a request to update a product price to \$100.00 the amount should be sent as 10000.

Dates are all stored in UTC time. If the system you are integrating works in a timezone other than UTC you will need to convert the time for your requests and responses to UTC time.

## Throttle Limits

API throttle limits are 100 requests per minute, based on tenant. Future updates may provide burst capability with exponential backoff.
