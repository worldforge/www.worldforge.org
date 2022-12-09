---
title: "Varconf"
menu:
    main:
        weight: 8
        parent: "Components"

---

Varconf is a C++ utility library for handling configuration and settings. It includes:

* A framework for storing and retrieving configuration data.
* Loading and saving of config files.
* Handling of complex command line arguments.
* Signals to notify the application of configuration changes.
* Server, client and tool developers can use Varconf to handle the configuration of their application.

While it has good support for handling flat configuration data, it is not suited for more complex structured data. It's recommended that developers use Atlas to store complex data.

### Source

The source code for Varconf can be found on [Github](https://github.com/worldforge/varconf).