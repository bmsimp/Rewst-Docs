# October 18th, 2024

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Create Ticket Workflow
  * Updated workflow to remove deprecated actions
  * Added more subworkflows where appropriate
* Moved Security/Distribution Group additions for M365 into subworkflows.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Rewst: user Onboarding:&#x20;
  * Created new subworkflow to encapsulate the add user to group graph call and catch failure on assign to group. Integrated it into new user workflow.
* Rewst: User Offboarding:
  * Fixed password reset failures due to invalid `usageLocation` by adding Add `usageLocation` to select for GET user call and modified location to be `{{ CTX.user_details.usageLocation|d or "US" }}`
* Amend Calendar Permissions on user
  * Added a sub-workflow to handle with-items failures and not fail the entire workflow

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* New Crate - Sonicwall Firmware Update
  * Initiate a firmware update via NSM
  * Support one or more firewall firmware upgrades at once
  * Support scheduling of firmware updates and restart times
* New Crate - Workstation Offboarding
* Utility crate - Error Handling and Reporting

</details>

