# Liquids

Material:

* Just like glass, set transmission to 1, and use pure white color.
* Decrease the indice of refraction IOR down to 1.33 (1.31 for boiling liquid) - lookup correct value.	

* Add Volume absorption in case the liquid is colored and not fully transparent.

## In a glass

Because of a bug in blender, water should slightly overlap the glass material. Otherwise, refraction is incorrect (thin layer of air betwen the glass and the liquid).


## Troubleshooting

Make sure that face orientation is OK (mesh not inside out).
