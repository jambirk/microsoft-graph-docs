
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFont
var font = new WorkbookRangeFont
{
	Bold = true,
	Color = "#4B180E",
	Size = 26,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["Sheet1"].Range('$A$1').Format.Font
	.Request()
	.UpdateAsync(font);

```