# Certificate Installation

## Why install the certificate?

Listen uses Man-in-the-Middle (MITM) technology to capture and analyze HTTPS traffic. When a client communicates with the proxy server, the proxy server needs to re-sign the SSL certificate of the remote server. To ensure a successful SSL handshake between the client and the proxy server, the proxy server's root certificate must be installed in the client's local certificate management center.

## How to install the certificate

Listen provides a one-click installation feature. Simply click the "Install Certificate" button in the upper right corner to automatically install the certificate to the local user certificate management center. You can also follow the wizard to install the certificate manually.

![](img/light/安装证书1.png?version=1.1.0)

Once the installation is successful, the SSL icon will be highlighted.

![](img/light/安装证书2.png?version=1.1.0)