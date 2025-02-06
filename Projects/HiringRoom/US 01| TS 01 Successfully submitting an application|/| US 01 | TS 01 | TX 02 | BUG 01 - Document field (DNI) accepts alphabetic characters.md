# | US 01 | TS 01 | TX 02 | BUG 01 - Document field (DNI) accepts alphabetic characters #

Severity: Low 

Priority: Low

Description: In the document field (DNI), the user can enter alphabetic characters. While this can be corrected later when the employer contacts the user, the system still accepts invalid data.

### PRECONDITIONS: ###

1. The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website 
2. The user selects the option "Manually fill out"
3. The user is on the section 2 of the application

### STEPS TO REPRODUCE: ###

The user completes the document field with alphabetic characters (e.g., ABCDE )
               
### EXPECTED RESULTS ###

Error messages are displayed above document field for invalid characters    **✓** 

### ACTUAL RESULTS ###

No error message displayed.

### Environment: ###

OS: Windows 10

Browser: Google Chrome

### Attachment ###

https://github.com/AlexBugsHunter/QA-Portfolio/blob/d845c5a1b3ba5f286aa9a577a7122b0dc6542680/Projects/HiringRoom/Attachment/bug%20tx%2002.png

### Links ###

*Related to: TX 02 Validate error messages for invalid data in section 2*

*Blocks: US 01 Successfully submitting an application*
