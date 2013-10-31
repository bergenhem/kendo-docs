---
title: MapLayerDefaultsShapeStyleFill
slug: php-dataviz-ui-maplayerdefaultsshapestylefill
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill

A PHP class representing the fill setting of MapLayerDefaultsShapeStyle.


## Methods

### color
The default fill color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $fill = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill();
    $fill->color('value');
    ?>

### opacity
The default fill opacity (0 to 1) for layer shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $fill = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill();
    $fill->opacity(1);
    ?>

