
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  address: "",
  hasHeaders: false
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/tables/$/add')
		.version('beta')
		.post({String : add});
	console.log(res);
} catch (error) {
	throw error;
}

```