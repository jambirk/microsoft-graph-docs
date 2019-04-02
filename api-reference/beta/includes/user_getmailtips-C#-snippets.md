
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var EmailAddresses = new List<String>();

var MailTipsOptions = "automaticReplies, mailboxFullStatus";

await graphClient.Me
	.GetMailTips(emailAddresses,mailTipsOptions)
	.Request()
	.PostAsync()

```