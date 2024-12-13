# December 13, 2024 - Dev Update

Explore what new changes the Dev team has deployed in the last week!

This can be anything from new features, bug fixes, or QoL changes!

<details>

<summary><strong>New features and items</strong></summary>

* Bitdefender integration
* ConnectSecure v4 integration

- Customize app favicons with a URL.
- Improved name and domain validation during app creation.
- Show custom domains in the App Builder editor page header.
- Enhanced JSON mode support for OpenAI integration models.

* Configurable page size and max pages for custom integrations.
* Google Workspace OAuth tokens now included in refresh jobs.
* New context variable support for engine URLs to support new Rewst regions.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Fixed refresh options and suggest values for BitDefender, Xero, Addigy, Webroot, and DNS filter
* Removed SAS token from request when it's part of the URL to prevent failures
* Fixed pagination in Tiongard Get Metric Values V2
* Fixed crashing options gen form fields
* Prevented custom input on form drop down passing null values
* Fixed issues with the `clean_request_kwargs` function in the Kaseya BMS integration
* Prevented issue where initial login of forms users was thrwing 403 error
* Added light mode fixes for the Microsoft bundle integration page.
* Allow for adding text fields to App Builder pages via page navigator.
* Various fixes for App themes
* Added missing completed workflow context during workflow-re-run.
* Fixed org mapping of Connectwise PSA in non US-east regions.
* Fixed bug preventing disabling cloned triggers in EU region.
* Updated `response_format` in New OpenAI API handling.
* Allow users to change org vars from General to Secret category.
* Fixed `max_pages`issue with custom integrations.
* Added missing permissions on forms from unpacked crates.
* Updated graphQL queries to fix broken domains and site statuses on change.
* Dynamic scope configuration added for Google Workspace Admin.
* Updated JumpCloud and Duo tags.
* Deprecated old dashboard code
* Fixed mismatched Datto PSA actions between regions
* Improved Cronitor site monitoring
* Removed deprecated Warrant code
* Library bumps

</details>

<details>

<summary><strong>Deployed behind feature flags awaiting QA review and feedback</strong></summary>

* Google Enterprise License Manager
* Pax8 Refactor to OAuth authentication (Releasing December 14th)
* Github integration (Staff Review)
* Granular forms permissions (QA review)
* IT Portal integration (QA review)
* Cove integration (QA review)
* App Builder cloning/syncing of apps (Staff review)

</details>

<details>

<summary><strong>In code review and development</strong></summary>

* Crushbank integration (Code review)
* SQL Database integration refactor (Code review)
* Pax8 Refactor (In development)

</details>
