
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const getMemberObjects = {
  securityEnabledOnly: false
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/getMemberObjects')
		.post({Boolean : getMemberObjects});
	console.log(res);
} catch (error) {
	throw error;
}

```