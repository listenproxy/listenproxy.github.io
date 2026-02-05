# Breakpoint

> The **Breakpoint** feature allows you to pause a request before it is sent to the server or before a response is returned to the client, enabling manual inspection and modification of the request and response data.

### Enabling the Breakpoint Feature

**Path:** Go to **Breakpoint Menu** -> **Enable Breakpoint**. Once enabled, a small green dot will appear under the Breakpoint menu to indicate the feature is active.

![](img/light/断点1.png?version=1.1.0)

### Adding a Breakpoint Rule

1. **Operation Path:** **Breakpoint Menu** -> **Manage Rules** -> Click the **"+"** button at the top right of the rule list.
2. In the popup window, fill in the **Matching Rule** and **Breakpoint Type**, then click the **"OK"** button to add the rule. Matching rules support wildcards.

![](img/light/断点2.png?version=1.1.0)

### Breakpoint Types

There are two types of breakpoints: Request Breakpoints and Response Breakpoints.

* **Request Breakpoint:** Pauses the request before it is sent to the server, allowing the user to inspect and modify the request content, then manually resume sending it to the server.
* **Response Breakpoint:** Pauses the response before it is returned to the client, allowing the user to inspect and modify the response content, then manually resume returning it to the client.

**Example:** If the request URL is `https://listen-proxy.com/`, the configuration below will cause the browser to hang and wait after initiating the request.

![](img/light/断点3.png?version=1.1.0)

At this point, open the Listen client and select the **"Execute Breakpoint"** button. You will see the request listed in the Breakpoint Executor. Click on the request to view and modify its content. You can manually edit the request method, path, parameters, headers, and body. After modification, click the **"Execute"** button to send the request to the server. Once the server responds, the browser will continue loading the page.

![](img/light/断点4.png?version=1.1.0)

![](img/light/断点5.png?version=1.1.0)

If you prefer not to open the executor manually, you can check the **"Auto-popup"** option in the Breakpoint menu. This way, when a request hits a breakpoint rule, the executor will open automatically for convenient inspection and modification.

The usage of Response Breakpoints is the same as Request Breakpoints, except they are used to inspect and modify the content returned by the server. After modification, click the **"Execute"** button to return the response to the client, and the browser will continue loading the page.

*When configuring, you can select both "Request" and "Response" at the same time, allowing you to inspect and modify data both before the request is sent and before the response is returned.*

![](img/light/断点6.png?version=1.1.0)