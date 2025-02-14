# Completion handlers

Completion Handlers are workflows that execute after another workflow has been completed. These workflows have a context variable that can be used to reference previous contexts from the workflow that was completed.

### Example workflow use-cases

Let's look at a few use cases for using Completion Handlers:

1. Adding additional functionality to sync workflows
2. Taking additional steps after the onboarding workflow is complete.
   * You can add additional functionality to an existing synced workflow without having to unsync it from the template.
3. Alerting for failed workflow executions, i.e. kicking off the listener based on a failed status.

### How to Access the Context of the Previous Workflow

Contexts from the previously run workflow can be accessed with the `COMPLETED_WORKFLOW` variable. You can access most info via the context including ORG and CTX such as:

1. `{{ COMPLETED_WORKFLOW.ORG.VARIABLES.cw_manage_company_id }}`
2. `{{ COMPLETED_WORKFLOW.CTX.user.username }}`

{% hint style="danger" %}
Completion Handlers will always run in the context of the parent MSP. If you are taking actions on a sub-organization in the workflow then you must utilize the run-as-organization functionality and overrides set at the Completion Handler level.

The organization id that was used in the previous workflow context can be referenced with the following Jinja:

`{{ COMPLETED_WORKFLOW.ORG.ATTRIBUTES.id }}`
{% endhint %}

### How to configure a Completion Handler

You can configure a Completion Handler in one of two ways.

#### 1: When this workflow completes (Creating from the workflow this is set to run from)

1. **Open** the workflow that you want to run after.
2. **Click** on the Monitor icon.
3. **Click** Add at the top right.
4. **Select** the workflow you would like to run.
5. **Select** the statuses that you would like for the workflow to be triggered on.
6. **Add** the overrides for the integrations used in your Completion Handler.
7. **Click** Submit.
   * Make sure enabled is checked.

#### 2: Run this workflow when (Creating from the Completion Handler itself)

1. **Repeat** steps 1 and 2 from above.
2. **Repeat** steps 4-9, but instead of choosing the Completion Handler workflow, you will choose the workflows that you would like the to execute after they complete.

<figure><img src="../../.gitbook/assets/Listener-workflow.png" alt=""><figcaption></figcaption></figure>
