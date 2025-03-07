# Migrating between Crate versions

## Considerations When Migrating

When officially migrating to a newer version of a Crate, various items should be taken into consideration as part of this process. Below is a common list of actionable items to consider when migrating to v2 of the offboarding crate.

* Disabling workflow triggers for v1 of the offboarding crate
* Updating any workflow wrappers or completion handlers (aka workflow listeners) to utilize v2 of the offboarding crate
* Update references to the v1 form. For example, this may include any workflows that add form links to tickets
* Update any custom forms that currently utilize v1 to be compatible with and utilize v2

## Crate migration steps

1. Unpack the new Crate in your environment.
2. Test the setup to verify that your organizational variables are correctly configured.
   * The same org variables are used as in the previous version.
   * If updates are required, refer to the [Organizational Variables Guide](https://www.notion.so/Draft-Microsoft-User-Onboarding-Crate-Part-1-19fb56f9907180118ca4c28be86cda8a?pvs=21).
3. Once testing is complete, transition to the new workflow:
   * If using the new form:
     * Disable form triggers in the previous onboarding workflow.
     * Update internal documentation with the new form URL.
     * If necessary, provide customers with the new onboarding form link.
   * If keeping the previous form linked:
     * The previous form can be linked to this version, but will not receive future updates.
     * Rewst will only maintain this version moving forward.
