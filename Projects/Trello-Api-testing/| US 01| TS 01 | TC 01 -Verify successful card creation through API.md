# |US 01|TS 01 |TC 01 - Verify successful card creation through API| #

### PRECONDITIONS: ###

1. Postman installed and configured
2. Trello URL (https://trello.com/1) available
3. Authentication token and API key

### TEST DATA: ###

Method: POST

Endpoint: https://trello.com/1/card

Authorization: Basic Auth

Params:

    •key: <user-key> (Trello API key)
        
    •token: <user-token> (User's Trello token)
        
    •idList: <list-id> (ID of the list where the card will be created)
        
    •name: "Happy card" (Card title)
        
    •desc: lorem ipsum (Card description)

### STEPS TO EXECUTE ON POSTMAN ###

1. Open Postman
2. Select method POST
3. Enter the URL for the endpoint: https://api.trello.com/1/cards
4. Add the following parameters:
   
       •key: <user-key> (Trello API key)
   
       •token: <user-token> (User’s Trello token)
   
       •idList: <list-id> (ID of the list where the card will be created)
   
       •name: "Happy card" (Card title)
     
       •desc: lorem ipsum (Card description)
   
5. Click on "Send" button
           
### EXPECTED RESULTS ###
1. Statud code:200     **✓**
2. Headers content type: JSON    **✓** 
3. Headers date: present (10/02/2025)    **✓**
4. The card id is automatically generated   **✓**
5. The card is saved with the provided data (name, description, list)    **✓** 
6. The card's title and description match the input data **✓**
7. No errors are shown in the Postman console   **✓**
8. The card can be verified by making a GET request: https://trello.com/1/card adding the path variable id = {card id automatically generated}

## Status: Passed ✓ ##

### Links ###

*Related to: TS 01 Create, modify and delete cards successfully*

*Test: US 01 Create, modify and delete cards successfully*

API Documentation: [Trello API Documentation](https://developer.atlassian.com/cloud/trello/rest/api-group-actions/#api-group-actions)
