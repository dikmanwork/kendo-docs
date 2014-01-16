---
title: Local binding
meta_title: How to bind Kendo Sparkline for PHP to PHP array
meta_description: Learn how to bind Kendo UI Sparkline for PHP to array of data
slug: php-sparkline-local-binding
publish: true
relatedDocs: php-dataviz-ui-sparkline, php-sparkline-overview
---

# Local Binding to Array

This help topic shows how to bind Kendo Sparkline for PHP to a PHP [array](http://php.net/manual/en/language.types.array.php). This array
can be populated from a data base or declared inline (in the page).

## Binding to array returned by PDO

PHP Data Objects ([PDO](http://www.php.net/manual/en/intro.pdo.php)) is an interface for accessing various databases in PHP. Here is how to bind Kendo Sparkline to array
returned by PDO.

First we will configure a Kendo Sparkline for PHP binding and then we will implement the remote service which will return JSON.


> The following demo is using the sample SQLite database shipped with the **UI for PHP** demos (**/wrappers/php/sample.db**).

1. Follow the steps from the [introduction](/kendo-ui/getting-started/using-kendo-with/php/introduction) - include the autoloader, JavaScript and CSS files.
1. Create a PDO connection

        <?php
        $db = new PDO('sqlite:../sample.db');
        ?>
1. Retrieve all records from the `Weather` table

        <?php
        $statement = $db->prepare('SELECT TMax FROM Weather LIMIT 10');
        $statement->execute();
        $weather = $statement->fetchAll(PDO::FETCH_ASSOC);
        ?>
1. Create a [data source](/kendo-ui/api/wrappers/php/Kendo/Data/DataSource) and set its [data](/kendo-ui/api/wrappers/php/Kendo/Data/DataSource#data) and [schema](/kendo-ui/api/wrappers/php/Kendo/Data/DataSource#schema). Setting the schema is required to specify the model fields. Those fields are required for filtering and editing.

        <?php
        // Create the schema model
        $model = new \Kendo\Data\DataSourceSchemaModel();

        // Create a field for the 'TMax' column of the 'Weather' table
        $tmaxField = new \Kendo\Data\DataSourceSchemaModelField('TMax');
        $tmaxField->type('number');

        $model->addField($tmaxField);

        // Create the schema
        $schema = new \Kendo\Data\DataSourceSchema();

        // Set its model
        $schema->model($model);

        // Create the data source
        $dataSource = new \Kendo\Data\DataSource();

        // Specify the schema and data
        $dataSource->data($weather)
                   ->schema($schema);
        ?>
1. Create a [sparkline](/kendo-ui/api/wrappers/php/Kendo/Dataviz/UI/Sparkline), configure its [series](/kendo-ui/api/wrappers/php/Kendo/Dataviz/UI/Sparkline#addSeriesItem).

        <?php
        $sparkline = new \Kendo\Dataviz\UI\Sparkline('sparkline');

        $tmaxSeries = new \Kendo\Dataviz\UI\SparklineSeriesItem();
        $tmaxSeries->field('TMax');

        $sparkline->addSeriesItem($tmaxSeries)
              ->dataSource($dataSource);
        ?>
1. Output the sparkline by echo-ing the result of the [render](/kendo-ui/api/wrappers/php/Kendo/UI/Widget#render) method.

        <?php
        echo $sparkline->render();
        ?>

