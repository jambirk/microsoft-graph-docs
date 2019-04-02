
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const series = {
  index: 2
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/itemAt')
		.post({workbookChartSeries : series});
	console.log(res);
} catch (error) {
	throw error;
}

```