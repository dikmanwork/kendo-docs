---
title:CalendarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarEventBuilder
Defines the fluent interface for configuring datepicker client events.



## Methods

### Change(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the Change client-side event

For additional information check the [change](/kendo-ui/api/web/calendar#events-change) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    <%= Html.Kendo().Calendar()
    .Name("DatePicker")
    .Events(events => events.Change(
            @<text>
                function(e) {
                //event handling code
                }
                </text>
                ))
                %>


### Change(`System.String`)
Defines the name of the JavaScript function that will handle the the Change client-side event.

For additional information check the [change](/kendo-ui/api/web/calendar#events-change) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    <%= Html.Kendo().Calendar()
    .Name("Calendar")
    .Events(events => events.Change("change"))
    %>


### Navigate(`System.Func<System.Object,System.Object>`)
Defines the inline handler of the Navigate client-side event

For additional information check the [navigate](/kendo-ui/api/web/calendar#events-navigate) event documentation.


#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).




#### Example (ASPX)
    <%= Html.Kendo().Calendar()
    .Name("Calendar")
    .Events(events => events.Navigate(
            @<text>
                %>
                function(e) {
                //event handling code
                }
                </text>
                ))
                %>


### Navigate(`System.String`)
Defines the name of the JavaScript function that will handle the Navigate client-side event.

For additional information check the [navigate](/kendo-ui/api/web/calendar#events-navigate) event documentation.


#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.




#### Example (ASPX)
    <%= Html.Kendo().Calendar()
    .Name("Calendar")
    .Events(events => events.Navigate("navigate"))
    %>



