---
title: map-controls
slug: jsp-map-controls
tags: api, java
publish: true
---

# \<kendo:map-controls\>

The configuration of built-in map controls.

#### Example
    <kendo:map>
        <kendo:map-controls></kendo:map-controls>
    </kendo:map>

## Configuration Attributes

### navigator `boolean`

Enables or disables the built-in navigator control (directional pad). Further configuration is available via [kendo:map-controls-navigator](#kendo-map-controls-navigator). 

#### Example
    <kendo:map-controls navigator="navigator">
    </kendo:map-controls>

### zoom `boolean`

Enables or disables the built-in zoom control (+/- button). Further configuration is available via [kendo:map-controls-zoom](#kendo-map-controls-zoom). 

#### Example
    <kendo:map-controls zoom="zoom">
    </kendo:map-controls>


##  Configuration JSP Tags

### kendo:map-controls-navigator

Enables or disables the built-in navigator control (directional pad).

More documentation is available at [kendo:map-controls-navigator](map/controls-navigator).

#### Example

    <kendo:map-controls>
        <kendo:map-controls-navigator></kendo:map-controls-navigator>
    </kendo:map-controls>

### kendo:map-controls-zoom

Enables or disables the built-in zoom control (+/- button).

More documentation is available at [kendo:map-controls-zoom](map/controls-zoom).

#### Example

    <kendo:map-controls>
        <kendo:map-controls-zoom></kendo:map-controls-zoom>
    </kendo:map-controls>

