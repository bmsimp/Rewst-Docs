# Data type brainstorming

Think about a process you want to automate and identify the types of data it involves. Recognizing data types early helps you design efficient workflows in Rewst.

#### **Why this matters**

When you automate a process in Rewst, understanding data types helps you:

* Structure your workflows efficiently
* Avoid errors (e.g., treating a number as a string)
* Make smart decisions (e.g., using Booleans for approvals)

***

#### **Step 1: Choose a process to automate**

Pick a real-world process you’d like to automate. As you think through your automation, keep these key points in mind:

* **You can’t automate what doesn’t exist** (Aharon’s Law) – make sure there’s an actual process in place first.
* **Start small** – focus on a simple, repetitive task rather than a complex workflow.
* **Ask yourself:** What’s one quick, routine task you’d love to eliminate from your to-do list?

For example, you might automate processes like:

* **Adding PTO requests to a calendar** once they’re approved
* **Sending an alert** when a ticket is overdue
* **Automatically welcoming new employees** with a personalized email

***

#### **Step 2: Identify the data types**

For your chosen process, identify the data you'll use. The table provides an example of brainstorming data types for overdue ticket alerts.

| Data element                      | Example value                                                                                | Data type  |
| --------------------------------- | -------------------------------------------------------------------------------------------- | ---------- |
| Ticket number                     | 42                                                                                           | Integer    |
| Employee assigned                 | Jane Doe                                                                                     | String     |
| Overdue                           | Yes/No                                                                                       | Boolean    |
| Manager email                     | manager@example.com                                                                          | String     |
| Ticket information                | <p>Date submitted: 5/12/24 Original priority level: Low </p><p>Ticket type: Login issues</p> | Dictionary |
| Other tickets submitted by client | \["Ticket #12345", "Ticket #12346", "Ticket #12347"]                                         | List       |

Write down your own workflow and data type brainstorm somewhere accessible - they will come in handy when you get to Rewst Foundations!

***
