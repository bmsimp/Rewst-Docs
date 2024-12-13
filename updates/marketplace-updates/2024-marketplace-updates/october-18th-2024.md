# October 25th, 2024

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Clean up Global Address List from Disabled Users
  * Added ability to give an exclusion list via org variable `remove_disabled_users_from_gal_exclude_list`. This list will contain the ids of the users to be excluded from being removed.
* Document Groups Crate
  * Implemented automation log
  * Followed proper workflow naming convention
  * Added actions related to automation logging and build best practice.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* GDAP Setup crate
  * Fixed "No Domain Name" appearing in the relationship title
* Billing Count Report Crate
  * Fixed bug where IDs were missing for M365 tennants, causing an incomplete set of licenses.
* Pax8: Purchase Licence workflow
  * Fixed error where licence cannot remediate due to `start_date` being in the past by updating `CTX.start_date` once the workflow resumes to the current date and time

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

