
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PhysicalAddress
var homeAddress = new PhysicalAddress
{
	Street = "123 Some street",
	City = "Seattle",
	State = "WA",
	PostalCode = "98121",
};

//create instance of Contact
var contacts = new Contact
{
	HomeAddress = homeAddress,
	Birthday = "1974-07-22",
};

await graphClient.Me.Contacts["{id}"]
	.Request()
	.UpdateAsync(contacts);

```