
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "required";

//create instance of EmailAddress
var emailAddress = new EmailAddress
{
	Address = "adelev@contoso.onmicrosoft.com",
	Name = "Adele Vance",
};

//create Attendee list and populate it
var attendees = new List<Attendee>();
attendees.Add(new Attendee(emailAddress,type));

//create instance of Location
var location = new Location
{
	DisplayName = "Harry's Bar",
};

//create instance of DateTimeTimeZone
var end = new DateTimeTimeZone
{
	DateTime = "2019-03-10T14:00:00",
	TimeZone = "Pacific Standard Time",
};

//create instance of DateTimeTimeZone
var start = new DateTimeTimeZone
{
	DateTime = "2019-03-10T12:00:00",
	TimeZone = "Pacific Standard Time",
};

//create instance of ItemBody
var body = new ItemBody
{
	ContentType = "HTML",
	Content = "Does next month work for you?",
};

//create instance of Event
var events = new Event
{
	Subject = "Let's go for lunch",
	Body = body,
	Start = start,
	End = end,
	Location = location,
	Attendees = attendees,
};

await graphClient.Me.Calendars["AAMkAGViNDU7zAAAAAGtlAAA="].Events
	.Request()
	.AddAsync(events);

```