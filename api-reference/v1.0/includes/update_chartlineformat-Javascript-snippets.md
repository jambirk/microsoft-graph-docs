
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const line = {
  color: "color-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/line')
		.update({workbookChartLineFormat : line});
	console.log(res);
} catch (error) {
	throw error;
}

```