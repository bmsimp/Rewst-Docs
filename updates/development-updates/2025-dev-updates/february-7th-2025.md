# February 7, 2025 - Dev update

Explore what new changes the Dev team has deployed in the last week!

This can be anything from new features, bug fixes, or QoL changes!

<details>

<summary><strong>New features and items</strong></summary>

* Introduced support for custom HTML in SendMail, allowing more advanced email formatting
* Added success/fail stats to the GraphQL TimeSavedGroupByWorkflow endpoint for better workflow analytics
* Ensured only enabled organizations appear in the “Test as User” feature
* Show Windows shortcut keys on right click in workflow canvas
* Increased max page and page size settings for Datto PSA
* Updated Org Picker to remove “Rewst Staff” for non-staff users
* Changed estimated hours parameter in Datto PSA actions to number instead of integer

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Fixed missing Custom Integration icons in favorites menu
* Fixed note resizing issue
* Fixed Bitdefender integration issues for generic requests
* Stopped Google Workspace Admin Create Now Organizational Unit action from crashing page&#x20;
* Corrected dropped query parameters for forms users requiring log in
* Added fix for forms with empty dropdowns causing Jinja evaluation failure
* Corrected the ConnectWise Manage date formatting
* Corrected the pop-out button URL in Workflow Builder opening to Scripts rather than Templates
* Displayed boolean fields as checkboxes in forms
* Fixed error when refreshing Datto PSA Get Roles action parameter
* Removed duplicate ConnectWise PSA - Update Contact action fields for Type, which load the same information
* Fixed IT Portal Update Field for ID action name
* Updated IT Portal Update Field for ID action Value parameter to string
* Handled null values in the Workflow Builder’s TaskForm more gracefully
* Added categories to crates for upcoming searchability improvements
* Added actions for upcoming SyncMonkey integration
* Added new UI libraries&#x20;
* Removed unnecessary console warnings for cleaner logs
* Pruned workflow executions in batches to optimize database performance
* Updated integration refresh to run twice per day

</details>

<details>

<summary><strong>Coming Soon</strong></summary>

* Generic GraphQL Request Action to the Rewst Integration
* Configurable Rewst support access
* Granular forms permissions
* SyncMonkey integration

</details>
