# Glossary of terms

{% hint style="info" %}
This page is a work in progress! Check back for more terms as they're added. \


Our glossary is organized alphabetically, with each tab containing 2-3 letters. Click through the tabs to find your term that starts with the corresponding letter. We include terms specific to Rewst, as well as some industry and programming terms for general reference when reading through our other documentation and training.
{% endhint %}

{% tabs %}
{% tab title="ABC" %}


<table data-full-width="true"><thead><tr><th>Term</th><th>Definition</th></tr></thead><tbody><tr><td>Actions</td><td><em>Actions</em> are specific tasks that live inside a workflow in Rewst. Actions are grabbed from the menu, dragged onto the workflow builder canvas, and executed as a task when the workflow runs.</td></tr><tr><td>Anti-patterns</td><td><em>Anti-patterns</em> are common but harmful practices that increase complexity and maintenance challenges. Unlike design patterns, which offer best-practice solutions, anti-patterns often make your code less clear and more error-prone.</td></tr><tr><td>API</td><td>Short for Application Programming Interface, an <em>API</em> is a set of protocols that allow actions on a platform in a programmatic manner. APIs power Rewst's integrations, enabling actions that workflows perform.</td></tr><tr><td>API key</td><td>An <em>API key</em> is a unique identifier used during integration setup, allowing secure communication between platforms without re-entering the key for each action.</td></tr><tr><td>Authentication method</td><td>The process of verifying the identity of a user or application. The required <em>authentication method</em> will depend on the API you're attempting to access. For more detail, or information on more complex authentication methods check out <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication">Mozilla's Developer Network (MDN) documentation on HTTP authentication methods</a>.</td></tr><tr><td>Automation</td><td><em>Automation</em> refers to the process of using technology, including Rewst's platform, to perform repetitive tasks without human intervention. It enables businesses to increase efficiency, accuracy, and consistency by automating various processes, from simple notifications to complex multi-step workflows.</td></tr><tr><td>Basic authentication</td><td><em>Basic authentication</em> is a method that requires a username and password, often used for web server login.</td></tr><tr><td>Body</td><td>Regarding APIs, a <em>body</em> is the part of an HTTP request containing data sent to the API, typically structured in formats like JSON or XML. <br>Example JSON body: <code>{"username": "john_doe", "password": "secret"}.</code></td></tr><tr><td>Cookies</td><td><em>Cookies</em> are small pieces of data stored on a user's computer by a web server, used by APIs to manage sessions or track user behavior.</td></tr><tr><td>Content type</td><td>A <em>content type</em> is a specific header used in HTTP requests to indicate the media type, such as <code>application/json</code> for JSON data.</td></tr><tr><td>The context</td><td>T<em>he context</em> is where all data generated, captured, or used in a workflow is stored. Think of it as a shared memory for a specific workflow. Data aliases are stored in the context, making them available for reuse at any step without re-fetching the data.</td></tr><tr><td>Context variables</td><td><em>Context variables</em> are variables accessed via the CTX prefix within a running workflow in Rewst, for dynamic processing. They are specific to the workflow run and hold data generated or used during that instance, such as the current ticket ID or timestamp.</td></tr><tr><td>Crate</td><td>A <em>Crate</em> is a pre-built automation. Crates within Rewst contain workflows, forms, triggers, templates, and scripts bundled together for easy deployment.</td></tr><tr><td>Crate Marketplace</td><td>The Rewst <em>Crate Marketplace</em> is the area of the Rewst platform where users can find and install Crates, offering a range of pre-built automation solutions.</td></tr></tbody></table>
{% endtab %}

