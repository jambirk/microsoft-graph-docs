
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const assignLicense = {
  addLicenses: [
    {
      disabledPlans: [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      skuId: "skuId-value-1"
    },
    {
      disabledPlans: [ "a571ebcc-fqe0-4ca2-8c8c-7a284fd6c235" ],
      skuId: "skuId-value-2"
    }
  ],
  removeLicenses: []
};

//make the request to Graph
try{
	let res = await client.api('/me/assignLicense')
		.version('beta')
		.post({assignedLicense : assignLicense});
	console.log(res);
} catch (error) {
	throw error;
}

```