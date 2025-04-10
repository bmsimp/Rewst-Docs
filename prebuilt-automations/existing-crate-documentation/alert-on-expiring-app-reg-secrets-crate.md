# &#x20;Alert on Expiring App Reg Secrets Crate

{% hint style="info" %}
If you’re new to Crates, read through our introductory Crate documentation [here](https://docs.rewst.help/prebuilt-automations/crates). Find the Crate in our Crate Marketplace.
{% endhint %}

## What does the Alert on Expiring App Reg Secrets Crate do?

Our Alert on Expiring App Reg Secrets Crate identifies any expiring client secrets in your application registrations and logs individual tickets for each client, as well as a detailed overall summary ticket. Reduce disruptions by getting notified on expiring application registration secrets.

## Crate prerequisites

* The [Microsoft Graph integration](../../documentation/integrations/individual-integration-documentation/cloud/microsoft-cloud-integration-bundle/microsoft-graph/microsoft-graph-integration-setup.md) must be set up before unpacking this Crate
* psa\_default\_board\_id organization variable
* default\_psa organization variable

## Unpack the Alert on Expiring App Reg Secrets Crate

1. Navigate to **Crates > Crate Marketplace** in the left side menu of the Rewst Platform.
2. Search for `Alert on Expiring App Reg Secrets`.\
   \
   ![](<../../.gitbook/assets/Screenshot 2025-04-10 at 4.51.31 PM.png>)
3. Click **Unpack Crate**.
4. Click **Continue.**
5.  Enter your **Time Saved**.\
    \


    <figure><img src="../../.gitbook/assets/Screenshot 2025-04-10 at 4.52.39 PM.png" alt="Screenshot of the Rewst platform showing the unpacking screen for a workflow crate titled &#x22;[Rewst Master v3] Azure: Alert on Expiring App Secrets [Part 1]&#x22;. The page displays a description: &#x22;Identify any Application Registrations that have expiring certificates and log a ticket per client, with an overall ticket with all detailed information.&#x22; Below that, there&#x27;s a &#x22;Crate Configuration&#x22; section with fields for &#x22;Workflow Name&#x22; (pre-filled), &#x22;Time Saved (seconds)&#x22; (set to 0), and a trigger configuration showing a Cron Job marked as &#x22;Enabled&#x22;. Buttons for &#x22;Previous&#x22; and &#x22;Unpack&#x22; appear at the bottom right."><figcaption></figcaption></figure>
6. Click **Unpack**.

## Test the Crate

To test this Crate, you'll need to adjust the cron trigger's schedule to a few minutes in the future, then adjust it back to your regular schedule after the test. Alternatively, you could wait until the regularly scheduled run occurs and check your result, which would not require you to update the cron trigger schedule.

1. Navigate to **Automations > Workflows**.
2.  Search for `Alert on Expiring App Client Secrets [Part 1]`.\
    \


    <figure><img src="../../.gitbook/assets/image (57) (2).png" alt="Screenshot of the Workflows page in the Rewst platform with a search for &#x22;expiring&#x22; applied. One workflow is listed: [ROC] Azure: Alert on Expiring App Client Secrets [Part 1], last updated on 2025-03-29 at 17:28. The row includes options to Configure, view Triggers (1), and Clone (Sync). A linked crate labeled Alert on Expiring App Reg Sec... is also visible. Filter icons appear under the &#x22;Updated By,&#x22; &#x22;Attributes,&#x22; and &#x22;Tags&#x22; columns. On the right, there are additional controls including a three-dot menu and a right-arrow for further actions."><figcaption></figcaption></figure>
3.  Click on the workflow to open it in the workflow builder.\
    \


    <figure><img src="../../.gitbook/assets/image (58) (2).png" alt="Screenshot of the Cron Trigger configuration for the workflow [ROC] Azure: Alert on Expiring App Client Secrets [Part 1] in the Rewst platform. The trigger type is fixed as Cron Trigger. Under Integration Overrides, three integration UUIDs are shown, with an indicator that 6 more items are hidden.  The External Status section confirms &#x22;No errors detected&#x22; with a green checkmark.  In the Trigger Parameters section:  Timezone Canonical Names is set to UTC.  Cron Schedule is 0 7 1 * *.  The parsed output for the cron expression is displayed as: &#x22;At 07:00 AM, on day 1 of the month.&#x22; Various top-bar icons are also visible for editing, syncing, and settings."><figcaption></figcaption></figure>
4. Adjust the cron trigger's schedule to five minutes from your current time. The workflow will run on its own, and tickets will be created if expiring secrets are found.

{% hint style="info" %}
Got an idea for a new Crate? Rewst is constantly adding new Crates to our Crate Marketplace. Submit your idea or upvote existing ideas here in our [Canny feedback collector](https://rewst.canny.io/crates).
{% endhint %}
