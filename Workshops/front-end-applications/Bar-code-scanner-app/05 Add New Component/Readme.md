Previous Step : <a href="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/Readme.md"> 04 Create Logic</a>

# Add New Component

1. Drag and drop <b>Title component</b> to UI canvas and change the content to “<b><i>Product Information</b></i>”.
  
  <img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/05%20Add%20New%20Component/1%20New%20Component.png" alt=" Title component">

2. Drag and drop a <b>Text component</b> to UI canvas and click on <b>ABC</b> icon to open the Binding menu
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/05%20Add%20New%20Component/2.Formula.png" alt="text comp">

3. Select <b>Formula</b>.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/05%20Add%20New%20Component/3.%20Formula.png" alt="formula">

4. Open formula editor.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/05%20Add%20New%20Component/4.%20Formula%20Editor.png" alt="formula editor">

5. Clear the formula editor now select <b>Data Variable</b>. A list of available data variables will be displayed, now select <i><b>data.OpenFoodFacts1</i></b> and click on the <b>Enter+</b> icon.  
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/Screenshot%202022-09-13%20at%2016.11.38.png?raw=true" alt="datavarform">

6. Now a list of values available under <b>data.OpenFoodFacts1</b> appears. Now select <b>data.OpenFoodFacts1.product</b> and click on the <b>Enter+</b> icon to include it in the formula.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/Screenshot%202022-09-13%20at%2016.12.56.png?raw=true" alt="datavarform">

7. A big list of values under <b>data.OpenFoodFacts1.product</b> will be shown. Scroll down to <b>data.OpenFoodFacts1.product.nutriments</b> and click on the <b>Enter+</b> icon to include it in the formula. If you are not able to find it, type ``` .nutriments``` after <b>data.OpenFoodFacts1.product</b> in the formula editor.
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/replace.png?raw=true" alt="datavarform">

8. Under <b>data.OpenFoodFacts1.product.nutriments</b>, a big list of values will be displayed. Here you can select what value you want your app to show. To display the energy per 100g select <b>data.OpenFoodFacts1.product.nutriments.energy_100g</b> and click on the <b>Enter+</b>. 

<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/04%20Create%20Logic/images/Screenshot%202022-09-13%20at%2016.14.57.png?raw=true" alt="datavarform">



9.{Optional} Or you can simply enter this formula : <pre> "Energy(kJ per 100g) : "+data.OpenFoodFacts1.product.nutriments.energy_100g
</pre>

&emsp;&emsp;click on Save
<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/01%20App%20Interface/images/Screenshot%202022-09-14%20at%2012.20.47.png" alt="enter formula">

10. Click on <b>Save</b> to save the changes made to the application.

<img src="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/01%20App%20Interface/images/Screenshot%202022-09-14%20at%2012.23.03.png" alt="Save">

Now it's time to see how your app works!!

Next Step: <a href="https://github.com/KanishkaRaghuraman/Bar-Code-Scanner-App/blob/main/06%20Preview%20the%20App/Readme.md"> 06 Preview App</a>.
