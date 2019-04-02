
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names('name')/range/format/fill/clear')
		.version('beta')
		.post();
	console.log(res);
} catch (error) {
	throw error;
}

```