{% tab title="DEF" %}
| Term        | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Data alias  | A _data alias_ is a shortcut that extracts specific pieces of information from a JSON response and stores them in an easy-to-use variable. Instead of navigating the entire JSON structure every time, a data alias pulls out exactly what you need—like a user’s name or email—and makes it accessible throughout your workflow.                                                                                                                             |
| Datetime    | In Rewst, `datetime` usually refers to working with dates and times using Jinja.                                                                                                                                                                                                                                                                                                                                                                              |
| Endpoint    | An _endpoint_ is a specific path added to the URL where an API can call back specific object's properties. E.g., `https://api.example.com/users/123`                                                                                                                                                                                                                                                                                                          |
| File upload | Regarding APIs, _file uploading_ is the process of sending files such as images, documents, or other binary data as part of an HTTP request to an API. Typically used with the content type multipart/form-data when passing files within form submissions. For more information on sending form data, including file uploads, see [MDN Web Docs - Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data). |
| Filter      | Specific to Rewst's extension of Jinja, _filters_ are python functions surfaced in the platform and used to modify variables or expressions within a workflow, providing additional control over data processing.                                                                                                                                                                                                                                             |
| For loop    | _For loops_ in Jinja enable you to iterate through JSON lists, executing actions for each item. The pointer, such as `thing`, points to items within the list, facilitating dynamic data processing.                                                                                                                                                                                                                                                          |
| Form        | A _form_ is a way to collect data within Rewst. Forms can contain static and dynamic fields to retrieve information, which is then passed into the workflow upon submission. End-users can be given Form URLs to fill out necessary information  prior to triggering a workflow's execution.                                                                                                                                                                  |


{% endtab %}

{% tab title="GHI" %}
| Term                 | Definition                                                                                                                                                                                                                                                                                                                                           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| HTTP Request Method  | This specifies the action to be performed on a resource within an API, e.g., GET (retrieve data), POST (create data), PUT (update data), DELETE (remove data).                                                                                                                                                                                       |
| Header               | Regarding APIs, this is additional information sent with an HTTP request. E.g., `content type`.                                                                                                                                                                                                                                                      |
| Integration          | _Integrations_ in Rewst allow the platform to connect and communicate with other software or services. Through integrations, Rewst can interact with various third-party applications, such as your PSA, RMM, email platforms, or cloud services, enabling you to extend the functionality of your automations and create more cohesive experiences. |
| Integration override | _Integration overrides_ allow you to specify which integration configurations should be used. Otherwise, the default integration configuration for the triggering organization will be used.                                                                                                                                                         |
|                      |                                                                                                                                                                                                                                                                                                                                                      |
|                      |                                                                                                                                                                                                                                                                                                                                                      |


{% endtab %}

{% tab title="JKL" %}
| Term               | Definition                                                                                                                                                                                                                                                                                                         |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Jinja              | _Jinja_ is a templating language used in Rewst for processing data within workflows. Based on Python, Jinja allows for more powerful manipulation of data, including filtering and custom formatting.                                                                                                              |
| JSON               | Short for JavaScript object notation, _JSON_ is a format designed for human readability and quick editing, JSON allows you to structure complex data in a way that's both accessible and efficient. It's a go-to choice for sending and receiving data with APIs, making it a vital part of Rewst's functionality. |
| List comprehension | <p></p><p><em>List comprehension</em> is a way to create a new list by transforming or filtering items from an existing one, all in one Jinja expression. </p><blockquote><p>“Give me a list of all X from Y, but only if Z.”</p></blockquote>                                                                     |


{% endtab %}

{% tab title="MNO" %}
| Term                   | Definition                                                                                                                                                                                                                                                                                                     |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Markdown               | _Markdown_ is a lightweight markup language that you can use to add formatting elements to plaintext text documents. When you create a Markdown-formatted file, you add Markdown syntax to the text to indicate which words and phrases should look different.                                                 |
| Multipart/Form-Data    | A media type used to send files as part of an HTTP request, allowing for the uploading of files along with textual data.                                                                                                                                                                                       |
| Nopp                   | In Jinja, a _noop_ is an empty action used to create custom transitions.                                                                                                                                                                                                                                       |
| OAuth                  | Short for open authorization, _OAuth_ is an open standard for access delegation, often used to grant token-based authentication and authorization.                                                                                                                                                             |
| Option Generator       | An _option generator_ is a workflow that generates options, and can be connected to specific field types. For example, you would use this to curate what shows up in a workflow's dropdown, rather than showing every single group in that menu.                                                               |
| Organization           | A group or entity within the Rewst platform that may have its own variables, forms, workflows, and users, _organizations_ enable multi-tenanted management and customization of the platform according to specific client needs. You may see us refer to an organization as an _org_ for short.                |
| Organization Variables | Also known as _org variables,_ these are specific variables used within an organization or sub-organization in Rewst. They can be referenced in workflows and may be inherited or overridden by sub-organizations. They apply across all workflows, storing consistent data like company settings or API keys. |
| Output                 | Regarding APIs, _output_ is the content returned by a server in response to a request, including messages, data objects, or other information. E.g., `{"status": "success", "token": "abc123"}.`                                                                                                               |


