---
title: kendo.mobile.ui.Widget
slug: api-framework-mobilewidget
tags: api,framework
publish: true
---

# kendo.mobile.ui.Widget

Base class of all Kendo UI Mobile widgets. Inherits from [kendo.ui.Widget](/kendo-ui/api/framework/widget).

## Methods

### view

Returns the [kendo.mobile.ui.View](/kendo-ui/api/mobile/view) which contains the widget. If the widget is contained in a splitview, modalview, or drawer, the respective widget instance is returned.

#### Example

    <div data-role="view" id="foo" data-init="getButtonView">
        <a id="button" data-role="button">I am a mobile button</a>
    </div>

    <script>
        new kendo.mobile.Application();
        function getButtonView() {
            console.log($("#button").data("kendoMobileButton").view()); // the foo mobile view instance
        }
    </script>
