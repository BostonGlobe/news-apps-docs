# Spreadsheet cron job
Steps for setting up a cron job that will automatically convert a Google spreadsheet to jsonp at regular intervals.

### Create a Jira ticket
```
Project: operations
Issue type: cron job
Summary: php to jsonp
Add watchers: Mike Devlin

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

**Note**: If you are using a sheet in the spreadsheet other than *main* one, you might have to replace `gid=0` in the URL with a different number. When you have the sheet open in the browser, you will see the `gid` value in the address bar.

### Load data in JavaScript file
When the cron job is setup, you will receive notice from Jira. The url to the data will most likely be `http://www.boston.com/partners/[your-filename-date].jsonp`.

In your js file, you will need to create a function to fetch the jsonp. If you are using jQuery, it can look like this:
```
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