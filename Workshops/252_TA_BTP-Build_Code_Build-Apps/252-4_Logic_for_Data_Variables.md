# Module 2 - Unit 4: Logic for Data Variables  



1. Go to UI Canvas > Switch to Variables > Go to Data Variables > Add 2 data variables: *A_ProductBasicText* and *Customers* 

**Note**: Please make sure that you have same data variable names in your screen: **A_ProductBasicText1** and **Customers1**

![](./Images/252-4_Screenshot_116.png)

2. Select *Customers1* data entity. Click on the *X* icon under Filter condition. Go to Object with Properties

![](./Images/252-4_Screenshot_117.png)

3. Add a condition. Property: *customerNumber*. Condition type: *equal*. Click on the little icon under Compared value

![](./Images/252-4_Screenshot_118.png)

4. Go to Formula > Click into the Formula field

![](./Images/252-4_Screenshot_119.png)

5. Type the formula below > Save the Formula > Save the condition
<br>

>INTEGER(params.SelectedCustomerNumber)

![](./Images/252-4_Screenshot_120.png)

6. Drag & Drop the UI Components with the following order: List divider > Dropdown field > Input field > Button

![](./Images/252-4_Screenshot_121.png)

7. Switch to Variables > Go to Page Variables > Create 2 Page Variables > Save

<br>

>Variable 1: *PurchaseValue* Value type: number
>Variable 2: *SelectedProduct* Value type: text

![](./Images/252-4_Screenshot_122.png)

8. Switch back to View > Select Dropdown field. Rename the Label text: *Select Product*. Then, Click on the little icon under *Option list*

![](./Images/252-4_Screenshot_123.png)

9. Go to formula > Type the formula below > Save the Formula 

<br>

>MAP(data.A_ProductBasicText1, {label:item.Product, value:item.Product})

![](./Images/252-4_Screenshot_124.png)

10. Go to Selected value > Data and Variables > Page Variable > SelectedProduct > Save

![](./Images/252-4_Screenshot_125.png)

11. Select Input field > Rename label: *Purchase Value* > Click on the little icon under *Value*

![](./Images/252-4_Screenshot_126.png)

12. Data and Variables > Page Variable > PurchaseValue > Save

![](./Images/252-4_Screenshot_127.png)

13. Select Button > Raname label: *Add Points!* > Open Logic Canvas

![](./Images/252-4_Screenshot_128.png)

14. Drag & Drop the logic components below to create the logic flow shown below

![](./Images/252-4_Screenshot_129.png)

15. Select Create record function > Select the data entity: *Purchases* > Click on the Custom Object

![](./Images/252-4_Screenshot_130.png)

16. Click on the ABC icon under ID > Formula > Click on the Formula bar

![](./Images/252-4_Screenshot_131.png)

17. Type the following formula and Save: *GENERATE_UUID()*

![](./Images/252-4_Screenshot_132.png)

18. Click on the X icon under customer_ID > Formula > Create formula

![](./Images/252-4_Screenshot_133.png)

19. Type the following formula and Save: *data.Customers1[0].ID* 

![](./Images/252-4_Screenshot_134.png)

20. Click on the X icon under purchaseValue > Formula > Create formula

![](./Images/252-4_Screenshot_135.png)

21. Type the following formula and Save: *INTEGER(pageVars.PurchaseValue)* 

![](./Images/252-4_Screenshot_136.png)

22. Click on the X icon under selectedProduct > Data and Variables > Page Variable > SelectedProduct

![](./Images/252-4_Screenshot_137.png)

23. Save the window

![](./Images/252-4_Screenshot_138.png)

24. Select *Alert* component > CLick on the ABC icon under Dialog title > Formula 

![](./Images/252-4_Screenshot_139.png)

25. Type the formula below > Save

<br>

>data.Customers1[0].name + " has successfully earned " + outputs["Create record"].response.rewardPoints + " points!"

![](./Images/252-4_Screenshot_140.png)

26. Go to the next page: *Redeem Points*

![](./Images/252-4_Screenshot_141.png)

27. Drag & Drop the UI Components with the following order: List divider > Input field > Button

![](./Images/252-4_Screenshot_142.png)

28. Switch to Variables > Go to Page Variables > Create a Page Variable > Save

<br>

>Variable: *RedemptionAmount* Value type: number


![](./Images/252-4_Screenshot_143.png)

29. Go to Data Variables > Create Data Variable > Go to Filter Condition of the created variable

![](./Images/252-4_Screenshot_144.png)

30. Object with Properties > Add Condition > Property: *customerNumber* > Condition type: *equal* > Click on the little icon under Compared value

![](./Images/252-4_Screenshot_145.png)

31. Formula > Click on the Formula Bar > Type the following formula: *INTEGER(params.SelectedCustomerNumber)* > Save > Save

![](./Images/252-4_Screenshot_146.png)

32. Select Input field > Rename label: *Redemption Amount* > Click on the little icon under *Value*

![](./Images/252-4_Screenshot_147.png)

33. Data and Variables > Page Variable > Redemption Amount > Save

![](./Images/252-4_Screenshot_148.png)

34. Select Button > Raname label: *Redeem Points!*

![](./Images/252-4_Screenshot_149.png)

35. Drag & Drop the logic components below to create the logic flow shown below. Save

![](./Images/252-4_Screenshot_150.png)

36. Select Create record function > Select the data entity: *Redemptions* > Click on the Custom Object

![](./Images/252-4_Screenshot_151.png)

37. Click on the ABC icon under ID > Formula > Click on the Formula bar

![](./Images/252-4_Screenshot_152.png)

38. Type the following formula and Save: *GENERATE_UUID()*

![](./Images/252-4_Screenshot_153.png)

39. Click on the X icon under customer_ID > Formula > Create formula

![](./Images/252-4_Screenshot_154.png)

40. Type the following formula and Save: *data.Customers1[0].ID* 

![](./Images/252-4_Screenshot_155.png)

41. Click on the X icon under redeemedAmount > Formula > Create formula

![](./Images/252-4_Screenshot_156.png)

42. Type the following formula and Save: *INTEGER(pageVars.RedemptionAmount)* 

![](./Images/252-4_Screenshot_157.png)

43. Save the window

![](./Images/252-4_Screenshot_158.png)

44. Select Alert component > Click on the ABC icon under Dialog title > Formula

![](./Images/252-4_Screenshot_159.png)

45. Type the formula below > Save

<br>

>data.Customers1[0].name + " has redeemed " + pageVars.RedemptionAmount + " successfully"

![](./Images/252-4_Screenshot_160.png)


**[Next Module 2 - Unit 5: Logic for UI Components](./252-5_Logic_for_UI_Components.md) >**
