# IT Glue integration setup

{% hint style="success" %}
**This Integration supports multiple instances**

[Check out the instructions to set up multiple instances here](../../general/multi-instance-integration/multi-instance-integration-setup.md).
{% endhint %}

{% hint style="warning" %}
IT Glue's API access is limited to users of the legacy **Classic** (pre 2018) and **Enterprise** level plans only. See **\[yourdomain].itglue.com/account/plan** for details on your organization's plan and usage.

For more information on IT Glue's plans and pricing review the [IT Glue pricing page](https://www.itglue.com/pricing/).
{% endhint %}

Integrating Rewst with IT Glue brings powerful documentation capabilities to your applications, enhancing IT knowledge management and streamlining workflows. With the integration, Rewst users can seamlessly access and collaborate on IT Glue's documentation repository, gaining centralized access to critical information, configurations, and processes. By leveraging IT Glue's robust documentation features, Rewst users can improve efficiency, ensure consistency, and enhance IT service delivery. This integration empowers IT teams to leverage the collective knowledge and expertise stored in IT Glue, enabling them to troubleshoot issues, onboard new team members, and deliver exceptional IT support through Rewst's integrated platform.

## Setup

1. **Generate** an API key in IT Glue by referring to the [IT Glue documentation](https://helpdesk.kaseya.com/hc/en-gb/articles/4407484149265-Getting-started-with-the-IT-Glue-API).
2. **Navigate** to the integrations page in Rewst.
3. **Click** on the IT Glue integration.
4. **Fill out** the configuration form.
5. **Click** on the Save Configuration button.

## Generating an API key

All API endpoints require authentication using a private API key. You can generate one or more API keys for your account. To generate a new API key:

Generate an API key in IT Glue by referring to their guide [here](https://help.itglue.kaseya.com/help/Content/1-admin/it-glue-api/getting-started-with-the-it-glue-api.html?cshid=1038).

In the IT Glue console:

1. Navigate to **Admin > Settings**
2.  Click the **API keys** tab\


    <figure><img src="../../../../.gitbook/assets/Screenshot 2025-01-28 at 6.30.03 PM.png" alt=""><figcaption></figcaption></figure>
3. Scroll to bottom and click the **+** on the right side
4. Enter a **name** for the API key
5.  Click **Generate API key**\


    <figure><img src="../../../../.gitbook/assets/Screenshot 2025-01-28 at 6.30.43 PM.png" alt=""><figcaption></figcaption></figure>
6. Check the **Password Access** box
7. Copy and Save the API key - you will not be able to view the API key again once it has been generated



## Integration setup in Rewst

1. Log in to the Rewst platform.
2.  Navigate to **Configuration > Integrations**.\


    <figure><img src="../../../../.gitbook/assets/Screenshot 2025-01-28 at 6.26.06 PM.png" alt=""><figcaption></figcaption></figure>
3. Locate and click on the IT Glue integration.
4. Complete the configuration:
   1. Name
   2. Description (Optional)
   3. Is Default checked or unchecked
   4. API Key copied from IT Glue platform
   5. Base URL for IT Glue environment (Region based from drop down)
   6. Use Rewst IP Address: Select True or False
5. **Save** the configuration.
