# Halo PSA integration setup

{% hint style="info" %}
If you’re new to integrations in Rewst, read through our introductory integration documentation [here](https://docs.rewst.help/documentation/integrations).
{% endhint %}

{% hint style="success" %}
**This Integration supports multiple instances**

[Check out the instructions to set up multiple instances here](../../general/multi-instance-integration/multi-instance-integration-setup.md).
{% endhint %}

## What does the Halo PSA integration do?

Our Halo PSA integration provides automation and workflow capabilities by connecting Halo PSA’s IT service management functions with Rewst’s automation platform. This integration allows users to manage and interact with various components of their PSA system directly from Rewst.

### Integration use cases

#### **Automated Ticket Handling**

A new support ticket is submitted in Halo PSA. Automation: A Rewst workflow can automatically classify the ticket, assign it to the correct team based on predefined criteria, and send an acknowledgment email to the customer.

#### **Asset Management & Tracking**

When a new asset (laptop, server, etc.) is assigned to a client, update inventory records. Automation: Rewst can capture the asset details and update Halo PSA records, ensuring real-time inventory tracking.

#### **Client Onboarding Automation**

A new client signs a contract for IT services. Automation: Rewst can automatically create the client profile, set up relevant permissions, and initiate onboarding tasks.



## Integration prerequisites

* Access to the Rewst platform with administrative rights
* You must have a Halo administrator account.

## Set up the Halo PSA Integration

### Set up steps in Halo PSA

Before configuring the Rewst integration you must generate an API user. Here is the instruction for the generation of the integration user:

1. Log in to Halo PSA as an Administrator.
2.  Navigate to **Configuration > Teams & Agents > Agents > New**.\
    \


    <figure><img src="../../../../.gitbook/assets/Screenshot 2025-03-11 at 10.40.25 AM.png" alt=""><figcaption></figcaption></figure>
3. Create an agent for Rewst to use. We suggest naming this user `Rewst API` or similar.
4. Grant the user permissions according to what you would like Rewst to do for you. However, for optimal functionality and reliability of the Halo integration, assign administrator permissions to the service account. We’ve consistently observed higher success rates and fewer connectivity issues when using admin-level access for this integration. While lower permission levels may work in limited scenarios, they often lead to unexpected failures during automated workflows.
5. Click **Save**.
6. Navigate to **Configuration > Integrations > HaloPSA API** ([Halo Authorization Docs](https://halo.haloservicedesk.com/apidoc/authorisation)).
7. Select **View Applications**.
8.  Click **New**.\
    \


    <figure><img src="../../../../.gitbook/assets/Screenshot 2025-03-11 at 10.43.40 AM.png" alt=""><figcaption></figcaption></figure>
9. Name the application `Rewst` .
10. Choose the authentication method for **Client ID and Secret (Services)**.
11. Click the **Permissions** tab.
12. Check the **all** checkbox on.\
    \


    <figure><img src="../../../../.gitbook/assets/Screenshot 2025-03-11 at 10.45.18 AM.png" alt=""><figcaption></figcaption></figure>
13. Click **Save**.
14. Navigate to **Configuration > Teams & Agents > Agents**
15. Click on the user you set up for your Rewst integration.
16. Click the **Departments & Teams** tab.
17. Click **Edit** on the top left. Within **Teams**, select **Add**.\


    <figure><img src="../../../../.gitbook/assets/Screenshot 2025-03-11 at 12.57.22 PM.png" alt=""><figcaption></figcaption></figure>
18. Add all teams from the **Team** drop-down selector.\
    \
    ![](<../../../../.gitbook/assets/Screenshot 2025-03-11 at 12.58.11 PM.png>)
19. Click **Save**.

{% hint style="warning" %}
**Required for Mapping Customers in the Integration**

When creating the API Agent, ensure that the **Allow use of all Customers** Client Restriction setting is set to **Yes** if you want to allow Rewst to interact with your customer records.
{% endhint %}

### Set up steps in Rewst

1. Navigate to **Configuration > Integrations** in the left side menu of your Rewst platform.
2. In the Integrations page, search for the Halo PSA integration.\
   \
   ![](<../../../../.gitbook/assets/Screenshot 2025-03-10 at 11.09.57 AM.png>)
3. Click on the integration tile to launch the **Configuration** setup page.
4. Fill out the form with the details you created:
   1. **Resource Server Hostname**: Halo PSA Resource Server hostname, e.g. `example.halopsa.com`.
   2. **Client ID**: Fill in the ID for the application registered in Halo PSA.
   3. **Tenant ID**: When using a cloud-hosted Halo PSA instance, this must be specified. This value can be found in the Halo PSA web application under **Configuration > Integrations > HaloPSA API > API Details**.
   4. **Auth Server Hostname**: Halo PSA Auth Server hostname, e.g. `example.halopsa.com/auth,` if different from the Resource Server Hostname.
   5. **Client Secret**: Fill in the authentication secret for the application registered in Halo PSA.
   6. **Is On-Premise?**: Clarify whether or not the Halo PSA instance is hosted on an on-premise server.
5.  Save the configuration. Rewst will do a quick validation of your input.&#x20;

    Beneath that integration authentication section you'll see the following options:

    1. **Suggest Values**: This option will attempt to generate mappings between Rewst organizations and child organizations in this integration.
    2. **Refresh Options**: This will re-read the potential mapping options - both organizations and companies in Halo.
    3. **Save Mappings** This will apply mapping configuration changes.

## Test the Integration

1. Navigate to **Automation > Workflows** in Rewst.
2. Create a new workflow and name it with something short and descriptive, such as `Test Halo Integration`.
3. Add the action **List Agents** to the workflow builder canvas, by dragging it from the left pane.\
   \
   ![](<../../../../.gitbook/assets/image (21).png>)
4. Add a trigger to your test workflow by clicking on the /lightning bolt image. Name your trigger whatever you’d like.
5. Click into the trigger’s settings.
6. Toggle **Enabled** to on.\
   \
   ![](<../../../../.gitbook/assets/image (22).png>)
7. Set the **Trigger Type** to **Core - Always Pass**.
8. Click **+** next to **Integration Overrides**. Add **Halo PSA** as your integration override.\
   \
   ![](<../../../../.gitbook/assets/image (24).png>)
9. In the **Activate Trigger To Run For** section, keep **Selected Organization** toggled on. **Toggle All current and future managed organizations** on, or choose just one or individually selected organizations from the **Organizations** drop-down selector.\
   \
   ![](<../../../../.gitbook/assets/image (25).png>)
10. Click **Submit** to save your trigger.
11. Click **Publish** to save your changes.
12. Click Test to run your workflow. Note that this will bring up a drop-down selector to choosing organizations.
13. Select your MSP level.
14. Click **Test** and confirm that the execution finishes without errors.\
    ![](<../../../../.gitbook/assets/image (26).png>)
15. If the test for your MSP is successful, do the same test again. At this point in your steps, select a client organization instead, and ensure that it finishes with no errors.

## Crates related to the Halo PSA integration

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><strong>Bulk Create Client from PSA</strong></td><td><a href="../../../../.gitbook/assets/Screenshot 2025-01-21 at 11.05.26 AM.png">Screenshot 2025-01-21 at 11.05.26 AM.png</a></td></tr><tr><td><strong>OpenAI Ticket Categorization</strong></td><td><a href="../../../../.gitbook/assets/Openai ticket categorization.png">Openai ticket categorization.png</a></td></tr><tr><td><strong>Add Rewst Form Link to New User Request Tickets</strong></td><td><a href="../../../../.gitbook/assets/Add rewst form link to new user request tickets.png">Add rewst form link to new user request tickets.png</a></td></tr><tr><td><strong>OpenAI Ticket Sentiment Analysis</strong></td><td><a href="../../../../.gitbook/assets/Open ai ticket sentiment analysis.png">Open ai ticket sentiment analysis.png</a></td></tr><tr><td><strong>Add Rewst Form Link to Offboarding Request Tickets</strong></td><td><a href="../../../../.gitbook/assets/Add REwst form link to offboarding.png">Add REwst form link to offboarding.png</a></td></tr><tr><td><strong>Assign Asset/Config to Ticket based on Contact</strong></td><td><a href="../../../../.gitbook/assets/Screenshot 2025-03-11 at 10.28.57 AM.png">Screenshot 2025-03-11 at 10.28.57 AM.png</a></td></tr><tr><td><strong>Use</strong> <strong>OpenAI to Suggest Responses to New Tickets</strong></td><td><a href="../../../../.gitbook/assets/Screenshot 2025-03-11 at 10.29.33 AM.png">Screenshot 2025-03-11 at 10.29.33 AM.png</a></td></tr><tr><td><strong>Browse Rewst Form Triggers within a Form and Attach to a Ticket</strong></td><td><a href="../../../../.gitbook/assets/Screenshot 2025-03-11 at 10.29.57 AM.png">Screenshot 2025-03-11 at 10.29.57 AM.png</a></td></tr></tbody></table>



## Troubleshooting Halo PSA integration setup

{% hint style="info" %}
Click on any of the issues below to expand and view its solution. If your issue isn't included here, contact Rewst support in your dedicated support Discord channel.
{% endhint %}

<details>

<summary>Customers are not showing up when refreshing options</summary>

Customers not showing when refreshing options is due to an issue with permissions. Make sure to check that both the user and API user have the following permissions, at minimum:

* View Customers
* View Support Tickets
* Add Time Entries
* Create Support Tickets

{% hint style="warning" %}
You may need to uninstall and reinstall the Halo integration for the new permissions to take place.&#x20;
{% endhint %}



</details>

<details>

<summary>Boards and teams are not visible in configure organizational variable form</summary>

If you can't see boards or teams in the configure organizational variable form, this is due to incorrect permissions. You’ll need to add the API User to the teams that you want to see in the form.

</details>

<details>

<summary>Email, name, department is missing or CAB ID is invalid</summary>

If you run into an issue where the Email, Name, Department, or other information is missing, or you see that the CAB ID is either invalid or mandatory, this is due to custom fields used in creating tickets. To use these custom ticket fields:

* The Custom Field IDs need to be added as an organization variable
* The Custom Field should not be marked as mandatory

</details>

<details>

<summary>New User Onboarding and Offboarding Crate Halo Issues</summary>



Rewst only uses the bare minimum of fields for ticket creation in these Crates.

#### Ticket Creation

* team
* source
* summary
* user\_id
* client\_id
* site\_name
* status\_id
* category\_1
* category\_2
* category\_3
* category\_4
* priority\_id
* details\_html
* tickettype\_id
* new\_approvalprocess\_cab
  * type
  * cab\_id

#### Ticket Updates

* note
* outcome
* ticket\_id
* new\_status
* who\_agent\_id
* timetaken

{% hint style="warning" %}
It's possible that Halo is set up to require multiple other fields. If this is the case, there are two paths:

1. You can make sure additional fields are not checked as required.
2. You can unsync the Crate and modify it to include the required fields in your setup.&#x20;
{% endhint %}



</details>

<details>

<summary>General workflow issues</summary>

When creating custom workflows, you may encounter the error **Halo PSA integration is not installed**. To resolve this, either install the integration or implement integration overrides.

{% hint style="info" %}
To execute workflows at the MSP level across client accounts, you must configure Halo integration overrides to ensure proper functionality in the workflow and form field triggers
{% endhint %}



</details>

## Halo PSA actions and endpoints

{% hint style="info" %}
For more on how actions work in Rewst, check out our [introductory actions documentation here](https://docs.rewst.help/documentation/workflows/actions-in-rewst).
{% endhint %}

Halo's own API documentation can be found [here](broken-reference).&#x20;

| Action Name                           | Description                                                                                                                                                  | Endpoint Related to Action     |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------ |
| Add or Update Actions                 | Adds or updates one or more action(s). If id is included then updates, if not included then creates new. Ticket ID is mandatory                              | /Actions                       |
| Add or Update Agents                  | Adds or updates one or more agents(s). If id is included then updates, if not included then creates new.                                                     | /Agent                         |
| Add or Update Appointments            | Adds or updates one or more appointment(s). If id is included then updates, if not included then creates new.                                                | /Appointment                   |
| Add or Update Assets                  | Adds or updates one or more asset(s). If id is included then updates, if not included then creates new.                                                      | /Asset                         |
| Add or Update Attachments             | Adds or updates one or more attachment(s). If id is included then updates, if not included then creates new. The attachment must be posted in Base64 format. | /Attachment                    |
| Add or Update Clients                 | Adds or updates one or more client(s). If id is included then updates, if not included then creates new.                                                     | /Client                        |
| Add or Update Contracts               | Adds or updates one or more contract(s). If id is included then updates, if not included then creates new.                                                   | /ClientContract                |
| Add or Update Invoices                | Adds or updates one or more invoice(s). If id is included then updates, if not included then creates new.                                                    | /Invoice                       |
| Add or Update Items                   | Adds or updates one or more item(s). If id is included then updates, if not included then creates new.                                                       | /Item                          |
| Add or Update Knowledge Base Articles | Adds or updates one or more knowledge base article(s). If id is included then updates, if not included then creates new.                                     | /KBArticle                     |
| Add or Update Opportunities           | Adds or updates one or more opportunities. If id is included then updates, if not included then creates new.                                                 | /Opportunities                 |
| Add or Update Organisations           | Adds or updates one or more organisation(s). If id is included then updates, if not included then creates new.                                               | /Organisation                  |
| Add or Update Projects                | Adds or updates one or more project(s). If id is included then updates, if not included then creates new.                                                    | /Projects                      |
| Add or Update Quotes                  | Adds or updates one or more quote(s). If id is included then updates, if not included then creates new.                                                      | /Quotation                     |
| Add or Update Reports                 | Adds or updates one or more report(s). If id is included then updates, if not included then creates new.                                                     | /Report                        |
| Add or Update Sites                   | Adds or updates one or more site(s). If id is included then updates, if not included then creates new.                                                       | /Site                          |
| Add or Update Statuses                | Adds or updates one or more status(es). If id is included then updates, if not included then creates new.                                                    | /Status                        |
| Add or Update Suppliers               | Adds or updates one or more supplier(s). If id is included then updates, if not included then creates new.                                                   | /Supplier                      |
| Add or Update Teams                   | Adds or updates one or more team(s). If id is included then updates, if not included then creates new.                                                       | /Team                          |
| Add or Update Tickets                 | Adds or updates one or more ticket(s). If id is included then updates, if not included then creates new.                                                     | /Tickets                       |
| Delete Action                         | Deletes the Action and related objects with the specified id                                                                                                 | /Actions/{action\_id}          |
| Delete Agent                          | Deletes the agent and related objects with the specified id                                                                                                  | /Agent/{agent\_id}             |
| Delete Appointment                    | Deletes the Appointment and related objects with the specified id                                                                                            | /Appointment/{appointment\_id} |
| Delete Asset                          | Deletes the asset and related objects with the specified id                                                                                                  | /Asset/{asset\_id}             |
| Delete Attachment                     | Deletes the attachment and related objects with the specified id                                                                                             | /Attachment/{attachment\_id}   |
| Delete Client                         | Deletes the Client and related objects with the specified id                                                                                                 | /Client/{client\_id}           |
| Delete Contract                       | Deletes the contract and related objects with the specified id                                                                                               | /ClientContract/{contract\_id} |
| Delete Invoice                        | Deletes the invoice and related objects with the specified id                                                                                                | /Invoice/{invoice\_id}         |
| Delete Item                           | Deletes the item and related objects with the specified id                                                                                                   | /Item/{item\_id}               |
| Get Action                            | Returns a single Action object                                                                                                                               | /Actions/{action\_id}          |
| Get Agent                             | Returns a single Agent object                                                                                                                                | /Agent/{agent\_id}             |
| Get Appointment                       | Returns a single Appointment object                                                                                                                          | /Appointment/{appointment\_id} |
| Get Asset                             | Returns a single Asset object                                                                                                                                | /Asset/{asset\_id}             |
| List Actions                          | Returns an object containing the count of actions, and an array of action objects for a given ticket.                                                        | /Actions                       |
| List Agents                           | Returns an array of Agents                                                                                                                                   | /Agent                         |
| List Appointments                     | Returns an array of appointments                                                                                                                             | /Appointment                   |
| List Assets                           | Returns an object containing the count of Assets, and an array of Asset objects                                                                              | /Asset                         |
| List Attachments                      | Returns an array of attachments. Each attachment returned will be in Base64 format.                                                                          | /Attachment                    |
| Preview Report                        | Previews a report from Halo PSA.                                                                                                                             | /Report                        |
| List Users                            | Returns an object containing the count of Users and an array of User objects                                                                                 | /Users                         |
| List Top Levels                       | Returns an object containing the count of top levels, and an array containing the top level tree                                                             | /Toplevel                      |
| List Ticket Types                     | Returns an array of Ticket Types                                                                                                                             | /TicketType                    |
| List Tickets                          | Returns an object containing the count of tickets, and an array of ticket objects                                                                            | /Tickets                       |
| List Teams                            | Returns an array of Teams                                                                                                                                    | /Team                          |
| List Suppliers                        | Returns an array of suppliers                                                                                                                                | /Supplier                      |
| List Statuses                         | Returns an array of Statuses                                                                                                                                 | /Status                        |
| List Sites                            | Returns an object containing the count of Sites, and an array of Site objects                                                                                | /Site                          |
| List Reports                          | Returns an object containing the count of reports, and an array of report objects                                                                            | /Report                        |
| List Quotes                           | Returns an object containing the count of quotes, and an array of quote objects                                                                              | /Quotation                     |
| List Projects                         | Returns an object containing the count of projects, and an array of project objects                                                                          | /Projects                      |
| List Organisations                    | Returns an array of organisations                                                                                                                            | /Organisation                  |
| List Opportunities                    | Returns an object containing the count of opportunities, and an array of opportunity objects                                                                 | /Opportunities                 |
| List Knowledge Base Articles          | Returns an array of knowledge base articles                                                                                                                  | /KBArticle                     |
| List Items                            | Returns an object containing the count of items, and an array of item objects                                                                                | /Item                          |
| List Invoices                         | Returns an object containing the count of invoices, and an array of invoice objects                                                                          | /Invoice                       |
| List Contracts                        | Returns an array of contracts                                                                                                                                | /ClientContract                |
| List Clients                          | Returns an object containing the count of Clients, and an array of Client objects                                                                            | /Client                        |
| List Attachments                      | Returns an array of attachments. Each attachment returned will be in Base64 format.                                                                          | /Attachment                    |
| List Assets                           | Returns an object containing the count of Assets, and an array of Asset objects                                                                              | /Asset                         |
| List Appointments                     | Returns an array of appointments                                                                                                                             | /Appointment                   |
| List Agents                           | Returns an array of Agents                                                                                                                                   | /Agent                         |
| List Actions                          | Returns an object containing the count of actions, and an array of action objects for a given ticket.                                                        | /Actions                       |
| Halo PSA API Request                  | Generic action for making authenticated requests against the Halo PSA API                                                                                    |                                |

{% hint style="info" %}
Got an idea for a new Integration? Rewst is constantly adding new integrations to our integrations page. Submit your idea or upvote existing ideas here in our [Canny feedback collector](https://rewst.canny.io/integrations).
{% endhint %}

