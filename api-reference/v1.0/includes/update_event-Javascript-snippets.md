
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const events = {
  originalStartTimeZone: "originalStartTimeZone-value",
  originalEndTimeZone: "originalEndTimeZone-value",
  responseStatus: {
    response: "",
    time: "datetime-value"
  },
  recurrence: null,
  iCalUId: "iCalUId-value",
  reminderMinutesBeforeStart: 99,
  isReminderOn: true
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}')
		.update({event : events});
	console.log(res);
} catch (error) {
	throw error;
}

```