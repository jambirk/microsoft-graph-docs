
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var index = 5;

//create Int32 list and populate it
var values = new List<Int32>();

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Rows
	.Add(index,values)
	.Request()
	.PostAsync()

```