# Find Inactive Computers in RMM Crate

{% hint style="info" %}
If you’re new to Crates, read through our introductory Crate documentation [here](https://docs.rewst.help/prebuilt-automations/crates). Find the Crate in our Crate Marketplace.
{% endhint %}

## What does the Find Inactive Computers in RMM Crate do?

Our Find Inactive Computers in RMM Crate identifies endpoints in the RMM platform that have not checked in within a specified time window. It helps you maintain an accurate view of active devices by highlighting machines that may be offline, decommissioned, or otherwise stale.

### How the Crate works

* Defines how long a device can be offline before being considered stale
* Removes the need for manual stale device audits
* Notifies the appropriate team or technician by creating a detailed service ticket
* Keeps RMM inventory accurate and useful by surfacing forgotten or decommissioned endpoints

The Crate is typically triggered by a scheduled cron trigger, which allows for regular check-ins.

## Unpack the Find Inactive Computers in RMM Crate

1. Navigate to **Crates** > **Crate Marketplace** in the left side menu Rewst platform.
2.  Search for `Find Inactive Computers in RMM`.

    \
    ![](<../../../.gitbook/assets/image (223).png>)
3. Click on the Crate tile to begin unpacking.
4. Click **Unpack Crate**.
5. Click **Continue**.
6. Ensure that **Enabled** is toggled on for the **Cron Job** accordion menu under **Configure Triggers**. Note that you have the option to activate the Crate for all future organizations in addition to the current one. You may also set activation to certain [tags](../../settings/tags-in-rewst.md), and set [trigger criteria](../../automations/intro-to-triggers/trigger-criteria.md) or [integration overrides](../../automations/intro-to-triggers/).
7. Click **Unpack**.

### Use the Crate

1. Navigate to **Automations > Forms** in the left side menu of your Rewst platform.
2. Search for `Get Form Links and Add to Ticket`.
3. Click **⋮ > Usages > View Direct URLs.**
4. Click on the link for the organization which contains the user you wish to manage. This will launch the form in a new tab.
5. Choose the organization you'd like to run the form on from the **Organization** drop-down selector.\
   \
   ![](<../../../.gitbook/assets/image (196).png>)
6. Click **Submit** to run the workflow. The workflow will run and automatically add notes to your PSA with the results of the software operation.

### Adjust the cron trigger

#### Test the Crate

To test this Crate, you'll need to adjust the cron trigger's schedule to a few minutes in the future, then adjust it back to your regular schedule after the test. Alternatively, you could wait until the regularly scheduled run occurs and check your result, which would not require you to update the cron trigger schedule.

1. Navigate to **Automations > Workflows** in the left side menu of your Rewst platform.
2.  Search for `[REWST - CRATE] RMM: Find Inactive Computers`.\


    <figure><img src="../../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>
3.  Click on the workflow to view it in the Workflow Builder.



    <figure><img src="../../../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure>
4. Adjust the cron trigger's schedule to five minutes from your current time. The workflow will run on its own. Check in your RMM's portal to ensure that the workflow is able to find the inactive computers as expected.

#### Update the cron trigger schedule

The Crate runs on a cron trigger, and will execute the workflow to generate the ticket at the same time each day. You can adjust the chosen time for execution in the workflow itself. To edit a cron trigger in the workflow to change the timing it will routinely run:

1. Navigate to **Automations > Workflows**.
2. Search for  `[REWST - CRATE] RMM: Find Inactive Computers`.
3. Click on the workflow to open it in the workflow builder.
4.  Click <img src="../../../.gitbook/assets/image (189).png" alt="" data-size="line"> to open the edit trigger menu.



    <figure><img src="../../../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>
5. Update the timing of the cron trigger as desired in the fields under **Trigger Parameters**. Note that when entering the time into the **Cron Schedule** field, the correct format is minutes followed by hour. For example, 18 3, not 3 18.
6. Click **Submit**.

{% hint style="info" %}
Got an idea for a new Crate? Rewst is constantly adding new Crates to our Crate Marketplace. Submit your idea or upvote existing ideas here in our [Canny feedback collector](https://rewst.canny.io/crates).
{% endhint %}
