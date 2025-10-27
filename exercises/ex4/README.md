# Exercise 4: Test Joule Standalone

In this exercise, you will learn how to navigate to the Joule standalone service, create a Role Collection to include the Joule end_user Role and assign that to a newly created shadow user.


## <a name="step1"></a>Step 1: Log In to Joule

First, we need to ensure that a shadow user from our IAS is created in our BTP subaccount so that we can assign roles to it. To do this:

Navigate to the BTP Subaccount Account Level.

Navigate to **Global Subaccount Level > Instances and Subscriptions**.

1. Click on "Go to Application".
<br>![](/exercises/ex4/images/14_01_btp_joule_test.png)

2. Log in using your user credentials.
<br>![](/exercises/ex4/images/14_02_btp_joule_test.png)

3. You will see the current service status.
<br>![](/exercises/ex4/images/14_03_btp_joule_test.png)

4. Append /joule to the URL.
<br>![](/exercises/ex4/images/14_04_btp_joule_test.png)

## <a name="step2"></a>Step 2: Create a Role Collection and Assign it to Your User

Navigate to the BTP Subaccount Account Level.

1. On the Subaccount level, navigate to "Role Collections" and create a new one by clicking "Create".
<br>![](/exercises/ex4/images/14_05_btp_joule_test.png)

2. Give it a name like "Joule" and optionally a description.
<br>![](/exercises/ex4/images/14_06_btp_joule_test.png)

3. Edit the created Joule Role Collection and use the selection menu for "Roles".
<br>![](/exercises/ex4/images/14_07_btp_joule_test.png)

4. Use the "Role name" field to search for "end_user". Select it and click "Add". This is the role that grants us access to the Joule Webclient.
<br>![](/exercises/ex4/images/14_08_btp_joule_test.png)

5. Now "Save" the Role Collection.
<br>![](/exercises/ex4/images/14_09_btp_joule_test.png)

6. Head over to the menu point "Users" and select the user with the UUID formatted user-id on the non-platform user IDP.
<br>![](/exercises/ex4/images/14_10_btp_joule_test.png)

7. Choose "Assign Role Collection" (this may be hidden in a context menu "..."). Select the "Joule" Role Collection and click "Add".
<br>![](/exercises/ex4/images/14_11_btp_joule_test.png)

## <a name="step3"></a>Step 3: Log In to Joule Again and Start Testing

Navigate again to the Joule Application as in step 

1. Append /logout to the URL to perform a logout.
<br>![](/exercises/ex4/images/14_12_btp_joule_test.png)

2. Navigate back to the application url to log in again.
<br>![](/exercises/ex4/images/14_13_btp_joule_test.png)

3. Now append **/joule** to the application url and you can start testing Joule.
<br>![](/exercises/ex4/images/14_14_btp_joule_test.png)

4. Try out the prompts:
„Can I bring my dog to work?“ 
„What is the dresscode in our office?“
<br>![](/exercises/ex4/images/14_15_btp_joule_test.png)

**Note:** The provided SharePoint repository includes a sample document outlining an employee policy for Giggle Tec, a company with distinct internal policies. You can observe Joule generating answers based on this document — even referencing the original source through a link.

## <a name="summary"></a>Summary
You have successfully enabled your user to access the Joule Webclient and interact with Joule. With the exercises completed, you can now explore Joule further. Use this opportunity to chat with Joule and discover its features and capabilities.
