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

## Performance Sanity
* Response is received in a timely manner with respect to time expected for each request process time. Discuss with Dev team or PO.
  
## API Testing Scripts
A comprehensive collection of API testing scripts is included, covering various modules:

#### General Tests
* G001 Registration: Validates user registration.
* G002 Registration with required data only: Checks minimal data registration.
* G003 Email Verification: Tests the email verification process.
* G004 Authorization: Verifies login and authorization.
* G003.1 Check Email Verified: Ensures email verification status is correctly updated.
* G005 GetUserByID: Retrieves a user by their ID.
* G006 GetAllUsers: Gets a list of all users.
* G007 Registration w/o First Name: Tests registration without a first name.
* G008 Registration w/o Last Name: Tests registration without a last name.
* G009 Registration w/o Email: Tests registration without an email.
* G010 Registration w/o Password: Tests registration without a password.
* G011 Login with invalid data: Verifies login with incorrect credentials.
* G012 Login w/o Email: Tests login without an email.
* G013 Login w/o Password: Tests login without a password.
* G014 Registration with Existing Email: Checks registration with an already used email.
* G015 Space trimming: Verifies that spaces are trimmed in user data.
