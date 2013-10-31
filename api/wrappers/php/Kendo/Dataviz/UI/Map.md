---
title: Map
slug: php-dataviz-ui-map
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\Map

A PHP wrapper for Kendo UI [Map](/api/dataviz/map).

Inherits from [\Kendo\UI\Widget](/api/wrappers/php/Kendo/UI/Widget).

## Usage

To use Map in a PHP page instantiate a new instance, configure it via the available
configuration [methods](#methods) and output it by `echo`-ing the result of the [render](/api/wrappers/php/Kendo/UI/Widget#render) method.

### Using Kendo Map

    <?php
    // Create a new instance of Map and specify its id
    $map = new \Kendo\Dataviz\UI\Map('Map');

    // Configure it
    $map->maxZoom(1)

    // Output it

    echo $map->render();
    ?>


## Methods

### center
The map center. Coordinates are listed as [Latitude, Longitude].
You can also use a kendo.dataviz.map.Location instance.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `array`



#### Example 
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->center(new array());
    ?>

### click
Fired when the user clicks on the map.
For additional information check the [click](/api/web/map#events-click) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->click('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onClick(e) {
            // handle the click event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->click('onClick');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->click(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### controls

The configuration of built-in map controls.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapControls|array`


#### Example - using [\Kendo\Dataviz\UI\MapControls](/api/wrappers/php/Kendo/Dataviz/UI/MapControls)
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $controls = new \Kendo\Dataviz\UI\MapControls();
    $navigator = true;
    $controls->navigator($navigator);
    $map->controls($controls);
    ?>

#### Example - using array

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $navigator = true;
    $map->controls(array('navigator' => $navigator));
    ?>

### layerDefaults

The default configuration for map layers by type.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerDefaults|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerDefaults](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerDefaults)
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $layerDefaults = new \Kendo\Dataviz\UI\MapLayerDefaults();
    $shape = new \Kendo\Dataviz\UI\MapLayerDefaultsShape();
    $layerDefaults->shape($shape);
    $map->layerDefaults($layerDefaults);
    ?>

#### Example - using array

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $shape = new \Kendo\Dataviz\UI\MapLayerDefaultsShape();
    $map->layerDefaults(array('shape' => $shape));
    ?>

### addLayer

Adds one or more MapLayer to the Map.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\MapLayer|array`

#### Example - using \Kendo\Dataviz\UI\MapLayer

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $autoBind = true;
    $layer->autoBind($autoBind);
    $map->addLayer($layer);
    ?>

#### Example - using array

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $autoBind = true;
    $map->addLayer(array('autoBind' => $autoBind));
    ?>

#### Example - adding more than one MapLayer

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $first  = new \Kendo\Dataviz\UI\MapLayer();
    $second = new \Kendo\Dataviz\UI\MapLayer();
    $map->addLayer($first, $second);
    ?>

### markerDefaults

The default options for all markers.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapMarkerDefaults|array`


#### Example - using [\Kendo\Dataviz\UI\MapMarkerDefaults](/api/wrappers/php/Kendo/Dataviz/UI/MapMarkerDefaults)
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $markerDefaults = new \Kendo\Dataviz\UI\MapMarkerDefaults();
    $color = 'value';
    $markerDefaults->color($color);
    $map->markerDefaults($markerDefaults);
    ?>

#### Example - using array

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $color = 'value';
    $map->markerDefaults(array('color' => $color));
    ?>

### addMarker

Adds one or more MapMarker to the Map.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\MapMarker|array`

#### Example - using \Kendo\Dataviz\UI\MapMarker

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $marker = new \Kendo\Dataviz\UI\MapMarker();
    $color = 'value';
    $marker->color($color);
    $map->addMarker($marker);
    ?>

#### Example - using array

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $color = 'value';
    $map->addMarker(array('color' => $color));
    ?>

#### Example - adding more than one MapMarker

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $first  = new \Kendo\Dataviz\UI\MapMarker();
    $second = new \Kendo\Dataviz\UI\MapMarker();
    $map->addMarker($first, $second);
    ?>

### maxZoom
The maximum zoom level.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->maxZoom(1);
    ?>

### minSize
The size of the map in pixels at zoom level 0.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->minSize(1);
    ?>

### minZoom
The minimum zoom level.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->minZoom(1);
    ?>

### pan
Fired while the map viewport is being moved.
For additional information check the [pan](/api/web/map#events-pan) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->pan('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onPan(e) {
            // handle the pan event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->pan('onPan');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->pan(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### panEnd
Fires after the map viewport has been moved.
For additional information check the [panEnd](/api/web/map#events-panEnd) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->panEnd('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onPanEnd(e) {
            // handle the panEnd event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->panEnd('onPanEnd');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->panEnd(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### reset
Fired when the map is reset, e.g. on initial load or during zoom.
For additional information check the [reset](/api/web/map#events-reset) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->reset('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onReset(e) {
            // handle the reset event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->reset('onReset');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->reset(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### shapeClick
Fired when a shape is clicked or tapped.
For additional information check the [shapeClick](/api/web/map#events-shapeClick) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeClick('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onShapeClick(e) {
            // handle the shapeClick event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeClick('onShapeClick');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeClick(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### shapeCreated
Fired when a shape is created, but is not rendered yet.
For additional information check the [shapeCreated](/api/web/map#events-shapeCreated) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeCreated('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onShapeCreated(e) {
            // handle the shapeCreated event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeCreated('onShapeCreated');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeCreated(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### shapeMouseEnter
Fired when the mouse enters a shape.
For additional information check the [shapeMouseEnter](/api/web/map#events-shapeMouseEnter) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeMouseEnter('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onShapeMouseEnter(e) {
            // handle the shapeMouseEnter event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeMouseEnter('onShapeMouseEnter');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeMouseEnter(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### shapeMouseLeave
Fired when the mouse leaves a shape.
For additional information check the [shapeMouseLeave](/api/web/map#events-shapeMouseLeave) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeMouseLeave('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onShapeMouseLeave(e) {
            // handle the shapeMouseLeave event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeMouseLeave('onShapeMouseLeave');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->shapeMouseLeave(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### theme
The map theme name.The built-in themes are:

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->theme('value');
    ?>

### zoom
The initial zoom level.Typical web maps use zoom levels from 0 (whole world) to 19 (sub-meter features).The map size is derived from the zoom level and minScale options: size = (2 ^ zoom) * minSize

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->zoom(1);
    ?>

### zoomEnd
Fired when the map zoom level has changed.
For additional information check the [zoomEnd](/api/web/map#events-zoomEnd) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->zoomEnd('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onZoomEnd(e) {
            // handle the zoomEnd event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->zoomEnd('onZoomEnd');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->zoomEnd(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### zoomStart
Fired when the map zoom level is about to change.
For additional information check the [zoomStart](/api/web/map#events-zoomStart) event documentation.

#### Returns
`\Kendo\Dataviz\UI\Map`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->zoomStart('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onZoomStart(e) {
            // handle the zoomStart event.
        }
    </script>
    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->zoomStart('onZoomStart');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $map = new \Kendo\Dataviz\UI\Map('Map');
    $map->zoomStart(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

