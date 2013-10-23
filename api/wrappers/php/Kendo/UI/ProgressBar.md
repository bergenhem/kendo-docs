---
title: ProgressBar
slug: php-ui-progressbar
tags: api, php
publish: true
---

# \Kendo\UI\ProgressBar

A PHP wrapper for Kendo UI [ProgressBar](/api/web/progressbar).

Inherits from [\Kendo\UI\Widget](/api/wrappers/php/Kendo/UI/Widget).

## Usage

To use ProgressBar in a PHP page instantiate a new instance, configure it via the available
configuration [methods](#methods) and output it by `echo`-ing the result of the [render](/api/wrappers/php/Kendo/UI/Widget#render) method.

### Using Kendo ProgressBar

    <?php
    // Create a new instance of ProgressBar and specify its id
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');

    // Configure it
    $progressBar->chunkCount(1)

    // Output it

    echo $progressBar->render();
    ?>


## Methods

### animation

Configures the progress animation. Currently only the duration of the animation could be set.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `\Kendo\UI\ProgressBarAnimation|array`


#### Example - using [\Kendo\UI\ProgressBarAnimation](/api/wrappers/php/Kendo/UI/ProgressBarAnimation)
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $animation = new \Kendo\UI\ProgressBarAnimation();
    $duration = 1;
    $animation->duration($duration);
    $progressBar->animation($animation);
    ?>

#### Example - using array

    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $duration = 1;
    $progressBar->animation(array('duration' => $duration));
    ?>

### change
Fired when the value of the ProgressBar has changed. If the progress animation is enabled, the event will be fired after the animation has completed (does not applies to chunk ProgressBar).
For additional information check the [change](/api/web/progressbar#events-change) event documentation.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->change('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onChange(e) {
            // handle the change event.
        }
    </script>
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->change('onChange');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->change(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### chunkCount
Specifies the number of chunks.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->chunkCount(1);
    ?>

### complete
Fired when the value of the ProgressBar reaches the maximum value.
For additional information check the [complete](/api/web/progressbar#events-complete) event documentation.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->complete('function(e) { }');
    ?>

#### Example - using string which defines a JavaScript name
    <script>
        function onComplete(e) {
            // handle the complete event.
        }
    </script>
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->complete('onComplete');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->complete(new \Kendo\JavaScriptFunction('function(e) { }'));
    ?>

### enable
If set to false the widget will be disabled. It will still allow changing the value. The widget is enabled by default.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `boolean`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->enable(true);
    ?>

### max
The maximum value of the ProgressBar.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->max(1);
    ?>

### min
The minimum value of the ProgressBar.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->min(1);
    ?>

### orientation
The orientation of the ProgressBar. Possible values are horizontal and vertical.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->orientation('value');
    ?>

### reverse
Specifies if the progress direction will be reversed.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `boolean`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->reverse(true);
    ?>

### showStatus
Specifies if the progress status will be shown.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `boolean`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->showStatus(true);
    ?>

### type
Specifies the type of the ProgressBar. The supported types are value, percent and chunk.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->type('value');
    ?>

### value
The underlying value of the ProgressBar.

#### Returns
`\Kendo\UI\ProgressBar`

#### Parameters

##### $value `float`



#### Example 
    <?php
    $progressBar = new \Kendo\UI\ProgressBar('ProgressBar');
    $progressBar->value(1);
    ?>

