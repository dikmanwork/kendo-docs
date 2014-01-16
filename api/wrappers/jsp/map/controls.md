---
title: map-controls
slug: jsp-map-controls
tags: api, java
publish: true
---

# \<kendo:map-controls\>

The configuration of built-in map controls.

#### Example
    <kendo:map>
        <kendo:map-controls></kendo:map-controls>
    </kendo:map>

## Configuration Attributes

### attribution `boolean`

Enables or disables the built-in attribution control.

#### Example
    <kendo:map-controls attribution="attribution">
    </kendo:map-controls>

### navigator `boolean`

Enables or disables the built-in navigator control (directional pad). Further configuration is available via [kendo:map-controls-navigator](#kendo-map-controls-navigator). 

#### Example
    <kendo:map-controls navigator="navigator">
    </kendo:map-controls>

##  Configuration JSP Tags

### kendo:map-controls-attribution

Enables or disables the built-in attribution control.

More documentation is available at [kendo:map-controls-attribution](/kendo-ui/api/wrappers/jsp/map/controls-attribution).

#### Example

    <kendo:map-controls>
        <kendo:map-controls-attribution></kendo:map-controls-attribution>
    </kendo:map-controls>

### kendo:map-controls-navigator

Enables or disables the built-in navigator control (directional pad).

More documentation is available at [kendo:map-controls-navigator](/kendo-ui/api/wrappers/jsp/map/controls-navigator).

#### Example

    <kendo:map-controls>
        <kendo:map-controls-navigator></kendo:map-controls-navigator>
    </kendo:map-controls>


