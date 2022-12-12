---
title: "Create"
menu:
    main:
        weight: 4
---

{{< imgresize screenshot_20130922_203411.jpg "360x360" "Some carrots" "float:right; padding: 5px;">}}
One thing that sets Worldforge apart from most other online worlds is our focus on making sure that anyone can build and
host their own world. Since everything we do is Free Software you're free to use all of our code and assets for whatever
world you envision. Only your imagination sets the limit.

Whether you want a traditional MMORPG, with a medieval setting and monsters to fight, or a world filled with puzzles, or
just a world where you can hang out with your friends, Worldforge provides the tools that you need.

#### Starting out

Start out by first installing the [Ember](/components/ember) client and making yourself comfortable with it. The Ember
client is powerful and is used both by players as well as world authors. Once you've gotten the hang of it you should
run your own server. With your own server you're now free to alter the world to your whims. Using the client you can
create your own world, complete with your own terrain and your own entities. Initially you probably want to mainly focus
on reusing the existing assets, but in a new setting of your own choosing.

{{< imgresize screenshot_20140403_165440.jpg "360x360" "Some carrots" "float:left; padding: 5px;">}}

#### Going further

As you've become more familiar with the system you might want to go even further and start altering the game rules. The
default ruleset is called Deeds. The ruleset specifies all of the types of entities that are available (such as
creatures, vegetation, items and so on) as well as how these interact. This is all defined using a combination of
declarative specifications and Python code. And everything is available as Free Software. The Deeds ruleset is focused
on light combat and crafting. You can use that as a base for your own very specific world, with its own rules.

You should start by installing the [Cyphesis](/components/cyphesis) server. Either through a package for your operating
system, or through [building](/develop/build-source) the source yourself.