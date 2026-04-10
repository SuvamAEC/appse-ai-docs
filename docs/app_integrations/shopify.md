---
title: "Shopify"
slug: /app-integrations/shopify/
---

Shopify is a powerful e-commerce platform that enables businesses to build, customize, and manage their online stores with ease. With appse ai, you can connect your Shopify account to automate key operations such as order management, customer data synchronization, and product updates. This integration helps streamline your e-commerce workflows, reduce manual effort, and ensure that your online store runs efficiently across all connected systems.

---

## Authentication Methods

Appse AI supports two authentication methods: API Key and OAuth 2.0. Among these, OAuth 2.0 is the recommended option.

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="oauth2" label="OAuth 2.0" default>

## Setup Credential — OAuth 2.0

Follow the steps below to connect your Shopify store to appse ai using OAuth 2.0. This method uses a **Client ID** and **Client Secret** obtained from the Shopify Dev Dashboard.

### Prerequisites

Before starting, make sure:

- You have access to a Shopify store admin account.
- You can log in to the Shopify admin portal.

### Required Fields

You'll be asked to fill in the following details:

| Field           | Description                                                                              |
|-----------------|------------------------------------------------------------------------------------------|
| Connection Name | A name to help you identify this connection.                                             |
| Store Domain    | The domain of your Shopify store (e.g., `newstore`).                     |
| Client ID       | Obtained from your app's Settings page in the Shopify Dev Dashboard.                    |
| Client Secret   | Obtained from your app's Settings page in the Shopify Dev Dashboard.                    |
| Scope           | The OAuth 2.0 permission scopes for your credential.                                     |
| Callback URL    | Auto-filled automatically. This field is non-editable and pre-populated by appse ai. Use this URL to configure the Redirect URL while creating the Shopify App.   |

---

### Step-by-Step Guide

#### Step 1: Log in to Shopify Admin

