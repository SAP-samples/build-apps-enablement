**[Previous Module 1 - Unit 5: Add External Data Resource](./251-5_Add_External_Data_Resource.md) >**
# Module 1 - Unit 6: Admin UI



To Display and test the content we have already created for the customer loyalty program, we also create some Fiori Elements UIs.

Here is a video tutorial for this unit <a href="https://video.sap.com/media/t/1_wtxp2s27">UI Application</a>


1. Go to back to the Storyboard and add a first UI application.

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/e8b508af-5f36-4ebc-8da6-8a65fdc8c071)


2. We will start with the user interface for the data entity Purchases.<br> Enter the following values:
Display name: Purchases<br>
Description: Manage Purchases<br>
Data Source: <"your project name"> <br>

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/756dc227-d47d-4743-b487-f23c88b7b0a4)


3. As we are using the browser, we will select **Template-Based Responsive Application** as UI Application type.

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/69373b07-5ce5-4829-b188-2e1e232c5511)


4. And as an UI Application Template select **List Report Page**

![](./Images/251-6_UI4.jpg)

6. As a last step select the **Purchases** entity as Main entity and complete the setup. The page will be created now.

![](./Images/251-6_UI5.jpg)

You can repeat the same with the customer and redemption entity.

Customer:
  - Display name: Customers
  - Description: Manage Customers
  - UI Application type: Template-Based Responsive Application
  - UI Application Template: List Report Page
  - Main Entity: Customers

Redemptions:
  - Display name: Redemptions
  - Description: Manage Redemptions
  - UI Application type: Template-Based Responsive Application
  - UI Application Template: List Report Page
  - Main Entity: Redemptions


7. Now we are going to modify the UI for the purchases a bit. We will include the products from S4 as value help in the purchases and hide some fields. Therefore go back to the Storyboard, select the Purchases Ui and open it in the Page Map.

![](./Images/251-6_page1.jpg)

8. We want to modify the Object page. Therefore click on the **edit** icon

![](./Images/251-6_page2.jpg)

9. In the Sections, expand **General Information** then expand **Form** and then expand **Fields**. Afterwards it will look like this:

![](./Images/251-6_page3.jpg)

10. The reward points are calculated automatically by the logic Joule has created for us. Therefore we delete the **Reward Points** field by pressing the trash bin icon next to it and confirm the deletion.

![](./Images/251-6_page4.jpg)

11. We want to select the Products from S4 for the purchases. Therfore select the field **Selected Product** and change the Display Type in the properties on the right side to **Value Help**. 
Set the following:
  - Label: Product
  - Value Source Entity: A_ProductBasicText
  - keep the rest as it is and press apply


![](./Images/251-6_page5.jpg)
![](./Images/251-6_page6.jpg)

You can now preview the UI. here is a video tutorial to preview the backend app you created <a href="https://video.sap.com/media/t/1_eht1hhe4">Preview</a>.





**[Next Module 1 - Unit 7: Preview](./251-7_Preview.md) >**
