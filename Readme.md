
# Blazor Grid - Bind to a DataTable object

The **DxGrid** component works with **IEnumerable** collections. That is why you cannot pass a **DataTable** object directly to the Grid's [Data](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.Data) property. 

![Grid - Bind to DataTable](bind-grid-to-datatable.png)

When you know the structure of the **DataTable** object, you can create a class with the corresponding properties for each column in the **DataTable** object. After that, you need to generate an **IEnumerable** collection of based on the **Rows** collection of the **DataTable** object. The **Static Object** Grid demonstrates this approach.

When you generate a **DataTable** object dynamically, its structure is unknown. In this case, you can bind the **DxGrid** component to an **IEnumerable** collection of the [ExpandoObject](https://docs.microsoft.com/en-us/dotnet/api/system.dynamic.expandoobject?view=netframework-4.8) objects. This collection allows you to generate properties based on the structure of the **DataTable** dynamically (see the [ConvertDataTableToExpandoObjectList](./CS/BindToDataTable/Pages/Index.razor#L64) method). The **Dynamic Object** Grid demonstrates this approach.

<!-- default file list -->
## Files to look at

* [Index.razor](./CS/BindToDataTable/Pages/Index.razor)
<!-- default file list end -->

## Documentation

* [Grid - Data Binding](https://docs.devexpress.com/Blazor/403737/components/grid/bind-to-data)
* [Bind Components to Data with EF Core](https://docs.devexpress.com/Blazor/403167/common-concepts/data-binding/bind-components-to-data-with-entity-framework-core)

## More Examples

* [Grid - Bind to Web API Service](https://github.com/DevExpress-Examples/blazor-DxGrid-Bind-To-Web-Api-Service)