Open [Shopify Admin](https://admin.shopify.com) and log in using your Shopify admin credentials.

---

#### Step 2: Open Apps Settings

From the left-hand menu, click **Settings** at the bottom.
<img src="\img\credentials\shopify\s1.png"  width="700"/>

Then, from the Settings menu, click **Apps**.
<img src="\img\credentials\shopify\s2.png"  width="700"/>

---

#### Step 3: Open Develop Apps

On the Apps page, click **"Develop apps"** from the top-right section.
<img src="\img\credentials\shopify\s3.png"  width="700"/>

---

#### Step 4: Open the Dev Dashboard

Click **"Build apps in Dev Dashboard"**.
<img src="\img\credentials\shopify\s4.png"  width="700"/>

---

#### Step 5: Create a New App

In the Dev Dashboard, click **"Create app"** from the top-right section.
<img src="\img\credentials\shopify\s5.png"  width="700"/>

You will see the **"Start from Dev Dashboard"** section.

Enter a valid app name (must be within 30 characters), then click **"Create"**.
<img src="\img\credentials\shopify\s6.png"  width="700"/>

---

#### Step 6: App URL

In the **App URL** field, no modification is required since this app is intended for your organization's use only.

---

#### Step 7: Configure API Scopes

Go to the **Admin API scope configuration** section.
Select the scopes relevant to the APIs you want to use — such as customer, order, or product scopes — then **Save** the configuration. You can also use the default scopes displayed in the Shopify Credential form in appse ai platform.
<img src="\img\credentials\shopify\s7.png"  width="700"/>

---

#### Step 8: Configure the Redirect URL

In the **Redirect URL** section, add the Callback URL exactly as displayed in the Shopify Credential form in appse ai platform:

**For example**
```
https://embedded-ui.appse.ai/oauth-callback.html
```
<img src="\img\credentials\shopify\s8.png"  width="700"/>

> ⚠️ Make sure the URL is entered **exactly** as shown in credential form, including `https://`. This URL is required for appse ai to complete the OAuth 2.0 authorization flow.

---

#### Step 9: Release the App Version

Click **"Release"**.
<img src="\img\credentials\shopify\s9.png"  width="700"/>

You will be prompted for an app version value. Enter a version (e.g., `v1`) to keep track of your app versioning, then click **"Release"** again.

After this, the app version will become active.
<img src="\img\credentials\shopify\s10.png"  width="700"/>

---

#### Step 10: Get Client ID and Client Secret

Click **"Settings"** from the left menu inside your app.
<img src="\img\credentials\shopify\s11.png"  width="700"/>

You will see:

- **Client ID** — Copy this directly.
- **Client Secret** — Click the copy button next to it.
<img src="\img\credentials\shopify\s12.png"  width="700"/>

> ⚠️ Store both values securely. You will need them to complete the credential setup in appse ai.

---

#### Step 11: Configure the Credential Form in appse ai

1. **Enter the Shop Subdomain**  
   From the left-hand menu, click **Settings** at the bottom.
  <img src="\img\credentials\shopify\s1.png"  width="700"/>

   The Shop Subdomain is displayed at the top of the sidebar menu.
   <img src="\img\credentials\shopify\s19.png"  width="700"/>
   > **Example:** If your Shopify subdomain looks like **marcostore-9454.myshopify.com**, you only need to paste **marcostore-9454** in the credential form. 

   <img src="\img\credentials\shopify\s14.png" width="700"/>

2. **Enter the Client Credentials**  
   Fill in the following details:
   - **Client ID**
   - **Client Secret**  
   <img src="\img\credentials\shopify\s13.png" width="700"/>

3. **Save the Configuration**  
   Click on the **"Save"** button. A popup will appear prompting you to log in using your Shopify account.

4. **Authenticate Your Shopify Account**  
   Enter your Shopify Admin Account's:
   - **Email Address**
   - **Password**
   <img src="\img\credentials\shopify\s17.png" width="700"/>

5. **Install the App**  
   After logging in, proceed to install the app you developed.
   A warning maybe displayed stating that the app hasn’t been reviewed. This is expected for custom or private apps.

   <img src="\img\credentials\shopify\s15.png" width="700"/>

6. **Confirmation**  
   Once the installation is successful:
   - The credentials will be authenticated  
   - Saved securely  
   - Displayed on the **Credentials** page with a green tick that confirms that the credential is successfully validated

   You can now use the credential for the required workflow integrations.  
   <img src="\img\credentials\shopify\s18.png" width="700"/>

  </TabItem>
    <TabItem value="api-key" label="API Key">

## Setup Credential — API Key

Follow the steps below to quickly set up your Shopify credential using an Admin API Access Token.

### Required Fields

You'll be asked to fill in the following details:

| Field                  | Description                                                   |
|------------------------|---------------------------------------------------------------|
| Connection Name        | A name to help you identify this connection.                  |
| Store Subdomain        | Your Shopify store subdomain ID.                              |
| Admin API Access Token | Create a custom app in your Shopify account to obtain this.   |

First, log in to your [Shopify account](https://accounts.shopify.com/select?rid=539d146c-195f-4011-97ab-fe776d9c0e58). Then follow the step-by-step guide below.

---

### Step-by-Step Guide

#### Step 1: Find your Store Subdomain

<img src="\img\credentials\shopify\settings.png" alt="appse ai Shopify Settings" width="700"/>

Go to **Settings**. Under your store name, you will find your Shopify store subdomain.

<img src="\img\credentials\shopify\store-id.png" alt="appse ai shopify store id" width="700"/>

> **Example:** If your Shopify subdomain looks like `5bazzn-ja.myshopify.com`, you only need to paste `5bazzn-ja` in the credential form.

---

#### Step 2: Find your Admin API Access Token

<img src="\img\credentials\shopify\develop-apps.png" alt="appse ai shopify develop apps" width="700"/>

In the **Settings** section, navigate to **Apps and Sales Channels**, then click **Develop Apps**.

##### Enable Custom Legacy App Development

<img src="\img\credentials\shopify\allow-legacy-custom-app-development.png" alt="appse ai allow custom legacy apps shopify" width="400"/>

<img src="\img\credentials\shopify\allow-legacy-custom-app-development-2.png" alt="appse ai allow custom legacy app development shopify 2" width="400"/>

Click **"Allow custom legacy app development"**, then click **"Allow custom app development"**.

<img src="\img\credentials\shopify\allow-legacy-custom-app-development-3.png" alt="appse ai allow custom legacy app development shopify 3" width="400"/>

<img src="\img\credentials\shopify\create-legacy-app.png" alt="appse ai shopify create legacy app" width="400"/>

You should now see a **"Create a custom legacy app"** button — click on it.

---

#### Step 3: Create the App

<img src="\img\credentials\shopify\create-app-name.png" alt="appse ai shopify create app name" width="700"/>

Set a name for your custom app and click **"Create app"**.

---

#### Step 4: Configure Scopes

<img src="\img\credentials\shopify\choose-scopes-button.png" alt="appse ai shopify choose scopes button" width="700"/>

Click **"Configure Admin API scopes"** and enable the following scopes:

`read_all_orders` `read_customers` `write_customers` `read_fulfillments` `write_fulfillments` `read_inventory` `write_inventory` `read_locations` `write_locations` `read_orders` `write_orders` `read_products` `write_products` `read_publications` `write_publications` `read_discounts` `write_discounts` `read_shipping` `write_shipping`

<img src="\img\credentials\shopify\choose-scopes.png" alt="appse ai shopify choose scopes" width="700"/>

Once all scopes are selected, click **"Save"**.

---

#### Step 5: Install the App

<img src="\img\credentials\shopify\install-app.png" alt="appse ai shopify install app" width="700"/>

Return to the **Overview** tab and click the **"Install"** button.

---

#### Step 6: Copy the Admin API Access Token

<img src="\img\credentials\shopify\admin-api-access-token.png" alt="appse ai shopify admin api access token" width="700"/>

In the **API credentials** tab, your Admin API Access Token will be displayed.

Click the **"Reveal token once"** button. Copy the token and store it somewhere secure — you will **not** be able to see it again.

> ⚠️ **Important:** The Admin API Access Token is shown **only once**. If you lose it, you will have to create a new custom app.

---

#### Step 7: Add the Fields to Appse AI

Enter the **Store Subdomain** and **Admin API Access Token** in appse ai and click **"Save"**.

If you followed all the steps correctly, your credential will be connected successfully.

  </TabItem>
</Tabs>

---

Need help? Contact our support team at [hello@appse.ai](mailto:hello@appse.ai)