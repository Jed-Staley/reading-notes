# Class 12 Reading Notes

## Introduction

This reading covers the essentials of Web Sockets, their request/response handshake, and the differences between Socket.IO and native Web Sockets. It also touches on practical applications and debugging techniques for Socket.IO.

## Notes

### What is a Web Socket?

A Web Socket is a communication protocol that provides full-duplex communication channels over a single TCP connection, allowing real-time data transfer between the server and the client.

### Describe the Web Socket request/response handshake and what happens once the connection is established

The Web Socket handshake starts with the client sending an HTTP request to the server, requesting an upgrade to the Web Socket protocol. The server responds with an HTTP 101 status code, indicating the protocol switch. Once the connection is established, it remains open, enabling continuous bidirectional communication.

### Web Sockets provide a standardized way for the server to send content to a client without first receiving a request from that client

### What does the event handler `io.on()` do?

The event handler `io.on()` listens for connection events from clients. It triggers a callback function when an event occurs, allowing the server to handle incoming connections and define specific actions based on different events.

### Describe some possible proof of life or proof that the code works as expected

Possible proofs of life include:

- Successfully connecting to the server and receiving a welcome message.
- Emitting an event from the client and receiving a response from the server.
- Logging messages to the console indicating successful data transmission.

### What does `socket.emit()` do?

The `socket.emit()` function sends an event with data from the server to the client or from the client to the server. This allows for real-time communication between both ends.

### What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0)

WebSocket is a protocol that enables real-time communication, whereas Socket.IO is a library built on top of WebSocket that provides additional features such as automatic reconnection, event handling, and compatibility with various browsers.

### When would you use Socket.IO?

You would use Socket.IO when you need a robust, feature-rich library for real-time communication that handles reconnections, event broadcasting, and cross-browser compatibility.

### When would you use WebSockets?

You would use WebSockets when you need a lightweight, low-level protocol for real-time communication without the additional features provided by Socket.IO.

## Videos

### OSI Model Explained

Key takeaways:

- The OSI Model is a framework that standardizes the functions of a telecommunication or computing system into seven layers.
- Each layer serves a specific function and communicates with the layers directly above and below it.

### TCP Handshakes Explained

To explain to a non-technical friend:
The TCP handshake is like a greeting process between two devices. One device says "Hello, I want to talk to you," the other responds, "Hello, I’m here and ready to talk," and the first device replies, "Great, let’s start talking." This ensures both devices are ready to communicate before sending any actual data.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include understanding the technical aspects and practical applications of Web Sockets and Socket.IO, gaining proficiency in implementing real-time communication in web applications, and effectively troubleshooting and debugging Socket.IO implementations.
