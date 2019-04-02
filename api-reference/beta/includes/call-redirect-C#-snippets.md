
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var region = "westus";

var languageId = "en-US";

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

var endpointType = "default";

//create InvitationParticipantInfo list and populate it
var targets = new List<InvitationParticipantInfo>();
targets.Add(new InvitationParticipantInfo(endpointType,identity,languageId,region));

var targetDisposition = "default";

var timeout = 99;

var maskCallee = False;

var maskCaller = False;

await graphClient.App.Calls["{id}"]
	.Redirect(targets,targetDisposition,timeout,maskCallee,maskCaller)
	.Request()
	.PostAsync()

```