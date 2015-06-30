# Image resizer

If you aren't using Methode for images, here is a way to create optimized responsive images from command line.

### Requirements
[GraphicsMagick](http://www.graphicsmagick.org)

``` brew install graphicsmagick ```

### Setup
Store this function so you can use it from any directory:

With plain old bash in terminal, put the following snippet in your ```.bashrc``` file:

```
image-resizer() {
	gm mogrify -output-directory $2 -create-directories -filter TRIANGLE -thumbnail $1 -unsharp 0.25x0.25+8+0.065 -quality 75 -interlace Line -define jpeg:fancy-upsampling=false -strip *.{jpg,png}
	echo '-- DONE --'
}
```

With fish, create a new function file (in `.config/fish/functions/image-resizer.fish`):

```
function imager
	gm mogrify -output-directory $argv[2] -create-directories -filter TRIANGLE -thumbnail $argv[1] -unsharp 0.25x0.25+8+0.065 -quality 75 -interlace Line -define jpeg:fancy-upsampling=false -strip *.{jpg,png}
	echo '-- DONE --'
end
```

### Run
``` image-resizer [size] [output directory] ```

Navigate to the directory which contains all your images and run the command. For example:

``` image-resizer 1280 ../output ```

