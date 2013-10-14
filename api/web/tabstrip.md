---
title: kendo.ui.TabStrip
meta_title: Configuration, methods and events of Kendo UI TabStrip
meta_description: Easily disable all animations, set the parameters, used for the visual animation and the effects used in TabStrip UI widget.
slug: api-web-tabstrip
relatedDocs: gs-web-tabstrip-overview
tags: api,web
publish: true
---

# kendo.ui.TabStrip

Represents the Kendo UI TabStrip. Inherits from [Widget](/api/framework/widget).

## Configuration

### animation `Object`

A collection of visual animations used when **TabStrip** tab are selected through
user interactions. Setting this option to **false** will disable all animations.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
            animation: {
                // fade-out current tab over 1000 milliseconds
                close: {
                    duration: 1000,
                    effects: "fadeOut"
                },
               // fade-in new tab over 500 milliseconds
               open: {
                   duration: 500,
                   effects: "fadeIn"
               }
           }
        });
    </script>

### animation.close `Object`

The visual animation(s) that will be used when the current tab is closed.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
            animation: {
                close: {
                    duration: 200,
                    effects: "fadeOut"
                }
            }
        });
    </script>

### animation.close.duration `Number`*(default: 200)*

The number of milliseconds used for the visual animation when the current tab is closed.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
            animation: {
                close: {
                    duration: 1000
                }
            }
        });
    </script>

### animation.close.effects `String`

A whitespace-delimited string of animation effects that are utilized when the current tab
is closed. By default not specified - uses the opening animation with reverse.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
            animation: {
                close: {
                    duration: 1000,
                    effects: "fadeOut"
                }
            }
        });
    </script>

### animation.open `Object`

The visual animation(s) that will be used when the new tab is shown.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
            animation: {
                open: {
                    duration: 200,
                    effects: "expand:vertical"
                }
            }
        });
    </script>

### animation.open.duration `Number`*(default: 200)*

The number of milliseconds used for the visual animation when a new tab is shown.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
           animation: {
              open: {
                  duration: 1000
              }
           }
        });
    </script>

### animation.open.effects `String`*(default: "expand:vertical fadeIn")*

A whitespace-separated string of animation effects that are used when a new tab is shown. Options include
**"expand:vertical"** and **"fadeIn"**.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
            animation: {
                open: {
                    effects: "fadeIn"
                }
            }
        });
    </script>

### collapsible `Boolean`*(default: false)*

Specifies whether the TabStrip should be able to collapse completely when clicking an expanded tab.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        $("#tabstrip").kendoTabStrip({
            collapsible: true
        });
    </script>

### dataContentField `String`*(default: "")*

 Sets the field of the data item that provides the text content of
the tab content element.

#### Example

    <div id="tabstrip"></div>

    <script>
        $("#tabstrip").kendoTabStrip({
            dataTextField: "Name",
            dataContentField: "Content",
            dataSource: data
        });
    </script>

### dataContentUrlField `String`*(default: "")*

 Sets the field of the data item that provides the URL for
the ajax loaded tab content.

#### Example

    <div id="tabstrip"></div>

    <script>
        $("#tabstrip").kendoTabStrip({
            dataTextField: "Name",
            dataContentUrlField: "ContentUrl",
            dataSource: data
        });
    </script>

### dataImageUrlField `String`*(default: "")*

 Sets the field of the data item that provides the image URL of
the tab.

#### Example

    <div id="tabstrip"></div>

    <script>
        $("#tabstrip").kendoTabStrip({
            dataTextField: "Name",
            dataImageUrlField: "ImageUrl",
            dataSource: data
        });
    </script>

### dataSpriteCssClass `String`*(default: "")*

 Sets the field of the data item that provides the CSS class of
the tab.

#### Example

    <div id="tabstrip"></div>

    <script>
        $("#tabstrip").kendoTabStrip({
            dataTextField: "Name",
            dataSpriteCssClass: "CssClass",
            dataSource: data
        });
    </script>

### dataTextField `String`*(default: "")*

 Sets the field of the data item that provides the text name of the tab.

