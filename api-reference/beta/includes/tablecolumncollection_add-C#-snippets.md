
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Int32
var index = new Int32
{
};

//create Int32 list and populate it
var values = new List<Int32>();
values.Add(new Int32());

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns
	.Add(index,values,name)
	.Request()
	.PostAsync()

```