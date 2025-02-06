# |TS 01 |TC 02 - Validate error messages for invalid data in section 2| #

**Scenario**: User want to apply for a job in HiringRoom

GIVEN: The user is in the section 2 of the application

WHEN: The user completes the required information with invalid data

THEN: Error messages appear

### PRECONDITIONS: ###

1. The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website 
2. The user selects the option "Manually fill out"
3. The user is on the section 2 of the application

### TEST STEPS: ###

1. The user completes the name fields with no alphabetic characters (e.g., "465#2).
2. The user completes the email field with a invalid email address (e.g., PepaF.com)
3. The user completes the document field with alphabetic characters (e.g., ABCDE )
4. The user completes the telephone field with alphabetic characters(e.g., ABCDE)
5. The user completes the telephone field with fewer characters than necessary (e.g., 123)
               
### EXPECTED RESULTS ###
1. Error messages are displayed above name fields for invalid characters      **✓**
2. Error messages are displayed above email field for invalid email address    **✓** 
3. Error messages are displayed above document field for invalid characters    **✓** 
4. Error messages are displayed above telephone field for invalid characters   **✓** 
5. Error messages are displayed above telephone field for invalid phone number **✓**

## Status: FAILED ✘ ##

### Links ###

*Related to: TS 01 Successfully submitting an application*

*Test: US 01 Successfully submitting an application*
