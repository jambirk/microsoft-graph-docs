
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
	Uid = "iCalUId-value",
	ReminderMinutesBeforeStart = 99,
	IsReminderOn = true,
};

await graphClient.Groups["{id}"].Events["{id}"]
	.Request()
	.UpdateAsync(events);

```