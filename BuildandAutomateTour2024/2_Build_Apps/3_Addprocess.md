< [Previous lesson](./2_AppCustomisation.md)

# Add process trigger to the application


1. Select **Integrations** tab on the top and click on **ADD INTEGRATION**.<br><br>
![](./Images/2_1_11.png)

2. Select **LIBRARY** under SAP Build Library.<br><br>
![](./Images/2_1_12.png)

3. Select your recently published process in the library.<br><br>
![](./Images/2_1_13.png)

4. Click on **Enable process**.
![](./Images/2_1_14.png)

5. Switch back to **UI Canvas**.<br> Select the button and click on **Add logic to BUTTON 1** in the bottom to open the logic editor.
![](./Images/2_1_15.png)

6. Drag and drop **Trigger process** logic component into the logic editor.
![](./Images/2_1_16.png)

7. Connect the nodes.<br> select workpermitprocess and click on **{ }** to open the binding menu of the input parameters.<br><br>
![](./Images/2_1_17.png)

8. Select **Object with properites**.<br><br>
![](./Images/2_1_18.png)

9. Open the binding menu of **FilePath** by clicking on **ABC** and select the filepath page variable.<br>
similarily, bind the **Name** page variable to **EmployeeName** parameter.<br><br>
![](./Images/2_1_19.png)

10. Open the binding menu for the **EmployeeEmail**
![](./Images/2_1_25.png)

11. Select **System variable**.<br><br>
![](./Images/2_1_20.png)

12. Select **Currently loggen in user** for system varaible and **Currently logged in user.email** for system variable field and **SAVE** it. <br><br>
![](./Images/2_1_21.png)

13. **SAVE** again.
![](./Images/2_1_22.png)

7. Drag a **Toast** flow function onto the canvas.

    ![](./Images/logic-dragtoast.png)

Connect the **top** output of the **Trigger process** flow function to it.
![](./Images/logic-bind-toast.png)

8. Click on the **Toast** flow function and configure it in the **Properties** pane on the right.
For **Toast message**, click on the **ABC**.

    ![](./Images/toastmessage.png)

Select **Formula** > **Formula**.

```
"Triggered process with ID: " + outputs["Trigger process"].newProcessInstance.id
```

9. Save the formula using the **Save** button.

    ![](./Images/logic_toast_save.png)

10. Select **SAVE** on the top right corner of the screen to save your recent changes.

    ![](./Images/page_layout.png)

Congratulations, its time to Test your HCM Workpermit App and Process.

[Next Lesson](./4_Testing.md) >