# |US 01 |TS 01 |TC 03 - Validate that the buttons and dropdown menues works correctly| #

**Scenario**: User wants to apply for a job in HiringRoom

GIVEN: The user is in the job application form

WHEN: The user uses any of the dropdown menus in section 2 to selects an option

THEN: The selected option shows correctly

WHEN: The user clicks on "Continue" button

THEN: The user access the section 3

WHEN: The user clicks on "Add education" button

THEN: A form module appears to enter this information

AND: The user can use the dropdown menus of the education module properly

WHEN: The user clicks on radio buttons "Yes" or "NO" below the question "High school completed?"

THEN: Option selected shows correctly

AND: The user can not select more than one option

WHEN: The user clicks on "Add language" button

THEN: A form module appears to enter this information

AND: The user can use the dropdown menus of the language module properly

WHEN: The user clicks on "Add work experience" button

THEN: A form module appears to enter this information

AND: The user can use the dropdown menus of the work experience module properly

WHEN: The user clicks on "Add social network" button

THEN: A text field appears to enter this information

WHEN: The user clicks on "Add additional message" button

THEN: A text field appears to enter this information

WHEN: The user clicks on "Previous" button

THEN: The user goes back to section 2 without losing information

### PRECONDITIONS: ###

1. The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website 
2. The user selects the option "Manually fill out"
3. The user is on the section 2 of the application

### TEST STEPS: ###

1. Use the dropdown menu in section 2 to selects an option for "Type of Document"
2. Use the dropdown menu in section 2 to selects an option for "Phone country"
3. Use the dropdown menu in section 2 to selects an option for "Type of phone"
4. Use the dropdown menu in section 2 to selects an option for "Gender"
5. Use the dropdown menu in section 2 to selects an option for "Nationality"
6. Use the dropdown menu in section 2 to selects an option for "Country of residence"
7. Use the dropdown menu in section 2 to selects an option for "Province"
8. Use the dropdown menu in section 2 to selects an option for "City"
9. Use the dropdown menu in section 2 to selects an option for "Day of birth"
10. Use the dropdown menu in section 2 to selects an option for "month of birth"
11. Use the dropdown menu in section 2 to selects an option for "year of birth"
12. Click on "Continue" button
13. Click on "Add education" button and uses the dropdown menus that appears in the education module
14. Select an option from the radio button below the question "Highschool completed?"
15. Click on "Add language" button and uses the dropdown menues that appears in the language module
16. Click on "Add work experience" button and uses the dropdown menus that appears in the work experience module
17. Click on "Add social network" button
18. Click on "Add additional message" button
19. Click on "Previous" button
               
### EXPECTED RESULTS ###
1. Selected option from dropdown menus shows correctly      **✓**
2. User can move within sections without losing information filled out when clicks on "Previous" and "Continue" buttons    **✓** 
3. Option selected from radio buttons shows correctly    **✓** 
4. Clicking on "Add education", "Add language", "Add work experience" buttons causes a module to appear for entering this information   **✓** 
5. Clicking on "Add social network" and "Add message" buttons causes a text field to appear for entering this information **✓**

## Status: Passed ✓ ##

### Links ###

*Related to: TS 01 Successfully submitting an application*

*Test: US 01 Successfully submitting an application*
