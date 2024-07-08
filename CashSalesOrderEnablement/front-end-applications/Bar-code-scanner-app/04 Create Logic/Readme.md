Previous Step: <a href="https://github.com/SAP-samples/sap-build-apps/blob/main/Workshops/front-end-applications/Bar-code-scanner-app/03%20Create%20a%20Data%20Variable/readme.md"> 03 Create Data Variable</a>

# Create Logic

1. Now select the Button component and then click anywhere on the Grey tab below to add a logic for the button.<br><Br>
![](images/01%20Button%20Logic.png)

2. In the logic component, under Device you can find <b><i>Scan QR/barcode component</b></i>. Drag and drop the <b>QR component</b> to the logic canvas.<br><br>
![](images/2%20Scan%20QR.png)

3. Now connect the nodes.<br><br>
![](images/3%20Connect%20Nodes.png)

4. Now Drag and drop <b><i>Get Record</b></i> logic component.<br><br>
![](images/4%20Get%20Record.png)

5. Connect the <b>Get record</b> and <b>Scan QR/barcode</b> nodes. <br>Now select <b>Get record</b> component and click on <b>ABC</b> icon under Barcode to open the binding menu for the Get record.<br><br>
![](images/5%20Get%20Record%20an.png)

6. Select <b>Output value of another node</b>.<br><br>
![](images/6%20Op%20of%20another.png)

7. Under <i>select logic node</i>, select <b>Scan QR/barcode</b>. <br> 
Under <i>select node output</i>, select <b>Scan QR/barcode / QR barcode content</b>.<br>
Now click on <b>SAVE</b>.<br><br>
![](images/7%20Scan%20QR.png)

8. Now drag and drop <b>Set data variable component</b> to the logic canvas and connect it with <b>Get record</b>  node.<br><br>
![](images/8%20Set%20Data%20Variable.png)

9. Now select the <b>Set data variable</b> component. Click on the <b>{&ensp;}</b> icon under data to open the binding menu for the logic component.<br><br>
![](images/9%20Bind%20Data.png)

10. Select <b>Output value of another node</b>.<br><br>
![](images/10%20OP%20of%20another.png)

11. Under <i>Select logic node</i>, select <b>Get record</b> <br>
Under <i>select node output</i>, select <b>Record</b> <br>
Now click on <b>SAVE</b>.<br><br>
![](images/11%20Get%20Record.png)


Next Step: <a href="https://github.com/SAP-samples/sap-build-apps/blob/main/Workshops/front-end-applications/Bar-code-scanner-app/05%20Add%20New%20Component/Readme.md"> 05 Add New Component</a>







