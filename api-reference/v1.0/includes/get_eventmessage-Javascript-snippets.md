
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkADYAAAImV_lAAA=')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```