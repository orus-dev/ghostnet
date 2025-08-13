# Ghost Net
Ghost Net is a protocol and specsheet built for privacy against censorship and surveillance.

## What is the goal of Ghost Net?
Ghost Net is a strict ruleset and a protocol for a client to communicate with a server, the server won't track or log anything the client does, including the client's IP address, we aim to make a censorship free, anti-surveillance internet with a safe and fast web browsing / internet experience.

## Ghost Chaining
Ghost Chaining is a peer-to-peer system where a client can swap and act like another client, A client has 2 connections, one connection is made by the client that it's swapping with, the connection is the next connection by the next client.

<img src="ghost-chaining.png" alt="Ghost Chaining" height=300 />

### The client has the following responsibilities:
- Listen for 2 connections, one connection is the mask client, and the other is the next client.
- Send the target TCP server ip:port to the parent after the connection is established.
- Establish a connection to a TCP server with the address from a child client.
- Send data to the parent client.
- Read from a child and send it to the TCP server that was provided on handshake.