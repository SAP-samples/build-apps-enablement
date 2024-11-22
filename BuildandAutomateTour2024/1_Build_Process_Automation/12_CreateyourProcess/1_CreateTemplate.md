< [Previous Lesson](/BuildandAutomateTour2024/1_Build_Process_Automation/11_Import_template/readme.md)

# Create Document Template

1. Download the document here 
<a href="https://github.com/SAP-samples/build-apps-enablement/blob/main/BuildandAutomateTour2024/1_Build_Process_Automation/Template/RP.png">Work Permit Document</a><br>
> Also free to use your own Work Permit document.

2. In your new created Build Process Automation project, click on **Create** and select **Document Template**.<br><br>
![](./Images/12_1_create.png)

3. Select ** Create a New Template** and click on **Next**.<br><br>
![](./Images/12_2.png)

4. Give a name to the template *Workpermitdocument* and select the document locally form your computer.<br><br>
![](./Images/12_3.png)

5. For the document type, select **Custom** and click **Next**.<br><br>
![](./Images/12_4.png)

6. To create a new extraction schema, click on **New** in the Custom Schemas menu.<br><br>
![](./Images/12_5.png)

7. Give a name to the schema **RpScan**.<br><br>
![](./Images/12_6.png)

8. In the schema, create the fields to be extracted from the document.<br>
**Add** a new header field and call it **Name** with the data type string and **Save** it.<br><br>
![](./Images/12_7.png)

9. Similarily, add **validity** and **ID** fields.<br><br>
![](./Images/12_8.png)

10. Review the template and *Add** it.
![](./Images/12_9.png)

[Next Lesson](./2_Annotatetemplate.md) >