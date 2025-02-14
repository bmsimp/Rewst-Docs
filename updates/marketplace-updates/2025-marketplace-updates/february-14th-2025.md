# February 14th, 2025 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Windows 11 Compatibility Checker

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Microsoft: User Onboarding
  * Removed unused input variable `m365_distribution_groups`.
  * Set default input value for `hide_from_gal` to `false`.
  * Added `user_exists` input variable.
* Licensing: MS Tier1: Purchase License
  * Added graph action to pull tenant ID instead of relying on `ORG.MAPPING.ms_tenant_id`.
  * Added checks to handle tenant ID retrieval.
* Microsoft: User Offboarding
  * Changed `shared_mailbox_no_automap` from string to boolean.
  * Added OneDrive invite functionality and updated form fields.
  * Updated workflow to continue running even if there is an error with `disabling_psa_contact`.
* Configure New GDAP Relationship
  * Trimmed tenant name in display name to meet the 50-character limit.
  * Fixed typo in crate description.
  * Made `list_groups` condition case-insensitive.
* Install Acronis Backup Agent on Devices
  * Fixed `ticket_id` data alias transition error.
* Agent Smith: Track Agent Inventory in Azure Tables
  * Fixed Jinja syntax and added whitespace control in task transitions.
* Billing Count Report
  * Changed data alias and variable names to align with IT Glue standards.
  * Updated subworkflow to return `company_id` to the main workflow.

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Automation Toolkit Crates
* Pax8 Licensing Enhancements

</details>

