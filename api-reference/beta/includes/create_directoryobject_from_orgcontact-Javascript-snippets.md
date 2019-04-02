
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const memberOf = {
  directoryObject: {
  }
};

//make the request to Graph
try{
	let res = await client.api('/contacts/{id}/memberOf')
		.version('beta')
		.post({directoryObject : memberOf});
	console.log(res);
} catch (error) {
	throw error;
}

```