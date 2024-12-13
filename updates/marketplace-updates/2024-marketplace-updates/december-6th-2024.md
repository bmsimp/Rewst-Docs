# December 6th, 2024

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* **Refactor of the following crates:**
  * Identify Duo Users in Bypass Mode
  * Document Groups in ITG / Hudu
  * Billing Reporting
  * Notify on CA Policy Changes

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Fixed cloud only groups not being removed during offboarding when `ad_configuration` is set to "hybrid\_synced".
* Added check for Datto PSA to distinguish if input is a ticket number or an id. Updated deprecated task for Datto Autotask PSA list tickets.
* Fixed some erroneous jinja logic in ticket creation that was causing problems if certain configuration org variables were not defined.
* Fixed an issue in conditional logic that was causing issues with initial ticket update for Datto PSA in the offboarding crate.
* Added missing trigger on calendar permissions form.
* Added filter for `list_computers` action to optimize workflow execution speed in NAble run powershell workflow.

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* App Builder Apps
  * Operational Analytics Portal - aggregates data from various tools and outputs actionable insights for MSPs to further streamline operations.
  * Forms Portal - allows employees and clients to easily access the necessary Rewst forms based on granular permissions.
  * All-In-One Client Portal - The portal transforms service delivery by empowering clients to instantly self-serve common IT requests —not just submit tickets.
* Top 10 crates - Improving success rates and implementing Rewst Best Practice&#x20;
  * Detailed MFA Reporting
  * Refactor of Change a Users Password form. (just needs QA)
  * Refactor of Identify DUO users in Bypass Mode. (just needs QA)

</details>

