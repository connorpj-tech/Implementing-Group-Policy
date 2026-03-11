<h1>Creating Group Policy</h1>

<h2>Objective</h2>
This SOP will layout a few basic group polices for workstations and users that are asociated with the Domain Controller Server
<h2>Utilities Used</h2>

- <b> Microsoft Azure</b>
- <b> Windows Server 2025</b>
- <b> Group Policy Manaement</b>
- <b> Windows 11 Pro Edition</b>

<h2>Key Steps</h2>

**1. Open Group Policy Management**

- <b> In Server Manager, select the Tools drop down and open Group Policy Management</b>
- <b> Under mydomain.com, use the drop down arrow to Group Policy Objects. Right click on Default Domain Controller Policy to edit</b>

**2. Configure Account Lockout Policy**

- <b> In Group Policy Editor, use the drop down menu Computer Configuration>Policies>Windows Settings>Security Settings>Account Policies</b>
- <b> Open Account Lockout Policy</b>
- <b> Click Account Lockout duration to change accounts to be locked out for 30 minutes</b>
- <b> Click Account lockout threshold to lock out accounts after 5 invalid login attempts</b>
- <b> Click Reset account lockout counter to reset accounts after 30 mintutes after they have been locked out</b>

**3. Set Password Policy for Users**

- <b> In the same Account Policies select Password Policy</b>
- <b> Edit the following parameters:
  - <b> Enforce password history: 24 passwords remembered
  - <b> Maximum password age: 60 days
  - <b> Minimum password age: 1 day
  - <b> Minimum password length: 12 characters
  - <b> Enable password must meet complexity requirements
 
**4. Disabe Removable Storage Access**
