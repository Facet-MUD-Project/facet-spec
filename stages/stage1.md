# Stage 1 - Echo Server

This is first stage of development and acts as a test for whatever networking library is used for this version of the MUD. 

## Required Features

The echo server needs to have a listening socket that can be connected to via either a mud or telnet client. It will then accept connections on said listening socket and wait for a user to connect. It will then create a new connection/player object for that user to send and receive data on. Until the user closes their connection any data sent to the listening socket will be outputed on the listening sockets side as well as being echoed back to the sending connection.