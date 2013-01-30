---
title: ChartValueAxisItemMinorGridLines
slug: php-dataviz-ui-chartvalueaxisitemminorgridlines
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines

A PHP class representing the minorGridLines setting of ChartValueAxisItem.


## Methods

### color
The color of the lines.Note that this has no effect if the visibility of the minor grid lines is not set to true.

#### Returns
`\Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines`

#### Parameters

##### $value `string`



#### Example 
    $minorGridLines = new \Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines();
    $minorGridLines->color('value');

### dashType
The dash type of the minor grid lines.

#### Returns
`\Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines`

#### Parameters

##### $value `string`



#### Example 
    $minorGridLines = new \Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines();
    $minorGridLines->dashType('value');

### visible
The visibility of the lines.

#### Returns
`\Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines`

#### Parameters

##### $value `boolean`



#### Example 
    $minorGridLines = new \Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines();
    $minorGridLines->visible(true);

### width
The width of the lines.Note that this settings has no effect if the visibility of the minor grid lines is not set to true.

#### Returns
`\Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines`

#### Parameters

##### $value `float`



#### Example 
    $minorGridLines = new \Kendo\Dataviz\UI\ChartValueAxisItemMinorGridLines();
    $minorGridLines->width(1);
