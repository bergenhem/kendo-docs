---
title: kendo.dataviz.ui.Map
meta_title: Configuration, methods and events of Kendo UI DataViz Map
meta_description: Learn how to configure Kendo UI Javascript chart widget in a few easy steps, use and change methods and events.
slug: api-dataviz-map
relatedDocs: gs-dataviz-map-overview
tags: api,dataviz,map,maps,spatial,geoviz
publish: true
---

# kendo.dataviz.ui.Map

## Configuration

### center `Array`

The map center. Coordinates are listed as `[Latitude, Longitude]`.
You can also use a `kendo.dataviz.map.Location` instance.

### controls `Object`

The configuration of built-in map controls.

### controls.navigator `Boolean|Object` *(default: true)*

Enables or disables the built-in navigator control (directional pad).

### controls.navigator.position `String` *(default: "topLeft")*

The position of the navigator control. Possible values include:

* "topLeft"
* "topRight"
* "bottomRight"
* "bottomLeft"

### controls.zoom `Boolean|Object` *(default: true)*

Enables or disables the built-in zoom control (+/- button).

### controls.zoom.position `String` *(default: "topLeft")*

The position of the zoom control. Possible values include:

* "topLeft"
* "topRight"
* "bottomRight"
* "bottomLeft"

### layerDefaults `Object`

The default configuration for map layers by type.

### layerDefaults.shape `Object`

The default configuration for shape layers.

### layerDefaults.shape.copyright `String`

The copyright message for all shape layers.

### layerDefaults.shape.style `Object`

The default style for shapes.

### layerDefaults.shape.style.fill `Object`

The default fill for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

### layerDefaults.shape.style.fill.color `String`

The default fill color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

### layerDefaults.shape.style.fill.opacity `Number`

The default fill opacity (0 to 1) for layer shapes.

### layerDefaults.shape.style.stroke `Object`

The default stroke for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

### layerDefaults.shape.style.stroke.color `String`

The default stroke color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

### layerDefaults.shape.style.stroke.dashType `String` *(default: "solid")*

The default dash type for layer shapes.
The following dash types are supported:

* "dash" - a line consisting of dashes
* "dashDot" - a line consisting of a repeating pattern of dash-dot
* "dot" - a line consisting of dots
* "longDash" - a line consisting of a repeating pattern of long-dash
* "longDashDot" - a line consisting of a repeating pattern of long-dash-dot
* "longDashDotDot" - a line consisting of a repeating pattern of long-dash-dot-dot
* "solid" - a solid line

### layerDefaults.shape.style.stroke.opacity `Number`

The default stroke opacity (0 to 1) for layer shapes.

### layerDefaults.shape.style.stroke.width `Number` *(default: 1)*

The default stroke width for layer shapes.

### layerDefaults.tile `Object`

The default configuration for tile layers.

### layerDefaults.tile.urlTemplate `String`

The URL template for tile layers. Template variables:

* x - X coordinate of the tile
* y - Y coordinate of the tile
* zoom - zoom level

### layerDefaults.tile.copyright `String`

The copyright message for all tile layers.

### layers `Array`

The configuration of the map layers.
The layer type is determined by the value of the type field.

### layers.autoBind `Boolean` *(default: true)*

If set to `false` the layer will not bind to the data source during initialization. In this case data binding will occur when the [change](/api/framework/datasource#events-change) event of the
data source is fired. By default the widget will bind to the data source specified in the configuration.

> Setting `autoBind` to `false` is useful when multiple layers (widgets) are bound to the same data source. Disabling automatic binding ensures that the shared data source doesn't make more than one request to the remote service.

### layers.type `String`

The layer type. Supported types are:

* "tile" - a generic "slippy map" tile layer
* "shape" - a vector shape layer, e.g. bound to GeoJSON data

### layers.dataSource `Object|Array|kendo.data.DataSource`

The data source of the layer. Can be a JavaScript object which represents a valid data source configuration, a JavaScript array or an existing [kendo.data.DataSource](/api/framework/datasource)
instance.

### layers.copyright `String`

The copyright message for the layer.

### layers.style `Object`

The default style for shapes.

### layers.style.fill `Object`

The default fill for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

### layers.style.fill.color `String`

The default fill color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

### layers.style.fill.opacity `Number`

The default fill opacity (0 to 1) for layer shapes.

### layers.style.stroke `Object`

The default stroke for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

### layers.style.stroke.color `String`

The default stroke color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

### layers.style.stroke.dashType `Number` *(default: 1)*

The default dash type for layer shapes.
The following dash types are supported:

* "dash" - a line consisting of dashes
* "dashDot" - a line consisting of a repeating pattern of dash-dot
* "dot" - a line consisting of dots
* "longDash" - a line consisting of a repeating pattern of long-dash
* "longDashDot" - a line consisting of a repeating pattern of long-dash-dot
* "longDashDotDot" - a line consisting of a repeating pattern of long-dash-dot-dot
* "solid" - a solid line

### layers.style.stroke.opacity `Number`

The default stroke opacity (0 to 1) for layer shapes.

### layers.style.stroke.width `Number` *(default: 1)*

The default stroke width for layer shapes.

### layers.urlTemplate `String`

The URL template for tile layers. Template variables:

* x - X coordinate of the tile
* y - Y coordinate of the tile
* zoom - zoom level

### markerDefaults `Object`

The default options for all markers.

### markerDefaults.color `String`

The default marker color. Accepts a valid CSS color string, including hex and rgb.

### markerDefaults.size `Number`

The default marker size in pixels.

### markerDefaults.shape `String`

The default marker shape. Supported shapes:

* "pin"
* "circle"

### markers `Array`

The initial markers to display on the map.

### markers.color `String`

The marker color. Accepts a valid CSS color string, including hex and rgb.

### markers.position `Array`

The marker position. Coordinates are listed as `[Latitude, Longitude]`.
You can also use a `kendo.dataviz.map.Location` instance.

### markers.size `Number`

The marker size in pixels.

### markers.shape `String`

The marker shape. Supported shapes:

* "pin"
* "circle"

### minZoom `Number` *(default: 2)*

The minimum zoom level.

### maxZoom `Number` *(default: 19)*

The maximum zoom level.

### minSize `Number` *(default: 256)*

The size of the map in pixels at zoom level 0.

### theme `String` *(default: "default")*

The map theme name.

The built-in themes are:

* "black"
* "blueopal"
* "bootstrap"
* "default"
* "flat"
* "highcontrast"
* "metro"
* "metroblack"
* "moonlight"
* "silver"
* "uniform"

### zoom `Number` *(default: 3)*

The initial zoom level.

Typical web maps use zoom levels from 0 (whole world) to 19 (sub-meter features).

The map size is derived from the zoom level and minScale options: `size = (2 ^ zoom) * minSize`

## Methods

### destroy

Prepares the widget for safe removal from DOM. Detaches all event handlers and removes jQuery.data attributes to avoid memory leaks. Calls destroy method of any child Kendo widgets.

> This method does not remove the widget element from DOM.

## Events

### click

Fired when the user clicks on the map.

### reset

Fired when the map is reset, e.g. on initial load or during zoom.

### pan

Fired while the map viewport is being moved.

### panEnd

Fires after the map viewport has been moved.

### shapeClick

Fired when a shape is clicked or tapped.

### shapeCreated

Fired when a shape is created, but is not rendered yet.

### shapeMouseEnter

Fired when the mouse enters a shape.

### shapeMouseLeave

Fired when the mouse leaves a shape.

### zoomStart

Fired when the map zoom level is about to change.

### zoomEnd

Fired when the map zoom level has changed.

