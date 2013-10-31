---
title: MapLayerStyleStroke
slug: php-dataviz-ui-maplayerstylestroke
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerStyleStroke

A PHP class representing the stroke setting of MapLayerStyle.


## Methods

### color
The default stroke color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyleStroke`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerStyleStroke();
    $stroke->color('value');
    ?>

### dashType
The default dash type for layer shapes.
The following dash types are supported:

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyleStroke`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerStyleStroke();
    $stroke->dashType(1);
    ?>

### opacity
The default stroke opacity (0 to 1) for layer shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyleStroke`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerStyleStroke();
    $stroke->opacity(1);
    ?>

### width
The default stroke width for layer shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyleStroke`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $stroke = new \Kendo\Dataviz\UI\MapLayerStyleStroke();
    $stroke->width(1);
    ?>

