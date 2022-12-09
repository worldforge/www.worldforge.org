---
title: "Worlds"
menu:
    main:
        weight: 9
        parent: "Components"

---

While the whole Worldforge project is designed to allow for you to create your own world we do provide some default
worlds. These are mainly meant to be used as examples of what you can do, and as starting points for your own creations.
The Worlds are defined using XML declarations, and are meant to be loaded into a running instance of [Cyphesis](/components/cyphesis), using the
cyimport command, like such:

`cyimport deeds/braga/world.xml`

Get the source from [Github](https://github.com/worldforge/worlds).

## Deeds

The default ruleset is called "Deeds". The ruleset defines the rules of the world, i.e. how things behave. By altering
the ruleset you change the rules of the world. The Deeds worlds are all set in a fictional fantasy world called Dural.
It's your basic medieval RPG setting.

The focus of Deeds is on simple combat and crafting mechanics.

## The island of Braga

{{< imgresize screenshot_20140802_154948.jpg "360x360" "Some carrots" "float:right; padding: 5px;">}}

Our default world is the island of Braga, a rather small island in unknown waters. The world is designed to teach the
user the basic gameplay mechanics and to introduce some simple combat and crafting situations.

## The demo world

We also provide a simple demonstration world. This world is only meant to be used by world creators as an example of the
various mechanics. Install it on a running server through (note that this will clear any existing world)

`cyimport --clear deeds/demo/world.xml`