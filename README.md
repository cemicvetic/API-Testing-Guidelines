# API-Testing-Guidelines

There are APIs for Registration, Clients, Vendors, Services, and Orders.

## Execution of API Calls
* Method Type: GET, POST, PUT/PATCH, DELETE.
* Endpoint: API service URL.
* Headers: Necessary headers like Content-Type, Authorization.
* Body: Data for POST/PUT requests.

## Validation of Status Code
* General Rule: All requests should return a 2XX status code.
   * Specific Status Codes:
    * 200 OK for GET requests. 
    * 201 for POST/PUT requests.
    * 200, 202, or 204 for DELETE operations.
      
## Payload Validation
* JSON Format: Ensure response is in a well-formed JSON.
* Schema Compliance: Verify field names, types, and nested objects.
* Data Integrity: Check if the field values are as expected.
* Non-Nullable Fields: Validate that essential fields are not null.

## State Validation
* GET Requests: Verify no state change.
* POST/DELETE/PATCH/PUT: Confirm correct reflection of action in the system.

## Header Validation
* Verify that HTTP headers are as expected, including content-type, connection, cache-control, expires, access-control-allow-origin, keep-alive, HSTS, etc., according to the HTTP request type.
