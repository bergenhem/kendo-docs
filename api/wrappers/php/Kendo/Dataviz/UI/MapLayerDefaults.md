---
title: MapLayerDefaults
slug: php-dataviz-ui-maplayerdefaults
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayerDefaults

A PHP class representing the layerDefaults setting of Map.


## Methods

### shape

The default configuration for shape layers.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaults`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerDefaultsShape|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerDefaultsShape](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerDefaultsShape)
    <?php
    $layerDefaults = new \Kendo\Dataviz\UI\MapLayerDefaults();
    $shape = new \Kendo\Dataviz\UI\MapLayerDefaultsShape();
    $copyright = 'value';
    $shape->copyright($copyright);
    $layerDefaults->shape($shape);
    ?>

#### Example - using array

    <?php
    $layerDefaults = new \Kendo\Dataviz\UI\MapLayerDefaults();
    $copyright = 'value';
    $layerDefaults->shape(array('copyright' => $copyright));
    ?>

### tile

The default configuration for tile layers.

#### Returns
`\Kendo\Dataviz\UI\MapLayerDefaults`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerDefaultsTile|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerDefaultsTile](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerDefaultsTile)
    <?php
    $layerDefaults = new \Kendo\Dataviz\UI\MapLayerDefaults();
    $tile = new \Kendo\Dataviz\UI\MapLayerDefaultsTile();
    $copyright = 'value';
    $tile->copyright($copyright);
    $layerDefaults->tile($tile);
    ?>

#### Example - using array

    <?php
    $layerDefaults = new \Kendo\Dataviz\UI\MapLayerDefaults();
    $copyright = 'value';
    $layerDefaults->tile(array('copyright' => $copyright));
    ?>

