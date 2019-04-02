
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const decline = {
  comment: "comment-value",
  sendResponse: true
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}/decline')
		.post({String : decline});
	console.log(res);
} catch (error) {
	throw error;
}

```