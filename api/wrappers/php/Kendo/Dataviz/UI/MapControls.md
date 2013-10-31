---
title: MapControls
slug: php-dataviz-ui-mapcontrols
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapControls

A PHP class representing the controls setting of Map.


## Methods

### navigator

Enables or disables the built-in navigator control (directional pad).

#### Returns
`\Kendo\Dataviz\UI\MapControls`

#### Parameters

##### $value `boolean|\Kendo\Dataviz\UI\MapControlsNavigator|array`




#### Example  - using boolean
    <?php
    $controls = new \Kendo\Dataviz\UI\MapControls();
    $controls->navigator(true);
    ?>


#### Example - using [\Kendo\Dataviz\UI\MapControlsNavigator](/api/wrappers/php/Kendo/Dataviz/UI/MapControlsNavigator)
    <?php
    $controls = new \Kendo\Dataviz\UI\MapControls();
    $navigator = new \Kendo\Dataviz\UI\MapControlsNavigator();
    $position = 'value';
    $navigator->position($position);
    $controls->navigator($navigator);
    ?>

#### Example - using array

    <?php
    $controls = new \Kendo\Dataviz\UI\MapControls();
    $position = 'value';
    $controls->navigator(array('position' => $position));
    ?>

### zoom

Enables or disables the built-in zoom control (+/- button).

#### Returns
`\Kendo\Dataviz\UI\MapControls`

#### Parameters

##### $value `boolean|\Kendo\Dataviz\UI\MapControlsZoom|array`




#### Example  - using boolean
    <?php
    $controls = new \Kendo\Dataviz\UI\MapControls();
    $controls->zoom(true);
    ?>


#### Example - using [\Kendo\Dataviz\UI\MapControlsZoom](/api/wrappers/php/Kendo/Dataviz/UI/MapControlsZoom)
    <?php
    $controls = new \Kendo\Dataviz\UI\MapControls();
    $zoom = new \Kendo\Dataviz\UI\MapControlsZoom();
    $position = 'value';
    $zoom->position($position);
    $controls->zoom($zoom);
    ?>

#### Example - using array

    <?php
    $controls = new \Kendo\Dataviz\UI\MapControls();
    $position = 'value';
    $controls->zoom(array('position' => $position));
    ?>

