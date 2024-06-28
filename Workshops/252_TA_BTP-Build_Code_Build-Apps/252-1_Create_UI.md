# Module 2 - Unit 1: Create UI  


1. Create a project

![](./Images/252-1_Screenshot_47.png)

2. Follow: Build an Application > SAP Build Apps > Web & Mobile Application and name your project

**Note**: you can use your initials to name your project. So that it will not be confusing for you if you are using the same lobby with outhers in a common workshop

![](./Images/252-1_Screenshot_48.png)

3. Remove *Text 1* 

![](./Images/252-1_Screenshot_49.png)

4. Rename *Title 1*: Scan & Add Points!

![](./Images/252-1_Screenshot_50.png)

5. Align the text centerally 

![](./Images/252-1_Screenshot_51.png)

6. Select *Page Master Heading* under Style tab

![](./Images/252-1_Screenshot_52.png)

7. Drag & Drop *Image* component above the *Title 1*. Then, click on the image icon under *Source*

![](./Images/252-1_Screenshot_53.png)

8. Save the  *Bonus_Barcode_Logo* below and Drag & Drop it to the box 

![Download the Bonus_Barcode_Logo](./Files/Logo_BonusBarcode.png)

![](./Images/252-1_Screenshot_54.png)

9. Click on *Use Image*

![](./Images/252-1_Screenshot_55.png)

10. Drag & Drop the *Button* component and rename the label: *New Purchase*

![](./Images/252-1_Screenshot_56.png)

11. Increase the *Top gap* to 100px 

![](./Images/252-1_Screenshot_57.png)

12. Open the Logic Canvas from the bottom of the page and Drag & Drop the following logic components component

**Note 1**: Please make sure that the New Purchase *Button* is selected

**Note 2**: You should go to Marketplace and install the *Action sheet* and  *Prompt number* logic components

![](./Images/252-1_Screenshot_58.png)

13. Select *Action sheet* and Click on *Custom list*

![](./Images/252-1_Screenshot_59.png)

14. Add 2 values and fill the input box as follows and save

label: Barcode Scanner 
value: Barcode

label: Manual Input
value: Manual

![](./Images/252-1_Screenshot_60.png)

15. Update the *Action sheet title text*: **How to enter customer ID**

![](./Images/252-1_Screenshot_61.png)

16. Select *If condition* and select the little icon

![](./Images/252-1_Screenshot_62.png)

17. Go to *Formula* and click on the false

![](./Images/252-1_Screenshot_63.png)

18. Type the following formula and save 

<br>

> outputs["Action sheet"].pickedAction.value=="Barcode"

![](./Images/252-1_Screenshot_64.png)

19. Select *Prompt number* component and add the following text under *Dialog title*

<br>

> Enter 7 digit customer ID

![](./Images/252-1_Screenshot_65.png)

20. Click on the Home Page from top left corner and add a new page called as: **New Purchase**

![](./Images/252-1_Screenshot_66.png)

21. Switch to Variables > Go to Page Parameters > Add Parameter > Rename the parameter: **SelectedCustomerNumber** > Save your Project

![](./Images/252-1_Screenshot_67.png)

22. Click on New Purchase from top left corner and go to Home Page

![](./Images/252-1_Screenshot_68.png)

23. Select *Open Page* component and update the Page with *New Purchase*

![](./Images/252-1_Screenshot_69.png)

24. Click on the X under SelectedCustomerNumber > go to Output value of another node

![](./Images/252-1_Screenshot_70.png)

25. Select *ScanQR/barcode* and select QR barcode content and save

![](./Images/252-1_Screenshot_71.png)

26. Select the second *Open Page* component and update the Page with *New Purchase*

![](./Images/252-1_Screenshot_72.png)

27. Click on the X under SelectedCustomerNumber > go to Formula > Create formula

![](./Images/252-1_Screenshot_73.png)

28. Type the following formula and save
<br>

>STRING(outputs["Prompt number"].userInput)

![](./Images/252-1_Screenshot_74.png)

29. Click on the Button component > Go to Layout > Set Width to 200px under Exact Size  

