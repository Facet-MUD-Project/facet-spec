# facet-spec

This repository contains specifications for the various implementations of the
Facet MUD Project.

Documents in this repository utilize the keywords for requirement levels lined
out in [RFC 2119]: `MUST`, `MUST NOT`, `SHOULD`, `SHOULD NOT`, `MAY`.

## Development Stages

These define the various stages of development for the implementations of the
Facet MUD project. This will help us measure and advertise the level of support
offered by them. They also help to ensure feature parity across all
implementations, as long as these are throughly defined and maintained.

* [Stage 0](./stages/stage0.md) - Skeleton repository
* [Stage 1](./stages/stage1.md) - Basic chat server
* Stage 2 - TBD

## Data Specifications

* [Player save files](./data/players.md)
* [Enums](./data/enums.md)

### Notes about type nomenclature

In this specification we will use a generic representation

* int - Denotes appropriately sized and typed integers.
* float - Denotes a representation of a decimal value. Does not denote how accurate it is.
* string - Denotes a text representation appropriate to language being used. May or may not be UTF-8 capable.
* map - Denotes a list containing key/pair values. Also known as a mapping, hashmap, associative array, and others. When a map in the specifications is defined it MUST give the key and value types.

[RFC 2119]: https://tools.ietf.org/html/rfc2119
