# |US 01 |TS 01 |TC 01 - Validate manually filling out required information with valid data| #

Scenario: User wants to apply for a job in HiringRoom 

GIVEN: The user is in the application form

WHEN: The user completes the required information from section 2 to section 3 with valid data.

THEN: No error messages displays

### PRECONDITIONS:###

• The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website 

• The user selects the option "Manually fill out"

• The user is on the section 2 of the application

### TEST STEPS: ###

1. Complete the name fields with valid alphabetic characters (e.g., Pepa Flores). 
2. Ccomplete the email field with a valid email address (e.g., PepaF@example.com)
3. Complete the document field with valid numeric identifier (e.g., 00000000 )
4. Complete the telephone field with valid phone number (e.g., 1154540101)
5. Click on "Continue" button 
6. Complete the degree field of the education module with valid alphabetic characters (e.g., Chemistry Technician). 
7. Complete the description field of the education module with valid paragraph format (e.g., Lorem Ipsum).
8. Complete the job position field of the work experience module with valid alphabetic characters (e.g., Technician).
9. Complete the company name field of the work experience module with valid alphabetic characters (e.g., Miramar S.A.). 
10. Complete the description field of the work experience module with valid paragraph format (e.g., Lorem Ipsum).
11. Complete the link field of the social network module with valid URL format (e.g., https://www.linkedin.com/in/alexandra-albornoz/)
12. Complete the message field of the work experience module with valid paragraph format (e.g., Lorem Ipsum)
               
### EXPECTED RESULTS ###

No error messages are displayed for any fields. **✓**

## Status: Passed ✓ ##

### Links ###

*Related to: TS 01 Successfully submitting an application*

*Test: US 01 Successfully submitting an application*
