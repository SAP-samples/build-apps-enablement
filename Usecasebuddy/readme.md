# UCB- Build Apps


# Details page (sub category). 

In the Details Page, basic information of the use case is collected, like Name, description, LoB and more. App variable has been used to collect this information. <br><br>
![](images/Detailspage.png)

# Adding More Options to the "Line of Business" List

To add the more options in the list for <b><i>Line of Business</b></i>, open and binding menu for the <b>Option list</b> and add the options.

![](images/loblist.png)

# Progress bar

A progress bar has been used in the app, to let the users track the progress of the questionnare using an app variable <i>completion</i> value.

![](images/progressbar.png)

Using <i>Set app variable</i> to assign value to progress bar, in every page to hardcode the progress based on the number of pages used.

![](images/bindingvalueforprgressnar.png)


# Creating question containers. 


Each question container will have a Title component and an Answer component. <br>
The questions are static, and can be changed in the properties of the component<br><br> 
![](images/questionbox.png)

The Answer component will have a text component and a slider component, and have page variables answer and question binded to text and slider components respectively.<br><br>
![](images/answerbox.png)

The slider have 5 values and text component will display dynamic values based on the slider value with logic created on the page level.

![](images/sliderlogic.png)

The answer page variable is binded with a formula to check the slider value and show the respective option accordingly. 
for example
<pre>IF(pageVars.question1==1, "1 Data source", IF(pageVars.question1==2, "2 Data sources", IF(pageVars.question1==3, "3 Data sources", IF(pageVars.question1==4, "4 Data sources", IF(pageVars.question1==5, "not sure about the number of data resources","")))))</pre>

A delay with 1 ms is used to make sure the value in answer page variable is updated immediately when the slider value is changed. 



