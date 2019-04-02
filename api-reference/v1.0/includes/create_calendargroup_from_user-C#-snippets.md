
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of CalendarGroup
var calendarGroups = new CalendarGroup
{
	Name = "name-value",
	ClassId = "classId-value",
	ChangeKey = "changeKey-value",
};

await graphClient.Me.CalendarGroups
	.Request()
	.AddAsync(calendarGroups);

```