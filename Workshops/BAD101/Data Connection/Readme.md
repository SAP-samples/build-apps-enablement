# Data connection

- Input data : Open Food Facts
- Output data : On-device storage


## Adding OpenFoodFacts.

1. Click on Data Tab to add the Data integrations.<br><br>
![data tab](Images/1.png)

2. Luckily, the Build App developers has made this open food facts integration as template. <br>
Click on <b>CREATE DATA ENTITY</b> and select <b>Marketplace search</b>.<br><br>
![](Images/2.png)

3. Select OpenFoodFacts data integration here.
<br><br>
![](Images/3.png)

4. Install it.<br><br>
![](Images/4.png)

5. Now select the integration.<br>
   Open <b>Get Record</b>.<br>
   Select barcode <b>URL Parameter</b> and change the value type to <b>Number</b>.<br><br>
![](Images/6.png)


6. Change the binding type to Static number and enter the following value <i>737628064502</i> and run the test.<br><br>
![](Images/7.png)

7. SET SCHEMA from the response. 
![](Images/8.png)

8. Click on SAVE DATA ENTITY.
![](Images/9.png).




## Adding On-Device storage.

1. Click on <b>CREATE DATA ENTITY</b>.<br><br>
![](Images/10.png)

2. Give a name to your Data Enity and click on ADD. <br><br>
![](Images/11.png)

3. Select the <b>ID</b> under fields and rename it to <b>food</b>. 
![](Images/12.png)

4. Add another field and name it as <b>energy</b>.<br> You can also more fields if you want to track more facts about the food.(Ex, Sugar levels, protiens etc.,) <br><br>
![](Images/13.png)


## Create Data Variables. 

- Open your UI Canvas. <br>
- Switch to variables view<br>
- Select Data Variables.<br>
- Add Data Variable<br>
<br>
![](Images/14.png)

- Under variable type select single data record. 
- Below in the logic composer, select all the logic and remove them by using either backspace key or delete key on your keyboard.<br><br>
![](Images/15.png)


