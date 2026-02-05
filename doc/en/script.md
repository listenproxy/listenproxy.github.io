# Scripting

> The **Scripting** feature allows you to modify requests and responses using custom JavaScript code, providing flexible control and processing capabilities.

### Enabling Scripting

**Path:** Go to **Script Menu** -> **Enable Scripting**. Once activated, a small green indicator will appear under the Script menu, signifying the feature is live.

![](img/light/脚本1.png?version=1.1.0)

### Adding Script Rules

1. **Navigation:** Script Menu -> Manage Rules -> Click the **"+"** button in the top-right corner of the rule list.
2. **Configuration:** In the popup window, enter your **Match Rules** and **Script Code**, then click "OK" to save. Match rules support **wildcards**.

![](img/light/脚本2.png?version=1.1.0)


### Script Methods

You can define two primary methods within your script:

* `onHttpRequest({header, body, bodyType, url, cookies})`: Triggered before the request is sent to the server. It returns `{header, body}` as the modified request headers and body.
* `onHttpResponse({header, body, bodyType, url, cookies})`: Triggered before the response is sent back to the client. It returns `{header, body}` as the modified response headers and body.

#### Parameter Descriptions:

| Parameter | Description |
| --- | --- |
| **header** | The headers of the request or response (Object). |
| **body** | The content of the request or response (String, JSON-serializable Object, or `Uint8Array`). |
| **bodyType** | The data type of the body (e.g., `"string"`, `"json"`, `"uint8array"`). |
| **url** | The full URL of the request. |
| **cookies** | Cookie information from the headers (Object). |

**Example:**
The following script adds a custom request header `test_add_req_header: req` and replaces the request body with `"request body"`. Similarly, it adds a response header `test_add_res_header: res` and replaces the response body with `"response body"`.

![](img/light/脚本2.png?version=1.1.0)

### Debugging & Logs

You can use `console.log()` within your code to print logs. These logs are displayed in the **Execution Records** of the client, making it easy to debug. If the script encounters an error, the error message will also appear in the execution records for troubleshooting.

![](img/light/脚本3.png?version=1.1.0)

![](img/light/脚本4.png?version=1.1.0)

To view the execution history of a specific rule, click the **History Icon** in the script rule list.