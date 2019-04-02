
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const progressTaskBoardFormat = {
  orderHint: "A6673H Ejkl!"
};

//make the request to Graph
try{
	let res = await client.api('/planner/tasks/{task-id}/progressTaskBoardFormat')
		.update({plannerProgressTaskBoardTaskFormat : progressTaskBoardFormat});
	console.log(res);
} catch (error) {
	throw error;
}

```