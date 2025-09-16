# Exercise 2: Run the Joule Booster

In this exercise, you will learn how to run the Joule Booster to install Joule into a Subaccount. After completing these steps you will have a Subaccount with Joule installed.

## <a name="step1"></a>Step 1: Start the Booster

To begin, we need to launch the Joule Booster from the BTP Global Account.  
Navigate to the BTP Global Account Level to access the Joule Booster:


1. Navigate to Global Account Level > Boosters.
  <br>![](/exercises/ex2/images/07_01_joule_booster.png)
  
2. Search for "Joule" in the search field.
3. Select the Booster "Setting up Joule" and click "Start".
   <br>![](/exercises/ex2/images/07_02_joule_booster.png)

## <a name="step2"></a>Step 2: Check Prerequisites
The booster will automatically check if all prerequisites are met:
1. The system will verify:
   - Checking Authorizations: DONE
   - Checking Entitlements: DONE  
   - Checking Identity Authentication Tenant: DONE
     <br>![](/exercises/ex2/images/07_03_joule_booster.png)
     
2. Once all prerequisites show as "DONE", click "Next" to proceed.

## <a name="step3"></a>Step 3: Set Up Subaccount

Configure the subaccount settings for the Joule installation:

1. In the "Set Up Subaccount" step, verify the following settings:
   - Service: das-application
   - Plan: Select "standard" from the dropdown
   - Subaccount: Select your previously created subaccount (AI164-XXX)
   - Org: The organization name will be auto-populated
   - Space: Leave as "dev"
     <br>![](/exercises/ex2/images/07_04_joule_booster.png)
2. Click "Next" to continue.


## <a name="step4"></a>Step 4: Select Integrations

Choose the integration settings for Joule:
1. In the "Select Integrations" step:
   - Products: No selection needed for this exercise
   - This integration is used for: Select "Production" (this should be pre-selected)
     <br>![](/exercises/ex2/images/07_05_joule_booster.png)

2. Click "Next" to proceed.

## <a name="step5"></a>Step 5: Select Capabilities

Configure the capabilities for your Joule installation:

1. You don't need to select anything in this step. Simply click "Next" to continue.

<br>![](/exercises/ex2/images/07_06_joule_booster.png)

## <a name="step6"></a>Step 6: Set Up Integrations

Complete the integration setup:

1. In the "Set Up Integrations" step:
   - Formation Name: This will be set up automatically
   - Identity Authentication System: This will be configured automatically
  
     
2. The system will automatically configure these settings. Click "Next" to proceed to the final review.
   <br>![](/exercises/ex2/images/07_07_joule_booster.png)

## <a name="step7"></a>Step 7: Review and Execute

Review all settings and execute the booster:

1. Review all the configuration settings you've made in the previous steps.
2. Verify that all settings are correct for your subaccount.
3. Click "Finish" to start the Joule installation process.

The booster will now provision Joule in your subaccount. This process may take several minutes to complete. Wait for the success confirmation message indicating that Joule has been successfully installed.

<br>![](/exercises/ex2/images/07_08_joule_booster.png)

Wait for the success confirmation message indicating that Joule has been successfully installed.

<br>![](/exercises/ex2/images/07_09_joule_booster.png)


## <a name="summary"></a>Summary

You have successfully run the Joule Booster and installed Joule into your subaccount. The booster has configured all necessary services, created the required space, and set up Joule for use. You can now access Joule through your BTP subaccount and begin exploring its AI capabilities.

Now that you have created the instance of the Joule Service, you are ready to go ahead to start the setup of Document Grounding in Exercise 3.
Continue to - [Exercise 3 - Setup Document Grounding](../ex3/README.md)
