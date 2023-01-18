<h1>FIM - File Integrity Monitoring</h1>

 FIM (File Integrity Monitoring) using PowerShell

<h2>Description</h2>
The project outlined in the instructions is a File Integrity Monitoring (FIM) system created using PowerShell. The goal of the project is to detect and alert authorized personnel to unauthorized changes to files and directories on a computer or network. The project will accomplish the following:

•	Create a new PowerShell script that will be used to perform FIM

•	Add a function to calculate the hash value of a file, which will be used to identify if a file has been modified.

•	Add a function to compare the current and previous hash values, which will be used to determine if a file has been modified.

•	Add a function to send an alert email if a file has been modified

•	Add a function to check the integrity of a file, which will use the functions defined above to calculate the current hash value of the file, compare it with the previous hash value, and send an alert email if the file has been modified. It also updates the previous hash file with the current hash value.

•	Test the script to make sure it's working as expected.

•	Automate the script to run on a regular basis.

By completing this project, you will learn how to use PowerShell to create a FIM system, including how to calculate the hash value of a file, compare the current and previous hash values, send an alert email, check the integrity of a file, and how to automate the process. Additionally, you will gain experience in using specific PowerShell cmdlets like Get-FileHash, Compare-Object, and Send-MailMessage.

<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
 <b></b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Step-by-step walkthrough guide:</h2>

<p align="left">

Here is a step-by-step tutorial that covers how to create a PowerShell script for file integrity monitoring:

 1.	<b>Create a new PowerShell script:</b> Open PowerShell and create a new script by typing <b>New-Item -ItemType File -Path "C:\path\to\fim.ps1"</b> and pressing enter. This will create a new script file named <b>fim.ps1</b> in the specified path.

 2.	<b>Add a function to calculate the hash value of a file:</b> In the script file, add the following function:
 <br/>
<img src="https://i.imgur.com/JtcxWcU.jpg" height="80%" width="80%"/>
<br />
<br />
 This function takes in a file path as a parameter and uses the <b>Get-FileHash</b> cmdlet to calculate the hash value of the file. It then stores the value in a variable and returns it.
<br />
<br />
 3.	<b>Add a function to compare the current and previous hash values:</b> In the script file, add the following function:
  <br/>
<img src="https://i.imgur.com/FKMOt9W.jpg" height="80%" width="80%"/>
 <br />
<br />
This function takes in the current and previous hash values as parameters and uses the <b>Compare-Object</b> cmdlet to compare them. It then stores the result in a variable and returns it.
<br />
<br />
 4.	<b>Add a function to send an alert email:</b> In the script file, add the following function:
 <br/>
<img src="https://imgur.com/9whBdfl.jpg" height="80%" width="80%"/>
<br />
<br />
 This function takes in the file path as a parameter and uses the <b>Send-MailMessage</b> cmdlet to send an email alert to the specified email address.
<br />
<br />
 5.	<b>Add a function to check the integrity of a file:</b> In the script file, add the following function:
 <br/>
<img src="https://i.imgur.com/7AxPdj1.jpg" height="80%" width="80%"/>
<br />
<br />
This function takes in the file path and the previous hash file path as parameters. It then uses the functions defined in steps 2 and 3 to calculate the current hash value of the file, compare it with the previous hash value, and send an alert email if the file has been modified. It also updates the previous hash file with the current hash value.
<br />
<br />
 6.	<b>Test the script:</b> Before using the script on a regular basis, you should test it first to make sure it's working as expected. To do this, you can use the <b>Check-FileIntegrity</b> function and pass in the path to a test file and a test previous hash file. For example, you can use the following command:
  <br/>
<img src="https://imgur.com/RylZzZ9.jpg" height="80%" width="80%"/>
<br />
<br />
This will run the function and check the integrity of the test file. If the file has been modified, it will send an alert email and update the test’s previous hash file with the current hash value.
<br />
<br />
 7.	<b>Automate the script:</b> Once you've confirmed that the script is working as expected, you can automate it to run on a regular basis. You can use the Windows Task Scheduler to schedule the script to run at specific intervals. For example, you can schedule it to run daily at a specific time.
<br />
<br />
 8.	<b>Using Get-ChildItem cmdlet to check all files in a directory:</b> To check all files in a directory and all of its subdirectories, you can use the <b>Get-ChildItem</b> cmdlet to get all the files in a specific directory, and then use a loop to iterate over each file and check its integrity using the <b>Check-FileIntegrity</b> function. For example, you can use the following command:
  <br/>
<img src="https://imgur.com/oDvaq5q.jpg" height="80%" width="80%"/>
<br />
<br />
This command gets all the files in the specified directory and its subdirectories and then iterates over each file, running the <b>Check-FileIntegrity</b> function on each file.
<br />
<br />
Keep in mind that you should use the appropriate path for your environment and also, this is just one way to create a file integrity monitoring system using PowerShell.
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
