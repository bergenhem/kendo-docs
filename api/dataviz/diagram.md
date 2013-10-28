---
title: kendo.diagram
meta_title: API Reference for methods, objects and properties in the math module of Kendo diagram
meta_description: Examples and detailed explanation of Kendo UI methods and properties.
slug: api-framework
tags: api,framework
publish: false
---

# kendo.dataviz.ui.diagram

## Configuration

### autoBind `Boolean` *(default: true)*

If set to `false` the widget will not bind to the data source during initialization. In this case data binding will occur when the [change](/api/framework/datasource#events-change) event of the
data source is fired. By default the widget will bind to the data source specified in the configuration.

> Setting `autoBind` to `false` is useful when multiple widgets are bound to the same data source. Disabling automatic binding ensures that the shared data source doesn't make more than one request to the remote service.

#### Example - disable automatic binding

	<div id="diagram"></div>
	<script>
	$("#diagram").kendoDiagram(
		{
	 		dataSource: [
	                 {
	
	                     "name" : "Telerik",
	                     "items": [
	                         {"name": "Kendo"},
	                         {"name": "Icenium"}
	                     ]
	                 }
	             ],
	 		template  : "#= item.name #",
			autoBind: false
		}
	);

	diagram.dataSource.read(); // "read()" will fire the "change" event of the dataSource 
	</script>

### name `String` *(default: "Diagram")*

![alt Attention](http://demos.telerik.com/aspnet-ajax/toolbar/examples/overview/Img/followUp.gif "We need to look into this.") *The name doesn't seem to be used or do anything, does it?*

### zoomRate `Number` *(default: 1.1)*

The scaling factor or the zoom when using the mouse-wheel to zoom in or out.

### dataSource `kendo.data.DataSource`

See the [dataSource field](#fields-dataSource).

### dragAndDrop `Boolean` *(default: false)*

![alt Attention](http://demos.telerik.com/aspnet-ajax/toolbar/examples/overview/Img/followUp.gif "We need to look into this.") *Can't see where or how this one is being used.*

### template `String|Function`

The [template](/api/framework/kendo#methods-template) which renders the content of the shape when bound to a dataSource. The names you can use in the template correspond to the properties used in the dataSource. See the dataSource topic below for a concrete example.


### dataTextField `String`

![alt Attention](http://demos.telerik.com/aspnet-ajax/toolbar/examples/overview/Img/followUp.gif "We need to look into this.") *Something to do with the underlying Kendo infrastructure?*

### resizable `Boolean` *(default: true)*

This defines whether the shapes can be resized. If set to false the adorner will not show the resizing thumbs, as can be seen below;

![Resizable configuration.](resizable.png)

### rotatable `Boolean` *(default: true)*

This defines whether the shapes can be rotated. If set to false the adorner will not show the rotating thumb, as can be seen below;

![Rotatable configuration.](rotatable.png)


### visualTemplate `Function`

A function returning a visual element to render for a given dataSource item. The following primitives can be used to construct a composite visual:

* Circle
* Rectangle
* Path
* Line
* Polyline
* TextBlock
* Image

![alt Attention](http://demos.telerik.com/aspnet-ajax/toolbar/examples/overview/Img/followUp.gif "We need to look into this.") *Should redirect here to a more comprehensive overview of how to use the primitives.*

#### Example - how to use the visualTemplate

	var getVisual = function(data)
					{
					    var g = new kendo.diagram.Group({
					        autoSize: true
					    });
					    var r = new kendo.diagram.Circle({
					        width : 100,
					        height: 60,
					        background: "LimeGreen"
					    });
					    g.append(r);
					    var fn = new kendo.diagram.TextBlock({
					        text: data.name,
					        fontSize: 16,
					        x   : 30,
					        y   : 30
					    });
					    g.append(fn);
					    return g;
					}
	var options = {
	    dataSource: [
	        {
	
	            "name" : "Telerik",
	            "items": [
	                {"name": "Kendo"},
	                {"name": "Icenium"}
	            ]
	        }
	    ],
	    autoBind  : true,
	    visualTemplate  : getVisual
	};
	diagram = $("#canvas").kendoDiagram(options).data("kendoDiagram");
	diagram.layout(); 

### tooltip `Object`
### copy `Object`
### allowDrop `Boolean` *(default: true)*

## Fields

### dataSource `kendo.data.DataSource`

The [data source](/api/framework/datasource) of the widget. Configured via the [dataSource](#configuration-dataSource) option.

> Changes of the data source will be reflected in the widget.

> Assigning a new data source would have no effect. Use the [setDataSource](#methods-setDataSource) method instead.

#### Example - add a data item to the data source

    <div id="diagram"></div>
    <script>
    $("#diagram").kendoDiagram({
      dataSource: [
                      {

                          "name" : "Telerik",
                          "items": [
                              {"name": "Kendo"},
                              {"name": "Icenium"}
                          ]
                      }
                  ],
      template  : "#= item.name #"
    });
    var diagram = $("#diagram").data("kendoDiagram");
    diagram.dataSource.add({ "name": "XAML" });
    </script>

#### Example - update a data item in the data source


![alt Attention](http://demos.telerik.com/aspnet-ajax/toolbar/examples/overview/Img/followUp.gif "We need to look into this.") *Doesn't work right now, need to hook up or amend the update of the source.*

 	<div id="diagram"></div>
    <script>
    $("#diagram").kendoDiagram({
      dataSource: [
                      {

                          "name" : "Telerik",
                          "items": [
                              {"name": "Kendo"},
                              {"name": "Icenium"}
                          ]
                      }
                  ],
      template  : "#= item.name #"
    });
    var diagram = $("#diagram").data("kendoDiagram");
    var data = diagram.dataSource.at(0);
    data.set("name", "Telerik AD");
    </script>

#### Example - remove a data item in the data source

![alt Attention](http://demos.telerik.com/aspnet-ajax/toolbar/examples/overview/Img/followUp.gif "We need to look into this.") *Same here, need to hook up or amend the update of the source.*
 

 	<div id="diagram"></div>
    <script>
    $("#diagram").kendoDiagram({
      dataSource: [
                      {

                          "name" : "Telerik",
                          "items": [
                              {"name": "Kendo"},
                              {"name": "Icenium"}
                          ]
                      }
                  ],
      template  : "#= item.name #"
    });
    var diagram = $("#diagram").data("kendoDiagram");
    var data = diagram.dataSource.at(0);
    diagram.dataSource.remove(data);
    </script>

### options `Object`

The [configuration](#configuration) options with which the diagram is initialized.



#### Example - changing the diagram options

    <div id="chart"></div>
    <script>
     $("#diagram").kendoDiagram();
     var diagram = $("#diagram").data("kendoDiagram");
     diagram.options.copy = {
                       enabled: true,
                       offsetX: 100,
                       offsetY: 100
                   };
    </script>