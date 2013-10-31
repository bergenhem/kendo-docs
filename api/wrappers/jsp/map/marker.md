---
title: map-marker
slug: jsp-map-marker
tags: api, java
publish: true
---

# \<kendo:map-marker\>

The initial markers to display on the map.

#### Example
    <kendo:map-markers>
        <kendo:map-marker></kendo:map-marker>
    </kendo:map-markers>

## Configuration Attributes

### color `java.lang.String`

The marker color. Accepts a valid CSS color string, including hex and rgb.

#### Example
    <kendo:map-marker color="color">
    </kendo:map-marker>

### position `java.lang.Object`

The marker position. Coordinates are listed as [Latitude, Longitude].
You can also use a kendo.dataviz.map.Location instance.

#### Example
    <kendo:map-marker position="position">
    </kendo:map-marker>

### shape `java.lang.String`

The marker shape. Supported shapes are "pin" and "circle".

#### Example
    <kendo:map-marker shape="shape">
    </kendo:map-marker>

### size `float`

The marker size in pixels.

#### Example
    <kendo:map-marker size="size">
    </kendo:map-marker>

