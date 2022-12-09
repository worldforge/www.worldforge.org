---
title: "Mercator"
menu:
    main:
        weight: 6
        parent: "Components"

---

Mercator is primarily aimed at terrain for multiplayer online games and forms one of the WorldForge core libraries. It
is intended to be used as a terrain library on the client, while a subset of features is useful on the server.

Mercator is designed in such a way that individual tiles can be generated on-the-fly from a very small source data set.
Each tile uses a fast deterministic random number generation to ensure that identical results are produced "anytime,
anywhere". This enables transmission of terrain across low bandwidth links as part of the standard data stream, or
server side collision detection with the same terrain that the player sees.

The use of tiles means that there is inherently a large degree of gross control of the shape of the terrain. Finer
control is implemented by allowing geometric modifications - for example, a polygonal area might be flattened, or a
crater could be applied.

### Source

The source code for Mercator can be found on [Github](https://github.com/worldforge/mercator).

### Dependencies
Mercator depends on WFMath.

### Height generation
* uses deterministic random number generation and seeds to generate detailed terrain from sparse control points.
* each tile is seeded using the four surrounding control points shape of each tile is influenced by height, roughness and
  falloff parameters
### Height Modifications
* geometric modifications can be applied for small features
* new modifications can be added quite easily
### Shading
* generate shading information based on height and gradient
* new shaders can be added quite easily
* used on the client side
### Collision

Basic intersection/collision functions are implemented for

* bbox
* point
* ray

### Current Limitations
* multiple resolutions in the one terrain are unsupported

### Implementations
As of August 2013 Mercator is implemented and in use in the Cyphesis server as well as the Ember and Sear clients.