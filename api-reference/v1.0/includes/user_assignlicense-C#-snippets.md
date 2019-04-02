
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var skuId = "guid";

//create Guid list and populate it
var disabledPlans = new List<Guid>();

//create AssignedLicense list and populate it
var addLicenses = new List<AssignedLicense>();
addLicenses.Add(new AssignedLicense(disabledPlans,skuId));

//create AssignedLicense list and populate it
var removeLicenses = new List<AssignedLicense>();

await graphClient.Me
	.AssignLicense(addLicenses,removeLicenses)
	.Request()
	.PostAsync()

```