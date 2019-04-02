
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Attachment
var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.fileAttachment",
	Name = "menu.txt",
	ContentBytes = "base64bWFjIGFuZCBjaGVlc2UgdG9kYXk=",
};

await graphClient.Me.Events["AAMkAGI1AAAt9AHjAAA="].Attachments
	.Request()
	.AddAsync(attachments);

```