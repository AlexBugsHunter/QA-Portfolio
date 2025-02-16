# | US 02 | TS 01 | TC 02- Validate Board Update via API Request | #

### PRECONDITIONS ###

Trello's API key and token must be created

Postman must have variables for Key and Token setted

BoardID collection variable must be set 

### STEPS IN POSTMAN ###

1. Add a new PUT request and enter the URL: https://api.trello.com/1/boards/:id
2. Add parameters for Key and Token with the correct value
3. Add parameter for Name with value: Board 1.1
4. Add parameter for description (desc) with value: lorem ipsum
5. In path variable ID, insert value {{boardID}}
6. Add the following scripts:
   
       const body = pm.response.json();

       pm.test("Validate that the board has been properly updated", () => {
           pm.response.to.have.status(200);
       });

       pm.test("Validate the response is in json format", () => {
           pm.expect(pm.response.headers.get("Content-Type")).to.include("application/json");
       });

       pm.test("Validate that the board´s name has been changed to 1.1 Board", ()=>{
           pm.expect(body.name).to.be.eql("1.1 Board").and.to.be.a("string")
       });
       
       pm.test("Validate that the description has been added and its no null", ()=>{
           pm.expect(body.desc).to.be.a("string").and.to.be.not.null
       });


7. Send request
   
### EXPECTED RESULTS ###

The POST request returns a 200 OK status      **✓**

Board has been properly updated      **✓**

Response is in json format      **✓**

Updated board name in the responses matches the requested name´s value      **✓**

Board description has been properly updated      **✓**

All test scripts passed      **✓**

### Links ###

Related to: TS 01 Board CRUD 

Test: US 02 Board CRUD 

https://github.com/AlexBugsHunter/QA-Portfolio/blob/QA-Portfolio/Projects/Postman-test-script/Trello/Attachment/postman%20test%203.png
