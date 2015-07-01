# Image resizer

If you aren't using Methode for images, here is a way to create optimized responsive images from command line.

### Requirements
[GraphicsMagick](http://www.graphicsmagick.org)

``` brew install graphicsmagick ```

### Setup
Store this function so you can use it from any directory:

With fish shell, create a new function file (in `.config/fish/functions/image-resizer.fish`):

```
function image-resizer
	set size $argv[1]
	set output $argv[2]
	mkdir $output
	for i in *.jpg
		set newfile $output/(basename $i .jpg)_$size.jpg
	    gm convert -filter TRIANGLE -thumbnail $size -unsharp 0.25x0.25+8+0.065 -quality 75 -interlace Line -define jpeg:fancy-upsampling=false -strip $i $newfile
	end
	for i in *.png
		set newfile $output/(basename $i .png)_$size.png
	    gm convert -filter TRIANGLE -thumbnail $size -unsharp 0.25x0.25+8+0.065 -quality 75 -interlace Line -define jpeg:fancy-upsampling=false -strip $i $newfile
	end
	echo '-- images resized and optimized --'
end
```

### Run
``` image-resizer [size] [output directory] ```

Navigate to the directory which contains all your images and run the command. For example:

``` image-resizer 1280 ../output ```

