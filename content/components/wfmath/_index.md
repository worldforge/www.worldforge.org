---
title: "WFMath"
menu:
    main:
        weight: 7
        parent: "Components"

---

The primary focus of WFMath is geometric objects. Thus, it includes several shapes (boxes, balls, lines), in addition to
the basic math objects that are used to build these shapes (points, vectors, matricies).

### Source

The source code for WFMath can be found on [Github](https://github.com/worldforge/worldforge/tree/master/libs/wfmath).

### Geometries

Most of the library classes can be divided into two sorts. The first kind are basic mathematical objects, whose members
are all fundamental types. The second kind are shapes, which implement the shape class interface described in
doc/shape.h. There are four classes of the first kind:

### Vector<>

A basic mathematical vector

### RotMatrix<>

An orthogonal matrix of determinant 1, useful for describing rotations.

### Point<>

A point in space. This basic class also implements the shape interface in doc/shape.h.

### Quaternion

A quaternion

The shape classes are:

### AxisBox<>

A box oriented parallel to the coordinate axes

### Ball<>

Ball<2> is a circle, Ball<3> is a sphere, etc.

### Segment<>

A line segment, defined by its endpoints

### RotBox<>

Like AxisBox<>, but it can be rotated to arbitrary angles

### Polygon<>

A 2 dimensional polygon contained in a (possibly) larger dimensional space

The library also contains some probability-related functions, as well as wrappers for system time and random number
functions.

### Dependencies

WFMath requires an ISO C++ compiler. Atlas-C++ is not required in order to build WFMath, but if it is present then some
inline conversion function tests will be built.