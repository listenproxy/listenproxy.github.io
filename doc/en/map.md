# Mapping

> The Mapping feature allows you to replace request URLs with specified local file paths or directories. This enables mapping for either individual files or entire websites, making front-end development and debugging significantly more convenient.

### Enabling the Mapping Feature

**Path:** Map Menu -> Enable Mapping. Once enabled, a small green dot will appear beneath the Mapping menu, indicating the feature is active.

![](img/light/映射1.png?version=1.1.0)

### Adding a Mapping Rule

1. **Path:** Mapping Menu -> Manage Rules -> Click the "+" button in the top right corner of the rule list.
2. In the popup window, fill in the matching rules and the local file or directory path, then click "OK" to add the rule.

![](img/light/映射2.png?version=1.1.0)

### Mapping Types

You can choose between two mapping methods: Map File or Map Directory.

* **Map File:** The requested URL is mapped to a specific local file path, allowing for single-file replacement.
* **Map Directory:** The requested URL is mapped to the corresponding file path within a local directory, enabling the mapping of an entire website or resource folder.

**Example:** If the request URL is `http://example.com/js/app.js`, and you configure a **Map File** rule with the local file path `D:/webroot/js/app.js` and the matching rule `http://example.com/js/app.js`, the response will return the contents of the local file `D:/webroot/js/app.js`.

![](img/light/映射2.png?version=1.1.0)

Furthermore, when selecting **Map File**, Regular Expressions (Regex) are supported for more flexible matching. Once Regex is enabled, you can use **$1-$100** in the local file path to represent sub-matching groups from the URL matching rule.

**Regex Example:** If the request URL is `http://example.com/js/app.js`, the local file path is configured as `D:/webroot/js/$1.js`, and the matching rule is `http://example\.com/js/([a-z0-9]+)\.js`, the response will return the contents of `D:/webroot/js/app.js`.

![](img/light/映射3.png?version=1.1.0)

In addition to mapping individual files, checking **Map Directory** allows you to map an entire URL path to a local directory.

**Directory Example:** If the request URL is `http://example.com/js/app.js`, you select **Map Directory** with the local directory `D:/webroot/js` and the matching rule `http://example.com/js`, the response will return the contents of `D:/webroot/js/app.js`.

![](img/light/映射4.png?version=1.1.0)