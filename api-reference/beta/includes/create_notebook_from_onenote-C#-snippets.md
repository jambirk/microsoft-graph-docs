
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Notebook
var notebooks = new Notebook
{
	DisplayName = "Notebook name",
};

await graphClient.Me.Onenote.Notebooks
	.Request()
	.AddAsync(notebooks);

```