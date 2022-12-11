---
title: "Recent changes to the client"
date: 2017-11-26
---

{{< imgresize "img.png" "360x360" "A vista" "float:left; padding: 5px;">}}

There's been a couple of changes to Ember lately. I'll try to summarize them here

\* The biggest one is that we now use OpenGL 3 and later. Previously we used OpenGL 2. The main reason is that OpenGL 3 has a couple of features that we really benefit from, especially when it comes to instancing techniques. Support for this version should also be solid, with all modern GPUs providing compatible drivers.

Using OpenGL 3 also allows us to use more modern features for diagnostics.

This also sets us up better for a possible migration to OGRE 2.1+.

As part of this I've also removed our support for DirectX. The main reason is that I simply don't have time enough to support a second render system, with the need to provide matching HLSL scripts for all of our GLSL shaders. OpenGL works on Windows as well, although performance might suffer in some cases.

\* The usage of Cg has been completely removed. The Cg shaders that we used have all been rewritten in GLSL.

\* Almost all use of the standard OGRE Entity class has been replaced with InstancedEntity. This means that we're now much more efficient when rendering multiple entities of the same type.

OGRE is especially inefficient when rendering multiple entities of the same type, since each entity will result in at least one (often many) rendering call. 

Modern GPUs are however designed to easily handle large sets of data, with as few rendering calls as possible.

This is one of the reasons Ember often struggle on seemingly powerful enough GPUs.

With this change performance should improve.

With OGRE 2.1+ a lot of this has been redesigned however, and my impression is that Ember should perform even better on this platform.

\* Hardware skinning has been added, so that all animated entities are now skinned on the GPU rather than the CPU.

\* Support for the OGRE profiler has been added, so that an overlay showing time spent in various parts of OGRE can be shown. Enable this through the "Developer" tab in the settings dialog.

\* We now have a benchmark in place, to be used for evaluating performance. It can be run by issuing the "/benchmark" command while logged in.

\* Ember will automatically now detect when some media has been changed on disk, and reload it automatically. It currently mainly supports textures. I.e. if you alter a texture while Ember is running it will automatically reload it. Pretty nifty when working with media.