
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PrivilegedRoleAssignment
var privilegedRoleAssignments = new PrivilegedRoleAssignment
{
	UserId = "userId-value",
	RoleId = "roleId-value",
};

await graphClient.PrivilegedRoleAssignments
	.Request()
	.AddAsync(privilegedRoleAssignments);

```