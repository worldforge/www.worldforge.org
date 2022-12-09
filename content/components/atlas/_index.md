---
title: "Atlas protocol"
menu:
    main:
        weight: 3
        parent: "Components"

---
The protocol which binds all of Worldforge together is called Atlas. It's a protocol meant to express a complete virtual worlds, and all communication between the servers and the clients uses it. The world itself as well as all actions that occur are all expressed through Atlas.

The canonical implementation is Atlas C++, which as the name hints is written in C++. The protocol itself is implementation independent, but so far there has been no need for alternative implementations. More information about the protocol specification can be found at the [wiki](http://wiki.worldforge.org/wiki/Atlas_Protocol).

Source
The source for Atlas-C++ is available at [Github](https://github.com/worldforge/atlas-cpp).