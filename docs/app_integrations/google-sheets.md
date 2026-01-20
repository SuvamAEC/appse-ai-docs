---
title: "Google Sheets"
slug: /app-integrations/google-sheets
---

Google Sheets is a powerful cloud-based spreadsheet application that allows users to create, edit, and collaborate on spreadsheets in real time. With **appse ai**, you can securely connect your Google Sheets account, automate data operations, and seamlessly integrate spreadsheet data into your workflows.

---

### Required Fields

You’ll need to provide the following details while creating the credential:

| Field             | Description                                                   |
|------------------|---------------------------------------------------------------|
| Connection Name   | A name to identify this Google Sheets connection              |
| Client ID         | OAuth 2.0 Client ID from Google Cloud Console                  |
| Client Secret     | OAuth 2.0 Client Secret from Google Cloud Console              |
| Callback API URL  | Redirect URI provided by our platform for OAuth authentication |

---

## Setup Credential

Follow the steps below to set up your Google Sheets credential and authorize access from our platform.

---

## Step 1: Create a Google Cloud Project

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Click the **Project selector** (top-left).
3. Click **New Project**.
4. Enter:
   - **Project name**
   - **Location**
5. Click **Create**.

---

## Step 2: Enable Required APIs

### Enable Google Sheets API

1. Go to **APIs & Services → Library**.
2. Search for **Google Sheets API**.
3. Click **Enable**.

### (Recommended) Enable Google Drive API

1. In the API Library, search for **Google Drive API**.
2. Click **Enable**.

> Enabling Google Drive API allows better file access and spreadsheet management.

---

## Step 3: Configure OAuth Consent Screen

1. Go to **APIs & Services → OAuth consent screen**.
2. You will see the message:  
   **“Google Auth Platform not configured yet”**
3. Click **Get started**.

---

### Step 3.1: App Information

Fill in the following details:

- **App name**
- **User support email**
- **Developer contact email**

Click **Next**.

---

### Step 3.2: Audience

Select:

- **External** (recommended for SaaS or third-party integrations)

Click **Next**.

---

### Step 3.3: Contact Information

- Enter **Developer contact email**

Click **Next**.

---

### Step 3.4: Finish Initial Setup

- Review the entered details
- Click **Finish**

✅ OAuth consent screen identity is now created  
⚠ Scopes are **not added yet** — this is expected

---

## Step 4: Add Test Users (Mandatory for External Apps)

> While the app is in **Testing** mode, only test users can authorize it.

1. Stay on **APIs & Services → OAuth consent screen**
2. Open **Audience**
3. Under **Test users**, click **Add users**
4. Add one or more Google email addresses  
   (Your own email is sufficient)
5. Click **Save**

---

## Step 5: Configure OAuth Scopes (Data Access)

⚠ Google now manages scopes under **Data Access** (not a separate Scopes tab).

1. Go to **APIs & Services → OAuth consent screen**
2. Open **Data Access**
3. Click **Add or remove scopes**

### Add the following scopes:

#### Required

#### Optional (Recommended)

4. Click **Update**
5. Click **Save**

---

## Step 6: Create OAuth Client ID & Client Secret

1. Go to **APIs & Services → Credentials**
2. Click **Create Credentials**
3. Select **OAuth client ID**

### Application Type

- Select **Web application**

### Configure Redirect URI

Add your application’s callback URL:


> ⚠️ This **must exactly match** the Callback API URL used in your platform.

4. Click **Create**

---

## Step 7: Copy Credentials

After successful creation, Google will display:

- **Client ID**
- **Client Secret**

✅ Copy these values and store them securely  
❗ Do not share them publicly

These values are used while creating the **Google Sheets credential** in your platform.

---

## Step 8: Add Credential in appse ai platform

1. Open the Google Sheets credential form
2. Use the Default Connection name or Customize as required
3. Paste the Client ID in the Client ID field
4. Paste the Client Secret in the Client Secret field
5. Click on Save & Authorize button
6. Use the google account credential for further sign in process
7. Click on Continue to provide access to appse.ai

---

## Next Steps

- Paste the **Client ID** and **Client Secret** into your application’s credential form
- Use the same **Callback API URL** configured above
- Click **Save and Authorize** to complete authentication

---

## Need Help?

If you face any issues during setup, please contact our support team at  
**hello@appse.ai**
