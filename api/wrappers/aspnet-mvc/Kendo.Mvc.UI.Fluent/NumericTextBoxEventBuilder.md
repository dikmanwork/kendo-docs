---
title:NumericTextBoxEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.numerictextboxeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder
Defines the fluent interface for configuring the NumericTextBox events.



## Methods

### Change(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the Change client-side event

For additional information check the [change](/kendo-ui/api/web/numerictextbox#events-change) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    @(Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Change(
                @<text>
                    function(e) {
                    //event handling code
                    }
                    </text>
                    ))
                )


### Change(`System.String`)
Defines the name of the JavaScript function that will handle the the Change client-side event.

For additional information check the [change](/kendo-ui/api/web/numerictextbox#events-change) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    @(Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Change("change"))
    )


### Spin(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the Spin client-side event

For additional information check the [spin](/kendo-ui/api/web/numerictextbox#events-spin) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    @(Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Spin(
                @<text>
                    function(e) {
                    //event handling code
                    }
                    </text>
                    ))
                )


### Spin(`System.String`)
Defines the name of the JavaScript function that will handle the the Spin client-side event.

For additional information check the [spin](/kendo-ui/api/web/numerictextbox#events-spin) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    @(Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Spin("spin"))
    )



