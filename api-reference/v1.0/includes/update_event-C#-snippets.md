
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of ResponseStatus
var responseStatus = new ResponseStatus
{
	Response = "",
	Time = "datetime-value",
};

//create instance of Event
var events = new Event
{
	OriginalStartTimeZone = "originalStartTimeZone-value",
	OriginalEndTimeZone = "originalEndTimeZone-value",
	ResponseStatus = responseStatus,
	Recurrence = null,
	ICalUId = "iCalUId-value",
	ReminderMinutesBeforeStart = 99,
	IsReminderOn = true,
};

await graphClient.Me.Events["{id}"]
	.Request()
	.UpdateAsync(events);

```