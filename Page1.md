---
fname: Sandip Patel
layout: demo_template
theme: jekyll-theme-cayman
---

# Getting Started

Your connections between Salesforce and external systems use an authentication protocol to confirm secure communication between the two systems.
Choose the authentication protocol that matches the configuration of the external system that your org connects to. 
When selecting which authentication protocol to use with your external system, keep the strengths and considerations of each protocol in mind.

|  Release  | Description   |
| --------- | -----------   |
| May '22   | New Topic     |
| April '22 | Modified Topic|


## Named Credentials

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
