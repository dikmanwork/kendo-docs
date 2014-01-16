---
title: map-markerDefaults
slug: jsp-map-markerDefaults
tags: api, java
publish: true
---

# \<kendo:map-markerDefaults\>

The default options for all markers.

#### Example
    <kendo:map>
        <kendo:map-markerDefaults></kendo:map-markerDefaults>
    </kendo:map>

## Configuration Attributes

### shape `java.lang.String`

The default marker shape. The following pre-defined marker shapes are available:Marker shapes are implemented as CSS classes on the marker element (span.k-marker).
For example "pinTarget" is rendered as "k-marker-pin-target".

#### Example
    <kendo:map-markerDefaults shape="shape">
    </kendo:map-markerDefaults>


##  Configuration JSP Tags

### kendo:map-markerDefaults-tooltip

Default Kendo UI Tooltip options for this marker.

More documentation is available at [kendo:map-markerDefaults-tooltip](/kendo-ui/api/wrappers/jsp/map/markerdefaults-tooltip).

#### Example

    <kendo:map-markerDefaults>
        <kendo:map-markerDefaults-tooltip></kendo:map-markerDefaults-tooltip>
    </kendo:map-markerDefaults>

