---
title: Local binding
meta_title: How to bind Kendo TreeView for PHP to PHP array
meta_description: Learn how to bind Kendo UI TreeView for PHP to array of data
slug: php-treeview-local-binding
publish: true
relatedDocs: php-ui-treeview, php-treeview-overview
---

# Local Binding to Array

This help topic shows how to bind Kendo TreeView for PHP to a PHP [array](http://php.net/manual/en/language.types.array.php). This array
can be populated from a data base or declared inline (in the page). Local binding means that all the treeview data will be initially available
on the client and will not be requested per-level.

## Binding to array returned by PDO

PHP Data Objects ([PDO](http://www.php.net/manual/en/intro.pdo.php)) is an interface for accessing various databases in PHP. Here is how to bind Kendo TreeView to array
returned by PDO.

First we will configure a Kendo TreeView for PHP binding and then we will implement the remote service which will return JSON.

> The following demo is using the sample SQLite database shipped with the **UI for PHP** demos (**/wrappers/php/sample.db**).

1. Follow the steps from the [introduction](/kendo-ui/getting-started/using-kendo-with/php/introduction) - include the autoloader, JavaScript and CSS files.
1. Create a PDO connection

        <?php
        $db = new PDO('sqlite:../sample.db');
        ?>

1. Retrieve all records from the `Employees` table

        <?php
        $statement = $db->prepare('SELECT EmployeeID, FirstName, ReportsTo FROM Employees');
        $statement->execute();
        $rows = $statement->fetchAll(PDO::FETCH_ASSOC);
        ?>

1. Convert the table rows to hierarchical data

        <?php
        function toHierarchy($rows, $idField = 'id', $foreignKey = 'parent') {
            $hash = array();

            $result = array();

            // hash to rows by id
            foreach ($rows as $row) {
                $hash[$row[$idField]] = $row;
            }

            foreach ($hash as &$row) {
                $parentId = $row[$foreignKey];

                if (!is_null($parentId)) {
                    // add items field, if not available
                    if (!in_array('items', $hash[$parentId])) {
                        $hash[$parentId] = $hash[$parentId] + array('items' => array());
                    }

                    // add row to parent item
                    $hash[$parentId]['items'][] =& $row;
                }
            }

            foreach ($hash as &$row) {
                $parentId = $row[$foreignKey];

                if (is_null($parentId)) {
                    $result[] =& $row;
                }
            }

            return $result;
        }

        $data = toHierarchy($rows, 'EmployeeID', 'ReportsTo');
        ?>

1. Create a [data source](/kendo-ui/api/wrappers/php/Kendo/Data/DataSource) and set its [data](/kendo-ui/api/wrappers/php/Kendo/Data/DataSource#data)

        <?php
        $dataSource = new \Kendo\Data\DataSource();

        $dataSource->data($data);
        ?>

1. Create a [treeview](/kendo-ui/api/wrappers/php/Kendo/UI/TreeView), configure its [dataTextField](/kendo-ui/api/wrappers/php/Kendo/UI/TreeView#dataTextField) and set its [data source](/kendo-ui/api/wrappers/php/Kendo/UI/TreeView#datasource).

        <?php
        $treeview = new \Kendo\UI\TreeView('treeview');

        $treeview
            ->dataTextField('FirstName')
            ->dataSource($dataSource);

        ?>

1. Output the treeview by echo-ing the result of the [render](/kendo-ui/api/wrappers/php/Kendo/UI/Widget#render) method.

        <?php
        echo $treeview->render();
        ?>

