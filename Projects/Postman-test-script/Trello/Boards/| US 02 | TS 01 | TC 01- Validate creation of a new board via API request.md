# | US 02 | TS 01 | TC 01- Validate creation of a new board via API request | #

### PRECONDITIONS ###

Trello's API key and token must be created

Postman must have variables for Key and Token setted

### STEPS IN POSTMAN ###

1. Add a new POST request and enter the URL: https://api.trello.com/1/boards
2. Add parameters for Key and Token with the correct value
3. Add parameter for Name with value: Board 1.0
4. Add the following scripts:
   
       const body = pm.response.json();

       pm.test("Validate that the board has been properly created", () => {
           pm.response.to.have.status(200);
       });

       pm.test("Validate the response is in json format", () => {
           pm.expect(pm.response.headers.get("Content-Type")).to.include("application/json");
       });

       pm.test("Validate that the board id has been properly generated", () => {
           pm.expect(body).to.have.property('id').and.to.be.a("string").and.to.not.null;
       });

       let boardID = pm.collectionVariables.set("boardID", body.id);

       pm.test("Validate that the collection variable 'boardID' has been created for the next test cases", () => {
           pm.expect(boardID).to.be.not.null
       });

5. Send request
6. Validate that the board have been properly created
7. Validate the response is in json format
8. Validate that the collection variable 'boardID' has been created for the next test cases
   
  ### EXPECTED RESULTS ###

The POST request returns a 200 OK status      **✓**

Board id has been properly generated      **✓**

The variable "boardID" has been set for the next test cases      **✓**

### Links ###

Related to: TS 01 Board CRUD 

Test: US 02 Board CRUD 

https://github.com/AlexBugsHunter/QA-Portfolio/blob/QA-Portfolio/Projects/Postman-test-script/Trello/Attachment/postman%20test%202.png
