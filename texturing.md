# Texturing

## UV unwrapping

References:

* [Blender Guru's Chair tutorial UV unwrapping](https://www.youtube.com/watch?v=XeBUfMKKZDo&list=PLjEaoINr3zgEL9UjPTLWQhLFAK7wVaRMR&index=8&t=0s)
* [Blender Guru's Anvil tutorial UV unwrapping](https://www.youtube.com/watch?v=scPSP_U858k&list=PLjEaoINr3zgHJVJF3T3CFUAZ6z11jKg6a&t=0s)

Time-saver: `Smart UV Project` does wonders for some meshes, mostly when there are no rounded parts on it.

### Checkerboard

It is useful to check that the UV unwrapping does not result in too much stretching of the texture using a checkerboard texture.

To activate:

* Click on the circle button on the right-hand side of principled shader's `Base color` field.
* Select `Checker texture`.
* adjust scale as suitable.


Alternative:

* In the image editor, create new image, selecting `UV Grid` Generated type option.
* Edit the material to use the new image instead of `Base color`.


### UV stretch check

In the UV image editor's side `View` menu, activate `Stretch` overlay in order to see a heat map of the stretching.

## Sculpt details and bake them into normals

Reference: [Anvil tutorial](https://www.youtube.com/watch?v=ywSq0bSYLWI&list=PLjEaoINr3zgHJVJF3T3CFUAZ6z11jKg6a&index=7).


## Apply different materials to different parts of a mesh


### Straight split

In case different portions of the mesh need to be applied a different material, create two materials, and click on "assign" with the relevant portion of the mesh selected in `edit mode`.

### gradual material shift

More often, it is desirable to have a managed transition between both materials, or to get a mix between both (think: rust over metal). 

In this case, a mix shader should combine both materials, using either noise + colorRamp or texture paint should be used as a masking factor.

Reference: [Anvil tutorial - Texturing part 2](https://www.youtube.com/watch?v=nx8Qq7kNKK8&list=PLjEaoINr3zgHJVJF3T3CFUAZ6z11jKg6a&index=10).
