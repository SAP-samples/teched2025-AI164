# Excercise 3: Setup Document Grounding

In this exercise, you will learn how to setup the Grounding Service and the data repository integration. Once this steps are completed, you can ingest your content and start testing Joule.


## Step 1: Create Destination

Navigate to the BTP Subaccount Account Level.

Navigate to **Global Subaccount Level > Destinations**.

1. Create a new destination.
<br>![](/exercises/ex3/images/08_01_destination_creation.png)

2. Create a new destination from a file.
<br>![](/exercises/ex3/images/08_02_destination_creation.png)

3. Select the **sharepoint_destination.json** from your local folder and create the destination.
<br>![](/exercises/ex3/images/08_03_destination_creation.png)

4. The destination needs to be populated with the following fields: Name, URL, Client ID, Client Secret, Token Service URL.
<br>![](/exercises/ex3/images/08_04_destination_creation.png)

## Step 2: Create Document Grounding Service

Next, we want to subscribe to the Document Grounding Service and create a service key. We can do that by following these steps:

1. Navigate to **Global Subaccount Level > Instances and Subscriptions** and create a new instance.

<br>![](/exercises/ex3/images/13_01_btp_service_creation.png)

2. Select the Document Grounding Service. The plan data-manager is auto-selected. For the name, we use "documentgrounding". Please make note of this as we will be using it later. 
<br>![](/exercises/ex3/images/13_02_btp_service_creation.png)

3. Clickt "Next" on the parameters section.
<br>![](/exercises/ex3/images/13_03_btp_service_creation.png)

4. Create the service instance.
<br>![](/exercises/ex3/images/13_04_btp_service_creation.png)

5. Now we need to create the service key. Click on the three dots on the instance and select "Create Service Binding".
<br>![](/exercises/ex3/images/13_05_btp_service_creation.png)

6. Give a name to the key (here: "key") and create the binding.
<br>![](/exercises/ex3/images/13_07_btp_service_creation.png)

7. Once the key is created, we need to click on the three dots again to download the key.
<br>![](/exercises/ex3/images/13_08_btp_service_creation.png)

9. As part of the next step, we need to create a new subscription to the SAP Cloud Identity Services. Click on "Create" and select "Cloud Identity Services" with the application plan. For the name, we go with "documentgroundingcis".
<br>![](/exercises/ex3/images/13_09_btp_service_creation.png)

10. In the parameters section, enter the following values, where we put in the name of the Document Grounding service instance ("documentgrounding") from the second step of this exercise. Then, click on "create".
<br>![](/exercises/ex3/images/13_10_btp_service_creation.png)

11. Again, we need to create a service key for the Cloud Identity Services subscription. Select the three dots and then "Create Service Binding".
<br>![](/exercises/ex3/images/13_12_btp_service_creation.png)

12. Choose a name for the key (here: "key") and specify the followig parameters in JSON format:
```   
{
    "credential-type": "X509_GENERATED",
    "validity": 365,
    "validity-type": "DAYS"
}
```
<br>![](/exercises/ex3/images/13_13_btp_service_creation.png)

13. Click on the "documentgroundingcis" instance and download the service key.
<br>![](/exercises/ex3/images/13_14_btp_service_creation.png)

14. Make sure that the key has a clientid and a certificate and start the download.
<br>![](/exercises/ex3/images/13_15_btp_service_creation.png)




## Step 3: Prepare Key and Certificate File

In this step, we will use Visual Studio Code to make changes on the certificate file so that we can properly use it inside Bruno in Step 5.

1. Open the folder with the service keys in VS Code
<br>![](/exercises/ex3/images/10_01_pipeline_creation.png)

2. Open the ***document_grounding_cis_key.json***. Then, Copy the value after the "url" key.
<br>![](/exercises/ex3/images/10_02_pipeline_creation.png)

3, Create a new file ***document_grounding.key*** and paste the value from the previous picture.
<br>![](/exercises/ex3/images/10_03_pipeline_creation.png)

4. Type ***STR+F*** and replace the "/n" value with a line break.
<br>![](/exercises/ex3/images/10_04_pipeline_creation.png)

5. This is how the key file should look in the end. 
<br>![](/exercises/ex3/images/10_05_pipeline_creation.png)
6. Now we repeat the same process for the cert file: Copy the value from the JSON into a .crt file, replace the newline characters with actual newlines and hit save.

<br>![](/exercises/ex3/images/10_06_pipeline_creation.png)

7. And this is what the end result should look like: A key file and a cert file.
<br>![](/exercises/ex3/images/10_07_pipeline_creation.png)



## Step 4: Setup Bruno

In this step we will use Bruno to import the role collection for the Data Ingestion API.

1. Select the three dots next to the Bruno icon on the left side of the screen. Click on ***Import Collection***. 
<br>![](/exercises/ex3/images/11_01_bruno_setup.png)

2. Choose ***Bruno Collection*** and select the file ***dg_collection.json*** from your local folder.
<br>![](/exercises/ex3/images/11_02_bruno_setup.png)

## Step 5: Execute API Calls

Now, we will use the collection in Bruno to create the the pipelines for the data ingestion.

These pictures still need to be cut and pointers on

1. Select the three dots next to the name of the API collection ("DocumentGrounding) and click on ***Settings***.
<br>![](/exercises/ex3/images/12_01_01_bruno_api.png)

2. Go to the ***Client Certificates*** section. 
<br>![](/exercises/ex3/images/12_02_bruno_api.png)

3. 
<br>![](/exercises/ex3/images/12_03_bruno_api.png)
<br>![](/exercises/ex3/images/12_01_bruno_api.png)

<br>![](/exercises/ex3/images/12_05_bruno_api.png)
<br>![](/exercises/ex3/images/12_06_bruno_api.png)
<br>![](/exercises/ex3/images/12_07_bruno_api.png)



## Summary

Now that you have created the instance of the Joule Service. You are ready to go ahead to start the setup of Document Grounding in Excersise 3.
Continue to - [Exercise 3 - Setup Document Grounding](../ex3/README.md)
