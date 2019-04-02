
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const domains = {
  isDefault: true,
  supportedServices: [
    "Email",
    "OfficeCommunicationsOnline"
  ]
};

//make the request to Graph
try{
	let res = await client.api('/domains/contoso.com')
		.update({domain : domains});
	console.log(res);
} catch (error) {
	throw error;
}

```