#### Example

    <div id="tabstrip"></div>

    <script>
        $("#tabstrip").kendoTabStrip({
            dataTextField: "Name",
            dataSource: data
        });
    </script>

### dataUrlField `String`*(default: "")*

 Sets the field of the data item that provides the link URL for the
tab.

#### Example

    <div id="tabstrip"></div>

    <script>
        $("#tabstrip").kendoTabStrip({
            dataTextField: "Name",
            dataUrlField: "Url",
            dataSource: data
        });
    </script>

## Fields

### tabGroup `jQuery`

The jQuery object which contains the tabstrip items.

## Methods

### activateTab

Activates a tab specified as a selector. Note: Invoking this method will not trigger any events.

#### Example

    <div id="tabstrip">
        <ul>
            <li id="tab1">Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabToActivate = $("#tab1");
        $("#tabstrip").kendoTabStrip().data("kendoTabStrip").activateTab(tabToActivate);
    </script>

#### Parameters

##### item `jQuery`

The target tab, specified as a selector, to be activated.

### append

Appends a tab to the collection of tabs in a **TabStrip**.

#### Example

    <div id="tabstrip">
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.append(
            [{
                text: "Item 1",
                url: "http://www.kendoui.com"               // Link URL if navigation is needed, optional.
            },
            {
                text: "<b>Item 2</b>",
                encoded: false,                             // Allows use of HTML for item text
                content: "text"                             // Content for the content element
            },
            {
                text: "Item 3",
                contentUrl: "partialContent.html"           // From where to load the item content
            },
            {
                text: "Item 4",
                imageUrl: "http://www.kendoui.com/test.jpg" // Item image URL, optional.
            },
            {
                text: "Item 5",
                spriteCssClass: "imageClass3"               // Item image sprite CSS class, optional.
            }]
        );
    </script>

#### Parameters

##### tab `Array|Object`

Target tab, specified as a JSON object. You can pass tab text, content or contentUrl here. Can handle an
HTML string or array of such strings or JSON.

#### Returns

`kendo.ui.TabStrip` Returns the TabStrip object to support chaining.

### contentElement

Obtains the DOM element that encloses tab content by its tab index in the **TabStrip**.

> **Important:** To remove the tab contents safely, use **contentHolder** to get the element to empty.

#### Obtain the content element representing the first tab in a TabStrip

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        console.log(tabStrip.contentElement(0));
    </script>

#### Parameters

##### itemIndex `Number`

The index of the tab in the TabStrip.

#### Returns

`Element` The DOM element enclosing tab content by its tab index in the **TabStrip**.

### contentHolder

Obtains the DOM element that holds tab content by its tab index in the **TabStrip**.
The difference between contentElement and contentHolder is that contentHolder returns the DOM element that really holds the content, which on mobile is the scroll container.

> **Important:** To remove the tab contents safely, use this method to get the element to empty.

#### Obtain the content holder representing the first tab in a TabStrip

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        console.log(tabStrip.contentHolder(0));
    </script>

#### Parameters

##### itemIndex `Number`

The index of the tab in the TabStrip.

#### Returns

`Element` The DOM element holding tab content by its tab index in the **TabStrip**.

### deactivateTab

Deactivates a tab specified as a selector. Note: Invoking this method will not trigger any events.

#### Example

    <div id="tabstrip">
        <ul>
            <li id="tab1">Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabToDeactivate = $("#tab1");
        $("#tabstrip").kendoTabStrip().data("kendoTabStrip").deactivateTab(tabToDeactivate);
    </script>

#### Parameters

##### item `jQuery`

The target tab, specified as a selector, to be deactivated.

### destroy
Prepares the **TabStrip** for safe removal from DOM. Detaches all event handlers and removes jQuery.data attributes to avoid memory leaks. Calls destroy method of any child Kendo widgets.

> **Important:** This method does not remove the TabStrip element from DOM.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");

        // destroy the widget
        tabStrip.destroy();
    </script>

### disable

Disables a tab(s) of a **TabStrip**.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.disable(tabStrip.tabGroup.eq(0));
    </script>

#### Parameters

##### element `String|Element|jQuery`

The target tab(s), specified as a selector, to be disabled.

#### Returns

