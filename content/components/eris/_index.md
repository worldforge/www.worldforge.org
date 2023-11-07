---
title: "Eris"
menu:
    main:
        weight: 5
        parent: "Components"

---

Eris is designed to simplify client development (and promote code reuse) by providing a common system to deal with the
back-end Atlas tasks. Notably, Eris encapsulates most of the work in getting Atlas entities available on your client,
logging into a server, and managing updates from the server. Once the entities are made available locally, Eris also
manages updating them as required.

Thus it can be considered as a session layer above Atlas, providing persistent (for
an entire gaming session) objects as opposed to transient Atlas ones. It handles the client-side implementation of the
meta-server protocol, and querying game servers; out-of-game (OOG) operations (via the Lobby and Rooms), and most
important in-game (IG) operations such as entity creation, movement and updates.

### Source

The source code for Eris can be found on [Github](https://github.com/worldforge/worldforge/tree/master/libs/eris).