
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Attachment
var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.fileAttachment",
	Name = "name-value",
	ContentBytes = "contentBytes-value",
};

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"].Attachments
	.Request()
	.AddAsync(attachments);

```