# Glossary of Terms

{% hint style="info" %}
This page is a work in progress! Check back for more terms as they're added. \


Our glossary is organized alphabetically, with each tab containing 2-3 letters. Click through the tabs to find your term that starts with the corresponding letter. We include terms specific to Rewst, as well as some industry and programming terms for general reference when reading through our other documentation and training.
{% endhint %}

{% tabs %}
{% tab title="ABC" %}


<table data-full-width="true"><thead><tr><th>Term</th><th>Definition</th></tr></thead><tbody><tr><td>Actions</td><td><strong>Actions</strong> are specific tasks that live inside a workflow in Rewst. Actions are grabbed from the menu, dragged onto the workflow UI, and executed as a task when the workflow runs.</td></tr><tr><td>API</td><td>Short for Application Programming Interface, an <strong>API</strong> is a set of protocols that allow actions on a platform in a programmatic manner. APIs power Rewst's integrations, enabling actions that workflows perform.</td></tr><tr><td>API Key</td><td>An <strong>API key</strong> is a unique identifier used during integration setup, allowing secure communication between platforms without re-entering the key for each action.</td></tr><tr><td>Authentication Method</td><td>The process of verifying the identity of a user or application. The required <strong>authentication method</strong> will depend on the API you're attempting to access. For more detail, or information on more complex authentication methods check out <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication">Mozilla's Developer Network (MDN) documentation on HTTP authentication methods</a>.</td></tr><tr><td>Automation</td><td><strong>Automation</strong> refers to the process of using technology, including Rewst's platform, to perform repetitive tasks without human intervention. It enables businesses to increase efficiency, accuracy, and consistency by automating various processes, from simple notifications to complex multi-step workflows.</td></tr><tr><td>Basic Authentication</td><td><strong>Basic authentication</strong> is a method that requires a username and password, often used for web server login.</td></tr><tr><td>Body</td><td>Regarding APIs, a <strong>body</strong> is the part of an HTTP request containing data sent to the API, typically structured in formats like JSON or XML. <br>Example JSON body: <code>{"username": "john_doe", "password": "secret"}.</code></td></tr><tr><td>Cookies</td><td><strong>Cookies</strong> are small pieces of data stored on a user's computer by a web server, used by APIs to manage sessions or track user behavior.</td></tr><tr><td>Content Type</td><td>A <strong>content type</strong> is a specific header used in HTTP requests to indicate the media type, such as <code>application/json</code> for JSON data.</td></tr><tr><td>Context Variables</td><td><strong>Context variables</strong> are variables accessed via the CTX prefix within a running workflow in Rewst, for dynamic processing.</td></tr><tr><td>Crate</td><td>A <strong>Crate</strong> is a pre-built automation. Crates within Rewst contain workflows, forms, triggers, templates, and scripts bundled together for easy deployment.</td></tr><tr><td>Crate Marketplace</td><td>The Rewst <strong>Crate Marketplace</strong> is the area of the Rewst platform where users can find and install Crates, offering a range of pre-built automation solutions.</td></tr></tbody></table>
{% endtab %}

{% tab title="DEF" %}
| Term        | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Endpoint    | An **endpoint** is a specific path added to the URL where an API can call back specific object's properties. E.g., `https://api.example.com/users/123`                                                                                                                                                                                                                                                                                                          |
| File Upload | Regarding APIs, **file uploading** is the process of sending files such as images, documents, or other binary data as part of an HTTP request to an API. Typically used with the content type multipart/form-data when passing files within form submissions. For more information on sending form data, including file uploads, see [MDN Web Docs - Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data). |
| Filter      | Specific to Rewst's extension of Jinja, **filters** are python functions surfaced in the platform and used to modify variables or expressions within a workflow, providing additional control over data processing.                                                                                                                                                                                                                                             |
| Form        | A **form** is a way to collect data within Rewst. Forms can contain static and dynamic fields to retrieve information, which is then passed into the workflow upon submission. End-users can be given Form URLs to fill out necessary information  prior to triggering a workflow's execution.                                                                                                                                                                  |


{% endtab %}

{% tab title="GHI" %}
| Term                | Definition                                                                                                                                                                                                                                                                                                                                             |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| HTTP Request Method | This specifies the action to be performed on a resource within an API, e.g., GET (retrieve data), POST (create data), PUT (update data), DELETE (remove data).                                                                                                                                                                                         |
| Header              | Regarding APIs, this is additional information sent with an HTTP request. E.g., `content type`.                                                                                                                                                                                                                                                        |
| Integration         | **Integrations** in Rewst allow the platform to connect and communicate with other software or services. Through integrations, Rewst can interact with various third-party applications, such as your PSA, RMM, email platforms, or cloud services, enabling you to extend the functionality of your automations and create more cohesive experiences. |
|                     |                                                                                                                                                                                                                                                                                                                                                        |
|                     |                                                                                                                                                                                                                                                                                                                                                        |
|                     |                                                                                                                                                                                                                                                                                                                                                        |


