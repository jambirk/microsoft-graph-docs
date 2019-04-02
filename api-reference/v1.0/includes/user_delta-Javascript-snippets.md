
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/users/delta')
		.header('Prefer','return=minimal')
		.select('displayName,jobTitle,mobilePhone')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```