---
title:TooltipEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.tooltipeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TooltipEventBuilder
Defines the fluent interface for configuring tooltip client events.



## Methods

### Show(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the Show client-side event

For additional information check the [show](/kendo-ui/api/web/tooltip#events-show) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.Show(
                @<text>
                    function(e) {
                    //event handling code
                    }
                    </text>
                    ))
                )


### Show(`System.String`)
Defines the name of the JavaScript function that will handle the the Show client-side event.

For additional information check the [show](/kendo-ui/api/web/tooltip#events-show) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.Show("show"))
    )


### Hide(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the Hide client-side event

For additional information check the [hide](/kendo-ui/api/web/tooltip#events-hide) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.Hide(
                @<text>
                    function(e) {
                    //event handling code
                    }
                    </text>
                    ))
                )


### Hide(`System.String`)
Defines the name of the JavaScript function that will handle the the Hide client-side event.

For additional information check the [hide](/kendo-ui/api/web/tooltip#events-hide) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.Hide("hide"))
    )


### ContentLoad(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the ContentLoad client-side event

For additional information check the [contentLoad](/kendo-ui/api/web/tooltip#events-contentLoad) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.ContentLoad(
                @<text>
                    function(e) {
                    //event handling code
                    }
                    </text>
                    ))
                )


### ContentLoad(`System.String`)
Defines the name of the JavaScript function that will handle the the ContentLoad client-side event.

For additional information check the [contentLoad](/kendo-ui/api/web/tooltip#events-contentLoad) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.ContentLoad("contentLoad"))
    )


### Error(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the Error client-side event

For additional information check the [error](/kendo-ui/api/web/tooltip#events-error) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.Error(
                @<text>
                    function(e) {
                    //event handling code
                    }
                    </text>
                    ))
                )


### Error(`System.String`)
Defines the name of the JavaScript function that will handle the the Error client-side event.

For additional information check the [error](/kendo-ui/api/web/tooltip#events-error) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.Error("error"))
    )


### RequestStart(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the RequestStart client-side event

For additional information check the [requestStart](/kendo-ui/api/web/tooltip#events-requestStart) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.RequestStart(
                @<text>
                    function(e) {
                    //event handling code
                    }
                    </text>
                    ))
                )


### RequestStart(`System.String`)
Defines the name of the JavaScript function that will handle the the RequestStart client-side event.

For additional information check the [requestStart](/kendo-ui/api/web/tooltip#events-requestStart) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    @(Html.Kendo().Tooltip()
        .For("#element")
        .Events(events => events.RequestStart("requestStart"))
    )



