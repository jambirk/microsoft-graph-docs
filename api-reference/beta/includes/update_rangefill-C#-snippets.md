
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFill
var fill = new WorkbookRangeFill
{
	Color = "color-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["name"].Range().Format.Fill
	.Request()
	.UpdateAsync(fill);

```