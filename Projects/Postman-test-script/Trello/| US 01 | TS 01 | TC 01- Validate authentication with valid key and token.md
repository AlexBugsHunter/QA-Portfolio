*Trello uses authentication with API Tokens instead of username and password, ensuring greater security. In all these Postman requests, I will use my API Key and Token to authenticate properly*

# | US 01 | TS 01 | TC 01- Validate authentication with valid key and token | #

GIVEN: The user is logged into the Trello application via Atlassian

AND: The user has created API key and token from https://trello.com/power-ups/admin

WHEN: The user add a new GET request in Postman for the endpoint: *https://api.trello.com/1/members/me*

THEN: The request return correct user data (Name, email, id)

### PRECONDITIONS ###

Trello's API key and token must be created

Postman must have variables for Key and Token setted

### STEPS IN POSTMAN ###

1. Add a new GET request and enter the URL: https://api.trello.com/1/members/me/
2. Add parameters for Key and Token with the correct value
3. Add the following scripts:
   
            const body = pm.response.json()

            pm.test("Correct Authentication with valid credentials", () => {
                pm.response.to.have.status(200);
            });

            pm.test("Validate that the response return user´s id", () => {
                pm.expect(body).to.have.property("id")
            });

            pm.test("Validate that the response return user´s name", () => {
                pm.expect(body).to.have.property("fullName")
            });


            pm.test("Validate that the response return user´s email", () => {
               pm.expect(body).to.have.property("email")
            });

            pm.test("Validate properties are not null", ()=>{
                pm.expect(body.id, body.fullName, body.email).to.be.not.null
            });


3. Validate that the Postman response is a 200 OK status
4. Validate that the JSON response returns the user's id, name, and email
   
### EXPECTED RESULTS ###

The GET request returns a 200 OK status with user data       **✓**

The Json response returns user data (name, email, id) with the correct properties       **✓**

### Status: Passed ✓ ###

### Links ###

Related to: TS 01 Authentication

Test: US 01 Successfully authentication for Postman API testing
