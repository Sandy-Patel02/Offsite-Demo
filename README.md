---
fname: Sandip Patel
image: Markdown Image for Certification Exam
password: It must be alphanumeric..
layout: demo_template
---
![Company Logo](images/Conga.png)

# Choose an Authentication Protocol

Your connections between Salesforce and external systems use an authentication protocol to confirm secure communication between the two systems.
Choose the authentication protocol that matches the configuration of the external system that your org connects to. 
When selecting which authentication protocol to use with your external system, keep the strengths and considerations of each protocol in mind.

For more information: contact {{page.fname}} or {{site.author}}

{% for item in site.data.data_file %}
- **{{item.Release}}, {{ item.Description }}, {{ item.Date}}**
{% endfor %}

## Password

A static username and password are used to directly authenticate into the external system.
-  If you’re using the per-user identity type, each user accessing the external system manages their own username and password.

For Example: {{page.password}}

## AWS Signature Version 4

A protocol to authenticate callouts to resources in Amazon Web Services over HTTP.
-  The identity type must be named principal.
-  You can use it as an authentication protocol for Named Credentials
-  You can’t use it as an authentication protocol for external data sources.

|  Release  | Description   |
| --------- | -----------   |
| May '22   | New Topic     |
| April '22 | Modified Topic|

>  ### Note
>  If transmitting sensitive information such as healthcare data or credit card data, authenticated Named Credentials are required. 
Salesforce recommends that Customers consider providing their own Certificates for extra security of sensitive data transmissions.

See Also [Manage Scratch Orgs from Dev Hub](#manage-scratch-orgs-from-dev-hub)

# Named Credentials

A named credential specifies the URL of a callout endpoint and its required authentication parameters in one definition. 
To simplify the setup of authenticated callouts, specify a named credential as the callout endpoint. If you instead specify a URL as the callout 
endpoint, you must register that URL in your org’s remote site settings and handle the authentication yourself. For example, for an Apex callout, 
your code handles authentication, which can be less secure and especially complicated for OAuth implementations.

Salesforce manages all authentication for callouts that specify a named credential as the callout endpoint so that you don’t have to. 
You can also skip remote site settings, which are otherwise required for callouts to external sites, for the site defined in the named credential.

>  ### Important
>  All credentials stored within the NamedCredential, ExternalDataSource, and ExternalDataUserAuth entities are encrypted under a framework that is 
consistent with other encryption frameworks on the platform. 
>  Salesforce encrypts your credentials by auto-creating org-specific keys. Credentials encrypted using the previous encryption scheme were migrated to the new framework.

Named credentials are supported in these types of callout definitions:
-  Apex callouts
-  External data sources of these types:
   -  Salesforce Connect: OData 2.0
   -  Salesforce Connect: OData 4.0
   -  Salesforce Connect: Custom (developed with the Apex Connector Framework)
-  External Services

Named Credentials also include an OutboundNetworkConnection field that you can use to route callouts through a private connection. 
By separating the endpoint URL and authentication from the callout definition, named credentials make callouts easier to maintain. For example, 
if an endpoint URL changes, you update only the named credential. All callouts that reference the named credential simply continue to work.

## Manage Scratch Orgs from Dev Hub

You can view and delete your scratch orgs and their associated requests from the Dev Hub.

In Dev Hub, ActiveScratchOrgs represent the scratch orgs that are currently in use. ScratchOrgInfos represent the requests that were used to create scratch orgs and provide historical context.
1.  Log in to Dev Hub org as the [System Administrator](https://help.salesforce.com/) or as a user with the Salesforce DX permissions.
1.  From the App Launcher, select **Active Scratch Org** to see a list of all active scratch orgs. 
    To view more details about a scratch org, click the link in the Number column.
1.  To delete an active scratch org from the Active Scratch Org list view, choose Delete from the dropdown.
     Deleting an active scratch org does not delete the request (ScratchOrgInfo) that created it, but it does free up a scratch org so that it doesn’t count against   your allocations.
1.  To view the requests that created the scratch orgs, select Scratch Org Info from the App Launcher.
To view more details about a request, click the link in the Number column. The details of a scratch org request include whether it's active, expired, or deleted.
1.  To delete the request that was used to create a scratch org, choose **Delete** from the dropdown.
Deleting the request (ScratchOrgInfo) also deletes the active scratch org.

