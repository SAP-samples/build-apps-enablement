**[Previous Module 1 - Unit 3: Enhance Sample Data with Joule](./251-3_Enhance_Sample_Data_with_Joule.md) >**

# Module 1 - Unit 4: Create Backend Logic with Joule  

We already have created the entities, services, and sample data with Joule. Now we want to create some logic for our app. We would like to calculate the bonus points automatically when a customer makes a purchase. Additionally, we want to provide logic for customers to redeem these bonus points.


## Backend Logic

Here is a video tutorial for this unit: <a href="https://video.sap.com/media/t/1_ytxjgh48">Create Backend Logic with Joule</a>

1. Go to Storyboard. Click on one of the entities under Services and Open in Graphical Modeler

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/b2db1043-2517-49f8-a0ad-9b27b5286d7a)



2. Select Purchases entity by clicking on the title. Then, click on Add Logic.
   Note: if you can not see the Purchases entity you may have to zoom out the view.

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/f75ceece-5d65-4b82-b14b-17d0946728f6)


3. Leave the default value and click on **Add**
![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/7dec475e-0cc0-4e4d-9a38-563c569111df)


4. Under the **Standard Event** select **Create**. That means this logic will be automatically executed if a new purchase is done.
 Afterwards, go to **Application Logic** under **Open Code Editor**. This will open Joule again to create the logic for us.

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/aa1bbf4f-0205-4829-9cdd-c8b1f7586249)


5. Use the following prompt in Joule to create a backend logic:

```code
Reward points of each purchase will be the one tenth of the purchase value. Each purchase value will be added to the total purchase value of the related customer. Each reward points will be added to the total reward points of the related customer.
```
![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/13214108-5629-4ea6-b5b8-a89f2db5bcf3)


So Joule created now following logic:
 - Check if the customer exists
 - calculates the rewardPoints from the purchase value
 - updates the total purchase value and the total reward points in the customers entity

6. Accept the code created by Joule. 

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/ff1b9a4e-4d90-4ac8-b5de-4273018a7923)



> **Note:**
> Joule typically generates different code each time for the same prompt. So if yours differs, it is completely fine as long as it does the same job. If there are no obvious errors, just keep working on the exercise. If you are unsure, you can have Joule try again by clicking **Regenerate**.  

7. Now let's look at the Redemptions. Go to back service.cds tab. Select Redemptions entity by clicking on the title. Then, click on Add Logic

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/234c0fae-2810-4ce2-a5d5-80da83dac2ff)


8. Click on **Add**

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/e5c640d8-4e09-4877-87a7-a1ff504b21df)


9. Select **Create**. Then, choose **Application Logic** under **Open Code Editor**.

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/128633a9-12f0-4746-a149-7048d0257e4e)
![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/34d93f5f-d3ad-481c-aaed-da98d3914f8a)



10. Use the following Prompt in Joule to create a backend logic:

```code
Deduct the redemption amount from the customer's total reward points and add that to his total redeemed points.
```

![](./Images/251-4_Screenshot_34.png)

11. Accept the code created by Joule. 

![](./Images/251-4_Screenshot_35.png)

Have a closer look at the generate code. It even includes some checks if the customer has enough points for the redemption.


> **Note:**
> Joule might generate different codes for the same prompt. So, you might have a different code for the backend logic which is completely fine if it does the same job. You can ignore this and keep working on the exercise.  

12. Go back to Storyboard and open Service Center

![](./Images/251-4_Screenshot_36.png)


**[Next Module 1 - Unit 5: Add External Data Resource](./251-5_Add_External_Data_Resource.md) >**
