---
title: map-layer
slug: jsp-map-layer
tags: api, java
publish: true
---

# \<kendo:map-layer\>

The configuration of the map layers.
The layer type is determined by the value of the type field.

#### Example
    <kendo:map-layers>
        <kendo:map-layer></kendo:map-layer>
    </kendo:map-layers>

## Configuration Attributes

### autoBind `boolean`

If set to false the layer will not bind to the data source during initialization. In this case data binding will occur when the change event of the
data source is fired. By default the widget will bind to the data source specified in the configuration.

#### Example
    <kendo:map-layer autoBind="autoBind">
    </kendo:map-layer>

### copyright `java.lang.String`

The copyright message for the layer.

#### Example
    <kendo:map-layer copyright="copyright">
    </kendo:map-layer>

### type `java.lang.String`

The layer type. Supported types are "tile" and "shape".

#### Example
    <kendo:map-layer type="type">
    </kendo:map-layer>

### urlTemplate `java.lang.String`

The URL template for tile layers. Template variables:

#### Example
    <kendo:map-layer urlTemplate="urlTemplate">
    </kendo:map-layer>


##  Configuration JSP Tags

### kendo:map-layer-style

The default style for shapes.

More documentation is available at [kendo:map-layer-style](map/layer-style).

#### Example

    <kendo:map-layer>
        <kendo:map-layer-style></kendo:map-layer-style>
    </kendo:map-layer>

