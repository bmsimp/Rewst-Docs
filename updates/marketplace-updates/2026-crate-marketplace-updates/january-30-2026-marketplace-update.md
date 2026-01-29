# January 30, 2026 - Marketplace update

<details>

<summary><strong>New Crates</strong></summary>

No new Crates were released this week.&#x20;

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

### Crates

* [Microsoft: User Onboarding](../../../documentation/crates/existing-crate-documentation/microsoft-user-onboarding-crate-v2/)
  * Align license\_subscription variable naming with form and subworkflow
  * Uncheck create\_contact\_in\_psa by default when Advanced PSA Options is hidden
* [Configure Organizational Variables](../../../documentation/crates/existing-crate-documentation/configure-organization-variables.md)
  * Rename Datto PSA references/workflow names to Autotask
* [Time Savings Report](../../../documentation/crates/existing-crate-documentation/time-savings-report-crate.md)
  * Rename variable configs and set cron defaults to avoid overriding form inputs
* [Configure Out Of Office on Mailbox](../../../documentation/crates/existing-crate-documentation/configure-out-of-office-on-mailbox-crate.md)
  * Update run-as org Jinja for create\_ticket action (76165)
* [Alert on Low Disk Space](../../../documentation/crates/existing-crate-documentation/alert-on-low-disk-space-crate.md)
  * Add pre-check so generate\_tickets runs only when drives\_low\_freespace is not empty
* [Alert on Login from Non-Native Country](../../../documentation/crates/existing-crate-documentation/alert-on-login-from-non-native-country-crate.md)
  * Fix description to correctly reference the crate in docs (77942)
* [Amend Calendar Permission on User](../../../documentation/crates/existing-crate-documentation/amend-calendar-permission-on-user-crate.md)
  * Add default board ID to M365 Set Calendar Permissions create ticket action (76744)

### Subworkflows

* \[REWST - TASK] CW Control: Run Powershell - used by every Crate that works with RMM integrations
  * Add logging to check\_if\_device\_name\_id and old\_find\_session\_groups (68616)



</details>

<details>

<summary><strong>Coming soon</strong></summary>

REWST Conditional Access Policy Assistant Crate

</details>
