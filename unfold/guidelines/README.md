# Unfold: content guidelines

To add content to the story, reference the usage instructions below for each type of content.

## Defaults
All documents must contain a `hed`, `dek`, and `related` up top. Optionally, you can include an `image` which will be used for social sharing, not visible on the page, and a `section` tag, which defaults to *Metro*.

```
hed: Trump is president
dek: This will be a summary that explains how in two or three sentences.
related: http://www.bostonglobe.com
image: http://path/to/img.jpg 
```

## Subhed
Insert the `key: value` combination of `subhed: tk`.

```
subhed: How Trump made America great
```

## Text
Simply write text. Links can be included with standard html links (note: no quotations). Each new line creates a new graf.

```
In a landslide victory, Donald Trump will become the 45th president of the United States of America.

If you want a new paragraph, just make sure there is an empty line above like so.

There could be a <a href=http://bostonglobe.com>link</a> to something here.
```

## Image
There are 3 ways to use an image. **Only images hosted by the Globe** are allowed. Caption and credit are always optional.

1) Get the public url of an image:

```
{.image}
source: https://c.o0bg.com/rf/image_585w/Boston/2011-2020/2015/12/10/BostonGlobe.com/Business/Images/carmax-tweet.jpg
caption: Cars in a parking lot
credit: Joe Mahoney / Globe Staff
{}
```

2) If you directly publish from the methode **Images** folder, first you must portalPubBG the image. You must also find the date it was **CREATED**, and add a `date` field, including leading zeros.

```
{.image}
source: /Boston/Content/Politics/Images/05430749.jpg
date: 2016-07-18
{}
```

3) You can add the image to a WebGraphics folder, much like a graphic (but the size will be exactly as you insert it). *Best option for graphics team.*

```
{.image}
source: /Boston/Content/Metro/WebGraphics/2016/07/18/test.jpg
{}
```

If you want to have it swap out a mobile-friendly image, you can add the `mobile` property. It will swap at **500px**

```
{.image}
source: /Boston/Content/Metro/WebGraphics/2016/07/18/test-desktop.jpg
mobile: /Boston/Content/Metro/WebGraphics/2016/07/18/test-mobile.jpg
{}
```

## Graphic
Get the public url of a published iframe graphic OR MWB path to index.html file.

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

## Tweet
Get the embed code of a tweet. *You just need from `<blockquote to </blockquote>`, but everything is okay too.*

```
{.tweet}
embed: <blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Everybody is so busy with <a href="https://twitter.com/hashtag/PokemonGo?src=hash">#PokemonGo</a> that we don&#39;t even have a &#39;Song of the Summer&#39; this year</p>&mdash; Chiqui Esteban (@chiquiesteban) <a href="https://twitter.com/chiquiesteban/status/757293263015538689">July 24, 2016</a></blockquote>
{}
```
