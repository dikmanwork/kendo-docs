---
title:ChartBulletSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbulletseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBulletSeriesBuilder
Defines the fluent interface for configuring bullet series.


## Properties
### Series
Gets or sets the series.



## Methods

### Gap(`System.Double`)
Set distance between category clusters. 
            
            A value of 1 means that there is a total of 1 bullet width / vertical bullet height between categories.
            The distance is distributed evenly on each side.
            The default value is 1.5




#### Example (ASPX)
    <%= Html.Kendo().Chart(Model)
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target).Gap(1))
    %>


### Spacing(`System.Double`)
Sets a value indicating the distance between bullets / categories.


#### Parameters

##### spacing `System.Double`
Value of 1 means that the distance between bullets is equal to their width.
            The default value is 0




#### Example (ASPX)
    <%= Html.Kendo().Chart(Model)
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target).Spacing(1))
    %>


### Border(`System.Int32,System.String,Kendo.Mvc.UI.ChartDashType`)
Sets the bullets border.


#### Parameters

##### width `System.Int32`
The bullets border width.

##### color `System.String`
The bullets border color (CSS syntax).

##### dashType [Kendo.Mvc.UI.ChartDashType](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartDashType)
The bullets border dash type.




#### Example (ASPX)
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bullet(s => s.Current, s => s.Target).Border("1", "#000", ChartDashType.Dot))
        .Render();
    %>


### Overlay(`Kendo.Mvc.UI.ChartBarSeriesOverlay`)
Sets the bullet effects overlay


#### Parameters

##### overlay [Kendo.Mvc.UI.ChartBarSeriesOverlay](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartBarSeriesOverlay)
The bullet effects overlay. The default is ChartBarSeriesOverlay.Glass




#### Example (ASPX)
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bullet(s => s.Current, s => s.Target).Overlay(ChartBarSeriesOverlay.None))
        .Render();
    %>


### Name(`System.String`)
Sets the series title displayed in the legend.


#### Parameters

##### text `System.String`
The title.




#### Example (ASPX)
    <%= Html.Kendo().Chart(Model)
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target).Name("Sales"))
    %>


### Opacity(`System.Double`)
Sets the series opacity.


#### Parameters

##### opacity `System.Double`
The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.




#### Example (ASPX)
    <%= Html.Kendo().Chart(Model)
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target).Opacity(0.5))
    %>


### Color(`System.String`)
Sets the bullet fill color


#### Parameters

##### color `System.String`
The bar bullet color (CSS syntax).




#### Example (ASPX)
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bullet(s => s.Current, s => s.Target).Color("Red"))
        .Render();
    %>


### Tooltip(`System.Action<Kendo.Mvc.UI.Fluent.ChartTooltipBuilder>`)
Configure the data point tooltip for the series.


#### Parameters

##### configurator System.Action<[Kendo.Mvc.UI.Fluent.ChartTooltipBuilder](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ChartTooltipBuilder)>
Use the configurator to set data tooltip options.




#### Example (ASPX)
    <%= Html.Kendo().Chart()
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target)
        .Tooltip(tooltip =>
        {
            tooltip.Visible(true).Format("{0:C}");
        })
    )
    %>


### Tooltip(`System.Boolean`)
Sets the data point tooltip visibility.


#### Parameters

##### visible `System.Boolean`
A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.




#### Example (ASPX)
    <%= Html.Kendo().Chart()
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target).Tooltip(true))
    %>


### Axis(`System.String`)
Sets the axis name to use for this series.


#### Parameters

##### axis `System.String`
The axis name for this series.




#### Example (ASPX)
    <%= Html.Kendo().Chart(Model)
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target).Name("Sales").Axis("secondary"))
    .ValueAxis(axis => axis.Numeric())
    .ValueAxis(axis => axis.Numeric("secondary"))
    .CategoryAxis(axis => axis.AxisCrossingValue(0, 10))
    %>


### Target(`System.Action<Kendo.Mvc.UI.Fluent.ChartBulletTargetBuilder>`)
Configure the data point tooltip for the series.


#### Parameters

##### configurator System.Action<[Kendo.Mvc.UI.Fluent.ChartBulletTargetBuilder](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ChartBulletTargetBuilder)>
Use the configurator to set data tooltip options.




#### Example (ASPX)
    <%= Html.Kendo().Chart()
    .Name("Chart")
    .Series(series => series.Bullet(s => s.Current, s => s.Target)
        .Tooltip(tooltip =>
        {
            tooltip.Visible(true).Format("{0:C}");
        })
    )
    %>



