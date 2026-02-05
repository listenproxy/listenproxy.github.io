# WebSocket

> **Listen** provides robust support for WebSocket debugging. You can easily view and search through messages and send messages directly to the client or server. By leveraging **Rewrite** and **Scripting** features, you can even intercept and modify messages sent by either party.

### Message Viewing

For WebSocket connections, double-click to open the details panel and switch to the **WebSocket** tab to view real-time messages between the server and the client.

* **Search:** Click the search icon in the top-left corner of the message interface to open the search panel.
* **Send Messages:** Click on the server or client avatar to manually send a message.

![](img/light/websocket1.png?version=1.1.0)

### Message Debugging

Listen offers two primary methods for intercepting and modifying WebSocket traffic:

#### 1. Using the Rewrite Feature

Configure [Rewrite](/en/rewrite) rules to intercept and edit messages sent by the server or client. When creating a rule, you can:

* Replace or modify the **WebSocket message body**.
* Optionally change the **WebSocket message type** (OpCode).

![](img/light/websocket2.png?version=1.1.0)

#### 2. Using the Scripting Feature

Use [Scripting](/en/script) to write JavaScript code for more flexible control over message manipulation. You can define two key methods in your script:

* **`onSendMessage({body, bodyType, url, opCode})`**: Called before a client message reaches the server. It returns `{opCode, body}` as the modified message.
* **`onReceiveMessage({body, bodyType, url, opCode})`**: Called before a server message reaches the client. It returns `{opCode, body}` as the modified message.

**Parameter Descriptions:**

| Parameter | Description |
| --- | --- |
| **body** | The content of the request or response (String, JSON-serializable Object, or `Uint8Array`). |
| **bodyType** | The data type of the body (e.g., `"string"`, `"json"`, `"uint8array"`). |
| **url** | The full URL of the request. |
| **opCode** | The WebSocket OpCode (message type). |

**Example:**
The following script modifies every outgoing client message to `"send message"` and every incoming server message to `"receive message"`.

![](img/light/websocket3.png?version=1.1.0)