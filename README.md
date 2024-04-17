<h1>Active Directory Home Lab - Recover Account</h1>

<h2>Description</h2>
In this lab, I am going to demonstrate a scenario depicting how a Tier 1 helpdesk technician would recover a user's account. In this scenario, a user named John Doe cannot log on to his Outlook account because the password he entered was invalid. I will be using Active Directory to recover his account and reset his password.

<h2>Software Used</h2>

- <b>Virtual VM VirtualBox</b> 

<h2>Operating Systems Used </h2>

- <b>Windows Server 2019</b>

<h2>Program walk-through:</h2>

<p align="left">
1) Before doing anything, the first step is to allow the user (in this scenario, John) to explain his issue without interrupting. When the user finishes speaking, you (the helpdesk technician) will ask some questions. For example, you would ask what operating system he is using or whether the login issue occurs anywhere else besides Outlook. Then, allow the user to answer those questions, collecting info to resolve the problem.
<br />
  <br />
2) Typically, you would first ask what the user's username is. Then find that user by opening 'Active Directory Users and Computers'. : <br />
<img src="https://i.imgur.com/wJMopVy.png" height="80%" width="80%" alt="Change System Name"/>
<br />
<br />
3) Once the window opens, right-click on the 'Users' folder and click on 'Find'. Then, type in the user's name (John Doe) and click on 'Find Now'. : <br />
<img src="https://i.imgur.com/mqO7c6r.png" height="80%" width="80%" alt="Change System Name"/>
  <img src="https://i.imgur.com/g6L9Fa5.png" height="80%" width="80%" alt="Change System Name"/>
<br />
<br />
4) After clicking 'Find Now', a name 'John Doe' will be listed below. Double-click on it to view the user's properties. : <br />
<img src="https://i.imgur.com/0j8Gab8.png" height="80%" width="80%" alt="Change System Name"/>
<br />
<br />
5) Here is how the user's properties would appear. :  <br/>
<img src="https://i.imgur.com/ldheoeV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
6) By default, the properties window will view the user's general info (name, email, phone #). Click on the 'Account' tab so you can work with the user's account. : <br/>
<img src="https://i.imgur.com/m4I5E9w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7) In the Accounts tab, check the box near the center where it says 'Unlock account'. If the user requests to change his password, check the box 'User must change password at next login'. Finally, click on either 'Apply' or 'OK'. Let the user know his account is now unlocked. :  <br/>
<img src="https://i.imgur.com/undefined.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
8) Confirm that the issue is resolved by asking the user to log in to his account. If the user confirms that login is successful, ask if he needs help with anything else. If not, you may wrap the call.
<br />
  <br />
9) If the user requested a password change, follow steps 1) - 3). However, instead of double-clicking on the user name, right lick on it and select 'Reset Password'. :  <br/>
<img src="https://i.imgur.com/wT2AzPE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
10) A new window should open asking for the new password. Type in the new password and make sure both checkboxes are checked. Click 'OK'. : <br/>
<img src="https://i.imgur.com/ixW9M9e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
11) You should receive a message confirming that the user's password was changed. : <br/>
<img src="https://i.imgur.com/EYDkU5j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
