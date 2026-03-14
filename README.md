<h1>Implementing Security Group Policy</h1>

<h2>Objective</h2>
This SOP will layout security group polices for workstations and implement basic security for the Windows Server and Clients associated with the Active Directory Domain Controller
<h2>Utilities Used</h2>

- <b> Microsoft Azure</b>
- <b> Windows Server 2025</b>
- <b> Group Policy Management</b>
- <b> Windows 11 Pro Edition</b>

<h2>Key Steps</h2>

**1. Open Group Policy Management**

- <b> In Server Manager, select the Tools drop down and open Group Policy Management</b>
- <b> Under mydomain.com, use the drop down arrow to Group Policy Objects. Right click on Default Domain Policy to edit</b>
<div align="left">
  <table>
    <tr>
      <td><img width="400" src="https://github.com/connorpj-tech/Implementing-Group-Policy/blob/main/Group%20Policy%20Management.png"/></td>
      <td><img width="400" src="https://github.com/connorpj-tech/Implementing-Group-Policy/blob/main/Default%20Domain%20Policy.png"/></td>
    </tr>
       <td align="center"><b>Group Policy </b></td>
       <td align="center"><b>Default Domain Policy</b></td>
       </tr>
  </table>
</div>

**2. Configure Account Lockout Policy**

- <b> In Group Policy Editor, use the drop down menu Computer Configuration>Policies>Windows Settings>Security Settings>Account Policies</b>
- <b> Open Account Lockout Policy</b>
- <b> Click Account Lockout duration to change accounts to be locked out for 30 minutes</b>
- <b> Click Account lockout threshold to lock out accounts after 5 invalid login attempts</b>
- <b> Click Reset account lockout counter to reset accounts after 30 mintutes after they have been locked out</b>
- <b> Click apply to save settings
<div align="left">
  <table>
    <tr>
      <td><img width="400" src="https://github.com/connorpj-tech/Implementing-Group-Policy/blob/main/Group%20Policy%20Management.png"/></td>
      <td><img width="400" src="https://github.com/connorpj-tech/Implementing-Group-Policy/blob/main/Default%20Domain%20Policy.png"/></td>
    </tr>
       <td align="center"><b>Group Policy </b></td>
       <td align="center"><b>Default Domain Policy</b></td>
       </tr>
  </table>
</div>

**3. Set Password Policy for Users**

- <b> In Group Policy Editor, use the drop down menu Computer Configuration>Policies>Windows Settings> Security Settings> Account Policies>Password Policy</b>
- <b> Edit the following parameters:
  - <b> Enforce password history: 24 passwords remembered
  - <b> Maximum password age: 60 days
  - <b> Minimum password age: 1 day
  - <b> Minimum password length: 12 characters
  - <b> Enable password must meet complexity requirements
- <b> Click apply to enforce the new password requirements for users
 
**4. Disabe Removable Storage Access**

- <b> In Group Policy Editor, use the drop down menu Computer Configuration>Policies>Administrative Templates>System>Removable Storage Access
- <b> Select All Removable Storage classes: Deny All Access
- <b> Click apply to deny any removable storage to be used by users
