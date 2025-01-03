# January 3rd, 2025 - Marketplace Update

Explore the new changes to the Marketplace in the last week!

This can be anything from new crates, enhancements, or bug fixes!

<details>

<summary><strong>New crates and enhancements</strong></summary>

* [Google Workspace User Onboarding](https://app.rewst.io/marketplace/crates/0193d4e1-2a5c-7b77-b8a4-f636e7b044a3)
* [Google Workspace User Offboarding](https://app.rewst.io/marketplace/crates/01942d85-e360-796e-ac09-9acfbe0b5bbb)
* App Builder Apps (available by request to the ROC or your CSM only, not in the Crate Marketplace)
  * Operational Analytics Portal - aggregates data from various tools and outputs actionable insights for MSPs to further streamline operations.
  * Forms Portal - allows employees and clients to easily access the necessary Rewst forms based on granular permissions.
  * All-In-One Client Portal - The portal transforms service delivery by empowering clients to instantly self-serve common IT requests —not just submit tickets.

</details>

<details>

<summary><strong>Bug fixes and chores</strong></summary>

* Detailed MFA Reporting
  * In multiple data aliases, added jinja checks to make sure the response object exists.
  * Added boolean input of `no_reporting` and outputs of `success` and `per_user_data`(list) to make crate workflow useable as subworkflow.
* User Offboard V2
  * Accounted for form output indicating that it was unable to retrieve users for entra when running onprem only.
* GWS: User Onboard / Offboard
  * Fixed bad references causing time to always evaluate as UTC now (and never delay).
  * Made references match the inputs. Removed timezone conversions on delay\_time and check\_delay aliases.
  * Made new alias to create a vanity DT object to feed into ticketing with the timezone.
* New Employee Onboarding
  * Updated options generator for list subscribed products to include `Microsoft_Teams_Enterprise_New` which is no longer included in the Microsoft sku CSV.
  * Updated the license lookup JSON template for the license assignment workflow to include more skus

</details>

<details>

<summary><strong>Coming soon!</strong></summary>

* Refactor: Documenting M365 Environments (ITG/Hudu)
* Alert on Users without MFA Enforced

</details>

