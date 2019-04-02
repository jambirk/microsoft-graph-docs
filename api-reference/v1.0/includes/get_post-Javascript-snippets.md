
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/threads/{id}/posts/{id}')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```