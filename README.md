# Worldforge main site

[![Join us on Gitter!](https://badges.gitter.im/Worldforge.svg)](https://gitter.im/Worldforge/Lobby)
[![Build site](https://github.com/worldforge/www.worldforge.org/actions/workflows/build_site.yml/badge.svg)](https://github.com/worldforge/www.worldforge.org/actions/workflows/build_site.yml)

This contains the Worldforge main site, which would normally be served at www.worldforge.org.

It uses the [Hugo](https://gohugo.io/) static site generator.

## Instructions

* Install Hugo. Last working version is 0.108
* Run ```hugo```
* Upload the content of the "public" directory to the www.worldforge.org site. Typically through rsync,
  like ```rsync -aP public/* www.worldforge.org:www```

## Development

During development you can keep an instance of Hugo running, to allow for automatic updates while you edit the site.

Do this through

``` bash
hugo server -D
```