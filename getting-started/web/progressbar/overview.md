---
title: Overview
meta_title: Overview of ProgressBar UI widget | Kendo UI Documentation
meta_description: Quick steps to help you create Kendo UI ProgressBar, read the documentation to get started.
slug: gs-web-progressbar-overview
relatedDocs: api-web-progressbar
tags: getting-started, web
publish: true
---

# ProgressBar Overview

The **ProgressBar** offers rich functionality for displaying and tracking progress. It supports multiple types, horizontal or vertical orientation and also different directions.


## Getting Started

### Create an HTML div element

	<div id="progressbar"></div>

### Initialize the ProgressBar using a jQuery selector

	$(document).ready(function(){
      $("#progressbar").kendoProgressBar();
	});

## ProgressBar types

The **ProgressBar** supports three different types:

* **value** - regular progressbar which displays the progress status as absolute value.
* **percent** - regular progressbar which displays the progress status in percentages.
* **chunk** - progressbar divided in chunks which displays the progress step-wise.

### Initialize a chunk ProgressBar

	<div id="progressbar"></div>
	<script>
	  $("#progressbar").kendoProgressBar({
	    type: "chunk",
		chunkCount: 10
	  });
	</script>

## ProgressBar configuration

Many of the **ProgressBar** options can be configured through it's properties, including:

* Horizontal or vertical orientation
* Reversed direction
* Minimum and maximum value
* Animation duration

### Configure a complex ProgressBar

	$("#progressbar").kendoProgressBar({
      min: 100,
      max: 500,
      value: 100,
      type: "percent",
	  orientation: "vertical",
      reverse: true,
      complete: function(e) {
        console.log("Progress completed");
      },
      animation: {
        duration: 600
      }
    });

## Accessing an Existing ProgressBar

You can reference an existing **ProgressBar** instance via [jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can use the [ProgressBar API](/api/web/progressbar) to control its behavior.

## Subscribing to the events of Kendo UI ProgressBar

The **ProgressBar** supports the following [events](http://docs.kendoui.com/api/web/progressbar#events):

* **change** - Fired each time when a new value is set.
* **complete** - Fired when the progress has completed i.e. when it reaches the maximum value for the first time.
* **start** - Fired when the progress has started i.e. when the value is changed for the first time.

There are two ways to handle events:

* Specify the JavaScript function which will handle the event during the widget initialization.
* Use the `bind` method of the widget after initialization.

### Accessing an Existing ProgressBar instance

	var progressbar = $("#progressbar").data("kendoProgressBar");

