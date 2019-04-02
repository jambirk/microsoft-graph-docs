
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/teams/{id}/installedApps')
		.version('beta')
		.expand('teamsAppDefinition')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```