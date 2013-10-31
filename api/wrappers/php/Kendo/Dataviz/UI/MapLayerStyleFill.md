---
title: MapLayerStyleFill
slug: php-dataviz-ui-maplayerstylefill
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerStyleFill

A PHP class representing the fill setting of MapLayerStyle.


## Methods

### color
The default fill color for layer shapes.
Accepts a valid CSS color string, including hex and rgb.

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyleFill`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $fill = new \Kendo\Dataviz\UI\MapLayerStyleFill();
    $fill->color('value');
    ?>

### opacity
The default fill opacity (0 to 1) for layer shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyleFill`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $fill = new \Kendo\Dataviz\UI\MapLayerStyleFill();
    $fill->opacity(1);
    ?>

