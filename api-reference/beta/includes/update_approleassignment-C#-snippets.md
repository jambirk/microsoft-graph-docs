
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of AppRoleAssignment
var appRoleAssignments = new AppRoleAssignment
{
	CreationTimestamp = "2016-10-19T10:37:00Z",
	PrincipalDisplayName = "principalDisplayName-value",
	PrincipalId = "principalId-value",
	PrincipalType = "principalType-value",
	ResourceDisplayName = "resourceDisplayName-value",
};

await graphClient.AppRoleAssignments["{id}"]
	.Request()
	.UpdateAsync(appRoleAssignments);

```