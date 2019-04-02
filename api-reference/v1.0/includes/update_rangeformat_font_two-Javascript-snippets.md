
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const font = {
  italic: true,
  size: 26
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$B$1')/format/font')
		.update({workbookRangeFont : font});
	console.log(res);
} catch (error) {
	throw error;
}

```