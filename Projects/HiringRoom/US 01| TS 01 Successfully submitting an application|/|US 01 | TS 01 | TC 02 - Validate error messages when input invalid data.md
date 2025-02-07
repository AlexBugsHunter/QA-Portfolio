# |US 01|TS 01 |TC 02 - Validate error messages when input invalid data| #

Scenario: User wants to apply for a job in HiringRoom

GIVEN: The user is in the application form

WHEN: The user completes the required information from section 2 to section 3 with invalid data.

THEN: Error message displays

### PRECONDITIONS: ###

1. The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website 
2. The user selects the option "Manually fill out"
3. The user is on the section 2 of the application

### TEST STEPS: ###

1. Complete the name fields with no alphabetic characters (e.g., "465#2).
2. Complete the email field with a invalid email address (e.g., PepaF.com)
3. Complete the document field with alphabetic characters (e.g., ABCDE )
4. Complete the telephone field with alphabetic characters(e.g., ABCDE)
5. Complete the telephone field with fewer numeric characters than required (9 to 10 digits) (e.g., 123)
6. Click on "Continue" button
7. Complete the link field of the social network module with invalid URL format (e.g., asd4654)
               
### EXPECTED RESULTS ###
1. Error messages are displayed below the name fields for invalid characters      **✓**
2. Error messages are displayed below the email field for invalid email address    **✓** 
3. Error messages are displayed below the document field for invalid characters    **✓** 
4. Error messages are displayed below the telephone field for invalid characters   **✓** 
5. Error messages are displayed below the telephone field indicating that the number of digits is insufficient **✓**
6. Error messages are displayed below link field for invalid URL   **✓** 

## Status: FAILED ✘ ##

### Links ###

*Related to: TS 01 Successfully submitting an application*

*Test: US 01 Successfully submitting an application*
