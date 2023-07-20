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

5. Open the Data Connection.<br>
   Click on <b>GET RECORD</b> and select the <b>TEST</b> tab.<br>
   In the input field, press <b>Space Bar</b> and <b>Backspace</b> immediately. <br>
   Now you will be able to run the test.
![](Images/Screenshot%202023-07-20%20at%2011.40.26.png) 

7. SET SCHEMA from the response. 
![](Images/8.png)

8. Click on SAVE DATA ENTITY.
![](Images/9.png)




## Adding On-Device storage.

1. Click on <b>CREATE DATA ENTITY</b>.<br><br>
![](Images/10.png)

2. Give a name to your Data Enity and click on ADD. <br><br>
![](Images/11.png)


3. Add two NEW Fields, <b>Energy</b> as Number  and <b>Food</b> as Text respectively.<br> You can also add more fields if you want to track more facts about the food.(Ex, Sugar levels, protiens etc.,) <br><br>
![](Images/Screenshot%202023-07-20%20at%2011.36.31.png)


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


