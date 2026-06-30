---
title: "Dynamics 365 Finance and Operations"
description: "Step-by-step guide to set up Dynamics 365 Finance and Operations credentials for appse ai integration"
slug: /app-integrations/d365fo/
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

Microsoft Dynamics 365 Finance and Operations helps organizations manage finance, supply chain, and core business processes in one integrated system. It provides real-time visibility, stronger control, and scalable operations across business functions. This guide explains how to configure credentials in appse ai using the available authentication options.

## Setup Credential
Follow the steps below to quickly set up your Dynamics 365 Finance and Operations credential.

## Required Fields
You’ll be asked to fill in the following details:

| Field | Description | Applies To |
|------|-------------|------------|
| Environment Name | If your D365FO login URL is, for example: `https://testenv.operations.dynamics.com/data`, then enter `testenv` in this field | Production / Sandbox |
| Environment Name | If your D365 Finance & Operations login URL is, for example: `https://usnconeboxax1aos.cloud.onebox.dynamics.com`, enter `usnconeboxax1aos` in this field | OneBox (Developer VM) |
| Tenant Id | Microsoft Entra ID | Tenant ID |

## Authentication Methods

<Tabs>
<TabItem value="envchoice" label="Environment Choice">

#### Step 1: Choose Environment Type
<img src="\img\credentials\dynamics-365-finance-and-operations\credentialchoice.png" alt="choice" width="500"/>
#### Step 2: Add Connection Name
Enter a **Connection Name** to help you identify this Dynamics 365 Finance and Operations Production or Sandbox credential within appse ai.

#### Step 3: Enter Environment Name

If your D365FO login URL is, for example:  
`https://testenv.operations.dynamics.com/data`, enter `testenv`.

The prefix `https://` and suffix `.operations.dynamics.com` are automatically applied by appse ai.

If your D365FO login URL is, for example:  
`https://testenv.operations.dynamics.com/data`, enter `testenv`.

The prefix `https://` and suffix `.operations.dynamics.com` are automatically applied by appse ai.

:::note
The base URL and API access scope are automatically generated using the environment name you provide.
:::

</TabItem>

<TabItem value="prod" label="Production / Sandbox" default>

#### Step 1: Add Connection Name
Enter a **Connection Name** to help you identify this Dynamics 365 Finance and Operations Production or Sandbox credential within appse ai.

#### Step 2: Enter Environment Name
Enter the **Environment Name** portion of your Dynamics 365 Finance and Operations Production or Sandbox URL.

If your D365FO login URL is, for example:  
`https://testenv.operations.dynamics.com/data`, enter `testenv`.

:::note
The base URL and API access scope are automatically generated using the environment name you provide.
:::

<img src="\img\credentials\dynamics-365-finance-and-operations\credential.png" alt="credential" width="500"/>

#### Save Your Credential
Click **Save & Authorize** to complete the setup.

- ✓ **Success:** The credential is saved and automatically verified by appse ai.  
- ! **Failure:** Verify that the environment name matches your Production or Sandbox URL and try again.

</TabItem>
</Tabs>

## Actions

The Dynamics 365 Finance and Operations integration currently supports the following actions. Use these actions in workflows to create, update, query, and retrieve D365 F&O records.

