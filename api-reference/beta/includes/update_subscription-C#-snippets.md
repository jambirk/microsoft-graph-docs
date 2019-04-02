
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Subscription
var subscriptions = new Subscription
{
	ExpirationDateTime = "2016-11-22T18:23:45.9356913Z",
};

await graphClient.Subscriptions["{id}"]
	.Request()
	.UpdateAsync(subscriptions);

```