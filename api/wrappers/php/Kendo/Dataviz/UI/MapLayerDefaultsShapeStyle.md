---
title: MapLayerDefaultsShapeStyle
slug: php-dataviz-ui-maplayerdefaultsshapestyle
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle

A PHP class representing the style setting of MapLayerDefaultsShape.


## Methods

### fill

The default fill for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerDefaultsShapeStyleFill)
    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle();
    $fill = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleFill();
    $color = 'value';
    $fill->color($color);
    $style->fill($fill);
    ?>

#### Example - using array

    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle();
    $color = 'value';
    $style->fill(array('color' => $color));
    ?>

### stroke

The default stroke for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerDefaultsShapeStyleStroke)
    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle();
    $stroke = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyleStroke();
    $color = 'value';
    $stroke->color($color);
    $style->stroke($stroke);
    ?>

#### Example - using array

    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerDefaultsShapeStyle();
    $color = 'value';
    $style->stroke(array('color' => $color));
    ?>

