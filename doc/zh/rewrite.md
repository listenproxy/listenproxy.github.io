# 重写

> 重写功能可以使用事先创建好的规则在请求发送到服务器之前对请求进行修改，从而实现对请求的重写和调整。也可以在响应返回给客户端之前对响应进行修改，从而实现对响应的重写和调整。

### 开启重写功能

开启步骤：重写菜单->启用重写。开启后，重写菜单下面会有小绿点，表示重写功能已开启。

![](img/light/重写1.png?version=1.1.0)

### 新增重写规则

1. 操作路径：重写菜单->管理规则->规则列表右上角"+"按钮。
2. 在弹窗里，填写匹配规则和行为，点击“确定”按钮即可新增规则。

![](img/light/重写2.png?version=1.1.0)

### 修改请求

修改请求时可以对发送到服务器的请求进行新增参数、修改参数、删除参数、新增请求头、修改请求头、删除请求头、替换请求体、修改请求体等修改。

#### 新增参数

在URL后面添加新的参数，格式为key=value。

**例：**请求URL为`https://listen-proxy.com/`，下面的配置会将发送到服务器的URL修改为`https://listen-proxy.com/?test=1`。

![](img/light/重写2.png?version=1.1.0)

#### 修改参数

对URL参数进行匹配（支持正则表达式、忽略大小写），替换匹配到的参数的值。

**例：**请求URL为`https://listen-proxy.com/?test=1`，下面的配置会将发送到服务器的URL修改为`https://listen-proxy.com/?test=2`。

![](img/light/重写3.png?version=1.1.0)

#### 删除参数

对URL参数进行匹配（支持正则表达式、忽略大小写），删除匹配到的参数和值。

**例：**请求URL为`https://listen-proxy.com/?test=1`，下面的配置会将发送到服务器的URL修改为`https://listen-proxy.com/`。

![](img/light/重写4.png?version=1.1.0)

#### 新增请求头

添加新的请求头字段，格式为key: value。

**例：**请求URL为`https://listen-proxy.com/`，下面的配置会在请求头中添加`test_add_header: 1`。

![](img/light/重写5.png?version=1.1.0)

#### 修改请求头

对请求头字段进行匹配（支持正则表达式、忽略大小写），替换匹配到的字段的值。

**例：**请求URL为`https://listen-proxy.com/`，下面的配置会把请求头中`Accept-Language`字段的值修改为`zh-CN`。

![](img/light/重写6.png?version=1.1.0)

#### 删除请求头

对请求头字段进行匹配（支持正则表达式、忽略大小写），删除匹配到的字段和值。

**例：**请求URL为`https://listen-proxy.com/`，下面的配置会把请求头中`Accept-Language`字段删除。

![](img/light/重写7.png?version=1.1.0)

#### 替换请求体

将请求体替换为指定的内容，支持文本和文件。

**例：**请求URL为`https://listen-proxy.com/`，下面的配置会把请求体数据替换为`替换请求体数据`。

![](img/light/重写8.png?version=1.1.0)

#### 修改请求体

对请求体进行文本匹配（支持正则表达式、忽略大小写），替换匹配到的文本。

**例：**请求URL为`https://listen-proxy.com/`，请求体为`{"test":1}`，下面的配置将会把请求体修改为`{"test1":1}`。

![](img/light/重写9.png?version=1.1.0)

### 修改响应

修改响应时可以对服务器的响应进行新增请求头、修改请求头、删除请求头、替换请求体、修改请求体等修改。这些修改规则和修改请求的规则类似，只不过是针对响应进行的。

![](img/light/重写10.png?version=1.1.0)