![](./Images/252-1_Screenshot_75.png)

30. Align the button horizontally to the middle

![](./Images/252-1_Screenshot_76.png)

31. Click on the Home Page from top left corner and add a new page called as: **Redeem Points**

![](./Images/252-1_Screenshot_77.png)

32. Switch to Variables > Go to Page Parameters > Add Parameter > Rename the parameter: **SelectedCustomerNumber** > Save your Project

![](./Images/252-1_Screenshot_78.png)

33. Click on Redeem Points from top left corner and go to Home Page

![](./Images/252-1_Screenshot_79.png)

34. Select *New Purchase* button and click on the little duplicate icon

![](./Images/252-1_Screenshot_80.png)

35. Select the duplicated button (the one below) and rename the label: **Redeem Points**

![](./Images/252-1_Screenshot_81.png)

36. Select the Open Page component and replace the page with **Redeem Points** page

![](./Images/252-1_Screenshot_82.png)

37. Select the second Open Page component and replace the page with **Redeem Points** page. Save your project

![](./Images/252-1_Screenshot_83.png)

38. Select Home Page from top left and go to *New Purchase*

![](./Images/252-1_Screenshot_88.png)

39. Remove *Text 1*

![](./Images/252-1_Screenshot_89.png)

40. Select *Title 1*, Rename: **New Purchase** and Align the text centerally

![](./Images/252-1_Screenshot_90.png)

41. Go to Style tab and select **Page Master Heading**

![](./Images/252-1_Screenshot_91.png)

42. Drag & Drop a Container. Rename the display name: **Main Container**

![](./Images/252-1_Screenshot_92.png)

43. Drag & Drop *Title 1* into the Main Container.

**Note**: You can check the Component Tree to see if the Title is now under the Main Container

![](./Images/252-1_Screenshot_93.png)

44. Drag & Drop a Card component inside of the Main Container 

![](./Images/252-1_Screenshot_94.png)

45. Drag & Drop another container under Card 1 but inside of the Main Container. 

**Note**: You can check the Component Tree to see if the Container 1 is now under the Main Container or not

![](./Images/252-1_Screenshot_95.png)


46. Select Container 1 and change the layout of the component to Horizontal

![](./Images/252-1_Screenshot_96.png)

47. Drag & Drop a Card component inside Container 1

**Note**: You can check the Component Tree to see if the Card 2 is now under the Container 1 or not

![](./Images/252-1_Screenshot_97.png)

48. Duplicate the Card 2 component twice until you have 3 horizontal card components


![](./Images/252-1_Screenshot_98.png)

49. Compare the Component Tree in your page with the screenshot below. Please make sure that you have the same layout

![](./Images/252-1_Screenshot_99.png)

50. Select Card 1. Rename the title: *Customer Number* Rename the content: *Customer Name*

![](./Images/252-1_Screenshot_100.png)

51. Select Card 2. Rename the content: *Available Reward Points*


![](./Images/252-1_Screenshot_101.png)

52. Select Card 3. Rename the content: *Total Redeemed Points*


![](./Images/252-1_Screenshot_102.png)


53. Select Card 4. Rename the content: *Total Purchase Value*

![](./Images/252-1_Screenshot_103.png)

54. Select the Main Container. Then, use keyboard shortcut to copy the container: **CRTL+C**.

**Note**: Make sure that you have the pop up that shows you successfully copied the component to the clipboard

![](./Images/252-1_Screenshot_104.png)

55. Go to the Page: Redeem Points

![](./Images/252-1_Screenshot_105.png)

56. Click into the middle of the page. Then, use keyboard shortcut to paste the container: **CRTL+V**.

![](./Images/252-1_Screenshot_106.png)

57. Remove *Title 1*. Remove *Text 1*. Save your project

![](./Images/252-1_Screenshot_107.png)

58. Select *Title 1* inside of the Main Container. Rename the content: *Redeem Points**

![](./Images/252-1_Screenshot_108.png)


**[Next Module 2 - Unit 3: Authentication and Data Integration](./252-3_Authentication_and_Data_Integration.md) >**



