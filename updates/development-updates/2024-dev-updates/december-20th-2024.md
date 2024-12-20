# December 20, 2024 - Dev Update

Explore what new changes the Dev team has deployed in the last week!

This can be anything from new features, bug fixes, or QoL changes!

<details>

<summary><strong>New features and items</strong></summary>

* Added `Australia 2` zone for Datto PSA Integration.
* Added `US6` region for the Auvik Integration.
* IT Portal Integration
* Added a loading indicator to "Create App" input fields during match search.
* Set inquiry task max timeout to match parent workflow's timeout.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Resolved `Microsoft Graph` JWT validation failures for non-custom app registrations.
* Improved responsiveness of the Workflow Canvas toolbar by preventing `Test` and `Publish` buttons from getting cut off on smaller screens.
* Corrected task count mismatches between Dashboard
* Made source field ID nullable for Jinja objects.
* Resolved dropdown form field issues with workflow-generated and dynamic options.
* Fixed pagination issues with ConnectSecure v4 integration.
* Addressed Addigy actions with excessively long descriptions.
* Improved error handling for invalid result set types in Hudu list requests.
* Resolved iframe rendering issues for HTML templates.
* Added `Liongard Get Metric Enabled Values (V2)` action.
* Removed stale feature flags from the platform.
* Refactored `Pax8` Integration Base Client.

</details>

<details>

<summary><strong>Deployed behind feature flags awaiting QA review and feedback</strong></summary>

* Added Generic GraphQL Request Action to the Rewst Integration.
* Google Enterprise License Manager
* Pax8 Refactor to OAuth authentication (Releasing December 21st)
* Github integration (Staff Review)
* Granular forms permissions (Staff Review)
* App Builder cloning/syncing of apps (Staff review)
* Cove integration (QA review)

</details>

<details>

<summary><strong>In code review and development</strong></summary>

* Crushbank integration (Code review)
* SQL Database integration refactor (Code review)

</details>
