

This tutorial is to Add Product to cart


# Pre-requisites

- [Place holder for S4/Hana Setup]
- [Placeholder for destination setup in the BTP cockpit]
- Create the following Page Variable <b>Item</b> as <b>object</b> type and add the following variables under it.
[Place holder for creating variables]<br><br>
  <table>
  <tr>
    <th>Variable Name</th>
    <th>Variable type</th>
    <th>Object variable</th>
    
  </tr>
  <tr>
    <td>ChosenProduct</td>
    <td>text</td>
    <td>x</td>
  </tr>
  <tr>
    <td>CurrentItemIndex</td>
    <td>number</td>
    <td>x</td>
  </tr>
<tr>
    <td>InputProduct</td>
    <td>text</td>
    <td>x</td>
  </tr>
  <tr>
    <td>ItemCount</td>
    <td>number</td>
    <td>x</td>
  </tr>
<tr>
    <td>ItemPrice</td>
    <td>object</td>
    <td>NetPrice<br>TaxAmount</td>
    <td>text<br>text</td>
  </tr>
<tr>
    <td>ProductName</td>
    <td>text</td>
    <td>x</td>
</tr>
<tr>
    <td>Quantity</td>
    <td>text</td>
    <td>x</td>
</tr>
</table>
<br><br>

![](images/Screenshot%202024-01-21%20at%2016.18.07.png)
<br><br><br>

- Check the app variable <b>CurrentUserSettings</b> as <b>object</b> data type.

<table>
  <tr>
    <th>Variable Name</th>
    <th>Variable type</th>
    
    
  </tr>
  <tr>
    <td>CashAccount</td>
    <td>text</td>
    
  </tr>
  <tr>
    <td>CashPaymentTerms</td>
    <td>text</td>
    
  </tr>
<tr>
    <td>CreditPaymentTerms</td>
    <td>text</td>
    
  </tr>
  <tr>
    <td>Currency</td>
    <td>text</td>
   
  </tr>
<tr>
    <td>DistributionChannel</td>
    <td>text</td>
 
  </tr>
<tr>
    <td>Division</td>
    <td>text</td>
    
</tr>
<tr>
    <td>DocumentType</td>
    <td>text</td>
</tr>
<tr>
    <td>OneTimeCustomer</td>
    <td>text</td>
</tr>
<tr>
    <td>SalesGroup</td>
    <td>text</td>
</tr>
<tr>
    <td>SalesOffice</td>
    <td>text</td>
</tr>
<tr>
    <td>SalesOrganization</td>
    <td>text</td>
</tr>
<tr>
    <td>UserEmail</td>
    <td>text</td>
</tr>
<tr>
    <td>id</td>
    <td>text</td>
</tr>

</table>

![](images/Screenshot%202024-01-21%20at%2016.20.15.png)

Create an On-device data entity and name it as <b>MaterialList</b>
![](images/Screenshot%202024-01-21%20at%2016.56.35.png)
- Add the following <b>text</b> fields in the MaterialList
   <b><i>id, EAN Product, SalesOrg and ProductDescription</b></i><br><br>
   ![](images/Screenshot%202024-01-21%20at%2017.02.51.png)

- Create a data variable and rename it to <b>Material_List</b> and clear the logic for the data variable.
![](images/Screenshot%202024-01-21%20at%2017.04.41.png)


Similariy create OrderItem and ItemVariable On-device Data entity.
For OrderItem create the following fields. 

<table>
  <tr>
    <th>Field Name</th>
    <th>Field type</th>
    
    
  </tr>
  <tr>
    <td>ID</td>
    <td>text</td>
    
  </tr>
  <tr>
    <td>Quantity</td>
    <td>text</td>
    
  </tr>
<tr>
    <td>Currency</td>
    <td>text</td>
    
  </tr>
  <tr>
    <td>TaxValue</td>
    <td>number</td>
   
  </tr>
<tr>
    <td>ProductID</td>
    <td>text</td>
 
  </tr>
<tr>
    <td>NetAmount</td>
    <td>text</td>
    
</tr>
<tr>
    <td>TaxAmount</td>
    <td>text</td>
</tr>
<tr>
    <td>ItemNumber</td>
    <td>number</td>
</tr>
<tr>
    <td>ProductName</td>
    <td>text</td>
</tr>
<tr>
    <td>GrossAmount</td>
    <td>text</td>
</tr>
<tr>
    <td>UnitOfMeasure</td>
    <td>text</td>
</tr>
<tr>
    <td>NetAmountValue</td>
    <td>number</td>
</tr>
</table>



<br><br>

# Enterting Product Name
After finding the searching the product from the SAP S4 Hana system, it needs to be added to the cart. 
The logic can be created to the <b>button</b>.<br><br>
![](images/Screenshot%202024-01-21%20at%2013.06.21.png)

By default a component tab is available which will trigger the following flow. 

1. Use an <b>If condition</b> logic component.<br><br>
![](images/Screenshot%202024-01-21%20at%2013.10.59.png)

2. Bind the following formula to the If condition. <br><pre>!IS_EMPTY(pageVars.Item.ChosenProduct)</pre>
![](images/Screenshot%202024-01-21%20at%2013.14.44.png)


3. Drag and drop a <b>Get Record</b> logic component and connect it with first node of the <b>If condition</b> component.
<br><br>
![](images/Screenshot%202024-01-21%20at%2016.05.46.png)

4. Now to bind the values, under the property of Get Record component, 
 - Select the data entity with the Product Description. (in this case its <b><i>A_ProductDescription</b></i>)
 - Open the binding open for the product, select <i>Data and Variables</i>-><i>Page Variable</i> and  select the page variable <b><i>Item.Chosen.Product</i></b>
 - Open the binding menu for the language and select <i>Static Text</i>. Now Enter <B><i>EN</b></i> in there. <br><br>
 ![](images/Screenshot%202024-01-21%20at%2016.10.04.png)<br><br>
 Additionally, An <b>Alert</b> component can be used to notify if the entered product is not a valid product. Drag and drop an <b>Alert</b> component from the library and connect it with the second node of the <i>If condition</i>. <br><br>
![](images/Screenshot%202024-01-21%20at%2016.36.52.png)

5. Drag and drop a <b> Set page variable</b> component and connect it with the first node of the Get record component. 
- select the variable <i><b>Item.ProductName</i></b>. 
- For the Assigned value, open the binding menu, select <b><i>Output value of another node</b></i> -> select <b><i>Get record</b></i> -> under the node output select <b><i>ProductDescription</b></i><br><br>
![](images/Screenshot%202024-01-21%20at%2016.44.56.png)<br><br>
Additionally, A toast component can be used  to know if there any error while retrieving the data from the <b><i>A_ProductDescription entity</b></i>, Drag and drop a <b>Toast</b> component from the library and connect it with the second node of the of the Get Record component. 
- And to bind the toast message, select  <b><i>Output value of another node</b></i> -> select <b><i>Get record</b></i>-> under the node output select <b><i>Error</b></i>. Now the there will be a toast with the error message if it fails to connect with the productdescription entity. 

