# Module 1 - Unit 6: Admin UI

To Display and test the content we have already created for the customer loyalty program, we also create some Fiori Elements UIs.

1. Go to back to the Storyboard and add a first UI application.

![](./Images/251-6_UI1.jpg)

2. We will start with the user interface for the data entity Purchases. Set the Display name to **Purchases** and the Description to **Manage Purchases**

![](./Images/251-6_UI2.jpg)

3. As we are using the browser, we will select **Template-Based Responsive Application** as UI Application type.

![](./Images/251-6_UI3.jpg)

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

Now continue with the deployment.

**[Next Module 1 - Unit 7: Deployment](./251-7_Deployment.md) >**
