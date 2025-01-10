# January 10th, 2025 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* Refactor: Documenting M365 Environments (ITG/Hudu)

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Alert on Users With No MFA Enforced et al
  * Swapped ordering of the type and subtype Jinja evals on the update ticket task so that WF inputs were evaluated first prior to defaulting to the new employee org var.
* Document Groups V2 - ITG/Hudu
  * Added a unique pipe because in unique scenarios sometimes there would be a contact that is a member of a group with the same mail attribute as another user's UPN attribute which would cause duplicate contact records to be tagged.
* Billing Count Report
  * Fixed `MyGlue: Get License Counts` workflow failing due to Jinja issues
  * Update transition criteria for 'handle failure actions' to 1
  * Updated Jinja used to generate CSV (in all three spots) to pop the company field out of it's index and then insert into the first index (so the CSV would always have Company first).
* Compromised User Response
  * Set ticket type to alert by default and falls back to new user if available
  * Fixed an issue where a new ticket is being created instead of updating the provided ticket from the form
* Add Client to Rewst
  * Fixed missing form resource for `Ingram Micro Customer` field
* GWS Onboard
  * Fixed issue with ticket id reference, change from `ticket_details.data.id` to `ticket_details.ticket_id`
  * Fixed issue with NULL approver email evaluating and causing a Jinja failure on the input for the approver task
  * Replaced ProofPoint subworkflow
  * Simplified approval input
  * There was a condition added to hide the Existing Ticket Number field if opened for a sub org. This would cause issues for the MSP running this form for any sub org themselves. Removed the condition.
* GWS Offboard
  * Fixed issue with ticket id reference, change from ticket\_details.data.id to ticket\_details.ticket\_id
  * Simplified approval input

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Alert on Users without MFA Enforced
* Update On-Premise User Attributes
* Microsoft Onboarding/Offboarding Refactors

</details>

