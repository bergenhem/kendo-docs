---
title: MapLayerDefaultsShapeStyleStroke
slug: php-dataviz-ui-maplayerdefaultsshapestylestroke
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke

A PHP class representing the stroke setting of MapLayerDefaultsShapeStyle.


## Methods

### color
The default stroke color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke();
    $stroke->color('value');
    ?>

### dashType
The default dash type for layer shapes.
The following dash types are supported:

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke();
    $stroke->dashType('value');
    ?>

### opacity
The default stroke opacity (0 to 1) for layer shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke();
    $stroke->opacity(1);
    ?>

### width
The default stroke width for layer shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke();
    $stroke->width(1);
    ?>

