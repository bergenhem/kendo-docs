---
title: progressBar
slug: jsp-progressBar
tags: api, java
publish: true
---

# \<kendo:progressBar\>
A JSP wrapper for Kendo UI [ProgressBar](/api/web/progressbar).

## Configuration Attributes

### chunkCount `float`

Specifies the number of chunks.

#### Example
    <kendo:progressBar chunkCount="chunkCount">
    </kendo:progressBar>

### enable `boolean`

If set to false the widget will be disabled. It will still allow changing the value. The widget is enabled by default.

#### Example
    <kendo:progressBar enable="enable">
    </kendo:progressBar>

### max `float`

The maximum value of the ProgressBar.

#### Example
    <kendo:progressBar max="max">
    </kendo:progressBar>

### min `float`

The minimum value of the ProgressBar.

#### Example
    <kendo:progressBar min="min">
    </kendo:progressBar>

### orientation `java.lang.String`

The orientation of the ProgressBar. Possible values are horizontal and vertical.

#### Example
    <kendo:progressBar orientation="orientation">
    </kendo:progressBar>

### reverse `boolean`

Specifies if the progress direction will be reversed.

#### Example
    <kendo:progressBar reverse="reverse">
    </kendo:progressBar>

### showStatus `boolean`

Specifies if the progress status will be shown.

#### Example
    <kendo:progressBar showStatus="showStatus">
    </kendo:progressBar>

### type `java.lang.String`

Specifies the type of the ProgressBar. The supported types are value, percent and chunk.

#### Example
    <kendo:progressBar type="type">
    </kendo:progressBar>

### value `float`

The underlying value of the ProgressBar.

#### Example
    <kendo:progressBar value="value">
    </kendo:progressBar>


##  Configuration JSP Tags

### kendo:progressBar-animation

Configures the progress animation. Currently only the duration of the animation could be set.

More documentation is available at [kendo:progressBar-animation](progressbar/animation).

#### Example

    <kendo:progressBar>
        <kendo:progressBar-animation></kendo:progressBar-animation>
    </kendo:progressBar>


## Event Attributes

### change `String`

Fired when the value of the ProgressBar has changed. If the progress animation is enabled, the event will be fired after the animation has completed (does not applies to chunk ProgressBar).


For additional information check the [change](/api/web/progressbar#events-change) event documentation.

#### Example
    <kendo:progressBar change="handle_change">
    </kendo:progressBar>
    <script>
        function handle_change(e) {
            // Code to handle the change event.
        }
    </script>

### complete `String`

Fired when the value of the ProgressBar reaches the maximum value.


For additional information check the [complete](/api/web/progressbar#events-complete) event documentation.

#### Example
    <kendo:progressBar complete="handle_complete">
    </kendo:progressBar>
    <script>
        function handle_complete(e) {
            // Code to handle the complete event.
        }
    </script>

## Event Tags

### kendo:progressBar-change

Fired when the value of the ProgressBar has changed. If the progress animation is enabled, the event will be fired after the animation has completed (does not applies to chunk ProgressBar).


For additional information check the [change](/api/web/progressbar#events-change) event documentation.

#### Example
    <kendo:progressBar>
        <kendo:progressBar-change>
            <script>
                function(e) {
                    // Code to handle the change event.
                }
            </script>
        </kendo:progressBar-change>
    </kendo:progressBar>

### kendo:progressBar-complete

Fired when the value of the ProgressBar reaches the maximum value.


For additional information check the [complete](/api/web/progressbar#events-complete) event documentation.

#### Example
    <kendo:progressBar>
        <kendo:progressBar-complete>
            <script>
                function(e) {
                    // Code to handle the complete event.
                }
            </script>
        </kendo:progressBar-complete>
    </kendo:progressBar>

