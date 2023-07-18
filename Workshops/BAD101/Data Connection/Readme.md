# Data connection

- Input data : Open Food Facts
- Output data : On-device storage


## Adding OpenFoodFacts.

1. Click on Data Tab to add the Data integrations.<br><br>
![data tab](images/Screenshot%202023-07-18%20at%2012.02.02.png)

2. Luckily, the Build App developers has made this open food facts integration as template. <br>
Click on <b>CREATE DATA ENTITY</b> and select <b>Marketplace search</b>.<br><br>
![](images/Screenshot%202023-07-18%20at%2013.04.00.png)

3. Select OpenFoodFacts data integration here.
<br><br>
![](images/Screenshot%202023-07-18%20at%2013.04.34.png)

4. Install it.

![](images/Screenshot%202023-07-18%20at%2013.04.54.png)

5. Now select the integration.<br>
   open <b>Get Record</b>.<br>
   Select barcode <b>URL Parameter</b> and change the value type to <b>Number</b>.<br><br>
![](images/Screenshot%202023-07-18%20at%2013.08.38.png)


6. Change the binding type to Static number and enter the following value <i>737628064502</i> and run the test.<br><br>
![](images/Screenshot%202023-07-18%20at%2013.11.57.png)

7. SET SCHEMA from the response. 
![](images/Screenshot%202023-07-18%20at%2013.14.13.png)

8. Click on SAVE DATA ENTITY.
![](images/Screenshot%202023-07-18%20at%2013.14.47.png).




## Adding On-Device storage.

1. Click on <b>CREATE DATA ENTITY</b>.<br><br>
![](images/Screenshot%202023-07-18%20at%2014.28.06.png)

2. Give a name to your Data Enity and click on ADD. <br><br>
![](images/Screenshot%202023-07-18%20at%2014.28.40.png)

3. Select the <b>ID</b> under fields and rename it to <b>food</b>. 
![](images/Screenshot%202023-07-18%20at%2014.30.36.png)

4. Add another field and name it as <b>energy</b>.<br> You can also more fields if you want to track more facts about the food.(Ex, Sugar levels, protiens etc.,) <br><br>
![](images/Screenshot%202023-07-18%20at%2014.31.51.png)


## Create Data Variables. 

- Open your UI Canvas. <br>
- Switch to variables view<br>
- Select Data Variables.<br>
- Add Data Variable<br>

![](images/Screenshot%202023-07-18%20at%2014.40.56.png)


