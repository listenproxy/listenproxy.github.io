# Mirror

> The Mirror feature allows you to replace the requested domain name with a specified domain, effectively redirecting the request. It works similarly to modifying a `hosts` file but is more convenient and flexible.

### Enabling the Mirror Feature

**Path:** Mirror Menu -> Enable Mirror. Once enabled, a small green dot will appear beneath the Mirror menu, indicating the feature is active.

![](img/light/镜像1.png?version=1.1.0)

### Adding a Mirror Rule

1. **Path:** Mirror Menu -> Manage Rules -> Click the "+" button in the top right corner of the rule list.
2. In the popup window, fill in the matching rules and the target mirror domain, then click "OK" to add the rule.

![](img/light/镜像2.png?version=1.1.0)

When the above rule is enabled, visiting [https://listen-proxy.com/](https://listen-proxy.com/) in your browser will return the content from [https://www.baidu.com/](https://www.baidu.com/).

### Replace Critical Headers

The Mirror feature supports replacing the **Host**, **Origin**, and **Referer** fields in the request headers. This ensures that the server can respond correctly (as some servers validate these fields and may block requests if they do not match the mirrored domain).