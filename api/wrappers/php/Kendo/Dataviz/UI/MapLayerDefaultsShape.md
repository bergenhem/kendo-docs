---
title: MapLayerDefaultsShape
slug: php-dataviz-ui-maplayerdefaultsshape
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerDefaultsShape

A PHP class representing the shape setting of MapLayerDefaults.


## Methods

### copyright
The copyright message for all shape layers.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShape`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $shape = new \Kendo\Dataviz\UI\MapLayerDefaultsShape();
    $shape->copyright('value');
    ?>

### style

The default style for shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShape`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerDefaultsShapeStyle)
    <?php
    $shape = new \Kendo\Dataviz\UI\MapLayerDefaultsShape();
    $style = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle();
    $fill = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill();
    $style->fill($fill);
    $shape->style($style);
    ?>

#### Example - using array

    <?php
    $shape = new \Kendo\Dataviz\UI\MapLayerDefaultsShape();
    $fill = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill();
    $shape->style(array('fill' => $fill));
    ?>

