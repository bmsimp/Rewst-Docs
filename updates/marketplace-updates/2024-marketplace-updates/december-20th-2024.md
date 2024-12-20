# December 20th, 2024 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* **Refactor of the following crates:**
  * OpenAI Ticket Categorization\*
  * OpenAI Ticket Sentiment Analysis\*
  * Detailed MFA Enforcement Reporting
  * Document User Details v2

\*If anyone does have issues, the first "fix" should be to unpack the crates again to ensure they have the latest variables set. This can be done by clicking Update Configuration in the crate details.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Rewst GDAP Configuration
  * Updated base engine url that was hardcoded to use the app.engine\_url namespace that was recently introduced
* In workflow `[PROD TASK] MyGlue: Get License Counts`, fixed issue there handle failure actions task cirteria sensivtivity to 1.
* Crate Just-In-Time Admin Access v2 -Added the ability to create a Org Variable for the username prefix. The Org Variable name is jit\_prefix
  * Modified PowerShell to handle creating a username larger then 20 characters.
* Removed issueTypeId/subIssueTypeId arguments for kaseya\_bms\_create\_ticket task to use typeId parameter only.
* Create PSA Service Ticket Workflow
  * Created "Get Ticket Types" subworkflow for PSA-Kaseya
  * Applied org var fallbacks for ticket type for the following PSAs: Halo PSA, ConnectWise PSA, Freshdesk, ServiceNow, Kaseya BMS
* Crate - Configure Out of Office: -Added a data alias to turn users into a list when its a string.
  * Updated timezone form value to match what is should be based on the options generator
* Crate Document Shared Mailbox Detail
  * Resolve issue where customer doesn't have a documentation platform installed.

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Google Workspace User Onboarding/Offboarding crate
* App Builder Apps
  * Operational Analytics Portal - aggregates data from various tools and outputs actionable insights for MSPs to further streamline operations.
  * Forms Portal - allows employees and clients to easily access the necessary Rewst forms based on granular permissions.
  * All-In-One Client Portal - The portal transforms service delivery by empowering clients to instantly self-serve common IT requests —not just submit tickets.

</details>

