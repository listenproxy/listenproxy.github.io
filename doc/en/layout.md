# Functional Layout

## Request Proxy Interface Layout

Listen provides two core functions: Request Proxy and Request Simulation. Request Proxy enables packet capturing and allows for the modification of sent and received data via custom rules. Request Simulation allows captured requests to be re-edited and re-sent.

### Request Proxy

* **Top Functional Area:** Contains all feature buttons related to proxy settings, including the enabling/disabling and rule editing for Gateway, Mirroring, Mapping, Rewriting, Scripting, and Breakpoint functions. It also includes the Pin button, Comparison Tool button, SSL Certificate Installation button, and the Global Proxy toggle.
* **Sidebar:** Used to switch between different functional interfaces (Request Proxy / Request Simulation).
* **Collection Area:** Aggregates currently captured requests, displaying a tree structure of domains and URLs. It also showcases request bookmarks, favorites, and history records.
* **Main Content Area:** Displays all currently captured requests. Double-click a request to view its detailed information.
* **Bottom Status Bar:** The left side contains the Collection ON/OFF toggle, while the right side features buttons to switch between layout modes (Horizontal / Vertical).

![](img/light/请求代理布局.png?version=1.1.0)

### Request Simulation

* **Top Functional Area:** Contains all feature buttons related to proxy settings, including the enabling/disabling and rule editing for Gateway, Mirroring, Mapping, Rewriting, Scripting, and Breakpoint functions. It also includes the Pin button, Comparison Tool button, SSL Certificate Installation button, and the Global Proxy toggle.
* **Sidebar:** Used to switch between different functional interfaces (Request Proxy / Request Simulation).
* **Collection Area:** Displays saved simulation requests.
* **Main Content Area:** Used for editing requests and displaying response data.
* **Bottom Status Bar:** The left side contains the Collection ON/OFF toggle, while the right side features buttons to switch between layout modes (Horizontal / Vertical).

![](img/light/请求模拟布局.png?version=1.1.0)