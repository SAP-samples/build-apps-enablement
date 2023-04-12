# Diet Tracker Extesnsion (Optional)

Now, as an optional step we can extend your barcord scanner app to a diet tracker by exploring on-device storage capabilities of Build Apps.

1. Open <b>Data</b> tab and select <b>CREATE DATA ENTITY</b> under <b>On-Device storage</b>.<br><br>
![start](images/ss1.png)

2. Give a name to the on-device storage enity and click on <b>ADD</b>.<br><br>
![](images/ss2.png)

3. In the newly created Data entity, add a Data Enities to save your data from application.<br> 
Click on <b>ADD NEW DATA ENTITY</b>.<br>
In the Field name enter "<i>food</i>", select <b>ABC text</b> as Field type. <br><br>
![](images/ss3.png)

4. Similarily, Add another data entity and name it as "<i>energy</i>" and select its field type as <b>123 Number</b>.<br><br>
![](images/ss4.png)

5. Click on <b>SAVE</b> and go back to the <b>UI Canvas</b>.<br><br>
![](images/ss5.png)

6. Add a <b>button</b> component to your UI and rename it as "<i>Add to my Diet</i>".
![](images/ss6.png)

7. Open Logic composer for the button. <br>
select the button and tap on the gray bar on the bottom of the screen. <br>
Add <b>Create record</b> logic to composer and connect it with <b>Component tap</b> node.
![](images/ss7.png)

8. Select the <b>Create record</b> node on your composer to open its properties.<br>
By default your on-device data entity will be selected as data source.<br>
Open the <b>binding menu</b> under <b>Record</b> in the properties.<br><br> 
![](images/ss8.png)

9. Select <b> Object with properties</b>.<br><br>
![](images/ss9.png)

10. Now the values need to be binded to the Data entities of your on-device storage. <br>
Open the binding menu and select Formula<br><br>
![](images/ss10.png)

11. Now enter the follwing formula <PRE>data.OpenFoodFacts1.product.brands </PRE> which will save the brand your barcode scanned.<br>click on save.<br><br>
![](images/ss11.png)

12. Similarily, bind the following value for <b>energy</b> data enity using <b>formula</b> binding <pre>data.OpenFoodFacts1.product.nutriments.energy_100g</pre>
Click on save.<br><br>
![](images/ss12.png)

13. Now, Click on <b>SAVE</b><br><br>
![](images/ss13.png)

14. Add a <b> Card</b> component to your UI.<br><br>
![](images/ss14.png)

15. Change the title of the card to "<i> Tap to view your Diet</i>" and bind the content value with the following formula. <pre>SUM_BY_KEY(data.tracker1, "energy")+" KJ"</pre>
![](images/ss15.png)

16. Now we need to create a new page. To create a new page click on the page name on top left.<br><br>
![](images/ss16.png)

17. Click on <b>ADD NEW PAGE</b>.<br><br>
![](images/ss17.png)

18. Call the new page as "<i>diet</i>".<br><br>
![](images/ss18.png)

19. Now open the <b>MARKETPLACE</b> of component library.<br><br>
![](images/ss19.png)

20. Search for "<i>table</i>" and select <b>Basic table with data adapter</b>.<br><BR>
![](images/ss20.png)

21. Open the <b>INSTALLED</b> tab of your component library, and the newly installed <b>Basic table with adapter</b> to your UI Canvas.<br><br>
![](images/ss21.png)

22. In the properties of the table component open the <b>Configure</b> menu under <b>Table resource</b>. <br><br>
![](images/ss22.png)

23. Select your On-device storage entity, i.e., <b>tracker</b>.<br><br>
![](images/ss23.png)

24. Make sure <b>food ,energy</b> data enity fields are selected. <br>
Click on <b>SAVE AND EXIT</b>.<br><br>
![](images/ss24.png)

25. Now, SAVE the changes and go back to the main page.<br><br>
![](images/ss25.png)

26. open the logic composer for your card component, and add a logic <b>Open page</b>. <br>
make sure <b>diet</b> page is selected in the properties of Open page logic node.
![](images/ss26.png)


# Congratulations your barcode scanner is a diet tracker now, preview your app to see how it works!!!