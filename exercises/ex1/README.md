# Exercise 1: Prepare the BTP Subaccount

In this exercise, you will learn how to prepare a Subaccount to subsequently setup Joule and Document Grounding. After completing these steps you will have a Subaccount with all the needed entitlements, you established trust to a IAS tenant and are ready to execute the Joule Booster.

## <a name="step1"></a>Step 1: Log in to BTP

For the live exercise at TechEd 2025, we provide a BTP Landscape to try on. The first step is to successfully log in via the custom platform IDP following this link:

https://emea.cockpit.btp.cloud.sap/cockpit/?idp=a8hrq53ve.accounts.ondemand.com#/globalaccount/fd5a03c5-21bc-4ed2-ba61-62e521144b11

When first logging in you will be redirected to a IAS login screen similar to this:

1. Log in using the username and password provided in the workshop room.

<br>![](/exercises/ex1/images/ias_login.png)

2. You will be redirected successfully to the BTP Global Account

<br>![](/exercises/ex1/images/01_btp_overview.png)


## <a name="step2"></a>Step 2: Create a Subaccount

Next up, we want to create a Subaccount. For that on the Global Account > Account Explorer:

1. Click Create.  
   Click the blue create button and subsequently choose "Subaccount".  
   <br>![](/exercises/ex1/images/02_01_btp_subaccount_create_detail.png)

2. In the Subaccount Create modal:  
   - Enter a name for your Subaccount. Please follow the naming convention AI164-XXX, where XXX is your code used to log in.  
   - Select the Data Center: Europe (Frankfurt) - AWS 
   - Click Create.  
   <br>![](/exercises/ex1/images/02_02_btp_subaccount_create_detail.png)

This will take a few seconds and you will be prompted once done.


## <a name="step3"></a>Step 3: Assign Entitlements to your Subaccount

Next up, we want to assign the Entitlement for Joule and Document Grounding to the newly created Subaccount. We can do that by:

1. Navigate to Global Account Level > Entitlements > Entity Assignments.
    Click on "Entity Assignments".  
   <br>![](/exercises/ex1/images/05_01_btp_subaccount_entity_assignements.png)


2. Use the center selection menu titled "Subaccount/Directories" to enter into the Subaccount selection context menu.
   <br>![](/exercises/ex1/images/05_02_btp_subaccount_entity_assignements.png)

3. In the context menu enter your Subaccount name "AI164-XXX" into the search to select your subaccount by selecting it via the checkbox.
   <br>![](/exercises/ex1/images/05_03_btp_subaccount_entity_assignements.png)

4. In the overview of the entitlements for your specific Subaccount, click "Edit".
   <br>![](/exercises/ex1/images/05_05_btp_subaccount_entity_assignements.png)

5. Click "Add Service Plan".
   <br>![](/exercises/ex1/images/05_06_btp_subaccount_entity_assignements.png)

6. It will open a context menu,In the context menu to add services and their service plans:  
   - Search for "Joule".  
   - Select the service "Joule".  
   - Mark the checkbox for the available "standard (Application)" plan.
     <br>![](/exercises/ex1/images/05_07_btp_subaccount_entity_assignements.png)

7. Now repeat the process for "Document Grounding":  
   - Search for "Document Grounding".  
   - Select the service "Document Grounding".  
   - Mark the checkbox for the available "data-manager" plan.  
   - Click "Add 2 Service Plans" to exit the menu
     <br>![](/exercises/ex1/images/05_08_btp_subaccount_entity_assignements.png)

8. Click "Save" and wait for the changes to be saved. This may take over 30 seconds.
   <br>![](/exercises/ex1/images/05_09_btp_subaccount_entity_assignements.png)
   

## <a name="step4"></a>Step 4: Establish Trust to the Custom Application IAS Tenant

Now we will go ahead navigate to our newly created Subaccount via the Account Explorer. 

1. In the Subaccount, select the left menu item Trust Configuration.
   <br>![](/exercises/ex1/images/06_01_btp_trust_config.png)

2. Click "Establish Trust" in the top right corner.  
   - You will be prompted with a list of selectable IAS tenants.  
   - Filter for "a8hrq53ve" and select the one that appears.  
   - Click "Next".
     <br>![](/exercises/ex1/images/06_02_btp_trust_config.png)

3. Leave all settings as is and click "Next".
   <br>![](/exercises/ex1/images/06_03_btp_trust_config.png)

4. Validate the details and click "Next".
   <br>![](/exercises/ex1/images/06_04_btp_trust_config.png)

5. Click "Finish" to complete the process.
   <br>![](/exercises/ex1/images/06_05_btp_trust_config.png)

**Note:** Joule needs to integrate seamlessly with other SAP solutions, which requires a consistent and unified user login experience between the hosting application and the embedded Joule interface. This is where establishing trust with a custom IAS tenant becomes essential. By connecting Joule to that IAS as the identity provider, all user logins are handled centrally, allowing Joule to recognize the authenticated user. This setup is crucial because Joule operates on behalf of the user, and its backend access must align with the user’s roles and authorizations. For this exercise we provide the IAS tenant to select - in your own landscape you would choose the IAS tenant your SAP cloud applications are connected to.

## <a name="summary"></a>Summary

Now that you have a Subaccount with the Joule and Document Grounding Entitlement - successfully trusted the custom IAS and are ready to run the Joule Booster in Exercise 2.  
Continue to - [Exercise 2 - Run the Joule Booster](../ex2/README.md)
