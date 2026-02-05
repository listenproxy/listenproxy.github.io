# Rewrite

> The **Rewrite** feature allows you to use pre-defined rules to modify requests before they are sent to the server, enabling request redirection and adjustment. It can also modify responses before they are returned to the client to adjust the response data.

### Enabling the Rewrite Feature

**Path:** Go to **Rewrite Menu** -> **Enable Rewrite**. Once enabled, a small green dot will appear under the Rewrite menu to indicate the feature is active.

![](img/light/重写1.png?version=1.1.0)

### Adding a Rewrite Rule

1. **Path:** **Rewrite Menu** -> **Manage Rules** -> Click the **"+"** button at the top right of the rule list.
2. In the popup window, fill in the **Matching Rules** and **Behaviors**, then click the **"OK"** button to add the rule.

![](img/light/重写2.png?version=1.1.0)

### Modifying Requests

When modifying requests, you can add, modify, or delete parameters; add, modify, or delete request headers; and replace or modify the request body.

#### Add Parameter

Adds a new parameter to the end of the URL in the format `key=value`.

**Example:** If the request URL is `https://listen-proxy.com/`, the configuration below will modify the URL sent to the server to `https://listen-proxy.com/?test=1`.

![](img/light/重写2.png?version=1.1.0)

#### Modify Parameter

Matches URL parameters (supports regular expressions and case-insensitivity) and replaces the value of the matched parameter.

**Example:** If the request URL is `https://listen-proxy.com/?test=1`, the configuration below will modify the URL sent to the server to `https://listen-proxy.com/?test=2`.

![](img/light/重写3.png?version=1.1.0)

#### Delete Parameter

Matches URL parameters (supports regular expressions and case-insensitivity) and deletes the matched parameters and their values.

**Example:** If the request URL is `https://listen-proxy.com/?test=1`, the configuration below will modify the URL sent to the server to `https://listen-proxy.com/`.

![](img/light/重写4.png?version=1.1.0)

#### Add Request Header

Adds a new request header field in the format `key: value`.

**Example:** If the request URL is `https://listen-proxy.com/`, the configuration below will add `test_add_header: 1` to the request headers.

![](img/light/重写5.png?version=1.1.0)

#### Modify Request Header

Matches request header fields (supports regular expressions and case-insensitivity) and replaces the value of the matched field.

**Example:** If the request URL is `https://listen-proxy.com/`, the configuration below will change the value of the `Accept-Language` field in the request header to `zh-CN`.

![](img/light/重写6.png?version=1.1.0)

#### Delete Request Header

Matches request header fields (supports regular expressions and case-insensitivity) and deletes the matched fields and values.

**Example:** If the request URL is `https://listen-proxy.com/`, the configuration below will remove the `Accept-Language` field from the request header.

![](img/light/重写7.png?version=1.1.0)

#### Replace Request Body

Replaces the request body with specified content, supporting both text and files.

**Example:** If the request URL is `https://listen-proxy.com/`, the configuration below will replace the request body data with `test replace body` (Replacement Body Data).

![](img/light/重写8.png?version=1.1.0)

#### Modify Request Body

Performs text matching on the request body (supports regular expressions and case-insensitivity) and replaces the matched text.

**Example:** If the request URL is `https://listen-proxy.com/` and the request body is `{"test":1}`, the configuration below will modify the request body to `{"test1":1}`.

![](img/light/重写9.png?version=1.1.0)

### Modifying Responses

When modifying responses, you can add, modify, or delete response headers, and replace or modify the response body. These modification rules are similar to the request modification rules, but are applied to the response.

![](img/light/重写10.png?version=1.1.0)