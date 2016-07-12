# Unfold: content guidelines

To add content to the story, reference the usage instructions below for each type of content.

## Defaults
All documents must contain a `hed` and `dek` up top. Optionally, you can include an `image` which will be used for social sharing, not visible on the page.

Example:
```
hed: Trump is president
dek: This will be a summary that explains how in two or three sentences.
image: http://path/to/img.jpg 
```

## Subhed
Insert the `key: value` combination of `subhed: tk`.

Example:
```
subhed: How Trump made America great
```

## Text
Simply write text. Links can be included with standard html links (note: no quotations)

Example:
```
In a landslide victory, Donald Trump will become the 45th president of the United States of America.

If you want a new paragraph, just make sure there is an empty line above like so.

There could be a <a href=http://bostonglobe.com>link</a> to something here.
```

## Image
Get the public url of an image published from Methode OR MWB path to image. Caption and credits are optional and can be left out.

Example: 
```
{.image}
source: https://c.o0bg.com/rf/image_585w/Boston/2011-2020/2015/12/10/BostonGlobe.com/Business/Images/carmax-tweet.jpg
caption: Cars in a parking lot
credit: Joe Mahoney / Globe Staff
{}
```

## Graphic
Get the public url of a published iframe graphic OR MWB path to index.html file.

Example:
```
{.graphic}
source: /Boston/Content/Metro/WebGraphics/2016/04/03school_lookup/index.html
{}
```

## Video
Get the id of a brightcove video
```
{.video}
id: 5012569570001
{}
```
