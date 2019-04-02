
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/education/classes/11021/assignments/19002/resources/22002')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```