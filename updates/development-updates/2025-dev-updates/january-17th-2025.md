# January 17, 2025 - Dev Update

Explore what new changes the Dev team has deployed in the last week!

This can be anything from new features, bug fixes, or QoL changes!

<details>

<summary><strong>New features and items</strong></summary>

* N-able N-sight integration
* Redesigned the chips used in workflows page
* Added functionality to remove trailing whitespace from org vars
* Updated dashboard CSV export format
* Improved description for the ‘Get Registered Storage Nodes’ Acronis action to clarify that it only works for on-premises installations.
* Enhanced messaging for the Trigger Criteria Tester
* Cloning and syncing of App Builder apps

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Fixed bug causing workflows to run twice when triggered from app builder
* Removed add page button for syncronized clones as these changes would be overwritten on sync
* Fixed ImmyBot New Computer Detected Trigger to not return all computers on initialization
* Fixed tag filtering when the tag is edited and you return to the page with the filter
* Fixed an issue with the cloning system where templates were not detected if a filter was applied to them.
* Allowed for workflows with integration overrides to be cloned
* Added missing \`forcereassign\` property to `add_or_update_tickets`HaloPSA action
* Fixed pagination for ConnectSecure V4 generic action
* Updated Ninja action for Reset Alert to accept string rather than int
* Show errors upon failure for Custom Integration actions
* Prevented tag color changes from reverting
* Fixed toast messages
* Improvements to automated test coverage
* Corrected alert inconsistency between the app details and page builder views
* Added dynamic slack scope configuration through our feature flagging tool
* Updated logging in org deletion
* Show the Slack "Authorize" button on the integration page

</details>

<details>

<summary><strong>Deployed behind feature flags awaiting QA review and feedback</strong></summary>

* Added Generic GraphQL Request Action to the Rewst Integration
* Github integration
* Granular forms permissions
* SQL database integration refactor

</details>
