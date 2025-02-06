# Automation feedback request

## Automation feedback request overview

Starting simple is the key to effective automation.

So, what’s one universal concept every MSP can embrace, regardless of their RMM, PSA, or integrations? A centralized system for automation feedback is an essential step toward fostering a culture of automation across your organization.

This quickstart guide walks you through creating your very first automation: a system to track and manage those requests effortlessly. By leveraging the core principles that will shape your future automations, this tool will collect all automation ideas directly into your inbox for easy access.

By the end of this guide, you’ll not only have your first automation up and running, but also a streamlined process for gathering automation requests from your entire team.

Let’s get cracking!

***

## Step 1: Create a form

Creating a form is a good way to collect information that you will use in your automation. By adding a Field Name for each field, you can easily use the data from each field in your automation. The Field Label and Field Descriptions on the other hand, will help you coach your form user on the type of information you are looking for.

In this case, we want to make sure they know the automation request should be a process that already exists, how much time this automation would save, and how often the automation should run.

1. Log in to the Rewst platform.
2. Navigate to **Automations** > **Forms** in the left side men&#x75;**.**
3. Click **+** to create a new form.
4. Enter `Automation Intake Form` into the **Form Name** field.\
   ![](<../../.gitbook/assets/Screenshot 2025-02-06 at 8.54.29 AM.png>)
5. Click **Submit**.
6.  Add the following fields by dragging the relevant elements into your form builder, with the values specified below:\


    * **Multi-Line Input:**
      * **Field Name:** `process_automation`
      * **Field Label:** What process should we automate?
      * **Field Description:** We can't automate a process that doesn't exist. Please explain the process you would like automated.&#x20;
      * **Field Required:** Yes
    * **Number Input**:
      * **Field Name:** `time_saved`
      * **Field Label:** Time (In minutes)
      * **Field Description:** How much time does this process take to do manually?
      * **Field Required:** Yes
    * **Text Input**:
      * **Field Name:** `frequency`
      * **Field Label:** Frequency
      * **Field Description:** How often does this task get done?
      * **Field Required:** Yes

    <figure><img src="../../.gitbook/assets/Screenshot 2025-02-06 at 9.00.13 AM.png" alt=""><figcaption></figcaption></figure>
7. Click the **Save** icon at the top right of the for&#x6D;**.**
8. Click **Submit**.

***

## **Step 2: Build the workflow**

A workflow is like the piping that your data will flow through. By setting up this workflow, we're telling Rewst to take the information from the form, format it, and send it in an email to you.

### Create a new workflow

1. Navigate to **Automations** > **Workflows.**
2. Click **Create** to create a new workflow.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2025-02-04 at 3.44.50 PM.png" alt=""><figcaption></figcaption></figure>

3. Enter `Automation Intake` in the **Name** field.
4. Add any **Tags** you'd like, to stay organized.&#x20;
5. Click **Submit**.

### Add the trigger

*   Click the **Trigger** button, denoted by a blue lightning bolt, in the top menu. Your load time to establish the trigger may take a moment.\


    <figure><img src="../../.gitbook/assets/Screenshot 2025-02-04 at 3.46.29 PM.png" alt=""><figcaption></figcaption></figure>
* Enter `Intake Form`  in the **Name** field.
* Toggle **Enabled** to on to activate this trigger.
  * With the trigger active, every form submission will start our new workflow.
* Choose the `Core - Form Submission` from the **Trigger Type** drop down menu field. You can type in this menu field to jump to your desired trigger type instead of scrolling through the long list.
* Select the `Automation Intake Form` you created under **Trigger Parameters.**
* Click **Submit** at the botto&#x6D;**.**

### Add the starting noop action to the canvas

1. Open the **Core** section in the left **Actions** menu.\
   ![](<../../.gitbook/assets/Screenshot 2025-02-06 at 9.07.48 AM.png>)
2. Drag and drop the noop action to the workflow canvas.
3. Replace the default core\_noop name with `send_message`.
4.  Type "This action starts the workflow" for the Description.\


    <figure><img src="../../.gitbook/assets/Screenshot 2025-02-06 at 9.09.16 AM.png" alt=""><figcaption></figcaption></figure>

### Add a sendmail action to send the message

1. Open the **Core** section in the left **Actions** menu, if it's not already open.
2. Drag and drop the sendmail action to the workflow canvas.
3. Replace the default core\_sendmail name with `to_email`.
4. Fill in the following for the next several fields:
   1. **Sender**: noreply@rewst.io
   2. **Recipient**: Your own email
   3. **Subject**: Automation Request
   4. **Title**: You have a new automation request

### Add basic Jinja to reference the form input:

1.  Click on the **View in** **Task Editor** button next to the message field to open up the Jinja editor.\


    <figure><img src="../../.gitbook/assets/Screenshot 2025-02-06 at 9.11.23 AM.png" alt=""><figcaption></figcaption></figure>
2. Type the following to reference what we type in the form:
   * **Requestor**: \{{ CTX.user.username \}}
   * **Automation Idea**: \{{ CTX.process\_automation \}}
   * **Time Saved**: \{{ CTX.time\_saved \}} minutes
   * **Frequency**: \{{ CTX.frequency \}}
3. Close the editor.

### Create a transition

1. Click and drag the transition from the noop action to the sendmail action.
   * To do this, you'll need to hover over the gray circle under the **On Success** section of the noop action.

### Publish to save the workflow

1. Enter a **Change Summary** and **Changes Description**.
2. Click **Publish** to save the workflow.
3. Click **Submit** on the pop-up to confirm.

## Step 3: Test the workflow&#x20;

### View the form URL

1. Click the **View Direct URLs** button next to **Dynamic Form URL**.
   * If the trigger isn't open, click **Edit Trigger** at the top menu next to our **Form Trigger**.
2. Click on the link.

### Submit an automation idea

1. Type your automation idea into the form fields.
2. Click **Submit**.
3. Check your email.

## What’s next?

Share the direct link with your colleagues. They'll have to have a role of form-users in Rewst, and they can submit their automation ideas.&#x20;

As your company develops a culture of automation, you'll likely want to make changes to this form to better calculate ROI. Ensure you document your workflows internally, and your team can iterate and build as your processes evolve.
