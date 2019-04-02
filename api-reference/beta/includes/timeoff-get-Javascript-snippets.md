
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/teams/{teamId}/schedule/timesOff/{timeOffId}')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```