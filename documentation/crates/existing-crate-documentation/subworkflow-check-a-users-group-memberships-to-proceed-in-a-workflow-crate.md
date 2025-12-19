# Subworkflow: Check a User's Group Memberships to Proceed in a Workflow Crate

{% hint style="info" %}
If you’re new to Crates, read through our introductory Crate documentation [here](https://docs.rewst.help/prebuilt-automations/crates). Find the Crate in our Crate Marketplace.
{% endhint %}

## What does the Subworkflow: Check a User's Group Memberships to Proceed in a Workflow Crate do?

The Crate uses the Microsoft Graph API Request action to get all groups a user belongs to.

1. Makes a GET request to the Microsoft Graph API
2. The response will include all groups the user is a member of
3. Checks if your target group is in the returned list

## Example Jinja template for checking membership

```django
jinja
{% set target_group_id = "your-group-id-here" %}
{% set user_groups = CTX.user_groups.groups %}
{% set is_member = false %}

{% for group in user_groups %}
  {% if group.group_id == target_group_id %}
    {% set is_member = true %}
  {% endif %}
{% endfor %}

{{ is_member }}
```

## Unpack the Subworkflow: Check a User's Group Memberships to Proceed in a Workflow Crate

1. Navigate to **Crates** > **Crate Marketplace** in the left side menu Rewst platform.
2.  Search for `Subworkflow: Check a User's Group Memberships to Proceed in a Workflow`.

    \
    ![](<../../../.gitbook/assets/image (320).png>)
3. Click on the Crate tile to begin unpacking.
4. Click **Unpack Crate**.
5. Click **Continue**.
6. Enter **Time Saved** under **Crate Configuration**.
7. Click **Unpack**.

{% hint style="info" %}
Got an idea for a new Crate? Rewst is constantly adding new Crates to our Crate Marketplace. Submit your idea or upvote existing ideas here in our [Canny feedback collector](https://rewst.canny.io/crates).
{% endhint %}
