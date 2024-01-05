# API-Testing-Guidelines

There are APIs for Registration, Clients, Vendors, Services, and Orders.

## Execution of API Calls
* Method Type: GET, POST, PUT, DELETE.
* Endpoint: API service URL.
* Headers: Necessary headers like Content-Type, Authorization.
* Body: Data for POST/PUT requests.

## Validation of Status Code
* General Rule: All requests should return a 2XX status code.
   * Specific Status Codes:
    * 200 OK for GET requests. 
    * 201 for POST/PUT requests.
    * 200, 202, or 204 for DELETE operations.