`kendo.ui.TabStrip` Returns the TabStrip object to support chaining.

### enable

Disables (**false**) or enables (**true**) a tab(s) of a **TabStrip**.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.enable(tabStrip.tabGroup.eq(0), false);
        tabStrip.enable(tabStrip.tabGroup.eq(0), true);
    </script>

#### Parameters

##### element `String|Element|jQuery`

The target tab(s), specified as a selector, to be enabled (**true**) or disabled
(**false**).

##### enable `Boolean` *(optional)*

Desired state of the tab(s) specified by the selector; enabled (**true**) or disabled
(**false**).

#### Returns

`kendo.ui.TabStrip` Returns the TabStrip object to support chaining.

### insertAfter

Inserts a newly-created tab after a specified tab.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab</li>
        </ul>
        <div>Content</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.insertAfter(
            [{
                text: "Item 1",
                url: "http://www.kendoui.com"               // Link URL if navigation is needed, optional.
            },
            {
                text: "<b>Item 2</b>",
                encoded: false,                             // Allows use of HTML for item text
                content: "text"                             // Content for the content element
            },
            {
                text: "Item 3",
                contentUrl: "partialContent.html"           // From where to load the item content
            },
            {
                text: "Item 4",
                imageUrl: "http://www.kendoui.com/test.jpg" // Item image URL, optional.
            },
            {
                text: "Item 5",
                spriteCssClass: "imageClass3"               // Item image sprite CSS class, optional.
            }],
            tabStrip.tabGroup.eq(0)
        );
    </script>

#### Parameters

##### item `String|Element|jQuery`

Target tab, specified as a JSON object. You can pass tab text, content or contentUrl here. Can handle an
HTML string or array of such strings or JSON.

##### referenceTab `String|Element|jQuery`

A reference tab to insert the new item after.

#### Returns

`kendo.ui.TabStrip` Returns the TabStrip object to support chaining.

### insertBefore

Inserts a newly-created tab before a specified tab.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab</li>
        </ul>
        <div>Content</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.insertBefore(
            [{
                text: "Item 1",
                url: "http://www.kendoui.com"               // Link URL if navigation is needed, optional.
            },
            {
                text: "<b>Item 2</b>",
                encoded: false,                             // Allows use of HTML for item text
                content: "text"                             // Content for the content element
            },
            {
                text: "Item 3",
                contentUrl: "partialContent.html"           // From where to load the item content
            },
            {
                text: "Item 4",
                imageUrl: "http://www.kendoui.com/test.jpg" // Item image URL, optional.
            },
            {
                text: "Item 5",
                spriteCssClass: "imageClass3"               // Item image sprite CSS class, optional.
            }],
            tabStrip.tabGroup.eq(0)
        );
    </script>

#### Parameters

##### item `String|Element|jQuery`

Target tab, specified as a JSON object. You can pass tab text, content or contentUrl here. Can handle an
HTML string or array of such strings or JSON.

##### referenceTab `String|Element|jQuery`

A reference tab to insert the new item before

#### Returns

`kendo.ui.TabStrip` Returns the TabStrip object to support chaining.

### items

Gets the list of DOM elements that represent the tabs.

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        console.log(tabStrip.items());
    </script>

#### Returns

`HTMLCollection` the tabs as an HTML collection of elements.

### reload

Reloads TabStrip tab(s) via AJAX.

    <div id="tabstrip"></div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip({
            dataSource: [{
                text: "Tab 1",
                contentUrl: "partialContent1.html"
            },
            {
                text: "Tab 2",
                contentUrl: "partialContent2.html"
            }]
        }).data("kendoTabStrip");

        tabStrip.reload("li:first");
    </script>

#### Parameters

##### element `String|Element|jQuery`

The target tab(s), specified as a selector or jQuery object, to be reloaded via AJAX.

#### Returns

`kendo.ui.TabStrip` Returns the TabStrip object to support chaining.

### remove

Removes a specified tab from a TabStrip.

#### Remove a tab with ID, tab1 from a TabStrip

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.remove("li:last");
    </script>

#### Parameters

##### element `String|Number`

The target tab(s), specified as a selector or jQuery object, to be removed.

