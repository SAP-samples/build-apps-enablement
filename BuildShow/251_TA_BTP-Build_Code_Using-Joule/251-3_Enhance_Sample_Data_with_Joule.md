**[Previous Module 1 - Unit 2: Create Data Entities with Joule](./251-2_Create_Data_Entities_with_Joule.md) >**

# Module 1 - Unit 3: Enhance Sample Data with Joule  

Joule created the Data Model and Services, now we will use Joule once again to enhance the sample data.


## Enhance Sample Data

Here is video tutorial for this unit : <a href="https://video.sap.com/media/t/1_kcyk0aea">Enhance Sample Data with Joule  
</a>

1. Open the the Sample Data editor in the Storyboard by selecting **Open Editor** -> **Sample Data**

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/c3cae943-c050-4835-b390-fd390e838ce8)



2. Select **Customers** data entity. Add 5 rows to the entity and push **Add** button

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/44496935-bd41-4cd2-b0e5-ae26d9792c19)



3. Click **Enhance**. This will reopen Joule to modify the sample data. Then, use the following Prompt in Joule:

```code
Enhance my sample data with meaningful data. Any phone numbers must be 10 digits. All customer numbers must be 7 digits and one customer must use the customer number 1200547. No fields may be empty. Total purchase value must be smaller than 10000 und unround. Total reward points and total redeemed reward points both must be unround and different and always sum to one-tenth of the total purchase value for each customer.
```

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/7288a865-16b8-4ed5-aa25-6fe9986dea4d)

 
4. You can see the customer names, email adresses and purchases are created. Accept the new Sample Data created by Joule. 

<i>Feel free to play with Joule to get meaningful names. Use prompts like "suggest me realnames" or "Let the names include marvel heros or DC heros if you are a fan of dark knight"</i>

5. Verify in the customer list that one customerNumber was changed to **1200547**, if not change one customer number manually to **1200547**. <br>
![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/b61bb2b0-30cb-405a-9c10-cb4093337a46)

**This step is needed for the demo purpose. Later in the exercise, we will be scanning a Customer Loyalty Card that will have a barcode with this number.**

Hint: If the data is not correct, regenerate Joule once again / correct the data manually.

NOTE : In case of any technical issues please import the Sample data from here:  [customer_loyal_aparna_Customers.csv](https://github.com/user-attachments/files/16173522/customer_loyal_aparna_Customers.csv)

6. Let's continue with sample data for the Purchases. Select the **Purchases** data entity. Add 10 rows to the entity and push **Add** button

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/569dbac3-db35-47b8-9533-b4af06909e00)


7. Click **Enhance**. Then, use the following prompt in Joule:

```code
Enhance my sample data with meaningful data. Purchase value must be between 50 and 1000. Reward points is always one-tenth of the purchase value.
```

8. Accept the Sample Data created by Joule.
![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/7d29b441-38a0-4541-8426-4987c5414ca0)

Hint: If the data is not correct, regenerate Joule once again / correct the data manually.

NOTE : In case of any techical issues, please import the Sample data from here:  [customer_loyal_aparna_Purchases.csv](https://github.com/user-attachments/files/16174118/customer_loyal_aparna_Purchases.csv)



9. Select Redemptions data entity. Add 5 rows to the entity and push **Add** button


10. Click **Enhance**. Then, use the following prompt in Joule:

```code
Ensure that each redeemed amount is arbitrary and between 10 and 100.
```

![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/c6837ef4-e618-401c-886b-7a9fddaef7d8)


11. Accept the changes proposed by Joule. 
![image](https://github.com/SAP-samples/build-apps-enablement/assets/173163567/2f835549-63a6-4eca-ac0f-e64888beebeb)

Hint: If the data is not correct, regenerate Joule once again / correct the data manually.

NOTE : In case of any technical issues please import the Sample data from here:    [customer_loyal_aparna_Redemptions.csv](https://github.com/user-attachments/files/16174127/customer_loyal_aparna_Redemptions.csv)


**[Next Module 1 - Unit 4: Create Backend Logic with Joule](./251-4_Create_Backend_Logic_with_Joule.md) >**
