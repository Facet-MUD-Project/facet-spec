# Telnet

The telnet protocol and a telnet server are at the heart of MUDs, as they are
how a user communications with the game, and vice versa. As such, as we need
specific pieces of the protocol implemented in order to make the game function.

A developer implementing the telnet protocol for a particular Facet
implementation SHOULD use a pre-existing external library. This not only helps
avoid too much [yak shaving], but abstracts the complexities of the protocol out
of the game engine. If a pre-existing library is not available, or if none of
the available options can be modified to suit our purposes, then a developer MAY
create a new library for the purpose. This library MUST be external to the game
implementation itself, but MAY be hosted in the FacetMUD organization.

Below are the most essential parts of the protocol and when they MUST be
implemented in the development of a game engine.

## Stage 1 - Basic Chat Server

For the beginning implementation of a game engine, a developer must include
support for the following:

* [RFC 854] - Telnet Protocol Specification<br>
  
  This is the core telnet protocol, and thus the entire protocol MUST be
  supported in order to build upon for the future stages.
* [RFC 857] - Telnet Echo Option

  This allows the server to either echo, or stop echoing, input back to the
  client. This option is key for when a user is entering their password. By
  using this option, said password is not echoed back to the user when entered.

## References

* [RFC 854] - Telnet Protocol Specification
* [RFC 855] - Telnet Option Specifications
* [RFC 856] - Telnet Binary Transmission
* [RFC 857] - Telnet Echo Option
* [RFC 858] - Telnet Suppress Go Ahead Option
* [RFC 859] - Telnet Status Option
* [RFC 860] - Telnet Timing Mark Option
* [RFC 861] - Telnet Extended Options: List Option

[RFC 854]: https://datatracker.ietf.org/doc/html/rfc854
[RFC 855]: https://datatracker.ietf.org/doc/html/rfc855
[RFC 856]: https://datatracker.ietf.org/doc/html/rfc856
[RFC 857]: https://datatracker.ietf.org/doc/html/rfc857
[RFC 858]: https://datatracker.ietf.org/doc/html/rfc858
[RFC 859]: https://datatracker.ietf.org/doc/html/rfc859
[RFC 860]: https://datatracker.ietf.org/doc/html/rfc860
[RFC 861]: https://datatracker.ietf.org/doc/html/rfc861
[yak shaving]: http://joi.ito.com/weblog/2005/03/05/yak-shaving.html