#### Returns

`kendo.ui.TabStrip` Returns the TabStrip object to support chaining.

### select

Get/set the selected tab. If called without arguments, it returns the
currently selected tab.

#### Example

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");

        tabStrip.select("li:first");        // Select by jQuery selector
        tabStrip.select(1);                 // Select by index
    </script>

#### Parameters

##### element `String|Element|jQuery|Number`

The target tab(s), specified as a selector, jQuery object or index in the tab group.

#### Returns

`jQuery` the selected tab if called without arguments. `kendo.ui.TabStrip` if called with arguments.

## Events

### activate

Triggered just after a tab is being made visible, but before the end of the animation

#### Attach activate event handler during initialization; detach via unbind()

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        // event handler for activate
        var onActivate = function(e) {
            // access the activated item via e.item (Element)

            // detach activate event handler via unbind()
            tabStrip.unbind("activate", onActivate);
        };

        // attach activate event handler during initialization
        var tabStrip = $("#tabStrip").kendoTabStrip({
            activate: onActivate
        }).data("kendoTabStrip");
    </script>

#### Attach activate event handler via bind(); detach via unbind()

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        // event handler for activate
        var onActivate = function(e) {
            // access the activated item via e.item (Element)

            // detach activate event handler via unbind()
            tabStrip.unbind("activate", onActivate);
        };

        // attach activate event handler via bind()
        var tabStrip = $("#tabStrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.bind("activate", onActivate);
    </script>

#### Event Data

##### e.item `Element`

The activated tab.

##### e.contentElement `Element`

The content element of the activated tab.

### contentLoad

Triggered when content is fetched from an AJAX request.

#### Attach contentLoad event handler during initialization; detach via unbind()

    <div id="tabstrip">
    </div>

    <script>
        // event handler for select
        var onError = function(e) {
            // access the selected item via e.item (Element)

            // detach select event handler via unbind()
            tabStrip.unbind("error", onError);
        };

        // attach select event handler during initialization
        var tabStrip = $("#tabstrip").kendoTabStrip({
            dataSource: [{
                text: "Tab 1",
                contentUrl: "partialContent1.html"
            },
            {
                text: "Tab 2",
                contentUrl: "partialContent2.html"
            }],
            error: onError
        }).data("kendoTabStrip");
    </script>

#### Event Data

##### e.item `Element`

The selected item

##### e.contentElement `Element`

The loaded content element that is retrieved via AJAX.

### error

Triggered when an AJAX request results in an error.

#### Attach error event handler during initialization; detach via unbind()

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        // event handler for select
        var onError = function(e) {
            // access the selected item via e.item (Element)

            // detach select event handler via unbind()
            tabStrip.unbind("error", onError);
        };

        // attach select event handler during initialization
        var tabStrip = $("#tabstrip").kendoTabStrip({
            error: onError
        }).data("kendoTabStrip");
    </script>

#### Event Data

##### e.xhr `jqXHR`

The jqXHR object used to load the content

##### e.status `String`

The returned status.

### select

Triggered before a tab is selected.

#### Attach select event handler during initialization; detach via unbind()

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        // event handler for select
        var onSelect = function(e) {
            // access the selected item via e.item (Element)

            // detach select event handler via unbind()
            tabStrip.unbind("select", onSelect);
        };

        // attach select event handler during initialization
        var tabStrip = $("#tabstrip").kendoTabStrip({
            select: onSelect
        }).data("kendoTabStrip");
    </script>

#### Attach select event handler via bind(); detach via unbind()

    <div id="tabstrip">
        <ul>
            <li>Tab 1</li>
            <li>Tab 2</li>
        </ul>
        <div>Content 1</div>
        <div>Content 2</div>
    </div>

    <script>
        // event handler for select
        var onSelect = function(e) {
            // access the selected item via e.item (Element)

            // detach select event handler via unbind()
            tabStrip.unbind("select", onSelect);
        };

        // attach select event handler via bind()
        var tabStrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabStrip.bind("select", onSelect);
    </script>

#### Event Data

##### e.item `Element`

The selected item chosen by a user.

##### e.contentElement `Element`

The content element of the tab going to be selected.