| Action | Description |
| --- | --- |
| **Create a new customer** | Creates a new customer account in Dynamics 365 Finance and Operations. |
| **Create a new product** | Creates a new product record in the D365 F&O product catalog. |
| **Create contact** | Creates a new contact record associated with a customer or other party in D365 F&O. |
| **Create customer address** | Adds a new address to an existing customer account in D365 F&O. |
| **Create draft purchase order** | Creates a new draft purchase order document in D365 F&O. |
| **Create exchange rate** | Creates a new exchange rate entry for currency conversion in D365 F&O. |
| **Create Ledger Journal Header** | Creates a new general ledger journal header in D365 F&O. |
| **Create Ledger Journal Lines** | Adds journal lines to a ledger journal in D365 F&O. |
| **Create Sales Order Header v3** | Creates a new sales order header using the Sales Order Header v3 API in D365 F&O. |
| **Create Sales Order Lines** | Adds line items to an existing sales order in D365 F&O. |
| **Get all sites** | Retrieves all site records from D365 F&O for use in inventory and warehouse workflows. |
| **Get contact by contact person ID** | Retrieves a contact record by its contact person ID in D365 F&O. |
| **Get customer by account** | Retrieves a customer record by customer account number in D365 F&O. |
| **Get customer credit limit** | Retrieves the credit limit details for a customer in D365 F&O. |
| **Get customer groups** | Retrieves the list of customer groups configured in D365 F&O. |
| **Get customer payment journal headers** | Retrieves customer payment journal header records from D365 F&O. |
| **Get dimension attributes** | Retrieves financial dimension attributes configured in D365 F&O. |
| **Get exchange rate** | Retrieves exchange rate details for a specified currency pair in D365 F&O. |
| **Get item sales tax groups** | Retrieves item sales tax group records from D365 F&O. |
| **Get overdue customer invoices** | Retrieves customer invoices that are past their due date in D365 F&O. |
| **Get packing slip lines** | Retrieves packing slip line details from D365 F&O. |
| **Get payment methods** | Retrieves the list of payment methods configured in D365 F&O. |
| **Get payment terms** | Retrieves the list of payment terms configured in D365 F&O. |
| **Get Posted Sales Invoice by Invoice Number** | Retrieves a posted sales invoice by its invoice number in D365 F&O. |
| **Get product by Product Number** | Retrieves a product record by product number in D365 F&O. |
| **Get product categories** | Retrieves product category records from the D365 F&O product catalog. |
| **Get Product Dimensions** | Retrieves product dimension configuration records from D365 F&O. |
| **Get product receipt headers** | Retrieves product receipt header records from D365 F&O. |
| **Get product variants** | Retrieves product variant records from D365 F&O. |
| **Get purchase orders by status** | Retrieves purchase orders filtered by status in D365 F&O. |
| **Get released product by item number** | Retrieves a released product record by item number in D365 F&O. |
| **Get released products** | Retrieves all released product records from D365 F&O. |
| **Get return order headers** | Retrieves return order header records from D365 F&O. |
| **Get return reason codes** | Retrieves return reason codes configured in D365 F&O. |
| **Get sales discount trade agreements** | Retrieves sales discount trade agreement records from D365 F&O. |
| **Get sales quotations by quotation status** | Retrieves sales quotations filtered by quotation status in D365 F&O. |
| **Get sales tax groups** | Retrieves sales tax group records from D365 F&O. |
| **Get sales trade agreements** | Retrieves sales trade agreement records from D365 F&O. |
| **Get SalesHeader Info by Customer Reference** | Retrieves sales order header information by customer reference in D365 F&O. |
| **Get vendor invoice headers** | Retrieves vendor invoice header records from D365 F&O. |
| **Get vendor transactions** | Retrieves vendor transaction records from D365 F&O. |
| **Get vendors** | Retrieves vendor records from D365 F&O. |
| **Get warehouse by site ID** | Retrieves warehouse details for a specified site ID in D365 F&O. |
| **Update a customer** | Updates an existing customer account record in D365 F&O. |
| **Update exchange rate** | Updates an existing exchange rate entry in D365 F&O. |

## Triggers

The Dynamics 365 Finance and Operations integration currently supports the following triggers. Use these triggers to start workflows when data changes occur in D365 F&O.

| Trigger | Description |
| --- | --- |
| **New contacts created** | Fetches data records when new contacts are created in D365 F&O. |
| **New customers created** | Fetches data records when new customer accounts are created in D365 F&O. |
| **New Orders created** | Fetches data records when new sales orders are created in D365 F&O. |
| **New packing slip created** | Fetches data records when new packing slips are created in D365 F&O. |
| **New products created** | Fetches data records when new products are created in D365 F&O. |
| **New Sales Invoice Created** | Fetches data records when new sales invoices are created in D365 F&O. |
| **Sales invoices created by date range** | Fetches sales invoice records created within a specified date range in D365 F&O. |

## Troubleshooting

- **Credential verification fails:**  
  Ensure the environment name entered matches the subdomain of the corresponding Dynamics 365 Finance and Operations URL for the selected credential option.

## Frequently Asked Questions

**Do I need to enter the full Dynamics 365 Finance and Operations URL?**  
No. Only the environment name is required. appse ai automatically constructs the full base URL.

**Do I need to configure OAuth details manually?**  
No. OAuth 2.0 authorization is handled internally by appse ai for both credential options.

## Support

Need help? Contact the support team at [support@appse.ai](mailto:support@appse.ai)