
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerPlan
var plans = new PlannerPlan
{
	Title = "title-value",
};

await graphClient.Planner.Plans["'id'"]
	.Request()
	.UpdateAsync(plans);

```