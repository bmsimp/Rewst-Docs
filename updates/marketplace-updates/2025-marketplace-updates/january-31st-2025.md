# January 31st, 2025 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Microsoft User Onboarding Refactor
* Microsoft User Offboarding Refactor

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* New User Approval et al
  * Added inline else to ticket update subworkflow action and added failure transitions
* Kaseya BMS: Create Ticket function
  * Added `or none` to Issue Type ID on the kaseya\_create\_ticket action
* Alert on Unused M365 Licenses
  * Added the following licenses in the Pax8 lookup table:
    * POWERAPPS\_PER\_APP\_NEW
    * STREAMSTORAGE\_500
    * STANDARDWOFFPACK\_STUDENT
    * CPC\_E\_4C\_16GB\_128GB
    * EOP\_ENTERPRISE
    * E3\_VDA\_only
    * SCHEDULER
  * Added organization variable `psa_alert_ticket_type` to ticket\_type fields for create\_psa\_service\_ticket actions in main workflow
* Alert on CA Policy Changes (V1 and V2)
  * Moved list of Microsoft role definitions to a common template instead of hardcoded JSON objects in each workflow.
* Alert on Expiring App Reg Secrets
  * Added the ability to enable/disable creation of aggregate ticket
* Add Rewst Form Link to Offboarding Request Tickets
  * Added Halo PSA support
* Assign Asset/Config to Ticket based on Contact
  * Matches are made just against usernames, instead of including matches in hostnames
* Sync AzureAD Account Information with ConnectWise PSA Contacts (v3)
  * Fixed workflow disabling active MS Graph contacts in PSA. Previous code was only selecting either mail or userPrincipalName. Therefore, some PSA contacts doesn't exist in the reference list and gets disabled.
* Compromised User Response
  * Add a reset password acton and pass the password to the ticket
* Prompt to Combine Similar Tickets
  * Fixed incorrect button labels in CWM pod prompt
* Configure Out of Office on Mailbox
  * Fixed data alias references when a new ticket is created from workflow

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Automation Toolkit Crates
* Pax8 / Sherweb Licensing Enhancements
* Windows 11 EoL / Compliance Checks

</details>