{% endtab %}

{% tab title="JKL" %}
| Term  | Definition                                                                                                                                                                                                                                                                                                       |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Jinja | **Jinja** is a templating language used in Rewst for processing data within workflows. Based on Python, Jinja allows for more powerful manipulation of data, including filtering and custom formatting.                                                                                                          |
| JSON  | Short for JavaScript object notation, JSON is a format designed for human readability and quick editing, JSON allows you to structure complex data in a way that's both accessible and efficient. It's a go-to choice for sending and receiving data with APIs, making it a vital part of Rewst's functionality. |
|       |                                                                                                                                                                                                                                                                                                                  |


{% endtab %}

{% tab title="MNO" %}
| Term                   | Definition                                                                                                                                                                                                                                         |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Multipart/Form-Data    | A media type used to send files as part of an HTTP request, allowing for the uploading of files along with textual data.                                                                                                                           |
| Nopp                   | In Jinja, a **noop** is an empty action used to create custom transitions.                                                                                                                                                                         |
| OAuth                  | Short for open authorization, **OAuth** is an open standard for access delegation, often used to grant token-based authentication and authorization.                                                                                               |
| Option Generator       | An **option generator** is a workflow that generates options, and can be connected to specific field types. For example, you would use this to curate what shows up in a workflow's dropdown, rather than showing every single group in that menu. |
| Organization           | A group or entity within the Rewst platform that may have its own variables, forms, workflows, and users, **organizations** enable multi-tenanted management and customization of the platform according to specific client needs.                 |
| Organization Variables | Also known as **org variables**, these are specific variables used within an organization or sub-organization in Rewst. They can be referenced in workflows and may be inherited or overridden by sub-organizations.                               |
| Output                 | Regarding APIs, **output** is the content returned by a server in response to a request, including messages, data objects, or other information. E.g., `{"status": "success", "token": "abc123"}.`                                                 |


{% endtab %}

{% tab title="PQR" %}


| Term            | Definition                                                                                                                                                                                 |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Path Parameter  | A **path parameter** is a unique identifier in the URL that identifies specific data, such as an ID in API calls. E.g., the `123` in `/users/123`.                                         |
| Query Parameter | A **query parameter** is an optional parameter available to be added to the Endpoint to filter the API call for some endpoints. E.g., `?status=active`.                                    |
| Redirects       | Regarding APIs, this is the automatic forwarding of an HTTP request from one URL to another. E.g., redirecting from `http://example.com` to `https://example.com` to enforce use of HTTPS. |
{% endtab %}

{% tab title="STU" %}
| Term         | Definition                                                                                                                                                                                                          |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Status Codes | **Status codes** are numeric codes returned by a server to indicate the result of an HTTP request. E.g., `200` (success), `404` (not found), and `500` (server error).                                              |
| Template     | In Rewst, **templates** are used as a central store for repeated text, allowing for consistency across different actions and workflows.                                                                             |
| Timeout      | Regarding APIs, **timeout** is the maximum time allowed for a request to be processed                                                                                                                               |
| Transitions  | **Transitions** are elements found at the bottom of every action in Rewst that determine the path the workflow will take. Transitions can be based on success, failure, always, or custom-defined Jinja conditions. |
| Triggers     | **Triggers** are components in Rewst used to initiate workflows or perform actions based on specific events or conditions. They can respond to various events, such as form submissions or webhook responses.       |


{% endtab %}

{% tab title="VWX" %}
| Term     | Definition                                                                                                                                                                                                                                                                                              |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Workflow | In the context of Rewst, a **workflow** is a series of automated actions that are executed in a specific sequence based on triggers and conditions. Workflows enable users to design, execute, and manage multi-step processes, bringing together various integrations to accomplish a particular task. |
| XML      | Short for extensible markup language, **XML** is used to encode data in a format that is both human-readable and machine-readable.                                                                                                                                                                      |


{% endtab %}

{% tab title="YZ" %}
| Term | Definition |
| ---- | ---------- |
|      |            |
|      |            |
|      |            |


{% endtab %}

{% tab title="#" %}

{% endtab %}
{% endtabs %}

