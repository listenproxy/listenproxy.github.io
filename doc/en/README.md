# Introduction

> **Listen** is a modern front-end proxy debugging tool that offers request modification, response modification, API Mocking, and other features to help you debug network requests efficiently.

## Features

Listen provides two core functions: Request Proxy and Request Simulation. Request Proxy allows for packet capturing and data modification through custom rules. Request Simulation allows captured requests to be edited and re-sent.

### Request Proxy

* [x] **Mapping:** Map server directories to local directories.
* [x] **Rewriting:** Use predefined rules to intercept and modify requests and responses.
* [x] **Breakpoints:** Interrupt and modify requests and responses in real-time.
* [x] **Scripting:** Write JavaScript code for programmatic modification of requests and responses.
* [x] **Gateway:** Block specific requests.
* [x] **Mirroring:** Map domain names.
* [x] **Gateway Proxy:** Use Virtual Network Interface Card (TUN mode) to proxy HTTP requests from all applications on the machine.
* [x] **Secondary Proxy:** Forward requests to other proxy servers.
* [x] **WebSocket:** Support for WebSocket debugging, allowing the sending and modification of WebSocket messages.


![](img/light/请求代理.png?version=1.1.0)

### Request Simulation

* [x] **Request Simulation:** Construct any HTTP/HTTPS request.
* [x] **Edit & Resend:** Works with the Request Proxy feature to quickly modify and re-send captured requests.

![](img/light/请求模拟.png?version=1.1.0)