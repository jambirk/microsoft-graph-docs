
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Identity
var user = new Identity
{
	Id = "550fae72-d251-43ec-868c-373732c2704f",
	TenantId = "72f988bf-86f1-41af-91ab-2d7cd011db47",
	DisplayName = "Heidi Steen",
};

//create instance of Identity
var identity = new Identity
{
	User = user,
};

//create instance of InvitationParticipantInfo
var transferTarget = new InvitationParticipantInfo
{
	EndpointType = "default",
	Identity = identity,
	LanguageId = "languageId-value",
	Region = "region-value",
	ReplacesCallId = "replacesCallId-value",
};

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"]
	.Transfer(transferTarget,target,replacesCallId)
	.Request()
	.PostAsync()

```