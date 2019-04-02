
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const rows = {
  index: 4
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/rows/itemAt')
		.post({workbookTableRow : rows});
	console.log(res);
} catch (error) {
	throw error;
}

```