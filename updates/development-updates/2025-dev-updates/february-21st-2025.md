# February 21, 2025 - Dev update

Explore what new changes the Dev team has deployed in the last week!

This can be anything from new features, bug fixes, or QoL changes!

<details>

<summary><strong>New features and items</strong></summary>

* **Support Access**\
  Allows users to enable/disable Rewst staff write access to their organization
* **Custom Integration Pre-Processing**\
  Removed the “vacuum” step in Custom Integration integrations to optimize performance.
* **Move Custom Integration Actions Between Categories**\
  Allows Custom Integration Actions to be reorganized under different Marketplace categories.
* **App Builder Element Name UI/UX Improvements**\
  Improved the user interface for naming elements within apps.
* **Performance improvements** \
  By moving certain elements of the workflow execution “conductor” into dedicated tables, we reduce row sizes in the WorkflowExecution table, improve performance, and make it easier to query data. These changes aim to enhance scalability and reduce locking overhead for faster workflow processing.
* **Easier Time-Saved Management**\
  Made the “Time Saved” field simpler to view and edit in the Workflows page.
* **Defang/Refang Jinja Filters**\
  Enhanced security workflows with the ability to automatically obfuscate (“defang”) or restore (“refang”) data as needed.
* **SynnexAu Integration Update**\
  Repointed the base URL to the updated production endpoint, ensuring more reliable connectivity.
* **Public Crates API**\
  Introduced a new Public Crates API and supporting fields to pave the way for improved crate documentation and communication.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* **Data Source & Table Columns**\
  Fixed issues with missing or mismatched column definitions that could cause data errors in apps.
* **Page Builder & Forms**\
  Addressed infinite recursion in linked node properties, corrected dropdown and regex handling, and improved error messaging for required fields and file uploads.
* **Sub-Org Marketplace Access**\
  Ensured that sub-org users have proper access to CI v2 actions while preventing overly long descriptions from causing UI breakage.
* **Action Dialog Data**\
  Confirmed dialogs always retrieve the latest data when confirming actions.
* **Crate Exports & Replication**\
  Fixed token-related errors and ensured triggers, completion handlers, and maturity links are all included in exported crates.
* **Google Workspace & Other Integrations**\
  Improved error handling for empty result sets and enforced required fields for various third-party integrations.
* **Pagination & Filtering**\
  Corrected totalCount calculations for more accurate pagination and allowed additional filtering options in workflow executions.
* **Support Access & App Builder**\
  Tightened support access checks so only authorized users or roles can request assistance, and improved re-render logic, domain-based logout, and chart displays in App Builder.
* **DevOps & Backport Workflows**\
  Refined automated processes for backporting changes to QA branches, ensuring consistent release management and clearer PR labeling.
* **Engine Configuration & Logging**\
  Increased retry/backoff factors for more robust error recovery and introduced structured (JSON) logging in non-local environments, with text logs for local development.
* **Integration Aliasing & Default Values**\
  Improved how custom integrations export, adding aliasing and default value extraction for CI v2 actions.
* **Dependency Updates**\
  Removed certain TailwindCSS preflight settings, temporarily downgraded versions to fix styling issues, and updated several libraries (e.g., cookies-next, deepmerge, export-to-csv, axios) for security and performance.

</details>

<details>

<summary><strong>Coming Soon</strong></summary>

* Generic GraphQL Request Action to the Rewst Integration
* Granular forms permissions
* SyncMonkey integration
* Support Access logs
* Workflow executions dashboard widget

</details>
