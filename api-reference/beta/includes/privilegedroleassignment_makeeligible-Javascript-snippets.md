
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/privilegedRoleAssignments/{id}/makeEligible')
		.version('beta')
		.post();
	console.log(res);
} catch (error) {
	throw error;
}

```