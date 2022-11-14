---
fname: Sandip Patel
layout: exam_template
---
# Setting up your IBM Cloud Account

## Step 5: Set preferences for receiving notifications

Complete the following steps to set your preferences for receiving various types of notifications:

1. To receive notifications about IBM Cloud platform-related, or resource-related items, go to the Avatar icon **Avatar** icon ![Avatar Logo](/New-Product-Documentation/images/avataricon.png) **Profile > Notification preferences**.

   - When you set IBM Cloud platform notifications, you receive email notifications that are associated with only the platform. 
     You do not receive notifications about events that are associated with IBM Cloud services. By default, all platform notifications 
	 are turned off.
   - If you update your preferences on resource activity, such as incidents, maintenance, security bulletins, or infrastructure service updates, 
     the notifications are for only the services you use or the devices that you have provisioned. By default, all infrastructure notifications 
	 are turned off.
2. To receive spending notifications, go to **Manage > Billing and usage > Spending notifications** in the IBM Cloud console. Or, you can access it 
   directly from the [Notification preferences](https://cloud.ibm.com/login?redirect=%2Fuser%2Fnotifications) page by clicking **Manage** in 
   the **Billing and Usage** section.
   
   You receive notifications when you reach 80%, 90%, and 100% of the spending thresholds that you specify. Enter the dollar amount to set a spending
   threshold when you set up your spending notification. For more information, see [Setting spending notifications](https://cloud.ibm.com/docs/billing-usage?topic=billing-usage-spending).
   
## Step 7: Set up access

IAM access groups provide a way for you to quickly and easily assign access to multiple resources in your account at one time.

1. Create an access group.

     a. Go to **Manage > Access (IAM) > Access Groups** in the IBM Cloud console.
     
     b. Click **Create**.
	 
	 c. Enter a name for your group, and click **Create**. For example, if you know multiple users in your account need to be able to apply subscription 
		codes, track usage, or perform other billed-related tasks, you might name your group ```Billing-Editor-Access```.
	  
2. Assign access to the group.

     a. Click **Access policies > Assign access**.
   
     b. Select the type of access to assign:
	 
	 - **IAM services**: Assigns access to IAM-enabled services, which are services that are managed by using IAM access control and assigned 
	      to a resource group.
	 - **Account management services**: Assigns access to manage platform services, such as billing, license and entitlements, and enterprises.

     c. Select all roles that apply.
   
     d. Click **Add > Assign**.

See [What makes a good access group strategy?](https://cloud.ibm.com/docs/account?topic=account-account_setup#resource-group-strategy) for details about how to best set-up your access groups.

## Step 9: Explore your support options

You can use the Support Center to get help with any issues that you might encounter. To access the Support Center, click **Support** in the console menu 
bar.

- The Help just for you section features links to common tasks, troubleshooting, and FAQs specific to the resources in your account.
- The Featured FAQs section provides FAQs related to platform tasks, for example, resetting your password, IAM, and upgrading your account.
- The Contact support section provides the options for getting in touch with a support representative: start a live chat, contact by phone, or create a support case.

