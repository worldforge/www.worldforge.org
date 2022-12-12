---
title: "Building from source"
menu:
    main:
        weight: 5
        parent: "Develop"

---
{{< imgresize screenshot_20140628_150933.jpg "360x360" "A wireframe view" "float:right; padding: 5px;">}}

If you're interested in helping out with the code, or just want to try the latest version, you should build from source.
Since Worldforge is made up of a lot of different components it's often cumbersome and confusing for new developers to
get everything built in order. For that reason we provide a build tool we call Hammer which we strongly recommend that
you use. It will download and build all necessary components. This page provides guidelines and help with building the
whole of Worldforge from source.

### Get access to a Linux system.

The core WorldForge system runs on Linux, MacOSX and Windows, and may well run on other unix like systems, but getting
involved in development is easiest if you are working on Linux, as that is the platform of choice of most of our
developers. This is not to say you must develop on Linux. We have developers who primarily use other systems, but life
is much easier if every developer at least has access to a Linux system to check stuff on. Most of the WorldForge C++
code uses standard GNU tools like autoconf and automake to manage the build, so it helps to be familiar with these. Any
up to date Linux distro should be fine. The best thing to do is get Linux installed on a machine you own, so you have
admin rights, and can work around any minor issues. It does not need to be your main desktop or laptop machine, and in
many ways your Linux system will not even need to have a monitor attached, as you can do almost everything by logging in
remotely.

### Fetch code and build.

The Worldforge project contains a large number of libraries and clients, which can be confusing for a newcomer. To
alleviate this we provide a script which will automatically fetch and build all the needed libraries used by Worldforge,
as well as the Cyphesis server and the Ember and Sear clients. This method is very much preferred for any new developer,
as it oftentimes can be time consuming to get all of the different libraries built in the correct order. Instructions on
how to use Hammer can be found [here](http://wiki.worldforge.org/wiki/Hammer_Script).
If you are impatient, here are the basic steps needed for building and running both the Cyphesis server and the Ember
client locally

    git clone git://github.com/worldforge/hammer.git
    cd hammer
    ./hammer.sh install-deps all
    ./hammer.sh checkout all
    ./hammer.sh build all
    ./work/local/bin/cyphesis&
    ./work/local/bin/ember

However, if you want to fetch and compile everything yourself we provide the instructions for this below.

### Get the code

We host all of our code on [Github](https://github.com/worldforge)

### Build and install the libraries.

Developers and users are encouraged to install WorldForge libraries from the binary packages available from our download
pages, or as part of many Linux distributions. As a developer, you should find this the best and easiest way to keep up
to date with the libraries, and help us test the packages.

However, building all the libraries from git source will provide an invaluable opportunity to learn how the WorldForge
system is put together. The libraries should be built in the following order, but feel free to change this order if you
want to find out how the dependencies work.

* [Atlas-C++](/components/atlas-cpp) 
* [Varconf](/components/varconf)
* [WFMath](/components/wfmath) 
* [Mercator](/components/mercator) 
* [Eris](/components/eris) 
* [Worlds](/components/worlds)

The [components section](/components) has details of what these libraries do, and you should make yourself familiar with
their roles.

### Build the Ember client

The [Ember](/components/ember) client is the main client used both for playing the game as well as authoring the world.
The main dependencies that you might need to install yourself are [Ogre3D](http://www.ogre3d.org/)
and [CEGUI](http://www.cegui.org.uk/).

### Build and install a WorldForge server.

The [Cyphesis](/components/cyphesis) server is the main game play server. Instructions for building from source are
available in the README file in the source directory, and on its page on the website. It is easiest to build and run on
Linux, but has also been tested on MacOSX and on Windows using [MingW](http://www.mingw.org/). Once you have it
installed and running, try connecting to it using Ember.