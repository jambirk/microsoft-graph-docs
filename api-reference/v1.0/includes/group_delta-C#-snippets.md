
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var delta = await graphClient.Groups.Delta()
	.Request()
	.Header("Prefer","return=minimal")
	.Select("displayName,description,mailNickname")
	.GetAsync();

```