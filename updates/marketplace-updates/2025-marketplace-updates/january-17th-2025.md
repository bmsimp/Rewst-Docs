# January 17th, 2025 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Alert on Users without MFA Enforced
* Update On-Premise User Attributes

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* GWS Onboard and Offboard
  * Fixed spelling of 'return' in options gen.
* Operational Analytics
  * Adjusted trigger check noop to follow first
* M365 User Onboarding
  * Updated licensing template and adjusted jinja to trim whitespace
* Sync AzureAD Account Information with ConnectWise PSA Contacts (v3)
  * Fixed "title" field for PSA contact not set correctly due to incorrect Jinja
* Rewst: User Onboarding
  * Included additional licenses on Pax8 to Microsoft Licence Lookup.
  * Fix "Licence Distributor: List Subscriptions" workflow failing when a product is not found in Pax8
* Export PSA Ticket Overview to CSV
  * Fixed inconsistent results due to date range not being set from beginning to end of day.
* Assign Asset/Config to Ticket based on Contact
  * Resolved JinjaEvaluationException by filtering Halo configurations to exclude items without an inventory\_number field.
* ConnectWise PSA Agreement Mapping
  * Fixed a JSON error when updating an agreement addition.
* Time Savings Report
  * Fixed an issue where it cannot group results by workflow on form submission if group by org is configured on cron trigger.
* PSA: Update Datto Ticket
  * Added lower filters when checking for `complete_workflow` parameters
* Kaseya VSA PS Workflow
  * Removed hardcoded engine address with variable
* Configure Out Of Office
  * Added handling for no value of `psa_default_board_id`
* Reset Microsoft MFA
  * Fixed workflow failing when configured PSA is ServiceNow or Halo PSA

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Microsoft Onboarding/Offboarding Refactors

</details>

