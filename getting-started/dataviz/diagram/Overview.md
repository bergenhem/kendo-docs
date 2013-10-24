---
title: Overview
meta_title: Documentation for the Diagram widget in Kendo UI DataViz
meta_description: How to create a diagram, add diagram elements, change properties, an overview of the widget's major features.
slug: gs-dataviz-diagram-overview
ordinal: 1
publish: false
---

# Kendo Diagramming Overview

## Getting started
To create a diagram, add an empty div in the HTML and give it an Id;

	<div id="canvas"></div>

and you can adorn it with CSS or a class like any other HTML;

	<div id="canvas" style="width:1024px; height:768px;"></div>

This div element is turned into a Kendo diagram by using a jQuery selector and calling the kendoDiagram() method like so;

	$("#canvas").kendoDiagram();

This renders an empty diagramming surface (SVG tags) and unless you look at the resulting HTML you won't see any changes on a visual level.  

The actual diagramming API can be accessed by calling the data() method;

	 var diagram = $("#canvas").kendoDiagram().data("kendoDiagram");

### Adding shapes

To add a rectangular shape to the diagram you simply call the addShape() method;

	diagram.addShape();

which will render a rectangle in the upper-left corner of the diagram surface. To have a different initial position you would call the addShape() method with an additional Point parameter, for example;

	var Point = kendo.diagram.Point;
	diagram.addShape(new Point(100,220));

