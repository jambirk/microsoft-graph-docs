
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const delete = {
  shift: "shift-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names('name')/range/delete')
		.version('beta')
		.post({String : delete});
	console.log(res);
} catch (error) {
	throw error;
}

```