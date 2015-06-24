
# Spreadsheet cron job
Steps for setting up a cron job that will automatically convert a Google spreadsheet to jsonp at regular intervals. Only use this if you have a project where the data is regularly being updated after it launches for either a long period of time or very frequently.

###  When to use and not

### Publish Google spreadsheet
- Make sure the spreadsheet is *not* on Globe and is on bostonglobegraphics@gmail.com account
- Publish to the web: file -> publish to web
- Make public: blue share button (top right corner)  -> advanced -> change "private only you can access" to "anyone with the link"

In the address bar, grab the key:
...com/document/d/**1IiA5a5iCjbjOYvZVgPcjGzMy5PyfCzpPF-LnQdCdFI0**/edit

### Create a Jira ticket
Go to [Jira](http://jira.boston.com) and create a new issue
```
Project: Operations
Issue type: Cronjob
Summary: php to jsonp
Add watchers: mike.devlin

Description:
URL - http://private.boston.com/newsprojects/gs-to-json/fetch.php?key=[your-key]&gid=0&callback=onLoadData
Save output as [your-filename-date].jsonp
Result should be public
Run every [number] minutes
End on [date]
```

Replace the brackets with your information (and remove brackets). Here is an example:
```
URL - http://private.boston.com/newsprojects/gs-to-json/fetch.php?key=1H2HdDUR-JD2na4GJovw57WRJeI8U_jJ54YAeP1PwCFc&gid=0&callback=onLoadData
Save output as example-06-23-15.jsonp
Result should be public
Run every 30 minutes
End on 6/30/15
```

**Important**: Also, always make sure to test the url in the browser before submitting issue.

**Note**: If you are using a sheet in the spreadsheet other than the *main* one, you might have to replace `gid=0` in the URL with a different number. When you have the sheet open in the browser, you will see the `gid` value in the address bar.

### Load data in JavaScript file
When the cron job is setup, you will receive notice from Jira. The url to the data will most likely be `http://www.boston.com/partners/[your-filename-date].jsonp`.

In your js file, you will need to create a function to fetch the jsonp. If you are using jQuery, it can look like this:
```javascript
var fetchData = function(url) {
	$.ajax({
		url: url,
		dataType: 'jsonp',
		jsonpCallback: 'onLoadData',
		error: function() {
			// handle error here
		}
	});
};

// callback function (must be global to allow jsonp to work)
window.onLoadData = function(json) {
	// do your thing
};

// to run the function:
fetchData('http://www.boston.com/partners/[your-filename-date].jsonp');
```
