# Intro to organizations and organization variables

{% hint style="warning" %}
#### PSA Setup **Prerequisite for Crates**

1. Integrate your PSA before using the Configure Organizational Variables crate.
2. We recommend adding the following **ticket statuses** in your PSA before using the Configure Organizational Variables form to make them available as default options:
   1. Automation in Progress (tracks ongoing automation)
   2. Automation Complete (prevents premature closure)
3. Ensure your PSA's **customer types** are set correctly, as Rewst uses them to import customers in the Bulk Add Client to Rewst crate.
{% endhint %}

## Overview of organizations and organization variables

Rewst uses a two-tier system to manage organizations, with your MSP as the parent and your customers as child organizations.&#x20;

Organization variables (_org variables_) store reusable data across workflows. To set up org variables, you can use the Configure Organizational Variables crate or configure them manually.

{% embed url="https://youtu.be/p0pYLEhPUTg?si=Kzw2r340uDcDaS6w" %}
Intro to organizations and org variables (_3:39 min_)
{% endembed %}

## Create organization variables with a crate

Use the Configure Organizational Variables crate to set up org variables for your MSP that will cascade to your child organizations by default. You'll learn how to override the defaults and create unique org variables for customers on the next page, [set-up-child-organizations.md](set-up-child-organizations.md "mention").

### Step 1: Unpack the crate

{% embed url="https://youtu.be/m8zb8X16OxU?si=yOs5YXazu8o9CA4l" %}
Unpacking the configure organizational variables crate (_1:34 min_)
{% endembed %}

### Step 2: Complete the form

{% embed url="https://youtu.be/ALgrBColujg" %}
Configuring default organization variables with a form (_6:20 min_)
{% endembed %}

## Resources

{% hint style="success" %}
Want live support? Register for **Prebuilt Crates - Organization Variables** [online group sessions](https://outlook.office365.com/book/RewstImplementation1@rewst.io/)!&#x20;

Refer to our documentation for additional guidance:

* [Rewst terminology: organizations and organization variables](https://docs.rewst.help/cluck-university/getting-started/rewst-terminology#organizations)
* [User management: Organization variables](https://docs.rewst.help/documentation/user-management/organization-variables)
* [Crate documentation: Configure Organizational Variables](https://docs.rewst.help/prebuilt-automations/existing-crate-documentation/configure-organization-variables)
{% endhint %}

<table data-view="cards" data-full-width="false"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><a href="set-up-child-organizations.md"><strong>Set up child organizations</strong></a></td><td><a href="../../../.gitbook/assets/NEXT.png">NEXT.png</a></td></tr></tbody></table>

