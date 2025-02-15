# | US 01 | TS 01 | TC 02- Validate authentication with valid key and token | #

### PRECONDITIONS ### 

The user set invalid API key/token in Postman or is not logged into the Trello application via Atlassian

### STEPS IN POSTMAN ###

1. Add a new GET request and enter the URL: https://api.trello.com/1/members/me/
2. Send request
4. Validate that the Postman response is a 401 Unauthorized status
5. Validate that the error message returned in the body is "invalid token" or a similar message.

 ### EXPECTED RESULTS ###

The GET request returns a 401 Unauthorized status      **✓**

The response body contains an error message for invalid credentials        **✓**

### Status: Passed ✓ ###

### Links ###

Related to: TS 01 Authentication

Test: US 01 Successfully authentication for Postman API testing
