# Gateway

> The Gateway feature allows you to block or hang requests, preventing them from reaching the server. This enables effective filtering and control over specific network traffic.

### Enabling the Gateway

**Path:** Gateway Menu -> Enable Gateway. Once enabled, a small green dot will appear beneath the Gateway menu, indicating that the feature is active.

![](img/light/网关1.png?version=1.1.0)

### Adding a Gateway Rule

1. **Path:** Gateway Menu -> Manage Rules -> Click the "+" button in the top right corner of the rule list.
2. In the popup window, fill in the matching rules and the blocking method, then click "OK" to add the rule. The matching rules support **wildcard** patterns.

![](img/light/网关2.png?version=1.1.0)

### Blocking Methods

The Gateway provides four types of blocking methods:

* **Block Request:** Directly prevents the request from being sent to the server. The client will receive a connection failure error.
* **Block Response:** The request is sent to the server, but the server's response is blocked. The client will receive a connection failure error.
* **Hang Request:** The request is not sent to the server, and the client will remain in a waiting state until it times out.
* **Hang Response:** The request is sent to the server, but the server's response is held (suspended). The client will remain in a waiting state until it times out.