---
description: >-
  This document outlines the requirements and setup for Rewst's Pax8
  integration.
---

# Pax8 integration setup

{% hint style="info" %}
If you’re new to integrations in Rewst, read through our introductory integration documentation [here](https://docs.rewst.help/documentation/integrations).
{% endhint %}

{% hint style="success" %}
**This Integration supports multiple instances**

[Check out the instructions to set up multiple instances here](../../../multi-instance-integration/multi-instance-integration-setup.md)
{% endhint %}

## **What does the Pax8 integration do?**

Our Pax8 integration allows MSPs to automate license procurement and billing reconciliation processes. By integrating Pax8 with Rewst, you can streamline operations, reduce manual tasks, and enhance accuracy in billing and license management.

### Why use the Pax8 integration?

* Automate the procurement of licenses for various services.
* Streamline billing reconciliation processes to ensure accurate invoicing.
* Reduce manual data entry and associated errors in license management.
* Enhance operational efficiency by integrating Pax8's offerings into Rewst workflows.

## Integration prerequisites

* An active Pax8 partner account with administrative privileges
* Access to the Rewst platform with administrative rights
* Ensure that your Pax8 account is set up for API access

## Set up the Pax8 integration

### Set up steps in Pax8

1. Log in to your Pax8 partner account.
2. If required, generate an API access token. Refer to Pax8's [API documentation](https://devx.pax8.com/) for detailed instructions.
3.  Click on your user profile name in the top right of the screen and select **Integrations**.\
    \


    <figure><img src="../../../../../.gitbook/assets/image (28) (1).png" alt=""><figcaption></figcaption></figure>
4.  Click Create.\


    <figure><img src="../../../../../.gitbook/assets/image (29) (2).png" alt=""><figcaption></figcaption></figure>
5.  Name your integration something recognizable, such as `Rewst API`.\
    \


    <figure><img src="../../../../../.gitbook/assets/image (30) (1).png" alt=""><figcaption></figcaption></figure>
6.  Copy your Client ID and Client Secret. You’ll need both to complete setup steps in Rewst.\


    <figure><img src="../../../../../.gitbook/assets/image (31) (1).png" alt=""><figcaption></figcaption></figure>

### Set up steps in Rewst

1. Navigate to **Configuration > Integrations** in the left side menu of your Rewst platform.
2. In the Integrations page, search for the **Pax8** integration.\
   \
   ![](<../../../../../.gitbook/assets/image (27) (1).png>)
3. Click on the integration tile to launch setup.
4. Enter your copied **Client ID** and **Client Secret** into their relevant fields.
5. Leave **Is Default** checked to on.
6. Click the **Authorize** button.
7. If prompted, log in to your Pax8 account by entering your username, password, and one-time code.
8.  Accept the authorization request. You'll know that the integration was successfully installed if you now see an option to **ReAuthorize**.\
    \


    <figure><img src="../../../../../.gitbook/assets/image (32) (1).png" alt=""><figcaption></figcaption></figure>

## Test the Integration

1.  After completing the setup, create a test workflow in Rewst that utilizes a Pax8 action, such as retrieving a list of licenses.\
    \


    <figure><img src="../../../../../.gitbook/assets/image (34) (1).png" alt=""><figcaption><p>An example of what your test workflow might look like</p></figcaption></figure>
2. Run the workflow and verify that it successfully interacts with your Pax8 account, confirming that the integration is functioning correctly.

## Crates related to the Pax8 integration

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><strong>Microsoft: User Onboarding</strong></td><td><a href="../../../../../.gitbook/assets/Screenshot 2025-03-12 at 10.11.58 AM.png">Screenshot 2025-03-12 at 10.11.58 AM.png</a></td></tr><tr><td><strong>Microsoft: User Offboarding</strong></td><td><a href="../../../../../.gitbook/assets/User offboarding (1).png">User offboarding (1).png</a></td></tr><tr><td><strong>Alert on Unused M365 Licenses</strong></td><td><a href="../../../../../.gitbook/assets/Screenshot 2025-03-12 at 10.12.26 AM.png">Screenshot 2025-03-12 at 10.12.26 AM.png</a></td></tr></tbody></table>

## Troubleshoot the **Pax8** integration

### **Authorization Issues**

If you encounter problems during authorization, ensure that your Pax8 credentials are correct and that your account has the necessary API access permissions.

### **API Connection Errors**

Verify that there are no network issues preventing Rewst from connecting to Pax8's API endpoints.

### **Data Retrieval Problems**

Ensure that the data you are trying to access in Pax8 exists and that your account has the appropriate permissions to retrieve it.

## Pax8 actions and endpoints

{% hint style="info" %}
For more on how actions work in Rewst, check out our [introductory actions documentation here](https://docs.rewst.help/documentation/workflows/actions-in-rewst).
{% endhint %}

Ensure that you have the necessary permissions and correct endpoint URLs as specified in Pax8's [API documentation](https://devx.pax8.com/docs/introduction) when configuring these actions.

| Action Name                   | Description                                                                                                                                                                        | Endpoint Related to Action                                                                                                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cancel subscription           | Cancels the Subscription specified by subscriptionId                                                                                                                               | <p>DELETE<br><a href="https://api.pax8.com/v1/subscriptions/%7BsubscriptionId%7D">https://api.pax8.com/v1/subscriptions/{subscriptionId}</a></p>                          |
| Create Company                | Creates a new Company. The Company will be placed in an “inactive” status until the Company has primary Contacts added. Once contacts are added, the company will move to “active” | <p>POST<br><a href="https://api.pax8.com/v1/companies">https://api.pax8.com/v1/companies</a></p>                                                                          |
| Create order                  | Create a new order. Currently NOT supported for scheduled orders (orders with a future date)                                                                                       | <p>POST<br><a href="https://api.pax8.com/v1/orders">https://api.pax8.com/v1/orders</a></p>                                                                                |
| Get company                   | Returns a single company record matching the companyId you specify                                                                                                                 | <p>GET<br><a href="https://api.pax8.com/v1/companies/%7BcompanyId%7D">https://api.pax8.com/v1/companies/{companyId}</a></p>                                               |
| Get company contact           | Returns a contact matching the companyId and contactId you specify                                                                                                                 | <p>GET<br><a href="https://api.pax8.com/v1/companies/%7BcompanyId%7D/contacts/%7BcontactId%7D">https://api.pax8.com/v1/companies/{companyId}/contacts/{contactId}</a></p> |
| Get order                     | Returns the Order record specified by OrderId. Currently NOT supported for scheduled orders (orders with a future date).                                                           | <p>GET<br><a href="https://api.pax8.com/v1/orders/%7BorderId%7D">https://api.pax8.com/v1/orders/{orderId}</a></p>                                                         |
| Get product                   | Returns only the product record for the productId you specify                                                                                                                      | <p>GET<br><a href="https://api.pax8.com/v1/products/%7BproductId%7D">https://api.pax8.com/v1/products/{productId}</a></p>                                                 |
| Get product provision details | Returns provisioning details for the specified productId. Provisioning details for a product are dynamic data.                                                                     | <p>GET<br><a href="https://api.pax8.com/v1/products/%7BproductId%7D/provision-details">https://api.pax8.com/v1/products/{productId}/provision-details</a></p>             |
| Get subscription              | Returns the Subscription record specified by the subscriptionId                                                                                                                    | <p>GET<br><a href="https://api.pax8.com/v1/subscriptions/%7BsubscriptionId%7D">https://api.pax8.com/v1/subscriptions/{subscriptionId}</a></p>                             |
| List companies                | Returns a paginated list of all your companies filtered by optional parameters                                                                                                     | <p>GET<br><a href="https://api.pax8.com/v1/companies">https://api.pax8.com/v1/companies</a></p>                                                                           |
| List company contacts         | Returns a paginated list of contacts ordered by createDate descending                                                                                                              | <p>GET<br><a href="https://api.pax8.com/v1/companies/%7BcompanyId%7D/contacts">https://api.pax8.com/v1/companies/{companyId}/contacts</a></p>                             |
| List orders                   | Returns a paginated list of orders. Currently NOT supported for scheduled orders(orders with a future date).                                                                       | <p>GET<br><a href="https://api.pax8.com/v1/orders">https://api.pax8.com/v1/orders</a></p>                                                                                 |
| List products                 | Returns a paginated list of Pax8 products filtered by optional query parameters                                                                                                    | <p>GET<br><a href="https://api.pax8.com/v1/products">https://api.pax8.com/v1/products</a></p>                                                                             |
| List subscriptions            | Fetch a paginated list of subscriptions. Default page is 0 and default size is 10. The maximum page size is 200                                                                    | <p>GET<br><a href="https://api.pax8.com/v1/subscriptions">https://api.pax8.com/v1/subscriptions</a></p>                                                                   |
| Update subscription           | Updates a subscription. Currently NOT supported for subscriptions with a future date.                                                                                              | <p>PUT<br><a href="https://api.pax8.com/v1/subscriptions/%7BsubscriptionId%7D">https://api.pax8.com/v1/subscriptions/{subscriptionId}</a></p>                             |

{% hint style="info" %}
Got an idea for a new Integration? Rewst is constantly adding new integrations to our integrations page. Submit your idea or upvote existing ideas here in our [Canny feedback collector](https://rewst.canny.io/integrations).
{% endhint %}

