# HDRI

## Usage

* Activate `Use nodes` for the world shading.
* Add an environment texture node, and load the `.hdr` file in there.
* It can be worth keeping the background node in order to remain able to manage the strength of the lighting. Plug the environment texture to it.
* If rotation is necessary:
  * plug in a `Mapping` node connected to `Generated` `Texture coordinates` into the vector input of the environment texture. <kbd>Ctrl</kbd> + <kbd>t</kbd> with Node Wrangler addon enabled.
  * set suitable rotation


## Creation

Resources:

* [How to Create Your Own HDR Environment Maps](http://blog.gregzaal.com/2016/03/16/make-your-own-hdri/)
* [What Makes a Good HDRI and How to Use It Correctly](http://blog.gregzaal.com/2016/02/23/what-makes-good-hdri/): update of the previous articles with more pro advice


### Night sky star map using NASA data

NASA provides a map of the sky in this page: [Deep star maps](https://svs.gsfc.nasa.gov/3895).

Credit: 

	NASA/Goddard Space Flight Center Scientific Visualization Studio. Constellation figures based on those developed for the IAU by Alan MacRobert of Sky and Telescope magazine (Roger Sinnott and Rick Fienberg). 

How to use as HDRI:

* Download **celestial coordinates** version of the star map (tif file).
* Convert to hdri format using command `convert` (linux / imageMagick):

    convert starmap_16k.tif  starmap_16k.hdr
    

* Profit!

For the higher resolution versinos of the sky map, imageMagick might throw the following error:

```
convert-im6.q16: width or height exceeds limit `starmap_16k.tif' @ error/cache.c/OpenPixelCache/3912.
convert-im6.q16: no images defined `starmap_16k.hdr' @ error/convert.c/ConvertImageCommand/3258.
```

In such case, limits should be increased in the `policy.xml` config file ([source](https://www.imagemagick.org/discourse-server/viewtopic.php?t=31438) with details).

Both height and memory limits might need to be increased. Adapt setup according to machine's power.

Location in debian buster: `/etc/ImageMagick-6/policy.xml`

```
  <policy domain="resource" name="temporary-path" value="/home/tmp"/>
  <policy domain="resource" name="memory" value="2GiB"/>
  <policy domain="resource" name="map" value="2GiB"/>
  <policy domain="resource" name="width" value="50KP"/>
  <policy domain="resource" name="height" value="50KP"/>
  <!-- <policy domain="resource" name="list-length" value="128"/> -->
  <policy domain="resource" name="area" value="1GiB"/>
  <policy domain="resource" name="disk" value="3GiB"/>
```

N.B. Using the `.tif` file directly as environment texture works in blender, but the brightness is way better in hdri format.
