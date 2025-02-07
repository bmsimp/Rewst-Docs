# Understanding webhooks activity

### **Part 1: Webhooks in everyday life**

**Instructions:** Webhooks help different systems communicate instantly. Think about situations where you receive **automatic updates** after doing something online. Match each scenario to what’s happening behind the scenes.

**Example scenario:** You order a package from Amazon and later receive a tracking email when your order ships.

**Webhook?** Yes

A webhook triggered an email when the order status changed, just like a webhook in Rewst triggers a workflow when new information arrives.

***

#### **Match the webhook scenario**

For each scenario below, first determine whether a webhook was involved or not. If a webhook was involved, think about what triggered the webhook. Try to answer each question on your own first, then click the accordion to check your response.

<details>

<summary>You sign up for a webinar and instantly receive a confirmation email. </summary>

**Webhook?** Yes \
\
Submitting the webinar sign-up form likely triggers a webhook, which sends data to the email service to generate and send the confirmation email.&#x20;

</details>

<details>

<summary>A customer submits a report request, and the request appears in a helpdesk system. </summary>

**Webhook?** Yes&#x20;



When the customer submits the support request form, a webhook is triggered to send the request data to the helpdesk system, creating a new ticket.&#x20;

</details>

<details>

<summary>You log into a website, and it asks for your two-factor authentication code. </summary>

**Webhook?** Likely not&#x20;



The two-factor authentication (2FA) prompt is usually handled internally by the authentication system, which checks whether 2FA is enabled and then requests a code. This process happens within the system rather than being triggered by an external webhook.&#x20;

</details>

<details>

<summary>A new post from your favorite celebrity automatically posts in a Discord channel you follow. </summary>

**Webhook?** Yes \
\
When the celebrity posts, a webhook from the social media site (or a third-party service) is triggered, sending the data to Discord's API, which then posts it in the designated channel.

</details>

***

### **Part 2: Spot the webhook in action**

**Instructions:** Below is a real webhook payload that was received in a Rewst workflow. Look at the data and answer the questions.

```json
{
  "ticket_id": 67890,
  "customer": "Jamie Smith",
  "priority": "high",
  "issue": "Password reset not working"
}
```

Try to answer each question on your own first, then click the accordion to check your response.

<details>

<summary>Who submitted the request? </summary>

We'll assume **Jamie Smith** submitted the request since the JSON only provides a "customer" field. However, in some cases, requests might be submitted by someone else (like an agent or another user). If that distinction matters, you'd want to check for a "submitted\_by" field.

</details>

<details>

<summary>What is the priority level of this request? </summary>

**High** - the "priority" field indicates this issue needs urgent attention.&#x20;

</details>

<details>

<summary>If Rewst was handling this webhook, what action should it take next? <br><br>a) Ignore it <br>b) Assign it to the support team <br>c) Wait for someone to check it manually </summary>

**b) Assign it to the support team**. Since the priority is high and the issue involves a password reset problem, Rewst should route it to the support team for immediate action.&#x20;

</details>

***

### **Part 3: Build your own webhook scenario**

**Instructions:** Think of a real-life situation where a webhook could be useful. Describe the idea by considering these key parts:

* **Trigger:** _(What event causes the webhook to send data?)_
* **Webhook data:** _(What important details would the webhook send?)_
* **Action taken:** _(What should happen in response to this webhook?)_
