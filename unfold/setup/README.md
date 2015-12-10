# Unfold: setup new story

Follow the steps below to setup a new developing story

## Create Doc
* Log in to the **bostonglobegraphics** gmail account
* In the `unfold` folder, create a new Document
* Rename it
* Copy over the content from the *unfold template* Doc

## Share Doc
* Click the **Share** button the top right, then **Advanced**
* Where it says "Private - Only you can access" click **Change**
* Select **On - Anyone with the link**
* Click **Save** and then **Done** on the next screen

## Publish Doc
* Click **File > Publish to the web**
* Click **Publish**

## Add Story to master list
* In the `unfold` folder, open the *Master List* doc
* Copy and paste the object below under **[stories]** 

Example:
```
id: 11wCzzpOOVg5g5o_MfAiP97mX2W_Cskyhv3cOZPmKoUM
year: 2015
month: 04
name: something-happened
```

## Notes when filling out the object:
* **id**: Grab the big chunk of random numbers and letters after the **document/d/** in the story Google Doc
* **year**: 4-digit year
* **month**: 2-digit with leading 0
* **name**: short, just letters and dashes instead of spaces

## Preview
Once the new object is in the *Master List*, the new page will be created and updated every minute. If done right, the new story will show up at http://dev.apps.bostonglobe.com/sandbox/unfold/. This will have a link to the Google Doc and the internal story. The internal story url will be http://dev.apps.bostonglobe.com/developing-story/year-month-name, and the public url will be https://apps.bostonglobe.com/developing-story/year-month-name.