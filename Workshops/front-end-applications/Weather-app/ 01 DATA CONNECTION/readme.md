# Data Connection

1. Login to Build Apps, Create a new project.

2. The newly created project will open. The first step is to connect your application to Current Weather API (<a href="https://openweathermap.org/current">API Documentaion</a>).<br>
Now click on the <b>DATA</b> tab on the top to open the Data connector. 
Using Data connector you can connect your application to different data sources.<br><br>
![](images/1%20Data%20tab.png)

3. Now click on <b>SAP Build Apps classic data entities</b> and select <b>REST API direct integration</b>.<br><br>
![](images/03.png)

4. Now a REST API configurator will pop-up.<br> 
The API is 
![](images/Screenshot%202023-02-07%20at%2011.36.09.png)
Now enter the following values in the Data configurator.<br>
<b>Resource ID</b>: WeatherApp<br>
<b>Short Description</b>: Weather App connection<br>
<b>Resource URL</b>: https://api.openweathermap.org/data/2.5/weather<br><br>
![](images/Screenshot%202023-02-07%20at%2011.29.54.png)

5. Now we have to add the query parameters. Click on ![](images/Screenshot%202023-02-07%20at%2011.51.48.png) to add a query paramater<br><br>
![](images/Screenshot%202023-02-07%20at%2011.40.10.png)

