# |US 01|TS 01 |TC 04 - Validate that the user can upload the CV from the device| #

Scenario 1: User wants to upload resume from device

GIVEN: The user is in section 3 of application form

WHEN: The user clicks on "My files" button in the Attachment module

THEN: A pop-up window appears where user can select files from device

AND: The file shows properly uploaded

### PRECONDITIONS: ###

The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website

The user is on the section 3 of the application

### TEST STEPS: ###

1. Click on "My files" button
2. Select a file with valid format and size 
3. Select the "Open" button

### EXPECTED RESULTS ###

The file shows properly uploaded **✓**

## Status: Passed ✓ ##

### Links ###

*Related to: TS 01 Successfully submitting an application*

*Test: US 01 Successfully submitting an application*
