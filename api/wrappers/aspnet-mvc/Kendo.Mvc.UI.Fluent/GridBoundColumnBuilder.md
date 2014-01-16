---
title:GridBoundColumnBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridboundcolumnbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridBoundColumnBuilder
Defines the fluent interface for configuring bound columns



## Methods

### Format(`System.String`)
Gets or sets the format for displaying the data.


#### Parameters

##### value `System.String`
The value.




#### Example (ASPX)
    <%= Html.Kendo().Grid(Model)
    .Name("Grid")
    .Columns(columns => columns.Bound(o => o.OrderDate).Format("{0:dd/MM/yyyy}"))
    %>


### EditorViewData(`System.Object`)
Provides additional view data in the editor template for that column (if any).


#### Parameters

##### additionalViewData `System.Object`
An anonymous object which contains the additional data




#### Example (ASPX)
    <%= Html.Kendo().Grid(Model)
    .Name("Grid")
    .Columns(columns => {
        columns.Bound(o => o.Customer).EditorViewData(new { customers = Model.Customers });
    })
    %>


### EditorTemplateName(`System.String`)
Specify which editor template should be used for the column


#### Parameters

##### templateName `System.String`
name of the editor template





### Sortable(`System.Boolean`)
Enables or disables sorting the column. All bound columns are sortable by default.




#### Example (ASPX)
    <%= Html.Kendo().Grid(Model)
    .Name("Grid")
    .Columns(columns => columns.Bound(o => o.OrderDate).Sortable(false))
    %>


### Groupable(`System.Boolean`)
Enables or disables grouping by that column. All bound columns are groupable by default.




#### Example (ASPX)
    <%= Html.Kendo().Grid(Model)
    .Name("Grid")
    .Columns(columns => columns.Bound(o => o.OrderDate).Groupable(false))
    %>


### Filterable(`System.Boolean`)
Enables or disables filtering the column. All bound columns are filterable by default.




#### Example (ASPX)
    <%= Html.Kendo().Grid(Model)
    .Name("Grid")
    .Columns(columns => columns.Bound(o => o.OrderDate).Filterable(false))
    %>


### Encoded(`System.Boolean`)
Enables or disables HTML encoding the data of the column. All bound columns are encoded by default.




#### Example (ASPX)
    <%= Html.Kendo().Grid(Model)
    .Name("Grid")
    .Columns(columns => columns.Bound(o => o.OrderDate).Encoded(false))
    %>


### Template(`System.Action<T>`)
Sets the template for the column.


#### Parameters

##### templateAction `System.Action<T>`
The action defining the template.




#### Example (ASPX)
    <% Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns
            .Add(c => c.CustomerID)
            .Template(() =>
            {
                %>
                >img
                alt="<%= c.CustomerID %>"
                src="<%= Url.Content("~/Content/Grid/Customers/" + c.CustomerID + ".jpg") %>"
                />
                <%
                }).Title("Picture");)
                .Render();
                %>


### Template(`System.Func<T,System.Object>`)
Sets the template for the column.


#### Parameters

##### inlineTemplate `System.Func<T,System.Object>`
The action defining the template.



#### Returns




### ClientTemplate(`System.String`)
Sets the client template for the column.


#### Parameters

##### value `System.String`
The template



#### Returns




### ClientGroupHeaderTemplate(`System.String`)
Sets the client group template for the column.


#### Parameters

##### value `System.String`
The template



#### Returns




### ClientGroupFooterTemplate(`System.String`)
Sets the client group footer template for the column.


#### Parameters

##### value `System.String`
The template



#### Returns




### FooterTemplate(`System.Action<Kendo.Mvc.UI.GridAggregateResult>`)
Sets the footer template for the column.


#### Parameters

##### template System.Action<[Kendo.Mvc.UI.GridAggregateResult](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/GridAggregateResult)>
The action defining the template.





### FooterTemplate(`System.Func<Kendo.Mvc.UI.GridAggregateResult,System.Object>`)
Sets the footer template for the column.


#### Parameters

##### template System.Func<[Kendo.Mvc.UI.GridAggregateResult](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/GridAggregateResult),System.Object>
The action defining the template.





### GroupFooterTemplate(`System.Action<Kendo.Mvc.UI.GridAggregateResult>`)
Sets the group footer template for the column.


#### Parameters

##### template System.Action<[Kendo.Mvc.UI.GridAggregateResult](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/GridAggregateResult)>
The action defining the template.





### GroupFooterTemplate(`System.Func<Kendo.Mvc.UI.GridAggregateResult,System.Object>`)
Sets the group footer template for the column.


#### Parameters

##### template System.Func<[Kendo.Mvc.UI.GridAggregateResult](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/GridAggregateResult),System.Object>
The action defining the template.





### GroupHeaderTemplate(`System.Action<Kendo.Mvc.UI.GridGroupAggregateResult>`)
Sets the group footer template for the column.


#### Parameters

##### template System.Action<[Kendo.Mvc.UI.GridGroupAggregateResult](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/GridGroupAggregateResult)>
The action defining the template.





### GroupHeaderTemplate(`System.Func<Kendo.Mvc.UI.GridGroupAggregateResult,System.Object>`)
Sets the group footer template for the column.


#### Parameters

##### template System.Func<[Kendo.Mvc.UI.GridGroupAggregateResult](/kendo-ui/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/GridGroupAggregateResult),System.Object>
The action defining the template.






