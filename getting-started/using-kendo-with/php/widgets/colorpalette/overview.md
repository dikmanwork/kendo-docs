---
title: Overview
meta_title: How to use the ColorPalette PHP class, server-side wrapper for Kendo UI ColorPalette widget
meta_description: Getting started with Kendo UI ColorPalette for PHP in quick steps - configure Kendo UI ColorPalette widget and operate Kendo UI ColorPalette events.
slug: php-colorpalette-overview
publish: true
relatedDocs: php-ui-colorpalette
---

# ColorPalette

The Kendo ColorPalette for PHP is a server-side wrapper for the [Kendo UI ColorPalette](/kendo-ui/api/web/colorpalette) widget.

## Getting Started

Here is how to configure a simple Kendo ColorPalette:

1. Follow the steps from the [introduction](/kendo-ui/getting-started/using-kendo-with/php/introduction) - include the autoloader, JavaScript and CSS files.

2. Create a [colorpalette](/kendo-ui/api/wrappers/php/Kendo/UI/ColorPalette).

        <?php
        $colorpalette = new \Kendo\UI\ColorPalette('colorpalette');
        $colorpalette->value('#ff0000');
        ?>

3. Output the colorpalette by echo-ing the result of the [render](/kendo-ui/api/wrappers/php/Kendo/UI/Widget#render) method.

        <?php
        echo $colorpalette->render();
        ?>

## Getting Client-side Reference

You can reference the client-side Kendo ColorPalette instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](/kendo-ui/api/web/colorpalette#methods) to control its behavior.


### Example

    <?php
    $colorpalette = new \Kendo\UI\ColorPalette('colorpalette');
    echo $colorpalette->render();
    ?>
    <script>
    $(function() {
        // The constructor parameter is used as the 'id' HTML attribute of the colorpalette
        var colorpalette = $("#colorpalette").data("kendoColorPalette")
    });
    </script>

## Handling Events

You can subscribe to all colorpalette [events](/kendo-ui/api/web/colorpalette#events).

### Example - subscribing by specifying JavaScript function name

    <?php
    $colorpalette = new \Kendo\UI\ColorPalette('colorpalette');

    // The 'colorpalette_change' JavaScript function will handle the 'change' event of the colorpalette
    $colorpalette->change('colorpalette_change');

    echo $colorpalette->render();
    ?>
    <script>
    function colorpalette_change() {
        // Handle the change event
    }
    </script>

### Example - providing inline JavaScript code

    <?php
    $colorpalette = new \Kendo\UI\ColorPalette('colorpalette');

    // Provide inline JavaScript code that will handle the 'change' event of the colorpalette
    $colorpalette->change('function() { /* Handle the change event */ }');

    echo $colorpalette->render();
    ?>
