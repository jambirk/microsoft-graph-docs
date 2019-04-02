
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const mailboxSettings = {
    @odata.context: "https://graph.microsoft.com/beta/$metadata#Me/mailboxSettings",
    automaticRepliesSetting: {
        status: "Scheduled",
        scheduledStartDateTime: {
          dateTime: "2016-03-20T18:00:00.0000000",
          timeZone: "UTC"
        },
        scheduledEndDateTime: {
          dateTime: "2016-03-28T18:00:00.0000000",
          timeZone: "UTC"
        }
    }
};

//make the request to Graph
try{
	let res = await client.api('/me/mailboxSettings')
		.version('beta')
		.update({mailboxSettings : mailboxSettings});
	console.log(res);
} catch (error) {
	throw error;
}

```