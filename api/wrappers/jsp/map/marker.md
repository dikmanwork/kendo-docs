---
title: map-marker
slug: jsp-map-marker
tags: api, java
publish: true
---

# \<kendo:map-marker\>

Static markers to display on the map.

#### Example
    <kendo:map-markers>
        <kendo:map-marker></kendo:map-marker>
    </kendo:map-markers>

## Configuration Attributes

### location `java.lang.Object`

The marker location on the map. Coordinates are listed as [Latitude, Longitude].

#### Example
    <kendo:map-marker location="location">
    </kendo:map-marker>

### shape `java.lang.String`

The marker shape. Supported shapes are "pin" and "circle".

#### Example
    <kendo:map-marker shape="shape">
    </kendo:map-marker>


##  Configuration JSP Tags

### kendo:map-marker-tooltip

Kendo UI Tooltip options for this marker.

More documentation is available at [kendo:map-marker-tooltip](/kendo-ui/api/wrappers/jsp/map/marker-tooltip).

#### Example

    <kendo:map-marker>
        <kendo:map-marker-tooltip></kendo:map-marker-tooltip>
    </kendo:map-marker>

