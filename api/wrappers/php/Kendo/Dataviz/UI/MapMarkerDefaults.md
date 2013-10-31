---
title: MapMarkerDefaults
slug: php-dataviz-ui-mapmarkerdefaults
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapMarkerDefaults

A PHP class representing the markerDefaults setting of Map.


## Methods

### color
The default marker color. Accepts a valid CSS color string, including hex and rgb.

#### Returns
`\Kendo\Dataviz\UI\MapMarkerDefaults`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $markerDefaults = new \Kendo\Dataviz\UI\MapMarkerDefaults();
    $markerDefaults->color('value');
    ?>

### shape
The default marker shape. Supported shapes:

#### Returns
`\Kendo\Dataviz\UI\MapMarkerDefaults`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $markerDefaults = new \Kendo\Dataviz\UI\MapMarkerDefaults();
    $markerDefaults->shape('value');
    ?>

### size
The default marker size in pixels.

#### Returns
`\Kendo\Dataviz\UI\MapMarkerDefaults`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $markerDefaults = new \Kendo\Dataviz\UI\MapMarkerDefaults();
    $markerDefaults->size(1);
    ?>

