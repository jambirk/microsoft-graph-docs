
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/drive/search(q='{search-query}')')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```