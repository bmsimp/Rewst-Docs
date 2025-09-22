# Reset Locked Accounts Crate

{% hint style="info" %}
If you’re new to Crates, read through our introductory Crate documentation [here](https://docs.rewst.help/prebuilt-automations/crates). Find the Crate in our Crate Marketplace.
{% endhint %}

## What does the Reset Locked Accounts Crate do?

The Reset Locked Out Accounts Crate automates the process of unlocking user accounts and resetting passwords for organizations in Rewst. It ensures seamless account recovery by verifying locked-out accounts, updating credentials, and creating or updating support tickets if an existing ticket is provided.

This Crate does not send email notifications to users or administrators.

### How the Crate works

1. The workflow collects organization name, email, and new password via form submission from the user.
2. The workflow checks Active Directory and identifies if the user account is locked.
3. It updates the account with the provided new password and restores user access by removing the account lock.
4. If an existing ticket is provided, it is updated. Otherwise, a new ticket is created.
5. Via activity log, it maintains a record of all actions for security auditing.

### Crate prerequisites

* The [Microsoft Cloud Integration Bundle](../../configuration/integrations/integration-guides/microsoft-cloud-integration-bundle/) must be set up before unpacking this Crate.
* This Crate requires one of the following PSA integrations:
  * [Kaseya BMS](../../configuration/integrations/integration-guides/kaseya-bms-integration-setup.md)
  * [ConnectWise PSA](../../configuration/integrations/integration-guides/connectwise-integration-setup.md)
  * [Freshdesk](../../configuration/integrations/integration-guides/freshdesk-integration-setup.md)
  * [SuperOps](../../configuration/integrations/integration-guides/superops-integration.md)

## Unpack the Reset Locked Accounts Crate

1. Navigate to **Crates > Crate Marketplace** in the left side menu of the Rewst platform.
2. Search for `Reset Locked Accounts`**.**\
   \
   ![](<../../../.gitbook/assets/Screenshot 2025-09-22 at 11.00.42 AM.png>)\

3. Click on the Crate tile to begin unpacking.
4. Click **Continue**.
5. Note that you have the option under the **Form Submission** accordion menu to activate the Crate for all future organizations in addition to the current one. You may also set activation to certain [tags](https://docs.rewst.help/documentation/settings/tags-in-rewst), [trigger criteria](../../automations/intro-to-triggers/trigger-criteria.md), or for integration overrides.
6. Ensure that **Enabled** is toggled on.
7. Click **Unpack**.

## Use the Crate

1. Navigate to **Automations > Forms** in the left side menu of your Rewst platform.
2. Search for `[REWST - CRATE] Reset Locked-Out Accounts`.
3. Click **⋮ > Usages > View Direct URLs**.
4. Click on the link for the organization which contains the user you wish to manage. This will launch the form in a new tab.
5. Select the org you want to reset authentication for via the **Organization** drop-down selector.
6. Choose your ticket from the **Existing Ticket** drop-down selector list, or leave the field empty to create a new ticket.
7. Select the locked-out user from the **Account** list.
8. Select or type a new password for the user in the **New Password** field.
9. Check **New Password Is Temporary** if you want the user to be required to enter a new password when they log in.
10. Check **Add New Password to Ticket Notes** to add the new password to the notes section of the ticket in your PSA.
11. Click **Submit**.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-09-22 at 11.21.05 AM.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Got an idea for a new Crate? Rewst is constantly adding new Crates to our Crate Marketplace. Submit your idea or upvote existing ideas here in our [Canny feedback collector](https://rewst.canny.io/crates).
{% endhint %}
