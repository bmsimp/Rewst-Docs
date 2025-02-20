# GitHub integration

{% hint style="info" %}
If you’re new to integrations in Rewst, read through our introductory integration documentation [here](https://docs.rewst.help/documentation/integrations).

GitHub’s own documentation for registering an app can be found [here](https://docs.github.com/en/apps/creating-github-apps/registering-a-github-app/registering-a-github-app).
{% endhint %}

## What does the GitHub integration do?

Our GitHub integration enables automation of GitHub’s version control system. Use GitHub’s API within Rewst workflows to automate aspects of version control in GitHub.

### Integration use cases

* Say you want to create a Crate that automatically backs up all workflow exports any time they change. You could use the GitHub integration to make a commit of each change of the file. This would give you a more fully featured option than Rewst’s built in version control.
* Use this integration to set up a system for sharing workflows you’ve created with other Rewst customers. Create a public repository, and post exported repositories of your shareable workflows.

## Set up the GitHub integration

### Set up steps in GitHub

1. Log in to the GitHub account linked to your organization.

### Set up steps in Rewst

1. Navigate to **Configuration > Integrations** in the left side menu of your Rewst platform.
2. In the Integrations page, search for the GitHub integration.\
   \
   ![](<../../../.gitbook/assets/Screenshot 2025-02-05 at 10.06.23 AM.png>)
3. Click the integration tile to launch the **Configuration** setup page.
4. Enter the following in the relevant fields of the form:
   1. The **Name** that will be used to refer to the integration configuration
   2. **Description**: this is optional.
   3. Check the **Is Default** checkbox.
   4. **Organization Name**: make sure that this is exact to how your organization name appears in GitHub.
5. Click **Save Configuration**.
6. Click **Authorize**.
7. Click **Continue** next to your desired installation location, from the list in the dialog that appears. The dialog will contain a list of organizations. It’s important that you choose the organization to match the one you entered for the organization name of the Rewst configuration form.\
   \
   ![](<../../../.gitbook/assets/Screenshot 2025-02-10 at 5.13.19 PM.png>)\

8. Click **Install & Authorize**.\
   \
   ![](<../../../.gitbook/assets/Screenshot 2025-02-10 at 5.13.32 PM.png>)
9. A green confirmation message will appear at the top of your screen. Now, the configuration form will have an option to **Re-Authorize**.

## Test the Integration

Whenever you save configuration and reauthorize, Rewst will run a test action to make sure the integration is working.\


<figure><img src="../../../.gitbook/assets/Screenshot 2025-02-10 at 5.22.03 PM.png" alt=""><figcaption></figcaption></figure>

For additional testing, click the Refresh Options button under the Organization Mapping section of the integration configuration page. This will return a list of repositories accessible by that organization.

## Troubleshoot the GitHub integration

{% hint style="warning" %}
The below error may also happen if you attempt to install the GitHub integration on multiple Rewst orgs using the same GitHub org.

If you encounter any errors, contact us in your Discord support channel for assistance.
{% endhint %}

If you uninstall the GitHub integration in Rewst but don’t uninstall our GitHub App in your organization, any attempt to re-install and authorize the integration will fail, and you’ll be stuck at this screen:\


<figure><img src="../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

To fix this failure:

1. Log in to GitHub.
2. Find the installed GitHub App.
3. Click the **Configure** button.
4. Uninstall the app. You should now be able to re-authorize in Rewst, and the GitHub App will be reinstalled once successful.

<figure><img src="../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

## GitHub actions and endpoints

{% hint style="info" %}
For more on how actions work in Rewst, check out our [introductory actions documentation here](https://docs.rewst.help/documentation/workflows/actions-in-rewst).
{% endhint %}



| Category    | Action                                          | Description                                                                                                                                                                                 |
| ----------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Billing** | Get Github Actions Billing For An Organization  | Gets the summary of the free and paid GitHub Actions minutes used. Paid minutes only apply to workflows in private repositories that use GitHub-hosted runners.                             |
| **Billing** | Get Github Packages Billing For An Organization | Gets the free and paid storage used for GitHub Packages in gigabytes. Paid minutes only apply to packages stored for private repositories.                                                  |
| **Billing** | Get Shared Storage Billing For An Organization  | Gets the estimated paid and estimated total storage used for GitHub Actions and GitHub Packages. Paid minutes only apply to packages stored for private repositories.                       |
| **Billing** | Get Github Actions Billing For a User           | Gets the summary of the free and paid GitHub Actions minutes used. Paid minutes only apply to workflows in private repositories that use GitHub-hosted runners.                             |
| **Billing** | Get Github Packages Billing For a User          | Gets the free and paid storage used for GitHub Packages in gigabytes. Paid minutes only apply to packages stored for private repositories.                                                  |
| **Billing** | Get Shared Storage Billing For a User           | Gets the estimated paid and estimated total storage used for GitHub Actions and GitHub Packages. Paid minutes only apply to packages stored for private repositories.                       |
| **Checks**  | Create a Check Run                              | Creates a new check run for a specific commit in a repository. To create a check run, you must use a GitHub App. OAuth apps and authenticated users are not able to create a check suite.   |
| **Checks**  | Get a Check Run                                 | Gets a single check run using its `id`. **Note:** The Checks API only looks for pushes in the repository where the check suite or check run were created.                                   |
| **Checks**  | Update a Check Run                              | Updates a check run for a specific commit in a repository. **Note:** The endpoints to manage checks only look for pushes in the repository where the check suite or check run were created. |
| **Checks**  | Rerequest a Check Run                           | Triggers GitHub to rerequest an existing check run, without pushing new code to a repository. This will trigger the `check_run` webhook event with the action `rerequested`.                |
| **Checks**  | List Check Runs In a Check Suite                | Lists check runs for a check suite using its `id`. **Note:** The endpoints to manage checks only look for pushes in the repository where the check suite or check run were created.         |
| **Checks**  | Rerequest a Check Suite                         | Triggers GitHub to rerequest an existing check suite, without pushing new code to a repository. This will trigger the `check_suite` webhook event with the action `rerequested`.            |

{% hint style="info" %}
Got an idea for a new Integration? Rewst is constantly adding new integrations to our integrations page. Submit your idea or upvote existing ideas here in our [Canny feedback collector](https://rewst.canny.io/integrations).
{% endhint %}
