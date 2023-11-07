---
title: "Squall"
menu:
  main:
    weight: 3
    parent: "Components"

---

Squall is the component which makes it possible to sync media from the server to the client.

### Requirements

Since we had a couple of extra requirements we didn't want to just use basic file transfers for syncing media. The main
requirements we had were:

* Allow the client to connect to different servers, each with slightly different media. The idea here is that we provide
  base media, and then will let servers extend this with their own media. Thus we envision that a lot of the media will
  be similar. So for example, a client would connect to two different servers, which share 90% of common assets. These
  common assets wouldn't need to be re-downloaded.
* Have a built in mechanism for when assets are updated. This ties in to the vision we have about a development loop
  where the world is created inside a running server, without the need to restart the server. To accomplish this we need
  a good way to inform the client about changed assets. Whenever something changes the client should download the
  changed asset only.
* Use simple and tested existing file transfer mechanisms. Such as HTTP. We want to make it simple to expose assets
  using a basic file server.

### Design

All of these requirements led to the design of Squall. It borrows ideas from both Git and BitTorrent, in the sense that
all assets are represented by hashes of their content. This also goes for directories.

An effect of this is that a client only needs to download any hashes that it's missing. Thus fulfilling requirement #1.

Since directories also are computed using hashes of their content, any change to an assets will resonate to all its
parent directories and in the end to the root directory. Thus every change will result in a new hash for the root, which
can be commnuicated to the client. Thus fulfilling requirement #2.

And since we only need to expose data attached to hashes it's easy to serve data using a standard file server. Thus
fulfilling requirement #3.

### Stand alone library

The Squall library is licensed under the MIT license, with the hope that it might find use outside of Worldforge. While
it's contained in the monorepo it's also possible to build standalone.

### Source

The source for Squall is available at [Github](https://github.com/worldforge/worldforge/tree/master/libs/squall).