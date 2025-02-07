# API activities

## Table of contents&#x20;

[Quick brainstorm ](api-activities.md#quick-brainstorm)

[API scavenger hunt](api-activities.md#api-scavenger-hunt)&#x20;

## Quick brainstorm&#x20;

Think about a workflow you’ve built (or want to build) in Rewst. Break it down into requests and responses—what information needs to be pulled (GET), added (POST), updated (PUT), or deleted (DELETE)? Reflect on how Rewst handles these API conversations behind the scenes to make automation seamless.

## API scavenger hunt&#x20;

Learn how to find and understand API documentation, identify endpoints, and interpret key details.

***

#### **Objective**

This activity will help you:

* Find and navigate API documentation
* Identify API endpoints and their purpose
* Understand authentication requirements
* Recognize the data structure of API responses
* Develop confidence in working with API docs

***

#### **How to find API documentation**

If you ever need to find API documentation for a service, follow these steps:

1. **Google it:**
   * Search for **“\[Service Name] API documentation”**
     * Example:  "Microsoft Graph API documentation"
2. **Check the official website:**
   * Most companies provide an API reference in their developer or integrations section.
     * Example: Microsoft’s API docs are on [this page](https://learn.microsoft.com/en-us/azure/api-management/).
3. **Look at API marketplaces:**
   * Sites like **Postman API Network**, **RapidAPI**, and **ProgrammableWeb** list popular APIs.
4. **Check developer portals:**
   * Many platforms (Microsoft, Google, AWS) have dedicated developer portals with API guides.

***

#### **Instructions**

1. **Pick an API from the list below or find one yourself.**
2. **Locate the official documentation.**
3. **Answer these questions:**

* **What does this API do?** (Summarize in simple terms.) You can often find this information in the **overview page**.&#x20;
* **Find one useful endpoint.** Write down its URL format (e.g., /users for listing users.) You can find this information in the **endpoints reference section**.&#x20;
* **What data does this endpoint return?** (Look for JSON responses.) Take a look at the **request and response exmples.**
* **What parameters does it use?** (Look for required fields like ?filter=email)
* **Does this API require authentication?** (Look for OAuth, API keys, or tokens.) These can be found in the **authentication section**.&#x20;
* **What’s a real-world scenario where this API could be used?**

**Bonus challenge:**

* Find an API request example in the documentation and explain what it does.
* Describe how this API might fit into an **automation workflow**.

***

#### **APIs to explore**

#### **1. Microsoft Graph API** – **Manage Microsoft 365 services**

**Link to docs:** [Microsoft Graph API](https://learn.microsoft.com/en-us/graph/)

**Example endpoints:**

* /users→ Get a list of users
* me/mailFolders/inbox/messages → Retrieve emails from an inbox
* /security/alerts → Access security alerts

**Authentication?** OAuth (requires Azure AD permissions)

**Things to look for:**

* What kind of authentication is required to access user data?
* How are permissions structured in Microsoft Graph?
* What are some filtering options when retrieving user or email data?

***

#### **2. Azure API (Azure Resource Manager API)** – **Manage Cloud resources**

**Link to docs:** [Azure Resource Manager API](https://learn.microsoft.com/en-us/rest/api/resources/)

**Example endpoints:**

* /subscriptions/{subscriptionId}/resources → Retrieve all resources in a subscription
* /resourceGroups/{resourceGroupName} → View and manage resource groups
* /virtualMachines → Get a list of virtual machines

**Authentication?** OAuth (requires Azure AD token)

**Things to look for:**

* What headers are required in a request?
* How are API calls structured to target specific resources?
* How does Azure handle API versioning?

***

#### **3. Microsoft Exchange Online API (Mail API in Graph)** – **Manage emails & mailboxes**

**Link to docs:** [Microsoft Graph Mail API](https://learn.microsoft.com/en-us/graph/api/resources/mail-api-overview?view=graph-rest-1.0)

**Example endpoints:**

* /me/messages → Retrieve emails from a mailbox
* /me/sendMail → Send an email programmatically
* /users/{userId}/mailFolders → Access mailbox folders

**Authentication?** OAuth (requires Microsoft 365 permissions)

**Things to look for:**

* What request body format is required to send an email?
* Can you retrieve only unread emails?
* How are email attachments handled in API requests?

***

#### **Want to explore other APIs?**

Try finding API documentation for:

* **NinjaOne API** – Automate endpoint management, patching, and alerts
* **Slack API** – Automate messages and manage channels
* **GitHub API** – Automate repositories, issues, and user management
* **Datto API** – Manage backups, disaster recovery, and device monitoring
* **ConnectWise API** – Automate ticketing, customer management, and billing

***

#### **Wrap-up discussion**

* Which API was easiest to navigate?
* What was the most confusing part of the documentation?
* How does authentication impact API access?
* What are some key takeaways for working with APIs in general?
