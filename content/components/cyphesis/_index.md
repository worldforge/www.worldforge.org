---
title: "Cyphesis server"
menu:
    main:
        weight: 2
        parent: "Components"

---
{{< youtube WTFL5hp5reI "Endless world" "float:right; padding: 5px;" >}}
Cyphesis is the main WorldForge server. It provides everything needed in order to run a virtual world.

Some of the features provided are:

* Automatic persistence of worlds through SQLite
* Full physics simulation through Bullet
* Powerful terrain generation through [Mercator](/components/mercator)
* Fully scriptable through Python
* Automatic update of all game rules and scripts during runtime
* Extensive AI system, with Goal Based behaviour and NavMesh based path finding
* Extremely extensible; core features are handled in C++ code, all game play is scriptable in C++

### Download

We provide pre-build binaries for Linux.

Either as a [Snap package](https://snapcraft.io/cyphesis)
Or as [native packages](https://software.opensuse.org//download.html?project=games%3AWorldForge&package=cyphesis) for
multiple distros
These packages are all automatically built from the latest source.

### Building

For building see the instructions found in the [source](https://github.com/worldforge/cyphesis).

### Running locally

If you're interested in building your own world we encourage you to run a local instance of Cyphesis. By running it
locally you can effortless connect with Ember in administrative mode, with the ability to fully alter the world. This is
demonstrated in this short video.

By running locally you also have access to a lot of administrative tools which will help you with keeping backups of the
world, inspecting code and so on.