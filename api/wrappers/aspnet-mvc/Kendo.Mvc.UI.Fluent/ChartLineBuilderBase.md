---
title:ChartLineBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlinebuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineBuilderBase
Defines the fluent interface for configuring ChartLine.



## Methods

### Color(`System.String`)
Sets the line color


#### Parameters

##### color `System.String`
The line color (CSS format).




#### Example (ASPX)
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.MajorGridLines(lines => lines.Color("#f00")))
        .Render();
    %>


### Width(`System.Int32`)
Sets the line width


#### Parameters

##### width `System.Int32`
The line width.




#### Example (ASPX)
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.MajorGridLines(lines => lines.Width(2)))
        .Render();
    %>


### DashType(`Kendo.Mvc.UI.ChartDashType`)
Sets the line dashType.


#### Parameters

##### dashType [Kendo.Mvc.UI.ChartDashType](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartDashType)
The line dashType.




#### Example (ASPX)
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.MajorGridLines(lines => lines.DashType(ChartDashType.Dot)))
        .Render();
    %>



