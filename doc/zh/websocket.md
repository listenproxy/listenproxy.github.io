# Websocket

> Listen对Websocket调试提供了良好的支持，可以方便的对消息进行查看与搜索，并且可以直接对客户端或服务器发送消息。利用重写和脚本功能，甚至可以拦截和修改服务器或客户端发送的消息。

### 消息查看

对于Websocket连接，双击打开详情面板，切换到Websocket选项卡中，即可实时查看服务端与客户端发送的消息。

* **搜索：**点击消息界面左上角的搜索按钮，可以打开搜索面板，进行消息搜索。
* **发送消息：**点击服务端或者客户端的头像，可以发送消息。

![](img/light/websocket1.png?version=1.1.0)

### 消息调试

Listen 提供了两种方式来拦截和修改消息。

#### 1. 使用重写功能调试

使用[重写功能](/zh/rewrite)编辑规则可以对服务端或客户端发送的消息进行拦截和修改。规则配置里可以选择对Websocket消息体进行替换或者修改，也可以选择是否对Websocket消息类型就行更改。

![](img/light/websocket2.png?version=1.1.0)

#### 2. 使用脚本功能调试

使用[脚本功能](/zh/script)可以编写JavaScript代码对服务端或客户端发送的消息进行更灵活的拦截和修改。

脚本里可以定义两个方法：

- `onSendMessage({body, bodyType, url, opCode})`： 在客户端发送消息到达服务器之前调用，返回的`{opCode, body}`为修改后的消息类型和消息体。
- `onReceiveMessage({body, bodyType, url, opCode})`： 在服务器发送消息到达客户端之前调用，返回的`{opCode, body}`为修改后的消息类型和消息体。

两个方法的参数说明：

| 参数 | 描述 |
| --- | --- |
| **body** | 客户端或服务端发送的消息体，为一个字符串或可以被`JSON.stringify`的对象或者`Uint8Array`对象 |
| **bodyType** | body的类型，可能的值为"string"、"json"、"uint8array"等。 |
| **url** | 请求的完整URL地址。 |
| **opCode** | Websocket消息类型。 |

**例：**下面的脚本代码会在客户端发送到消息到达服务器之前将消息内容修改为"send message"。在服务器发送消息到达客户端之前，将消息内容修改为"receive message"。

![](img/light/websocket3.png?version=1.1.0)