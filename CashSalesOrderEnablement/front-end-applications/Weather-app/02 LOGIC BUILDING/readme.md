Previous step: <a href="https://github.com/SAP-samples/build-apps-enablement/blob/main/Workshops/front-end-applications/Weather-app/%2001%20DATA%20CONNECTION/readme.md#enroll-beta"> Data Building</a>

# Logic Building 


In this step we will create logic for our application. In simpler terms we will now tell our application what it should do. 


1. Now, go back to UI canvas, and switch to <b>variables view</b>. <br><Br>
![](images/Screenshot%202023-05-04%20at%2015.03.07.png)

2. In VARIABLES view, select <b>DATA VARIABLES</b> tab, and click on <b>ADD DATA VARIABLE</b>.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.09.11.png)

3. You can see the Data Resource you created earlier, click on it to create a data variable.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.10.20.png)

4. Now select the value <b>Single data record</b> Data variable type property.<br><br>
Click on the gray bar in the bottom to open logic composer for the variable you created.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.10.59.png)

5. Remove the default logic as we will be adding our own logic to fetch data using the location of the device.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.12.19.png)

6. The next step is to build the application logic to fetch the weather data based on the physical location of the device that runs the app. 
<br>
Drag and drop <b>GPS location</b> flow logic under DEVICE in the logic component library. <br><br>
![](images/Screenshot%202023-05-04%20at%2015.13.32.png)

7. connect the <b>Page Focuse </b> and <b> GPS location nodes</b>.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.14.36.png)

8. Drag and drop <b>Get Record</b> under DATA from logic components and connect it with GPS location.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.15.44.png)

9. Drag and drop the <B>Set data variable</b> under VARIABLES from the logic components and connect with Get record.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.17.00.png)

10. Now select  <b>Get Record </b>node on the logic composer. Properties Tab will be opened, and the query parameter can be seen. Click on <b>X </b>to bind the respective values. 
<br><br>
![](images/Screenshot%202023-05-04%20at%2015.18.29.png)

11. Binding menu will pop up, click on <b>Output value of another node</b>.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.19.21.png)

12. All the logic nodes connected before GET record in the logic composer can be seen. <br>
Click on <b>GPS location</b>.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.19.37.png)

13. All the parameter from the GPS location node can been seen here. <br>
select <b>lattitude</b> and click on <b>SAVE</b>.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.20.32.png)

14. Similarily bind longitude value in the properties of GET RECORD node to longitude output from the GPS location node.<br><br>
![](images/Screenshot%202023-05-04%20at%2015.21.28.png)

15. Now, select the <b>Set data variable</b> node and open the binding menu for <b>data</b> in the properties. <br><br>
![](images/Screenshot%202023-05-04%20at%2015.21.56.png)

16. Select the <b> Output value of another node</b>.<br><bR>
![](images/Screenshot%202023-05-04%20at%2015.22.41.png)

17. Select <b>Get record</b> under Select logic node and click on <b>Record</b>. and click on <b>SAVE</b>.
<br><br>
![](images/Screenshot%202023-05-04%20at%2015.27.28.png)
