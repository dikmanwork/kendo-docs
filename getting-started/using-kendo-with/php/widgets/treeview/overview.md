---
title: Overview
meta_title: How to use the TreeView PHP class, server-side wrapper for Kendo UI TreeView widget
meta_description: Learn how to bind Kendo UI TreeView for PHP, handle Kendo UI TreeView Events, access an existing treeview.
slug: php-treeview-overview
publish: true
relatedDocs: php-ui-treeview
---

# TreeView

The Kendo TreeView for PHP is a server-side wrapper for the [Kendo UI TreeView](/kendo-ui/api/web/treeview) widget.

## Getting Started

Here is how to configure simple treeview:

1. Follow the steps from the [introduction](/kendo-ui/getting-started/using-kendo-with/php/introduction) - include the autoloader, JavaScript and CSS files.

1. Create a [treeview](/kendo-ui/api/wrappers/php/Kendo/UI/TreeView), configure its [items](/kendo-ui/api/wrappers/php/Kendo/UI/TreeView#addItem).

        <?php
        $treeview = new \Kendo\UI\TreeView('treeview');

        $root = new \Kendo\UI\TreeViewItem('Root');
        $root->expanded(true);

        $child = new \Kendo\UI\TreeViewItem('Child');
        $root->addItem($child);

        $treeview->addItem($root);
        ?>

1. Output the treeview by echo-ing the result of the [render](/kendo-ui/api/wrappers/php/Kendo/UI/Widget#render) method.

        <?php
        echo $treeview->render();
        ?>

## Getting Client-side Reference

You can reference the clien-side Kendo TreeView instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](/kendo-ui/api/web/treeview#methods) to control its behavior.


### Example

        <?php
        $treeview = new \Kendo\UI\TreeView('treeview');
        echo $treeview->render();
        ?>
        <script>
        $(function() {
            // The constructor parameter is used as the 'id' HTML attribute of the treeview
            var treeview = $("#treeview").data("kendoTreeView")
        });
        </script>

## Handling Events

You can subscribe to all treeview [events](/kendo-ui/api/web/treeview#events).

### Example - subscribing by specifying JavaScript function name

        <?php
        $treeview = new \Kendo\UI\TreeView('treeview');

        // The 'treeview_collapse' JavaScript function will handle the 'treeview_collapse' event of the treeview
        $treeview->collapse('treeview_collapse');

        echo $treeview->render();
        ?>
        <script>
        function treeview_collapse() {
            // Handle the collapse event
        }
        </script>

### Example - providing inline JavaScript code

        <?php
        $treeview = new \Kendo\UI\TreeView('treeview');

        // Provide inline JavaScript code that will handle the 'collapse' event of the treeview
        $treeview->collapse('function() { /* Handle the collapse event */ }');

        echo $treeview->render();
        ?>
