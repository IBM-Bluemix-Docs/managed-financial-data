---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-08"

---
<!-- {:new_window: target="_blank"} -->
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:faq: data-hd-content-type='faq'}

<!-- I will need to change xref references from SimulatedInstrumentAnalytics to simulated-instrument-analytics once the name change occurs-->

# Getting started with {{site.data.keyword.mfd_full_notm}}
{: #getting_started_mfd_short}

The {{site.data.keyword.mfd_full}} provides access to financial market data that is often required
when you are working with risk and investment management tools. The API provides users direct and
indirect access to simulation-complete records of financial securities that are compiled from IBM
and third-party data partners. These records can then be delivered in a format readable by other APIs
and services on the IBM Cloud.

The {{site.data.keyword.mfd_full_notm}} provides data from IBM and third-party data partners to provide
market data, terms and conditions, and time series for financial securities. This data spans
asset classes such as fixed income, equity, equity derivatives, and commodity products. 

## Working with {{site.data.keyword.mfd_full_notm}}
You have two ways of using the {{site.data.keyword.mfd_full_notm}}:
* Integrated access
* Direct access

### Integrated access
If you subscribe using IBM Cloud, you can use the {{site.data.keyword.mfd_full_notm}} to retrieve financial data and send that data to other APIs and services available on the IBM Cloud.
When you follow the integrated access approach, calls to {{site.data.keyword.mfd_full_notm}} are performed by the integrated service and not directly by the user.
In this case, see the API Reference documentation of the integrated service.
You don't need to refer to the API reference for {{site.data.keyword.mfd_full_notm}}.

You can integrate {{site.data.keyword.mfd_full_notm}} with the following APIs and services:
* [{{site.data.keyword.sia_full}}](/docs/services/simulated-instrument-analytics/index.html)
<!-- * [{{site.data.keyword.sia_full}}](/docs/services/simulated-instrument-analytics?topic=simulated-instrument-analytics-getting_started_siminstruanalshort)-->

Integrating a service requires the configuration of the service-to-service broker.
See the [Getting started with {{site.data.keyword.siminstruanalshort}}](/docs/services/simulated-instrument-analytics/index.html) documentation.
<!--See the [Getting started with {{site.data.keyword.siminstruanalshort}}](/docs/services/simulated-instrument-analytics?topic=simulated-instrument-analytics-getting_started_siminstruanalshort) documentation.-->

### Direct access
{: #direct_access_mfd}
If you have purchased the rights to use {{site.data.keyword.mfd_marketplace_full_notm}} from the IBM Marketplace, you may be eligible to interact directly with {{site.data.keyword.mfd_marketplace_short}}.  In this case, use the API Reference documentation.

<!--
If you subscribe by means of IBM Cloud, you can use the {{site.data.keyword.mfd_short}} service to retrieve financial data and then send it to the {{site.data.keyword.siminstruanalshort}} service for simulation and calculation. In this case, you do not interact with the {{site.data.keyword.mfd_short}} service directly. The {{site.data.keyword.siminstruanalshort}} service connects to the {{site.data.keyword.mfd_short}} service when you submit requests to the {{site.data.keyword.siminstruanalshort}} service.
See the documentation for {{site.data.keyword.siminstruanalshort}} about how to submit requests to {{site.data.keyword.siminstruanalshort}}.
-->

## Before you begin

To use the {{site.data.keyword.mfd_full_notm}}, you must first obtain access to an API key.

For direct access, refer to IBM Marketplace.
For indirect access, provision access from the IBM Cloud catalog. <!--Can we link to MFD in IBM Cloud catalog? Not yet.-->

<!-- If you plan on using {{site.data.keyword.mfd_full_notm}} with other APIs and services on the IBM Cloud, such  as the {{site.data.keyword.sia_full_notm}}, see [Getting started with {{site.data.keyword.mfd_short}}](/docs/services/managed-financial-data/index.html). -->


## Assigning access policies to users of {{site.data.keyword.mfd_short}}

Before you create instances of the service {{site.data.keyword.mfd_short}}, assign access policies to the users of the service.

In this case, the steps focus on assigning an access policy to your user name.

1. In the application catalog, open the service.
2. On the service dashboard, select **Manage** > **Access (IAM)**.
3. Click **Users** and then click the hyperlink for your user name. **Tip**: If you're managing several users, you can add users to an access group and assign the access policy to the group.
4. Click **Access policies**.
5. Click **Assign access** and then click **Assign access to resources**.
6. Enter the name of your service and select the service.
7. Under "Assign service access roles", check `Reader` and then click **Assign**.

Reader access is all you require to use {{site.data.keyword.mfd_short}}.
The assigned access policy applies to all the resources of the service.

If you are using {{site.data.keyword.mfd_short}} with {{site.data.keyword.siminstruanalshort}}, you also need to do these steps for {{site.data.keyword.siminstruanalshort}}.
This requirement is also discussed in [Getting started with {{site.data.keyword.siminstruanalshort}}](/docs/services/simulated-instrument-analytics/index.html).
<!--This requirement is also discussed in [Getting started with {{site.data.keyword.siminstruanalshort}}](/docs/services/simulated-instrument-analytics?topic=simulated-instrument-analytics-getting_started_siminstruanalshort).-->



## Getting your credentials

1. Create an instance of the service.
2. Review the service instance access credentials, similar to the following example:

```
{
  "apikey": "<api-key>",
  "uuid":"<uuid>",
  "url:": "<service-url>"
}
```
{:codeblock}
