
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/groups/45b7d2e7-b882-4a80-ba97-10b7a63b8fa4')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```