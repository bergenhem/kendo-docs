---
title: MapLayerStyle
slug: php-dataviz-ui-maplayerstyle
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerStyle

A PHP class representing the style setting of MapLayer.


## Methods

### fill

The default fill for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyle`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerStyleFill|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerStyleFill](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerStyleFill)
    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerStyle();
    $fill = new \Kendo\Dataviz\UI\MapLayerStyleFill();
    $color = 'value';
    $fill->color($color);
    $style->fill($fill);
    ?>

#### Example - using array

    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerStyle();
    $color = 'value';
    $style->fill(array('color' => $color));
    ?>

### stroke

The default stroke for layer shapes.
Accepts a valid CSS color string or object with detailed configuration.

#### Returns
`\Kendo\Dataviz\UI\MapLayerStyle`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerStyleStroke|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerStyleStroke](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerStyleStroke)
    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerStyle();
    $stroke = new \Kendo\Dataviz\UI\MapLayerStyleStroke();
    $color = 'value';
    $stroke->color($color);
    $style->stroke($stroke);
    ?>

#### Example - using array

    <?php
    $style = new \Kendo\Dataviz\UI\MapLayerStyle();
    $color = 'value';
    $style->stroke(array('color' => $color));
    ?>

