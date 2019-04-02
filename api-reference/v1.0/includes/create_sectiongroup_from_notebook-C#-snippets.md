
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of SectionGroup
var sectionGroups = new SectionGroup
{
	DisplayName = "Section group name",
};

await graphClient.Me.Onenote.Notebooks["{id}"].SectionGroups
	.Request()
	.AddAsync(sectionGroups);

```