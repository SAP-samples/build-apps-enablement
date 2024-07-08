# Process Automation


To configure the setup, 

- Select the email step called Notification to Build Admin and change the email adress to the Admin's email id who will reveiw the use cases. <br>
You can also change the body of the notification email. 

![](images/emailaddress.png)

You can change the link for Inbox with the link of your Build inbox.<br><Br>
![](images/mailbody.png)

Similarily you can edit the body of the other Email steps. 

- for the configuration of the action step <b><i>Post Ideas in Build COE</b></i>, 
<bR>make sure a destination variable is selected, if not create a destination variable and select it. 
<br>under <b>Run step on behalf of</b>, select the <b><i>Approval Form</b></i><br><br>
Leave the Inputs configuraton as it is.

![](images/Actionconfig.png)

After all the changes, save and release your project and Deploy<br><br>
![](images/release.png)

When deploying, select the destination that you created to conenct with SAP Build WorkZone. In this case it is <b>JAM_usecasebuddy</b>.<br><br>
![](images/Destination.png)







