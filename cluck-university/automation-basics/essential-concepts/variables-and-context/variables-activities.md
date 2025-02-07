# Variables activities

## Table of contents

[Quick brainstorm](variables-activities.md#quick-brainstorm)

[The power of variables ](variables-activities.md#the-power-of-variables)

## Quick brainstorm

Think of a process you often repeat—like sending a customer update or checking a user profile—and list the types of information that might change each time (e.g., name, date, status). Then, identify which of these could be stored as **variables** to make the process faster and more consistent. This will help you start recognizing where variables and data aliases can simplify tasks in Rewst.

## Activity: The power of variables

**Exploring the power of variables in JSON responses**

Let's explore just how helpful variables can be when working with JSON responses in Rewst workflows!

#### Step 1: Understanding JSON in context

Whenever Rewst receives a JSON response, it stores it in the **context** (CTX). Then, to reference a specific piece of information in a workflow, you need to navigate through the JSON structure, specifying each nested level.

#### Example JSON response:

<figure><img src="../../../../.gitbook/assets/Screenshot 2025-02-05 at 2.30.59 PM.png" alt=""><figcaption></figcaption></figure>

If we wanted to reference the user’s email in a workflow, we would write:

CTX.data.user.details.profile.contact.email

That’s pretty long! If we needed to use this reference multiple times, writing out CTX.data.user.details.profile.contact.email  repeatedly would be cumbersome. **This is where variables come in!**

#### Step 2: Creating a variable

Instead of writing the full reference every time, we can assign a **variable** as a shortcut.

For example, we can create a simple variable:

CTX.email&#x20;

instead of CTX.data.user.details.profile.contact.email

Now, whenever we need to reference the user’s email, we can simply write:

CTX.email

This makes our workflow cleaner and easier to manage!

#### Step 3: Practice identifying variables

Below is another JSON sample. Your task is to determine the best way to create a variable for more efficient references.

#### JSON sample:

<figure><img src="../../../../.gitbook/assets/Screenshot 2025-02-05 at 2.34.14 PM.png" alt=""><figcaption></figcaption></figure>

#### Questions

Try to answer each question on your own first, then click the accordion to check your response.

<details>

<summary>If we wanted to reference the customer's street address, how would we normally write it? </summary>

CTX.store.order.customer.address.location.street

</details>

<details>

<summary>What's a good variable name we could create to simplify referencing the customer's information? </summary>

Example answer: CTX.customer\_info&#x20;

</details>

<details>

<summary>Using your new variable, how would you reference the customer's phone number? </summary>

Example answer: CTX.customer\_info.personal.contact.details.phone

</details>

<details>

<summary>What's an even simpler variable you could create for the customer's email? </summary>

Example answer: CTX.customer\_email&#x20;

</details>

By using variables, we make JSON data easier to access and our workflows much more efficient!

#### Recap:

* JSON responses are stored in **CTX**
* Referencing deeply nested data can be tedious (CTX.level1.level2.level3...)&#x20;
* **Variables** provide shortcuts for cleaner and more readable workflows
* Once a variable is set, we can use it to reference data more efficiently

Now, think about how you might use variables in automation. How could storing and reusing data make processes more efficient? Jot down an example or discuss it with a partner—soon, you'll be applying these concepts in Rewst!
