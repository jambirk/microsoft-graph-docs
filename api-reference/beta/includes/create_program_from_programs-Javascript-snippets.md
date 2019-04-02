
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const programs = {
    displayName: "testprogram3",
    description: "test description"
};

//make the request to Graph
try{
	let res = await client.api('/programs')
		.version('beta')
		.post({program : programs});
	console.log(res);
} catch (error) {
	throw error;
}

```