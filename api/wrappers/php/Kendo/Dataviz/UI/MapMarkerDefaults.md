---
title: MapMarkerDefaults
slug: php-dataviz-ui-mapmarkerdefaults
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\MapMarkerDefaults

A PHP class representing the markerDefaults setting of Map.


## Methods

### shape
The default marker shape. The following pre-defined marker shapes are available:Marker shapes are implemented as CSS classes on the marker element (span.k-marker).
For example "pinTarget" is rendered as "k-marker-pin-target".

#### Returns
`\Kendo\Dataviz\UI\MapMarkerDefaults`

#### Parameters

##### $value `string`



#### Example 
    <?php
    $markerDefaults = new \Kendo\Dataviz\UI\MapMarkerDefaults();
    $markerDefaults->shape('value');
    ?>

### tooltip

Default Kendo UI Tooltip options for this marker.

#### Returns
`\Kendo\Dataviz\UI\MapMarkerDefaults`

#### Parameters

##### $value `\Kendo\Dataviz\UI\MapMarkerDefaultsTooltip|array`


#### Example - using [\Kendo\Dataviz\UI\MapMarkerDefaultsTooltip](/kendo-ui/api/wrappers/php/Kendo/Dataviz/UI/MapMarkerDefaultsTooltip)
    <?php
    $markerDefaults = new \Kendo\Dataviz\UI\MapMarkerDefaults();
    $tooltip = new \Kendo\Dataviz\UI\MapMarkerDefaultsTooltip();
    $autoHide = true;
    $tooltip->autoHide($autoHide);
    $markerDefaults->tooltip($tooltip);
    ?>

#### Example - using array

    <?php
    $markerDefaults = new \Kendo\Dataviz\UI\MapMarkerDefaults();
    $autoHide = true;
    $markerDefaults->tooltip(array('autoHide' => $autoHide));
    ?>

