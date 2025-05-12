# Azure OpenAI integration setup

{% hint style="info" %}
If you’re new to integrations in Rewst, read through our introductory integration documentation [here](https://docs.rewst.help/documentation/integrations).

For our general OpenAI integration, see [this documentation](openai-integration-setup.md).&#x20;
{% endhint %}

### Azure OpenAI set up Steps in Microsoft Azure

1. Navigate to your [Microsoft Azure Portal](https://portal.azure.com).
2. Click **+Create a Resource**.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-01 (1).png" alt=""><figcaption></figcaption></figure>

3. Search for `Azure OpenAI`.
4. Click the tile for **Azure OpenAI**.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-02.png" alt=""><figcaption></figcaption></figure>

5. Request access to the Azure OpenAI service.

{% hint style="info" %}
You must fill out a form to request access to the Azure OpenAI service
{% endhint %}

<figure><img src="../../../../../../.gitbook/assets/azure-ai-03.png" alt=""><figcaption></figcaption></figure>

6. Wait for the welcome email.

{% hint style="warning" %}
Note that activation of the service can take up to 48 hours, based on Microsoft's timelines.
{% endhint %}

<figure><img src="../../../../../../.gitbook/assets/azure-ai-04.png" alt=""><figcaption></figcaption></figure>

7. Return to the Azure Portal upon receiving the approval email.
8. Create the OpenAI Service in your Azure subscription.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-05.png" alt=""><figcaption></figcaption></figure>

9. Navigate to **Resource Management > Model deployments**.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-06.png" alt=""><figcaption></figcaption></figure>

10. Click **+Create a new Deployment**.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-07.png" alt=""><figcaption></figcaption></figure>

11. Choose **gpt-35-turbo model**.
12. Name the deployment **`gpt-35-turbo model.`**

<figure><img src="../../../../../../.gitbook/assets/azure-ai-08.png" alt=""><figcaption></figcaption></figure>

13. Return to the OpenAI Resource in the Azure Portal.
14. Navigate to **Keys and Endpoint**.
15. Copy a Key to your clipboard
16. Copy the region and endpoint and store them in a safe location. You'll need it to craft for your Base URL in Rewst.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-09.png" alt=""><figcaption></figcaption></figure>

### **Set up steps in Rewst**

If you have not yet set up the OpenAI integration in Rewst, follow our integration setup steps in Rewst in our general [OpenAI integration setup guide](openai-integration-setup.md).

### Configure Azure OpenAI with existing OpenAI integrations

If you already have an OpenAI integration configured, you can add an instance for Azure.

1. Navigate to the integration's configuration page by navigating to **Configuration > Integrations > OpenAI**.
2. Click **Default** **> Add Configuration**.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-10.png" alt=""><figcaption></figcaption></figure>

2. Name the configuration `Azure`.
3. Confirm that your Base URL reflects the accurate resource and region collected from Azure. Incorrect URLs will prevent Rewst from accessing the OpenAI service.
4. Enter the **Azure API Version**.

{% hint style="warning" %}
### Crafting the Base URL

The Base URL is what directs Rewst to communicate with the correct Azure OpenAI instance. Here’s how to construct it:

**Anatomy of the Base URL**: The standard structure of the Base URL provided by Azure typically looks like this: `https://<resource-name>.openai.azure.com/openai/deployments/<deployment-name>`

* If you are using GPT 3.5 Turbo, for example, you will append it to the URL like so: `https://<resource-name>.openai.azure.com/openai/deployments/gpt-35-turbo`

**Customize Your Base URL**: Depending on your service instance or specific requirements, you may need to alter the base URL. For example:

* If you have a custom deployment named `custom-model`, you might append it to the URL like so: `https://<resource-name>.openai.azure.com/openai/deployments/<custom-model>`
* Ensure you replace `<resource-name>, <deployment-name>, and/or` `<custom-model>` with the actual information from your Azure OpenAI service.
{% endhint %}

<figure><img src="../../../../../../.gitbook/assets/azure-ai-11.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
You must complete the Azure API Version field, otherwise, the integration will fail.
{% endhint %}

### Configure workflow triggers to use Azure OpenAI

If this is your second instance of OpenAI, meaning you configured the direct OpenAI integration before, then you may adjust your workflow triggers to choose which version of the integration you want to use in your workflows.

1. Navigate to the integration's configuration page by navigating to **Configuration > Integrations > OpenAI**.
2. &#x20;Find **Integration Overrides** under **Trigger Configuration**.
3. **Click** ![](<../../../../../../.gitbook/assets/Screenshot 2025-03-13 at 6.14.27 PM.png>).
4. Choose **OpenAI** in the **Integration** drop-down selector.
5. Choose which of your your OpenAI integration instances to use in the **Integration Configuration** drop-down selector.

<figure><img src="../../../../../../.gitbook/assets/azure-ai-12.png" alt=""><figcaption></figcaption></figure>
