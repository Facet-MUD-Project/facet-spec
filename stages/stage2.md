# Stage 2 - Basic chat server

This is the second stage of development, standing up a basic chat server. Users
are able to create accounts, which are saved to disk; log in to existing
accounts; and send chat messages which are broadcast to all connected users.

## Required Features

The following set of features MUST be implemented fully in order for the Facet
implementation to be considered complete for Stage 1.

### Required Commands

Other than what is required to log into an account the only other input that needs to be handled to meet this Stage are these commands.

* `say`or `chat` \<message to be sent> - sends a message to all other connected accounts as well as the sender. Formats as follows:

> self: You say/chat: <message>

> others: self.name says/chats: <message>

* `quit` - quits the mud causing the player's account to be saved to disk, all remaining output to be sent be written to the player's connection, and then the closing of the player's connection. Optionally 

### Telnet Server

The implementation MUST provide a way to start a telnet server which remains
open at a specified port number. This telnet server MUST support the parts of
the telnet protocol specified in [Telnet - Stage 1].

### Login

On login a user should be greated with some kind of welcome message, be it an ascii banner or just a simple line of text. They will then be asked if they would like to log into an exisiting account or a make a new account. 

If they want to log into an existing account, they will be asked for the account username and then the account password. The MUD will then try to find an account by that username. If the account does not exist the player will be informed that the password did not match and be disconnected. Otherwise they will be logged into the MUD.

### Account Creation

If the previously mentioned user wanted to make a new account, they will be asked what username they would like to use, this username will be checked against existing accounts. If the name is already in use the player will be informed that the name is not available and please try another. If after another two tries they have still not been able to secure an unused account username they will receive a message of condolence and be disconnected. 

They will then be asked to confirm if this username is the one they want and if not they will start over the previous process of choosing a username. 

Otherwise they will then be asked to choose a password that is at least 8-12 characters in length and then asked to confirm that password. If the confirmation matches, an account will be made using that username and password combination and logged into the MUD just as if they already had an account and succesfully logged in. Otherwise they will receive a condolence message and be disconnected.

[Telnet - Stage 1]: ../features/telnet.md
