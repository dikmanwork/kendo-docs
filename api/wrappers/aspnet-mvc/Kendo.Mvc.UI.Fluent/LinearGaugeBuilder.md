---
title:LinearGaugeBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.lineargaugebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.LinearGaugeBuilder
Defines the fluent interface for configuring the LinearGauge component.



## Methods

### Theme(`System.String`)
Sets the theme of the linear gauge.


#### Parameters

##### theme `System.String`
The linear gauge theme.




#### Example (ASPX)
    <%= Html.Kendo().RadialGauge()
    .Name("radialGauge")
    .Theme("Black")
    %>


### RenderAs(`Kendo.Mvc.UI.RenderingMode`)
Sets the preferred rendering engine.
            If it is not supported by the browser, the Chart will switch to the first available mode.


#### Parameters

##### renderAs [Kendo.Mvc.UI.RenderingMode](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/RenderingMode)
The preferred rendering engine.





### GaugeArea(`System.Action<Kendo.Mvc.UI.Fluent.GaugeAreaBuilder>`)
Sets the linear gauge area.


#### Parameters

##### configurator System.Action<[Kendo.Mvc.UI.Fluent.GaugeAreaBuilder](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeAreaBuilder)>
The linear gauge area.




#### Example (ASPX)
    <%= Html.Kendo().RadialGauge()
    .Name("radialGauge")
    .ChartArea(chartArea => chartArea.margin(20))
    %>


### Scale(`System.Action<Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder>`)
Configures the scale


#### Parameters

##### configurator System.Action<[Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeLinearScaleBuilder)>
The configurator




#### Example (ASPX)
    <%= Html.Kendo().RadialGauge()
    .Name("radialGauge")
    .Scale(scale => scale
        .Min(10)
    )
    %>


### Pointer(`System.Action<Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder>`)
Configures the pointer


#### Parameters

##### configurator System.Action<[Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeLinearPointerBuilder)>
The configurator




#### Example (ASPX)
    <%= Html.Kendo().RadialGauge()
    .Name("radialGauge")
    .Pointer(pointer => pointer
        .Value(10)
    )
    %>


### Transitions(`System.Boolean`)
Enables or disabled animated transitions on initial load and refresh.


#### Parameters

##### transitions `System.Boolean`
A value indicating if transition animations should be played.




#### Example (ASPX)
    <%= Html.Kendo().RadialGauge()
    .Name("radialScale")
    .Transitions(false)
    %>



