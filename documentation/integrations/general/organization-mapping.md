# Organization mapping

## What is organization mapping?

_Organization mapping_ is the process of connecting each Rewst integration with your child organizations, enabling automations that leverage that integration to work for your customers.

{% hint style="warning" %}
Organization mapping for Microsoft integrations is slightly different than the process outlined on this page. Refer to the video on mapping and consenting organizations for the Microsoft Cloud bundle.
{% endhint %}

## How to complete the organization mapping process

The general steps to map each organization are as follows.

{% stepper %}
{% step %}
### Access the integration setup

Navigate to **Configuration > Integrations** in the Rewst platform.

Select the integration that you want to map.
{% endstep %}

{% step %}
### Fetch customer accounts

Scroll down the page to the **Organization Mapping** submenu. Here you'll see your **Organizations** listed in a table.\


<figure><img src="../../../.gitbook/assets/Screenshot 2025-02-21 at 10.48.43 AM.png" alt="An image of the organizational mapping sub menu inside an integration. It contains four columns across a page with customer information."><figcaption><p>An example of the Organization Mapping sub menu, in an installed integration's configuration page</p></figcaption></figure>

Click **Refresh Options** to pull customer accounts from your integration.&#x20;

If the blank text box turns into a dropdown field, the sync was successful.

If accounts are missing:&#x20;

* Check if the customer account exists in your integrated tool.
* Adjust any applied filters that might be excluding accounts.
{% endstep %}

{% step %}
### Perform organization mapping

Click **Suggest Values**. Rewst will try to match organization names automatically.

Review the suggestions to ensure that organizations in Rewst and customer names in the integrated tool are aligned.

If a match is missing, manually select the correct organization from the dropdown menu.
{% endstep %}

{% step %}
### Final review and save

Double-check all mappings, especially if you have multiple pages of organizations. By default, only the first 10 organizations will be listed.

Click **Save Mappings** to finalize the connections.
{% endstep %}
{% endstepper %}
