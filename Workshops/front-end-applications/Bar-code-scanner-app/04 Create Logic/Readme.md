Previous Step: <a href="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/03%20Create%20a%20Data%20Variable/readme.md"> 03 Create Data Variable</a>

# Create Logic

1. Now select the Button component and then click anywhere on the Grey tab below to add a logic for the button.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/01%20Button%20Logic.png" alt="button logic">

2. In the logic component, under Device you can find <b><i>Scan QR/barcode component</b></i>. Drag and drop the <b>QR component</b> to the logic canvas.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/2%20Scan%20QR.png" alt="QR logic">

3. Now connect the nodes.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/3%20Connect%20Nodes.png" alt="node connect">

4. Now Drag and drop <b><i>Get Record</b></i> logic component.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/4%20Get%20Record.png" alt="Get record">

5. Connect the <b>Get record</b> and <b>Scan QR/barcode</b> nodes. Now select <b>Get record</b> component. Click on <b>ABC</b> icon under Barcode to open the binding menu for the Get record.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/5%20Get%20Record%20an.png" alt="Get recor">

6. Select <b>Output value of another node</b>.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/6%20Op%20of%20another.png" alt="output of another node">

7. Under <i>select logic node</i>, select <b>Scan QR/barcode</b>. <br> 
Under <i>select node output</i>, select <b>Scan QR/barcode / QR barcode content</b>.<br>
Now click on <b>SAVE</b>.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/7%20Scan%20QR.png" alt="Value">

8. Now drag and drop <b>Set data variable component</b> to the logic canvas and connect it with <b>Get record</b>  node.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/8%20Set%20Data%20Variable.png" alt="set data">

9. Now select the <b>Set data variable</b> component. Click on the <b>{&ensp;}</b> icon under data to open the binding menu for the logic component.
 <img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/9%20Bind%20Data.png" alt="set data variable">

10. Select <b>Output value of another node</b>.
 <img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/10%20OP%20of%20another.png" alt="output value">

11. Under <i>Select logic node</i>, select <b>Get record</b> <br>
Under <i>select node output</i>, select <b>Record</b> <br>
Now click on <b>SAVE</b>.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/11%20Get%20Record.png" alt="Get record">



Next Step: <a href="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/tree/main/05%20Add%20New%20Component"> 05 Add New Component</a>







