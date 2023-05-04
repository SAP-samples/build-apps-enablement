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
<b>Resource ID</b>  : WeatherApp<br>
<b>Short Description</b>: Weather App connection<br>
<b>Resource URL</b>: https://api.openweathermap.org/data/2.5/weather<br><br>
![](images/Screenshot%202023-02-07%20at%2011.29.54.png)

5. Now we have to add the query parameters. Click on <img src="https://github.com/SAP-samples/build-apps-enablement/blob/main/Workshops/front-end-applications/Weather-app/%2001%20DATA%20CONNECTION/Images/Screenshot%202023-02-07%20at%2011.51.48.png?raw=true" width="12"> to add a query paramater<br><br>
![](images/Screenshot%202023-02-07%20at%2011.40.10.png)

6. A new Query parameter gets created. According to the API documentation the API key parameter is “appid”. <br>Update the following properties of the newly created parameter.<br>
<b>Label</b>      : API Key<br>
<b>Key</b>         : appid<br>
<b>Value type</b>  : Text<br>
<b>Is Static</b>  : On<br>
<b>Value</b>      : <i><>your api key<> </i><br><br>
![](images/Screenshot%202023-02-07%20at%2012.02.07.png)


7. Add another Query parameter. <br>
<b>Label</b>      : Value units<br>
<b>Key</b>         : units<br>
<b>Value type</b>  : Text<br>
<b>Is Static</b>  : On<br>
<b>Value</b>      : <i>metric</i><br>
If  you need your results in Celcius, use the value as metric. If you need your results in Farenheit, use your value as imperial.<br><br>
![](images/Screenshot%202023-02-07%20at%2012.19.55.png)

8. Now switch to <b>GET RECORD</b> tab.<br>
Empty the value in the relative path.<br>
Select the <b>URL placeholder</b> and click on <b>REMOVE PARAMETER</b><br><br>
![](images/Screenshot%202023-02-07%20at%2012.28.24.png)

9. Add a query parameter for Lattitude. <br>
<b>Label</b>      : Lattitude<br>
<b>Key</b>         : lat<br>
<b>Value type</b>  : Number<br>
<b>Is Static</b>  : off<br>
<b>Value</b>      : <br>
<b>Is optional</b> : off<br><br>
![](images/Screenshot%202023-02-07%20at%2012.32.53.png)

10. Similarily, add a query parameter for Longitude. <br>
<b>Label</b>      : Longitude<br>
<b>Key</b>         : lon<br>
<b>Value type</b>  : Number<br>
<b>Is Static</b>  : off<br>
<b>Value</b>      : <br>
<b>Is optional</b> : off<br><br>
![](images/Screenshot%202023-02-07%20at%2012.39.36.png)

11.  Now we can test if this connection is working. Switch to TEST tab. <br>
Enter some sample value for lattitude and longitude. <br>
Click on <b>RUN TEST</b><br><br>
![](images/Screenshot%202023-02-07%20at%2012.42.21.png)

12. The Call response should be <b> STATUS: OK</b>.<br>
Click on <b> SET SCHEMA FROM RESPONSE</b>.
<br><br>
If you are not getting STATUS OK please review from step 4 again.<br><br>
![](images/Screenshot%202023-02-07%20at%2012.45.57.png)

13. Click on <b> SAVE DATA ENTITY</b>.
![](images/Screenshot%202023-05-04%20at%2015.24.38.png)

