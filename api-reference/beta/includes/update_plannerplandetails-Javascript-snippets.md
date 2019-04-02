
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const details = {
  sharedWith: {
    "6463a5ce-2119-4198-9f2a-628761df4a62" : true,
    "d95e6152-f683-4d78-9ff5-67ad180fea4a" : false,
  },
  categoryDescriptions: {
    category1: "Indoors",
    category3: null,
  }
};

//make the request to Graph
try{
	let res = await client.api('/planner/plans/xqQg5FS2LkCp935s-FIFm2QAFkHM/details')
		.version('beta')
		.update({plannerPlanDetails : details});
	console.log(res);
} catch (error) {
	throw error;
}

```