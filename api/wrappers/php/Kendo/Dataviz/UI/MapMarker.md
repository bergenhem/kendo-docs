---
title: MapMarker
slug: php-dataviz-ui-mapmarker
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapMarker

A PHP class representing the marker setting of MapMarkers.


## Methods

### color
The marker color. Accepts a valid CSS color string, including hex and rgb.

#### Returns
`\Kendo\Dataviz\UI\MapMarker`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $marker = new \Kendo\Dataviz\UI\MapMarker();
    $marker->color('value');
    ?>

### position
The marker position. Coordinates are listed as [Latitude, Longitude].
You can also use a kendo.dataviz.map.Location instance.

#### Returns
`\Kendo\Dataviz\UI\MapMarker`

#### Parameters

##### $value `array`



#### Example 
    <?php
    $marker = new \Kendo\Dataviz\UI\MapMarker();
    $marker->position(new array());
    ?>

### shape
The marker shape. Supported shapes are "pin" and "circle".

#### Returns
`\Kendo\Dataviz\UI\MapMarker`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $marker = new \Kendo\Dataviz\UI\MapMarker();
    $marker->shape('value');
    ?>

### size
The marker size in pixels.

#### Returns
`\Kendo\Dataviz\UI\MapMarker`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $marker = new \Kendo\Dataviz\UI\MapMarker();
    $marker->size(1);
    ?>

