
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/education/synchronizationProfiles/{id}/uploadUrl')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```