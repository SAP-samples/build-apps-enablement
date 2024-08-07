# Contents
Module 1 : <a href="https://github.com/SAP-samples/build-apps-enablement/blob/main/BuildShow/251_TA_BTP-Build_Code_Using-Joule/251-1_Build_Code.md">Build Code<br></a>
Module 2 : <a href="https://github.com/SAP-samples/build-apps-enablement/blob/main/BuildShow/251-A_TA_BTP-Build_Code_ProcessAutomation/251A_Build_Process_Automation_optional.md"><b>Build Process Automation</b></a><br>
Module 3 :<a href="https://github.com/SAP-samples/build-apps-enablement/blob/main/BuildShow/252_TA_BTP-Build_Code_Build-Apps/252-0_Build_Apps.md"> Build Apps</a><br>

# Module 2 


### Create an SAP Build Process Automation project from a template

1. Click <a href ="https://sap-build-academy-devtest.eu10.build.cloud.sap/lobby"> Lobby</a> to open the entry page of SAP Build Process Automation.
<br><i>Verify once that you are logged in with the right user id and copy the id for use later. </i><br><br>
![](./Images/Image0.png)

2. In the Lobby, use the search field to look for the project named**PM-Bonus Redemption Process(EU)**. <br><i>Hint: Switch to the options ‘All projects’ to find the template project</i>. <br><br>
![](./Images/Image1.png)

3. Prefix the user id (previously copied in step 1.1) and ‘Save As New’ project.<br><br>
![](./Images/Image3.png)

4. Open the project and go to the Redemption process, expand, and explore it. <br>
<b><u>NOTE</b></u>:  This process demonstrates a simple workflow that adds the conditional logic to decline a 'redemption only' purchase and approve any redemption only with a minimum value of the purchase. Here, the Decline and Approval is done via a Form notification. <br><br>
<i><b><u>Disclaimer</u></b>: The use case is intentionally kept simple for purpose of this tutorial to showcase the decline as a notification only. The redemption would still pass as we have not built any complex logic around it yet.<br><br></i>
Here is a video tutorial for this unit <a href="https://video.sap.com/media/t/1_14sg7rl1">Deploy redemption process</a><br><br>
![](./Images/Image6.png)<br><br>
![](./Images/Image7.png)<br><br>
![](./Images/Image8.png)




5. In the DeclineForm (General tab -> scroll to Users) change the mail id to <your user-id (in lower case only)>@sapexperienceacademy.com. eg:tac005323u01@sapexperienceacademy.com<br><br>
![](./Images/Image4.png)

6. In the Notification Form (General tab -> scroll to Users) change the mail id to <your user-id (in lower case only)>@sapexperienceacademy.com <br><br>
![](./Images/Image5.png)

7. Save and Release the project with default settings<br><br>
![](./Images/Image9.png)

8. Deploy the project in Public environment. <br><br>
![](./Images/image11.png)

9. Return to the SAP Lobby and Publish this process to SAP Build Library. <br><br>
![](./Images/image10.png)

10. Test the process.
    1. Go to Monitoring tab . <br><br> ![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/f0c973c8-5b31-4025-9b4c-782f344601c6)
    2. Select Processes and Workflows <br><br>![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/5d2c89cd-f017-4962-8898-a6d9546fde03)
    3. Search for your process. Hint. As the project is prefixed with your user id, search for your user id. <br> <br>![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/8134833b-d0a2-4eb2-8e76-7bc581acb159)
    4. Click on **Start New Instance** and replace it with the json object below and click on **Start New Instance and Close** and finally click on **Start Instances** :  <br><br> ![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/8480f4d0-70ca-440a-84e6-31733c16dfa6)
    <pre>
       {
        "redemption": {
            "CustomerNumber": 2093,
            "RedemptionPoints": 100,
            "PurchaseValue": 10
        }

    }</pre><br><br> ![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/6b4fe936-3764-489e-9b0d-b5b486dcac4f)
11. We can see the process instance with the Status **Running** .<br><br>
    ![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/a9ef60c2-4046-4531-ba28-ef3922f93c43)
13. Click on it and expand the Log files. We can observe that the Condition **Redemption approved** has been reached. <br><br> ![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/d584de0c-df91-4400-96f2-c30ad93ff9d3)
14. Click on **My Inbox** ![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/1d5b8bf9-e0f7-477a-89e3-181de25fbded) .<br><br> 
Here, you can find the notification form corresponding to **Redemption approved**. <br><br> ![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/06f19e17-fab6-47ec-9436-ccfc866f01bb)
We have tested the Redemption approved case successfully.
15. [OPTIONAL] To create an instance for the Decline redemption case, use the json below in step 4. (above).
<pre>
       {
        "redemption": {
            "CustomerNumber": 2093,
            "RedemptionPoints": 100,
            "PurchaseValue": 0
        }

    }
    </pre><br><br>
    Observe the process instance, explore the logs and check **My Inbox**.<br><br>
With this we have tested our process successfully.

Disclaimer:  Integration of this process with SAP Build Apps is not covered as part of this exercise. Refer to the blog post with this information for some inspiration to extend the SAP Build Apps to trigger this process: https://community.sap.com/t5/sap-builders-blog-posts/what-s-new-in-sap-build-seamless-integration-of-processes-and-apps/ba-p/13675739


**[Next Module 3: SAP Build Apps](../252_TA_BTP-Build_Code_Build-Apps/252-0_Build_Apps.md) >**

 
