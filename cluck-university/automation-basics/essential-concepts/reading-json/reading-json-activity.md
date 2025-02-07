# Reading JSON activity

This activity will help you:

* Recognize **JSON data** when viewing API responses in a browser.
* Break down **key-value pairs** and understand different data types.
* Practice reading and interpreting **real API responses** to extract meaningful information.
* Understand how **automation tools like Rewst** generate and use JSON for workflows.

***

### **Open a real API response in JSON format**

Let’s start by looking at **real JSON data from Microsoft Graph API!**

**Click this link:**

[Microsoft Graph "Get User" API response](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0\&tabs=http#response-1)

_This page contains a sample JSON response showing user data from Microsoft Entra ID (Azure AD)._

**Example of what you’ll see:**

<figure><img src="../../../../.gitbook/assets/Screenshot 2025-02-05 at 1.32.36 PM.png" alt=""><figcaption></figcaption></figure>

### Identify key-value pairs

JSON is made up of **key-value pairs**—think of it like entries in a dictionary.

Let's analyze this response by answering a few questions. Try to answer each question on your own first, then click the accordion to check your response.

<details>

<summary>What is the "displayName" of this user? <br><em>(Hint: Look for "displayName")</em></summary>

* "displayName": "Adele Vance"&#x20;
* The user's display name is Adele Vance

</details>

<details>

<summary>What type of data is stored in "id"? <br><em>(Is it a number, string, or Boolean?)</em> </summary>

* The "id" field contains a **string** (text) value: "id" : "3a2a1bcd-4a62-4865-b3c8-4a8e3b9f5f29"&#x20;

</details>

<details>

<summary>What is the difference between "givenName" and "displayName"? <br><em>(Why might a system need both?)</em> </summary>

* "givenName" refers to the user's **first name.** "givenName" : "Adele"
* "displayName" is typically a **full name** that appears in applications. "displayName" : "Adele Vance"&#x20;
* A system. might store both so it can show the full name in some places while using just the first name in others

</details>

<details>

<summary>What is missing from this user's data? </summary>

* "mobilePhone" : null&#x20;
* The mobile phone numer is **missing or unavailable**, which is why it has a value of null&#x20;
* This could mean the user hasn't provided one, or it's not required in this system&#x20;

</details>

<details>

<summary>What does "userPrincipalName" represent, and how is it different from "mail"? </summary>

* "userPrincipalName" : "AdeleV@contoso.com" is the **username used for logging in**&#x20;
* "mail" : "AdeleV@contoso.com" is the **email address used for communication**
* Sometimes they are the same, but in some systems, they can be different

</details>

***

### **Compare to other JSON structures**

Try looking at other types of JSON! Click the links below, then review the question and answers.&#x20;

**List of Users (Multiple User Accounts)** → [Get Users API Response](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0\&tabs=http#response)

<details>

<summary>How is this different from the single-user response? </summary>

Instead of a single object { ... }, this response contains an array \[ { ... }, { ...} ]&#x20;

</details>

<details>

<summary>What structure do you see when multiple users are returned? </summary>

The JSON response wraps multiple user objects inside **square brackets \[ ]**, making it a **list (array)**

</details>

**User's Messages (Emails in JSON format)** → [Get Messages API Response](https://learn.microsoft.com/en-us/graph/api/message-get?view=graph-rest-1.0\&tabs=http)

<details>

<summary>What fields appear in an email message? </summary>

Fields include "subject", "from", "to", "body", and "recievedDateTime"&#x20;

</details>

<details>

<summary>Can you find the "subject" field? What about "from"? </summary>

* The "subject" field contains the email's subject line&#x20;
* The "from" field contains the sender's details

</details>

***

### **See JSON in automation (a glimpse into Rewst)**&#x20;

Now that you’ve explored JSON structures, let’s look at **a real example from an automation tool**—Rewst!

When a workflow runs in Rewst, it generates **results in JSON format**, showing details about the action taken. Below is an example of a JSON result from a workflow that **adds or removes a user from Microsoft Graph (Azure AD).**

**Here’s a sample JSON output from this type of workflow:**

<figure><img src="../../../../.gitbook/assets/Screenshot 2025-02-05 at 2.00.43 PM.png" alt=""><figcaption></figcaption></figure>

#### Breaking it down

This JSON output is from a **workflow that adds a user to a group in Microsoft Graph.** Let’s analyze what we see here:

<details>

<summary>What action is being performed? <br><em>(Hint: Look for the "action" key)</em> </summary>

* The "action" key shows - "action" : "add"&#x20;
* This means the workflow is **adding** something (likely a user to a group)&#x20;

</details>

<details>

<summary>Which organization is this affecting? </summary>

* The "organization" section contains:&#x20;

<img src="../../../../.gitbook/assets/Screenshot 2025-02-05 at 2.05.05 PM.png" alt="" data-size="original">

* The affected organization is "pedroaviary"&#x20;

</details>

<details>

<summary>Who trigged this action? <br><em>(Hint: Find the "user" section)</em></summary>

* the "user" section shows:&#x20;

<img src="../../../../.gitbook/assets/Screenshot 2025-02-05 at 2.08.14 PM.png" alt="" data-size="original">

* The user who triggered this action is Eddie.Chow@rewst.io

</details>

<details>

<summary>What does "rewst" tell us? What information does it include? </summary>

* The "rewst" section contains:&#x20;

<img src="../../../../.gitbook/assets/Screenshot 2025-02-05 at 2.13.27 PM.png" alt="" data-size="original">

* This provides the **Rewst app URL.** This is where this automation was executed

</details>

<details>

<summary>The "execution_id" is a long, unique string - why do you think automation tools generate these? </summary>

* "execution\_id" : "01943d11-3b6e-7b9f-9e6f-0c0d92773e38"&#x20;
* Automation tools use unique execution IDs to **track and reference specific workflow runs**
* This helps in **logging, debugging, and tracing issues**

</details>

#### **Why does this matter?**

* **This is the type of JSON output you’ll see in Rewst when automating IT workflows.**
* Understanding JSON will help you **interpret automation results** and troubleshoot issues.
* Later in the Rewst Foundations course, you’ll start working with workflows like this!

💡 **Key Takeaway:** JSON isn’t just abstract data—it’s how automation tools like Rewst communicate and execute actions in IT environments.
