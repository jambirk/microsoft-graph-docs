
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/education/classes/11021/assignments/19002/submissions/850f51b7/submit')
		.version('beta')
		.post();
	console.log(res);
} catch (error) {
	throw error;
}

```