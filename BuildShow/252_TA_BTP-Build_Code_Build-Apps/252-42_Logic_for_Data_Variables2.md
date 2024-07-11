
# 


1.  Go to the next page: *Redeem Points*

![](./Images/252-4_Screenshot_141.png)

2. Drag & Drop the UI Components with the following order: List divider > Input field > Button

![](./Images/252-4_Screenshot_142.png)

3. Switch to Variables > Go to Page Variables > Create a Page Variable > Save

<br>

>Variable: *RedemptionAmount* Value type: number


![](./Images/252-4_Screenshot_143.png)

4. Go to Data Variables > Create Data Variable > Go to Filter Condition of the created variable

![](./Images/252-4_Screenshot_144.png)

5. Object with Properties > Add Condition > Property: *customerNumber* > Condition type: *equal* > Click on the little icon under Compared value

![](./Images/252-4_Screenshot_145.png)

6. Formula > Click on the Formula Bar > Type the following formula: *INTEGER(params.SelectedCustomerNumber)* > Save > Save

![](./Images/252-4_Screenshot_146.png)

7. Select Input field > Rename label: *Redemption Amount* > Click on the little icon under *Value*

![](./Images/252-4_Screenshot_147.png)

8. Data and Variables > Page Variable > Redemption Amount > Save

![](./Images/252-4_Screenshot_148.png)

9. Select Button > Raname label: *Redeem Points!*

![](./Images/252-4_Screenshot_149.png)

10. Drag & Drop the logic components below to create the logic flow shown below. Save

![](./Images/step35.png)

11. Select the trigger process node. <br>
    On right hand side make sure you select the right process and opne the binding menu for Redemption object.

![](./Images/step36.png)

12. Use the following formulas for Purchase Value and Customer number.<br><br>
<b>Purchase value</b><pre>data.Customers1[0].totalPurchaseValue</pre>
<b>Customer number</b><pre>data.Customers1[0].customerNumber</pre>
For Redemption value select the Page variable <i>Redemption Value</i>

![](./images/step37.png)

13. Select Create record function > Select the data entity: *Redemptions* > Click on the Custom Object

![](./Images/step38.png)

14. Click on the ABC icon under ID > Formula > Click on the Formula bar

![](./Images/252-4_Screenshot_152.png)

15. Type the following formula and Save: *GENERATE_UUID()*

![](./Images/252-4_Screenshot_153.png)

16. Click on the X icon under customer_ID > Formula > Create formula

![](./Images/252-4_Screenshot_154.png)

17. Type the following formula and Save: *data.Customers1[0].ID* 

![](./Images/252-4_Screenshot_155.png)

18. Click on the X icon under redeemedAmount > Formula > Create formula

![](./Images/252-4_Screenshot_156.png)

19. Type the following formula and Save: *INTEGER(pageVars.RedemptionAmount)* 

![](./Images/252-4_Screenshot_157.png)

20. Save the window

![](./Images/252-4_Screenshot_158.png)

21. Select Alert component > enter the following text <i>Please check your inbox</i>

![](./Images/formulastep.png)


**[Next Module 2 - Unit 5: Logic for UI Components](./252-5_Logic_for_UI_Components.md) >**