{% endtab %}

{% tab title="PQR" %}


| Term            | Definition                                                                                                                                                                                                                                                                                                    |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Parameters      | _Parameters_ in Rewst are like fill-in-the-blank options that make workflows adaptable. Example: Instead of hardcoding a date, you can use a parameter like `ReminderDate` to customize it each time the workflow runs.                                                                                       |
| Path parameter  | A _path parameter_ is a unique identifier in the URL that identifies specific data, such as an ID in API calls. E.g., the `123` in `/users/123`.                                                                                                                                                              |
| PowerShell      | _PowerShell_ is a command-line shell and scripting language, primarily designed for system administrators by Microsoft, allowing them to automate tasks and manage systems from the command line. The language is now cross-platform.                                                                         |
| Query parameter | A _query parameter_ is an optional parameter available to be added to the Endpoint to filter the API call for some endpoints. E.g., `?status=active`.                                                                                                                                                         |
| Redirects       | Regarding APIs, a _redirect_ is the automatic forwarding of an HTTP request from one URL to another. E.g., redirecting from `http://example.com` to `https://example.com` to enforce use of HTTPS.                                                                                                            |
| RoboRewsty      | _RoboRewsty_ is Rewst's AI integration feature. It integrates with the workflow builder canvas. It takes your workflows' JSON objects, and sends them to a private OpenAI Azure instance. The result is a quickly presented, well structured documentation breakdown of all selected tasks in your workflow.  |
{% endtab %}

{% tab title="STU" %}
| Term         | Definition                                                                                                                                                                                                        |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Status codes | _Status codes_ are numeric codes returned by a server to indicate the result of an HTTP request. E.g., `200` (success), `404` (not found), and `500` (server error).                                              |
| Template     | In Rewst, _templates_ are used as a central store for repeated text, allowing for consistency across different actions and workflows.                                                                             |
| Timeout      | Regarding APIs, _timeout_ is the maximum time allowed for a request to be processed                                                                                                                               |
| Transitions  | _Transitions_ are elements found at the bottom of every action in Rewst that determine the path the workflow will take. Transitions can be based on success, failure, always, or custom-defined Jinja conditions. |
| Triggers     | _Triggers_ are components in Rewst used to initiate workflows or perform actions based on specific events or conditions. They can respond to various events, such as form submissions or webhook responses.       |


{% endtab %}

{% tab title="VWX" %}
| Term       | Definition                                                                                                                                                                                                                                                                                            |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Variables  | A _variable_ is a labeled container that holds data you can reuse. Instead of locking in specific details like a customer's name, you can use a placeholder— e.g., CustomerName— that updates dynamically.                                                                                            |
| Webhook    | A _webhook_ is like a notification that triggers a workflow as soon as an event happens—no need to constantly check for updates. Example: When a customer submits a support ticket, a webhook instantly sends that information to Rewst, starting the workflow right away.                            |
| With Items | In Rewst, `with_items` is used in Loop blocks, and sometimes inline within block configurations, to iterate over a list of items. It's the Rewst equivalent of a `for` loop in Python or Jinja.                                                                                                       |
| Workflow   | In the context of Rewst, a _workflow_ is a series of automated actions that are executed in a specific sequence based on triggers and conditions. Workflows enable users to design, execute, and manage multi-step processes, bringing together various integrations to accomplish a particular task. |
| XML        | Short for extensible markup language, _XML_ is used to encode data in a format that is both human-readable and machine-readable.                                                                                                                                                                      |


{% endtab %}

{% tab title="YZ" %}
| Term | Definition                                                                                                 |
| ---- | ---------------------------------------------------------------------------------------------------------- |
| YAML | _YAML_ is a human-readable data serialization language that is often used for writing configuration files. |
|      |                                                                                                            |
|      |                                                                                                            |


{% endtab %}

{% tab title="#" %}

{% endtab %}
{% endtabs %}

