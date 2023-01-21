 Previous Step: <a href="https://github.com/SAP-samples/sap-build-apps/blob/main/Workshops/front-end-applications/Bar-code-scanner-app/01%20App%20Interface/README.md"> 01 App Interface</a>
 
 # DATA CONNECTION
 
  1. Now click on the <b> DATA </b> tab on the top to open the Data connector. In Data connector you can connect your application to different data sources.<br><br>
  ![](images/1%20Data%20tab.png)

  2. Now under “<b>AppGyver Classic data entities</b>” click on "<b>CREATE DATA ENTITY</b>" and select “<b>Rest API direct integration</b>”.<br><br>
  ![](images/2%20Data%20entity.png)
  
  3. Now configure the resource with the following details:<br>
        &emsp; &emsp;•	Resource ID&emsp;&emsp;&ensp;: OpenFoodFacts<br>
        &emsp; &emsp;•	Short description: Data from Open Food Facts API<br>
        &emsp;&emsp; •	Resource URL&emsp;&ensp;: https://world.openfoodfacts.org/api/v0<br> 
        <br>
        ![](images/3%20API%20Config.png)


4. You now need to configure which information should be taken from the Open Food Facts API. For your application, you need to configure this to fetch the barcode information, since that’s what’s being scanned with the device camera. This can be achieved using a ‘Get Record’ request.
<br><br>To configure this,click <b><i>Get Record</b></i> (Get).<br><br>
In the Relative path field enter:
``` /product/{barcode}.json ```<br><br>
![](images/4%20Get%20record.png)


5. In the relative path filed you can see that <i>"barcode"</i> is entered with <b>{ }</b> because it's a place holder which will have dynamic data. That is every time the API is called it will have a different barcode value in that place holder. To configure it click the existing <b><i>URL placeholder key</b></i> , and then configure the following settings:<br><br>
&emsp;&emsp;•	<b><i>Label</b></i>: Barcode<br><br>
&emsp;&emsp;•	<b><i>Key</b></i>: barcode<br><br>
&emsp;&emsp;•	<b><i>Value type</b></i>: Text<br><br>
&emsp;&emsp;•	<b><i>Description</b></i>: Resource ID to retrieve<br><br>
&emsp;&emsp;•	<b><i>Is encoded</b></i>: Enabled<br><br>
&emsp;&emsp;•	<b><i>Is static</b></i>: Disabled<br><br>
&emsp;&emsp;•	<b><i>Is optional</b></i>: Enabled<br> <br>
![](images/6%20placeholder.png)


6. Now, to test if the API is working correctly, click on the <b>Test</b> tab.<br><br>
![](images/API%20Test.png)


7. Click on “<b>X</b>” icon to open the Binding menu.<br><br>
![](images/X%20button.png)


8. Now select “<b>Static Text</b>”.<br><br>
![](images/8%20text%20type.png)


9. Enter <b>6416453061361</b> into the <i>Type a text</i> field. This is an example barcode number, taken from a confectionary wrapper.<br>
Now click on Run Test<br><br>
![](images/8%20Test%20value.png)

10. The test now runs, displaying a Test API call response. In this response, you can see information about the confectionary. This includes the product categories, allergen information, and the brand who manufactured the product. If you are facing any errors here, please review from step 8 of this exercise to check if all the configuration is done correctly.<br>
Now click on "<b>SET SCHEMA FROM RESPONSE</b>".<br><br>
![](images/9%20schema.png)


11. Setting Schema from response stores the data structure from the URL, enabling the application to easily identify the types of information it is fetching.
Now click on "<b>Save DATA Entity</b>".
![](images/10%20Save%20data%20entity.png)



Next Step: <a href="https://github.com/SAP-samples/sap-build-apps/tree/main/Workshops/front-end-applications/Bar-code-scanner-app/03%20Create%20a%20Data%20Variable"> 03 Create a Data Variable</a>
 



  
