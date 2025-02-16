# | US 02 | TS 01 | TC 03- Validate deleting Board via API Request | #

### PRECONDITIONS ###

Trello's API key and token must be created

Postman must have variables for Key and Token setted

BoardID collection variable must be set 

### STEPS IN POSTMAN ###

1. Add a new DELETE request and enter the URL: https://api.trello.com/1/boards/:id
2. Add parameters for Key and Token with the correct value
3. In path variable ID, insert value {{boardID}}
4. Add the following scripts:
   
       const body = pm.response.json();
   
       pm.test("Validate that the board has been deleted", () => {
           pm.response.to.have.status(200);
       });

5. Send request
6. Add a new GET request and enter the URL: https://api.trello.com/1/boards/:id
7. Add parameters for Key and Token with the correct value
8. In path variable ID, insert value {{boardID}}
9. Send request

### EXPECTED RESULTS ###

The DELETE request returns a 200 OK status      **✓**

Board has been deleted      **✓**

Test scripts passed      **✓**

The GET request returns a 404 not found status      **✓**

### Links ###

Related to: TS 01 Board CRUD 

Test: US 02 Board CRUD 

https://github.com/AlexBugsHunter/QA-Portfolio/blob/QA-Portfolio/Projects/Postman-test-script/Trello/Attachment/postman%20test%204.png
