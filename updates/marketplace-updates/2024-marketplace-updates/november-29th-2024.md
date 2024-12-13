# November 29th, 2024

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* **Halo Support Added to '\[Rewst Master] PSA: Get Service Tickets' Subworkflow**
  * Extended the subworkflow to integrate with Halo PSA, allowing users to retrieve service tickets seamlessly.
* **Expanded 'Create GDAP Relationship' Subworkflow**
  * Modified the subworkflow to include non-CSP customers, enabling broader customer relationship management.
* **Updated Marketplace Description for Contact Sync Feature**
  * Revised the Crate marketplace description to accurately reflect the ability to sync contacts from on-premises Organizational Units (OUs).

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* **Resolved Workflow Failure When 'Manage Ticket' Has No Notes**
  * Fixed an issue where the ticket categorization workflow would fail if no notes were present in the 'Manage Ticket' section.
* **Fixed User Onboarding Failure Caused by Listener Issue**
  * Addressed a problem where the user onboarding process was failing due to a malfunctioning listener.
* **Updated 'psa\_no\_ticket\_item' Implementation in Halo Tickets**
  * Corrected the implementation to ensure proper handling of tickets without items in Halo.
* **Corrected Path Error in 'Run PowerShell on Org DC' Action**
  * Fixed an issue where the action would take an incorrect path if the `Device_Name` was null.
* **Adjusted 'Create Service Ticket - Datto' Action to Use Only Active Contacts**
  * Modified the action to exclude inactive contacts, ensuring that service tickets are created only for active contacts.
* **Modified Pax8 Extra License Removal Process**
  * Updated the process to ignore 'Microsoft\_Teams\_Exploratory\_Dept' when removing extra licenses, preventing unintended license removals.
* **Restored Missing Context in ConnectWise Technician Toolkit**
  * Fixed the issue where the context (CTX) was missing, enhancing the toolkit's functionality.
* **Removed Hardcoded Site Name in 'Halo Create Ticket' Action**
  * Eliminated the hardcoded site name to allow dynamic site assignment when creating tickets in Halo.
* **Fixed 'Ticket Type Not Set' Error During Halo Ticket Creation**
  * Resolved an error that occurred when the ticket type was not specified during the creation process in Halo.
* **Fixed 'Get All OUs' Option Generator**
  * Addressed issues with the option generator not retrieving all Organizational Units correctly.
* **Corrected Transition in Offboarding Workflow for ADSync Check**
  * Fixed a faulty transition related to the ADSync check within the offboarding workflow.
* **Fixed 'Check for Existing User' Functionality**
  * Resolved an issue where the system failed to locate existing users during verification checks.
* **Corrected Transition Logic in 'Bulk Move Users to Specified OU' Workflow**
  * Fixed the transition logic to ensure users are moved correctly in bulk operations to specified OUs.
* **Fixed Active Directory Sync Failure During User Offboarding**
  * Addressed a synchronization failure with Active Directory that occurred during the user offboarding process.
* **Fixed Input Configuration Bug in '\[ROC] RMM: Run Ad-Hoc PowerShell on Computer' Subworkflow**
  * Resolved a bug in the input configuration, enhancing the execution of ad-hoc PowerShell commands on computers.

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* App Builder Apps
  * Operational Analytics Portal - aggregates data from various tools and outputs actionable insights for MSPs to further streamline operations.
  * Forms Portal - allows employees and clients to easily access the necessary Rewst forms based on granular permissions.
  * All-In-One Client Portal - The portal transforms service delivery by empowering clients to instantly self-serve common IT requests —not just submit tickets.
* Top 10 crates - Improving success rates and implementing Rewst Best Practice&#x20;
  * Alert when Mailbox Quota Full
  * Detailed MFA Reporting
  * Refactor of Change a Users Password form. (just needs QA)
  * Refactor of Identify DUO users in Bypass Mode. (just needs QA)

</details>

