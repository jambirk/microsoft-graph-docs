
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookWorksheetProtectionOptions
var options = new WorkbookWorksheetProtectionOptions
{
	AllowFormatCells = true,
	AllowFormatColumns = true,
	AllowFormatRows = true,
	AllowInsertColumns = true,
	AllowInsertRows = true,
	AllowInsertHyperlinks = true,
	AllowDeleteColumns = true,
	AllowDeleteRows = true,
	AllowSort = true,
	AllowAutoFilter = true,
	AllowPivotTables = true,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Protection
	.Protect(options)
	.Request()
	.PostAsync()

```