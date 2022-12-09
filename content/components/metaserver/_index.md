---
title: "Metaserver"
menu:
    main:
        weight: 4
        parent: "Components"

---
The metaserver-ng serves as a general repository of WorldForge server information ... "meta" information to be specific.  The primary goal of the metaserver-ng is to be a dynamic discovery service whereby enough information is available for clients to deterministically connect to available WorldForge servers.



### For WorldForge Servers
Servers register with the metaserver-ng and provide information about themselves.  Some examples of information currently sent are:

IP Address
IP Port
Server Name
Server Type
Latency
Number of Client Connections
Number of World Entities
Server Ruleset
This information from the server point of view can be both static or dynamic, and is at the discretion of the server operator and configuration.  These values are stored as attributes for the server record.


### For WorldForge Clients
Clients have a well known location in which currently registered servers, and their information can be requested.  In this way, the client(s) can determine what servers they want to connect to.  The connections are not brokered through the metaserver-ng, direct connection via information provided by the metaserver-ng is used.



### Future Plans
There are a few specific items that are on the list of TODO for the metaserver-ng, but nothing radical in terms of functionality.  The following are a list of things that may be on the list:

* Allowing automatic client-server matching.  This is not a priority, as it is less suited for an MMO style game, but is definitely doable for other types of games.
* Allowing context sensitive client searches.  Allow for example a client to say "i only want servers that have a latency less than 100" or "I only want servers of type cyphesis" or "I only want servers running ruleset xyz".
* Providing a central authoritative repository for security/authentication.  This is something that has been discussed frequently, and while it is a good idea and will have to be done eventually, I think that only need will be able to properly drive this, which we currently don't have.
* Exporting of data to DNS.

For a full list of bugs and blueprints, launchpad can be referenced [here](https://launchpad.net/metaserver-ng).



### Release Information
Currently, the metaserver-ng is not given a release, and instead treated like an internal WorldForge tool to provide those services.  In order to inhibit the accidental proliferation of the metaserver-ng into the wild, no official WorldForge releases will happen in the near future.  The metaserver-ng, along with all other WorldForge applications, is of course available via source, and can be built by those who have an interest.

The source for the metaserver-ng, as always is available via the worldforge github page located [here](https://github.com/worldforge/metaserver-ng).  Additional information can be viewed via the README and the github pages.