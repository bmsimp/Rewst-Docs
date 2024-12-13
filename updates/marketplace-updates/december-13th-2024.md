# December 13th, 2024

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* **Refactor of the following crates:**
  * Alert when Mailbox Quota Full
  * Document Shared Mailboxes
  * JIT Admin Access (new features on this one including M365 support!)
  * Change a User's Password

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Notify on Conditional Access Changes Crate:&#x20;
  * Handling if the CA policies couldn't be pulled&#x20;
  * Modified Jinja for input policy objects
  * Added GSA (Global Secure Access) support and fixed issue for if no match could be made for GUID (resulting in empty return) that was failing list comp.
* New Employee:
  * Form: Add check for missing username and email domain. Reporting back as option gen result to user.
  * Updated template to adjust \`if\` statement in the Jinja to work correctly for "Create-OnPremExchangeMailbox V2"
* Billing Count Report Crate:
  * Added a output for `workflows_dev_process_psa_create_ticket` and created a ticket\_id data alias.
  * Added automation logs to the \[PROD - TASK] Rewst: Send Email with Attachment subworkflow including a automation\_log output.
  * Added automation log to inner m365 action and replaced the pulling method with a get on the `subscribedSkus` endpoint
  * M365 User Licenses: instead of returning the whole object, only returning the `skupartnumber` if it doesn't find a match in the template
* Disabled Users with Licenses Crate:
  * Add protection in the org lookup workflow of the Disabled Users With Licenses crate to prevent the workflow from failing if a user decides to put bad JSON into the org var and run it with the json\_serialize set to true.
* Pax 8 License Purchase: Updated license name in template
* Amend Mailbox Permissions Crate:
  * Added a noop check for company\_id to gracefully fail if the org variable is missing

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* App Builder Apps
  * Operational Analytics Portal - aggregates data from various tools and outputs actionable insights for MSPs to further streamline operations.
  * Forms Portal - allows employees and clients to easily access the necessary Rewst forms based on granular permissions.
  * All-In-One Client Portal - The portal transforms service delivery by empowering clients to instantly self-serve common IT requests —not just submit tickets.
* Top 10 crates - Improving success rates and implementing Rewst Best Practice&#x20;
  * Detailed MFA Reporting
  * Document User Details v2

</details>

