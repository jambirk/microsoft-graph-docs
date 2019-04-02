
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var clientContext = "d45324c1-fcb5-430a-902c-f20af696537c";

var loop = 5;

//create instance of MediaInfo
var mediaInfo = new MediaInfo
{
	Uri = "https://cdn.contoso.com/beep.wav",
	ResourceId = "1D6DE2D4-CD51-4309-8DAA-70768651088E",
};

var @odata.type = "#microsoft.graph.mediaPrompt";

//create Prompt list and populate it
var prompts = new List<Prompt>();
prompts.Add(new Prompt(@odata.type,mediaInfo,loop));

await graphClient.App.Calls["{id}"]
	.PlayPrompt(prompts,clientContext)
	.Request()
	.PostAsync()

```