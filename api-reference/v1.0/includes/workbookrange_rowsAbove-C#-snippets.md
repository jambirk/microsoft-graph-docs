
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"]
	.Range()
	.RowsAbove(count)
	.Request()
	.PostAsync()

```