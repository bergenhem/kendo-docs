---
title: MapLayer
slug: php-dataviz-ui-maplayer
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapLayer

A PHP class representing the layer setting of MapLayers.


## Methods

### autoBind
If set to false the layer will not bind to the data source during initialization. In this case data binding will occur when the change event of the
data source is fired. By default the widget will bind to the data source specified in the configuration.

#### Returns
`\Kendo\Dataviz\UI\MapLayer`

#### Parameters

##### $value `boolean`



#### Example 
    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $layer->autoBind(true);
    ?>

### copyright
The copyright message for the layer.

#### Returns
`\Kendo\Dataviz\UI\MapLayer`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $layer->copyright('value');
    ?>

### dataSource

Sets the data source of the dataSource.

#### Returns
`\Kendo\Dataviz\UI\MapLayer`

#### Parameters

##### $value `\Kendo\Data\DataSource|array`

#### Example - using [\Kendo\Data\DataSource](/api/wrappers/php/kendo/data/datasource)

    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $dataSource = new \Kendo\Data\DataSource();
    $layer->dataSource($dataSource);
    ?>

#### Example - using array

    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $schema = new \Kendo\Data\DataSourceSchema();
    $layer->dataSource(array('schema' => $schema));
    ?>

### style

The default style for shapes.

#### Returns
`\Kendo\Dataviz\UI\MapLayer`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapLayerStyle|array`


#### Example - using [\Kendo\Dataviz\UI\MapLayerStyle](/api/wrappers/php/Kendo/Dataviz/UI/MapLayerStyle)
    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $style = new \Kendo\Dataviz\UI\MapLayerStyle();
    $fill = new \Kendo\Dataviz\UI\MapLayerStyleFill();
    $style->fill($fill);
    $layer->style($style);
    ?>

#### Example - using array

    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $fill = new \Kendo\Dataviz\UI\MapLayerStyleFill();
    $layer->style(array('fill' => $fill));
    ?>

### type
The layer type. Supported types are "tile" and "shape".

#### Returns
`\Kendo\Dataviz\UI\MapLayer`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $layer->type('value');
    ?>

### urlTemplate
The URL template for tile layers. Template variables:

#### Returns
`\Kendo\Dataviz\UI\MapLayer`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $layer = new \Kendo\Dataviz\UI\MapLayer();
    $layer->urlTemplate('value');
    ?>

