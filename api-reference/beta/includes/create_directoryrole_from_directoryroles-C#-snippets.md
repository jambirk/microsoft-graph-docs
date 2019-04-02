
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of DirectoryRole
var directoryRoles = new DirectoryRole
{
	Description = "description-value",
	DisplayName = "displayName-value",
	RoleTemplateId = "roleTemplateId-value",
};

await graphClient.DirectoryRoles
	.Request()
	.AddAsync(directoryRoles);

```