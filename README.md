<h1>Active Directory Home Lab - Recover Account</h1>

<h2>Description</h2>
In this lab, I am going to demonstrate a scenario depicting how a Tier 1 helpdesk technician would recover a user's account. In this scenario, a user named John cannot log on to his Outlook account. I will be using Active Directory to recover his account and reset his password.

<h2>Software Used</h2>

- <b>Virtual VM VirtualBox</b> 

<h2>Operating Systems Used </h2>

- <b>Windows Server 2019</b>

<h2>Program walk-through:</h2>

<p align="center">
Before doing anything, the first step is to allow the user (in this scenario, John) to explain his issue without interrupting. When the user finishes speaking, I (the helpdesk technician) will ask some questions. For example, I would ask what operating system he is using or whether the login issue occurs anywhere else besides Outlook. Then, I would allow the user to answer those questions, collecting info to resolve the problem.
<br />
  <br />
First, open 'Active Directory Users and Computers' under 'Tools' on the upper right-hand corner. : <br />
<img src="https://i.imgur.com/wJMopVy.png" height="80%" width="80%" alt="Change System Name"/>
<br />
<br />
A window will open, displaying the new domain I created (mydomain.com). Click on mydomain.com and it will open all the folders to the right. Each folder is categorized by type (eg. organizational unit, container). In an organizational unit type, you can apply group policies to that folder. However, with a container type, you cannot apply group policies. : <br />
<img src="https://i.imgur.com/10w2FXo.png" height="80%" width="80%" alt="Change System Name"/>
<br />
<br />
This is where we will create a new user. Right-click on mydomain.com and go to 'New' and to the right, click on 'User'.  :  <br/>
<img src="https://i.imgur.com/ldheoeV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
A new window will open, displaying the full name for that new user. Originally, the textboxes will be blank for you to fill in. Type in your first, middle, and last name separately, and the textbox for Full Name will automatically fill in. In this case, I used my own name. Next, type in a user logon name (I recommend using your first and last name separated by a period). Click 'Next'. : <br/>
<img src="https://i.imgur.com/iwDzSAq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
You will now be prompted to provide a password for the user. Create a password that is easy for you to remember. Below, you will see a list of checkboxes regarding what to do with the password. You will see that the first checkbox, which requires the user to change the password upon next login, is checked by default. You may uncheck this box if you do not want this option. However, for security purposes, it is recommended to require users to change their password upon next login. Click 'Next' and you will see a summary of the new user's information. Click 'Finish'. :  <br/>
<img src="https://i.imgur.com/QZU1K93.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Going back to the 'Active Directory Users and Computers' window, you can confirm that a new user, Ross Park', has been created. Right-click on the new user and click on 'Properties'. You will see all the information (name, address, member of, etc.) of that new user. :  <br/>
<img src="https://i.imgur.com/7fPOUJr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wxqurzI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Initially, the new user 'Ross Park' is currently a member of the group 'Domain Users'. To add the user to another group, click 'Add...' and a window should open. In this scenario, I want to add that user to the group 'Domain Admins'. I will type in 'Domain Admins' and select 'Check Names'. When the name becomes underlined, that group exists. Click 'OK'. :  <br/>
<img src="https://i.imgur.com/9ufy98H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/wZ64SIJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
When you go back to the Porperties window for the new user, you will see that 'Ross Park' now belongs to both groups. :  <br/>
<img src="https://i.imgur.com/5TEL1nM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
Before siging in as the new user, I will first log out of the Administrator account. This will then take me to the log on screen. On the log on screen, I will first click on 'Other user' because I am signing in as the new user. Next, I will type in my new user name (ross.park) and my password. :  <br/>
<img src="https://i.imgur.com/DyVnjrJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/ZiseTsY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
Now, I am logged in as the new user (ross.park). The Server Manager application will automatically open uopn login. :  <br/>
<img src="https://i.imgur.com/PbiiQt9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />
<br />
This time, I will create a new group. First, click on 'Tools', and select 'Active Directory Users and Computers'. Once the window opens, right-click on mydomain.com, navigate to New and select 'Group' on the right. :  <br/>
<img src="https://i.imgur.com/moEftJf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />
<br />
A new window will open and you will be prompted to create a group name. In this scenario, I named the group 'HR'. Below the group name is group scope. By default, the button will be selected as 'Global', but 'Domain Local' should be selected so that other servers/organizations may not access this group. Click OK. :
<img src="https://i.imgur.com/krrgEqQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
Now on the domain, a new folder (new group) has been created. :  <br/>
<img src="https://i.imgur.com/ada2AWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   <br/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
