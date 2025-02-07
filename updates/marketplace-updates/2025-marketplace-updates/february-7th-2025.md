# February 7th, 2025 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Added functionality for Agent Smith to refactored PS subworkflow.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>



* Microsoft: User Onboarding
  * Added missing trigger to `User: Check Exists`
  * Added in matching with Sherweb using a new CSV they have sent us
  * Fixed a jinja issue in new user creation when using Automate which could cause the action to fail.
* Microsoft: User Offboarding
  * Updated crate readme and input parameter descriptions
* Microsoft User Offboarding V2
  * Fixed ticket\_type\_id input filed for create\_psa\_service\_ticket task from CTX.ticket\_type to CTX.ticket\_type\_id
  * Fixed the typo of "details": TASKS.remove\_licence.result.result.data.value.error.response.error.message|d, to "details": TASKS.remove\_license.result.result.data.value.error.response.error.message|d, on the Failure - Remove Licences noop's On Success transition
* Google: User Onboard
  * Added additional check to condition that checks if the user was created on the user creation subs.
  * Added additional check in validate\_inputs to verify that the org var is set.
  * Added transition so if no user group is set, workflow will continue
  * Added input variable email\_domain and edited workflow to concatenate user id and email domain to pass to the get\_user subworkflow
  * Edited form to require email domain on username field
  * Updated check if user exist field to provide the email\_domain field value to the check if user exist options gen
* Google: User Offboard
  * Set company location id field's value to have the |d have the default param specified to be NULL. Field is an int so the old way of just doing |d would cause a "" value which can't be converted to an int/isn't actually NULL.
  * Fixed company ID for ParentID input on AutoTask contact upsert task.
  * Fixed missing contact ID on AutoTask contact upsert task.
* `List All PSA Contacts` Subworkflow
  * For HaloPSA, include email and contact\_id. This was aimed to fix issues with disabling PSA contacts in User Offboarding.
* Detailed MFA Reporting
  * Updated the Graph batch requests to only retry failed updates.
  * Switched to TASK references in places to reduce overall context size caused by Publish Results As
* Rewst: User Onboarding
  * Modified workflow to use PATCH to update contacts if a mobile exists and use POST if there is no existing mobile
  * Added TASKs: get\_mobile\_items , add\_mobile\_number
  * Modified TASK: update\_mobile\_number
* Subworkflow `[REWST - TASK] M365 Licensing: MS Tier1: Purchase License`
  * Updated the jinja on sub\_id alias to fix a issue with it locating a sub correctly.
* Mass Update Org Variables via CSV
  * Fixed issue in form that was preventing form submission
* Deactivate ConnectWise PSA Contacts when their Company is Deactivated
  * Implemented batching to prevent bad request error on large queries
* Agent Smith: Track Agent Inventory in Azure Tables
  * Fixed list\_tables task not finding the device table name by removing .value in the "Table Found" transition condition of list\_tables task.
* Billing Count Report
  * Removed .result in the sentinel\_counts data alias of sentinel\_one\_list\_sites task to fix Jinja logic.
* Organization Variables Setup Workflow
  * Changed onprem\_no\_adsync field description to a more straightforward one to avoid confusion.

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Automation Toolkit Crates
* Pax8 Licensing Enhancements
* Windows 11 EoL / Compliance Checks

</details>

