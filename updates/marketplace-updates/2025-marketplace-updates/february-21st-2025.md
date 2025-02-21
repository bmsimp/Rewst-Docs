# February 21st, 2025 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Duo: Manage Phones

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Microsoft: User Onboarding
  * Fixed subscriptions not being matched if not the exact name by Updated list comprehension condition of subscription\_id data alias from list\_subs task.
  * Updated the email\_domain options gen input on the user check field to be populated from the email\_domain field on the form
  * Fixed org variable reference call on at\_create\_contact task to correctly reference ORG.VARIABLES.datto\_company\_id on the Company ID field
  * Added automap checkbox for shared mailboxes on the form
    * Added functionality on the workflow to handle this
* Rewst: User Onboarding
  * Updated crate version
* Configure New GDAP Relationship
  * Added new BEGIN noop
  * On 'On Success' transition, added a data alias to overwrite the previous value from the trigger
  * New value will be the same but with any '-' replaced with an empty string and then trimmed
* Billing Count Report
  * Added input cleaning and support for different formats for email recipient list
  * Set value passed to send\_to parameter of workflows\_function\_send\_email\_with\_attachment task to `[]`
* Document Group Details v2
  *   Implemented fix on the json\_factory task's bulk\_json data alias on line 311:

      ```json
      "members-record":[]"
      ```
* Operational Analytics
  * Fixed task transition criteria in Get Ticket Data workflow
* Microsoft: User Offboarding
  * Added `|d` to target\_user\_id input value to prevent users from mistakenly selecting OneDrive without an Azure user
* Windows 11 Compatibility Report
  * Fixed filters for the RMMs so it shows devices correctly for each mapped client
  * Fixed conditional filtering in Jinja to exclude non-Windows computers (e.g., Macs)

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Microsoft365 Subscription Renewal Alerts
* Automation Toolkit Crates

</details>

