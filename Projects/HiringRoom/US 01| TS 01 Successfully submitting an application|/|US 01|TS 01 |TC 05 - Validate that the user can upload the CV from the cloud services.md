# |US 01|TS 01 |TC 05 - Validate that the user can upload the CV from the cloud services| #

Background:

GIVEN: The user is in section 3 of application form

Scenario 1: User wants to upload a resume from Dropbox

WHEN: The user clicks on "Dropbox" button in the Attachment module

THEN: A pop-up window appears where user can select the Dropbox account

AND: the user select the desired file from Dropbox

AND: The file shows properly uploaded

Scenario 2: User wants to upload a resume from Google Drive

WHEN: The user clicks on "Google Drive" button in the Attachment module

THEN: A pop-up window appears where user can select the Google Drive account

AND: the user select the desired file from Dropbox

AND: The file shows properly uploaded

### PRECONDITIONS: ###

The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website

The user is on the section 3 of the application

### TEST STEPS: ###

1. Click on "DropBox" button or "Google Drive" button
2. Select an account
3. Select a file with valid format and size
3. Select the "Open" button

### EXPECTED RESULTS ###

The file shows properly uploaded **✓**

## Status: FAILED ✘ ##

### Links ###

*Related to: TS 01 Successfully submitting an application*

*Test: US 01 Successfully submitting an application*