Additional properties can be specified via the options parameter. For instance, you can set the background color of the shape like so;

	diagram.addShape(new Point(100,220), {background: "red});

A more complete overview of the options can be found in the API documentation.

The addShape() method also accepts a Shape instance, so you can also add a new shape as follows;

	var shapeInstance = new kendo.diagram.Shape();
    var shape = diagram.addShape(shape);
    shape.position(new Point(100,220));


### Adding connections

Shapes can be connected using the connect() method;

	var shape1 = diagram.addShape(new Point(100,100));
	var shape2 = diagram.addShape(new Point(300,100));
	var connection = diagram.connect(shape1, shape2);

which results in something like the picture below

![Two shapes connected.](SimplyConnected.png)

Note that by default so-called caps are defined on the endpoints of the connection to render a directed connection.

You can alter the caps by means of the options:

	connection.redraw({
						startCap: "None",
						endCap: "FilledCircle"
					   });

![Changing connection caps.](ChangedCaps.png)

and additional properties can be changed in a similar fashion:

	var shape1 = diagram.addShape(new Point(100, 100));
	var shape2 = diagram.addShape(new Point(300, 150));
	var connection = diagram.connect(shape1, shape2);
	connection.redraw({
	    startCap: "None",
	    endCap: "FilledCircle",
	    stroke       : "red",
	    hoveredStroke: "green",
	    strokeWidth  : 3,
	    content: "Kendo"
	});

![Changing connection options.](ConnectionOptions.png)

### Layout

Diagram layout consists in an automatic organization of a diagram on the basis how its shapes are connected (the so-called incidence structure). The layout() method is the gateway to a variety of layout algorithms. To see the effect of the layout method you can generate a random diagram and call the method like so;

	diagram.randomDiagram();

this will give a random diagram, something like the follwing;

![A random diagram.](RandomDiagram.png)

and upon calling the layout method

	diagram.layout();

you will see a diagram similar to this:
![Layout of a random diagram.](LayoutRandomDiagram.png)


The default layout algorithm is the top-down tree layout. You can change this to another type (and subtype) by inserting it in the layout options;

	diagram.layout({ type: "ForceDirected")};

which would give something like

![Force directed layout.](ForceSample.png)

Other layout types and options are discussed in the API.

### Data binding

Make sure you have read [the general overview of how databinding works in Kendo](http://docs.kendoui.com/getting-started/framework/datasource/overview "Kendo data binding.") first since it contains essential information which applies to the diagramming framework as well.

There are various ways you can define and customize data binding and we'll only scratch the surface in this overview. The easiest way to create a hierarchical diagram is by passing a dataSource as an option together with a Kendo template like so;

	var options = {
    				dataSource: [{
							        "name" : "Telerik",
							        "items": [
							            {"name": "Kendo"},
							            {"name": "Icenium"}
							        ]
							    }],				
				    template : "#= item.name #"
				};
	var diagram = $("#canvas").kendoDiagram(options).data("kendoDiagram");
	diagram.layout();

which produces a tree diagram with the default rectangular shapes;

![Simple data binding.](SimpleDatabinding.png)

Alternatively, you can define the data binding through the setDataSource method;

	diagram.options.template = "#= item.name #";
 	diagram.setDataSource([{"name": ... }]);

If you need more flexibility you can fully control where and how data is displayed by defining a visualTemplate option rather than the template option. This entails the creation of a function which returns a visual, usually a Group element containing other visuals bound to your data. For instance, the following snippet reproduces the same diagram but with ellipses rather than the previous rectangular shapes:

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

Note that the function returning a visual has a parameter containing the data item to be displayed.
The result of this custom data binding would look something like this;

![Custom data binding visuals.](GetVisual.png)


### Custom shapes

The shape figures are standard SVG paths and can accordingly be customized by setting the path data. You can use any SVG editor ([Adobe Illustrator](http://blogs.adobe.com/webplatform/2013/07/30/exporting-svg-from-adobe-illustrator-cc/ "Export SVG in Adobe Illustrator."), [Google's online SVG editor](https://code.google.com/p/svg-edit/ "SVG Edit.") and many other) to create a path and plug it into a custom shape. For example, if an SVG editor generates the following path element

	 <path fill="#79ce25" stroke="#000000" stroke-width="2" d="m1,64.5l23.51292,-23.51407l0,11.75703l9.42804,0l0,-18.80006l18.802,0l0,-9.42883l-11.75703,0l23.51407,-23.51407l23.51317,23.51407l-11.75612,0l0,9.42883l18.80014,0l0,18.80006l9.42876,0l0,-11.75703l23.51405,23.51407l-23.51405,23.51407l0,-11.75702l-9.42876,0l0,18.80014l-18.80014,0l0,9.42876l11.75612,0l-23.51317,23.51404l-23.51407,-23.51404l11.75703,0l0,-9.42876l-18.802,0l0,-18.80014l-9.42804,0l0,11.75702l-23.51292,-23.51407z" id="smaplepath"/>

you can paste the "d" value into a new diagram Shape in the options

	var shape = new kendo.diagram.Shape({
                        data:"m1,64.5l23.51292,-23.51407l0,11.75703l9.42804,0l0,-18.80006l18.802,0l0,-9.42883l-11.75703,0l23.51407,-23.51407l23.51317,23.51407l-11.75612,0l0,9.42883l18.80014,0l0,18.80006l9.42876,0l0,-11.75703l23.51405,23.51407l-23.51405,23.51407l0,-11.75702l-9.42876,0l0,18.80014l-18.80014,0l0,9.42876l11.75612,0l-23.51317,23.51404l-23.51407,-23.51404l11.75703,0l0,-9.42876l-18.802,0l0,-18.80014l-9.42804,0l0,11.75702l-23.51292,-23.51407z"
                    })
	var s1 = diagram.addShape(shape);

and it will render as

![Custom shape data.](CustomShape.png)

The important thing at this point is that the path in your SVG editor should be located **at the origin of the coordinate system**, otherwise the custom path inside the Shape will be offset with respect to the shape adorner; 

![Offset due to not placing the path at the origin.](IncorrectCustomPath.png)


### Connectors

Connectors are specific points on a shape where connections can be attached. They light up on hovering over a shape and when dragging a new connection. A shape has by default five connectors (left, right, top, bottom and auto), one of which acts as a switchboard to the other ones. When you have a connection attached to the central auto-connector the endpoint of the connection will switch between the other four connectors to minimize the length of the connection.  If one the other hand you bind a connection to one of the four standard connectors the endpoint will remain bound to that one. 

![Connectors.](Connectors.png)

If your custom shape needs custom connectors you can do so by passing their definition in the Shape creation. For example, the custom shape below represents a three-way arrow and the default connectors would not suit the shape's design very well. 

![Custom connectors on custom shape.](ThreeWayShape.png)

You need to specify in this case a 'connectors' array and supply a unique name together with a position function. The diagramming framework defines various helpful methods to position the connectors;

	var shape = new kendo.diagram.Shape({
            data:"m1,53.69333l17.5647,-17.56445l0,8.78235l23.15292,0l0,-26.34678l-8.78181,0l17.56417,-17.56444l17.5647,17.56444l-8.78238,0l0,26.34678l23.15297,0l0,-8.78235l17.56473,17.56445l-17.56473,17.56466l0,-8.78231l-63.87057,0l0,8.78231l-17.5647,-17.56466l0,0z",
            connectors: [
                {
                    name    : "Upstream",
                    position: function(shape){return shape.transformPoint(shape.bounds().top());}
                },
                {
                    name    : "SideLeft",
                    position: function(shape){
                        var p = shape.bounds().left();
                        return shape.transformPoint(new kendo.diagram.Point(p.x, p.y+17));
                    }
                },
                {
                    name    : "SideRight",
                    position: function(shape)
                    {
                        var p = shape.bounds().right();
                        return shape.transformPoint(new kendo.diagram.Point(p.x, p.y + 17));
                    }
                } 
            ]
        });

The default connectors can be added more easily like so:

	connectors: [
                {
                    name: "Top",
                    description: "Top Connector"
                },
                {
                    name: "Right",
                    description: "Right Connector"
                },
                {
                    name: "Bottom",
                    description: "Bottom Connector"
                },
                {
                    name: "BottomRight",
                    description: "Bottom Connector"
                },
                {
                    name: "Left",
                    Description: "Left Connector"
                },
                {
                    name: "Auto",
                    Description: "Auto Connector",
                    position: function (shape) {
                        return shape.getPosition("center");
                    }
                }
            ]

Of course, you can combine default and custom connectors in any way you wish.