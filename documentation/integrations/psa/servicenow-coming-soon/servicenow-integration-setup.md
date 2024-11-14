---
description: >-
  This document outlines the requirements and setup for the ServiceNow
  integration.
---

# ServiceNow Integration Setup

{% hint style="success" %}
**This Integration supports multiple instances**

[Check out the instructions to set up multiple instances here](../../general/multi-instance-integration/multi-instance-integration-setup.md).
{% endhint %}

## Setting up the ServiceNow  account

1. **Login** to your ServiceNow account with your business credentials.
2. **Navigate** to the ServiceNow instance and find the hostname (i.e [dev12345.service-now.com](http://dev12345.service-now.com/)).
3. **Obtain** and set up ServiceNow Username and Password for that instance and place these values in the settings.

Once the above steps are completed and saved, an automatic credentials check will run and then you can start using the ServiceNow API within Rewst workflows.

## Endpoint Plugin Requirements

These endpoints requires the following plugins:

* Customer Service plugin ([com.sn](http://com.sn/)\_customerservice) + csm\_ws\_integration role and is provided within the now namespace.
* Order Management for Customer Service Management (app-csm-order-mgmt) + sn\_csm\_order\_mgmt role.
* Order Management for Telecommunications (sn\_ind\_tmt\_orm) - Optional.
* Telecommunications Assurance Workflows.
* Customer Service ([com.sn](http://com.sn/)\_customerservice).
* Customer Service Install Base Management (com.snc.install\_base).
