# | US 01 | TS 01 | TX 05 | BUG 04 - Error 'App Blocked' when selecting a Google Drive account, preventing file upload in the application process #

Severity: High   

Priority: High

Description: When the user clicks on "Google Drive" button, a pop-up windows appears but when the user selects an account appears an "App Blocked" error message.  This prevents users from uploading files. The message appears from different IPs and devices.

### PRECONDITIONS: ###

The user clicks on "Apply" from a job advertisement on HiringRoom or is redirected from an external website 
 
The user is on the section 3 of the application

### STEPS TO REPRODUCE: ###

1. Click on "DropBox" button or "Google Drive" button
2. Select an account
               
### EXPECTED RESULTS ###

User access google drive acount and can select a file    **✓** 

### ACTUAL RESULTS ###

Error message appears: *APP BLOCKED: This app has attempted to access sensitive information from your Google account. To protect your account, Google has blocked this access* **✘**

### Technical details from DevTools ###

Request URL: https://challenges.cloudflare.com/cdn-cgi/challenge-platform/h/g/pat/90e347111b65200d/1738930235371/eb817c8e42e47236284857546bfd792f66c429ef3407b772f1c31fb30d530e06/mmZWG9Mf8dc-Cpv

Request Method: GET

Status Code: 401 Unauthorized

### Environment: ###

OS: Windows 10

Browser: Google Chrome

### Attachment ###

Error message: https://github.com/AlexBugsHunter/QA-Portfolio/blob/QA-Portfolio/Projects/HiringRoom/Attachment/bug%20tx%2005%20.png

Dev Tools screenshot: https://github.com/AlexBugsHunter/QA-Portfolio/blob/QA-Portfolio/Projects/HiringRoom/Attachment/tx%2005%20devtool%201.bmp

Dev Tools screenshot 2: https://github.com/AlexBugsHunter/QA-Portfolio/blob/QA-Portfolio/Projects/HiringRoom/Attachment/tx%2005%20devtool%202.bmp

### Links ###

*Related to: TX 05 Validate that the user can upload resume from the cloud services*

*Blocks: US 01 Successfully submitting an application*
