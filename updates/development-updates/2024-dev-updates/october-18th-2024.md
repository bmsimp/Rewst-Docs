# October 18th, 2024

Explore what new changes the Dev team has deployed in the last week!

This can be anything from new features, bug fixes, or QoL changes!

<details>

<summary><strong>New features and items</strong></summary>

* New Org Picker
* Added new triggers for Webroot
* Added a new jinja filter `is_json` to test if a string is json serializable
* Added a new slack action to invite users to slack
* Added a trigger for Rewst Crate publish

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Fixed a bug where saving new variables to a workflow were being reverted on the UI despite being saved to the database
* Fixed a crate unpacking bug when the crate contains secret_key fields
* Added a flag to integrations to allow the public website to determine if the integration should be shown on the website or not
* Fixed login pages for App Platform so they respect the global theme for the app
* Fixed a performance issue with forms that have a large number of activated orgs load very slow
* Fixed a bug in App Platform that was causing the App and Page list screens to crash
* Refactored and improved the Datto RMM integration
* Fixed an unhandled exception with toast error messages in Custom Integrations v2
* Updated Custom Integrations v2 to prevent changing the runner_type or entry_point parameters which would break the integration
* Changed the Rewst Create Org Variable action to be an upsert instead of create to prevent errors in cases where the org var already exists
* Added a fallback to prevent canceled workflows from becoming stuck in the "canceling" status
* Fixed a bug with graphQL caching implementation
* Fixed Synnex AU authentication headers
* Fixed a bug in Custom Integrations v2 where query parameters were being ignored
* Allow generic api actions to provide an override url to fix an issue with Liongard
* Fixed padding for option generated drop down fields
* Fixed parameters for Create and Update Network actions for DNSFilter integration
* Increased the max page size for Liongard
* Fixed the following actions for Synnex AU: Check Domain Availability, Purchase Addon Plans CSP, Get Google Workspace Domain Availability, and Purchase Addon for Google Workspace
* Updated the `to_human_time_from_seconds` jinja filter to not round floats
* JSON RPC Base Client

</details>

<details>

<summary><strong>Deployed behind feature flags awaiting QA review and feedback</strong></summary>

* Multi-player workflows V1 (Launching soon)
* Bitdefender integration (QA review)
* Granular forms permissions (QA review)
* IT Portal integration (QA review)
* Synnex Australia integration (QA review)
* Cove integration (QA review)
* Github integration (QA Review)
* App Platform page export/import functionality

</details>

<details>

<summary><strong>In code review and development</strong></summary>

* Crushbank integration (Code review)
* Nodeware integration (Code review)
* SQL Database integration refactor (Code review)
* ConnectSecure v4 (In development)
* Pax8 Refactor (In development)

</details>
