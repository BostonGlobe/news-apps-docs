# Unfold: setup new story

Follow the steps below to setup a new developing story

## Create Doc
* Log in to the **bostonglobegraphics** gmail account
* In the `unfold` folder, make a copy of `unfold - TEMPLATE`
* Rename it to `unfold - some name`

## Share Doc
* Right click on the new doc and select **Get shareable link**

**Note:** If you share and edit from your Globe account, disable auto-caps by going to *Tools -> Preferences -> Automatically capitalize words (uncheck)*.

## Add Story to master list
* Open the `unfold - MASTER LIST` doc
* Create the following object below, under **[stories]** 

Example:
```
id: put-google-doc-id-here
year: 2016
month: 07
name: something-happened
```

## Notes when filling out the object:
* **id**: Grab the big chunk of random numbers and letters after the **document/d/** in the story Google Doc
* **year**: 4-digit year
* **month**: 2-digit with leading 0
* **name**: short, just letters and dashes instead of spaces

## Preview
Once the new contents are in the `unfold - MASTER LIST`, a new page will be created and updated every minute. If done correctly, the new story will show up on [the unfold internal page](http://unfold.bostonglobe.com).

## Disable
To stop updates and the ability to publish changes, simply remove the object from the `unfold - MASTER LIST`.

If you need to "delete" it from the public sphere, remove all the content (but leave the mandatory hed, dek, and [story] bits) and add `redirect: true` where the `hed` and `dek` are. When you publish again, it will have no content and will automatically go to the globe homepage.

## Remove paywall
Add `meter: false` to the top of google doc where `hed` and `dek` are.

## Errors 
If the preview doesn't look like it should, *or* the updated date is not within a minute or two of the real time, there is probably an issue with the google doc. If the preview doesn't match the doc content, simply scan through the doc from top to bottom and see where it differs. Then consult the [guidelines](../guidelines) to verify it is formatted properly. 
