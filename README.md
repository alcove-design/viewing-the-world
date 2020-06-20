# viewing-the-world

Personal knowledge base about blender and the 3D world.

Studying the 3D creation suite [Blender](https://www.blender.org/) is teaching me a lot not only about generating digital content, but also about physics, vision and photography.

This repository is used to keep track of the learnings.

Status: just getting started.


## Where to learn

I somehow got started using youtube videos, even though I usually prefer other medium to follow lessons. It's actually going very well.

Andrew Price - aka Blender Guru - is just amazing. He shares his experience openly, has a broad visual arts culture, provides very relevant and precise information, and the flow of his youtube videos is perfect. Strongly recommended.

Find him on [youtube](https://www.youtube.com/user/AndrewPPrice) and on [his website](blenderguru.com).

[Blender fundamentals](https://www.youtube.com/watch?list=PLa1F2ddGya_-UvuAqHAksYnB0qL9yWDO6&v=MF1qEhBSfq4) might also be a good source of information.

[Photorealism, explained](https://www.youtube.com/watch?v=R1-Ef54uTeU).


## Modelling

Good topology - Keeping quads: [this video guide](https://www.youtube.com/watch?v=HGL6QpVRyXk).

Procedural modelling addon: [Sverchok](http://nikitron.cc.ua/sverchok_en.html).



## Materials

### Texturing

C.f. [texturing.md](texturing.md).

### Liquids

C.f. [liquids.md](liquids.md).

### Procedural shading

Tip to obtain a smooth fall-off: [here](https://youtu.be/3UWHKtKsIbU?t=4566).

## Lighting

Useful setup for indoor / artificial light settings: Three point lighting setup. Source: [Blender 2.8: Getting started with EEVEE: Lights, Shadows, Shading, Reflections, Skies and HDRIs](https://www.youtube.com/watch?v=aJlk7n49m6Q&list=PLda3VoSoc_TRuNB-5fhzPzT0mBfJhVW-i&index=5&t=0s)

[HDRI generation](hdri.md).

## Composition

3 stages:

* Focal element
  * Saturation
  * Contrast
  * Camera Focus
  * Motion
  * Faces or figures
  * Influencers
    * Guiding lines
    * Framing
    * Geometry
* Structure
  * Rule of thirds
  * Golden ratio
  * Pyramid
  * Symmetry
  * Full frame
* Balance
	Visual weight management, using size, high contrast, saturation, faces, figures.


## Post-processing

To have a glow effect in cycles, add in a `glare` node in the compositing ([source](https://youtu.be/Tu3U6wD7lu4?t=70)), then play with the options. `Fog glow` is probably a better start than the default `streaks` mode.


## Rendering

### Denoising

Steps to activate the AI denoiser:

1. In 'View layer properties' panel, activate `Passes > Data > Denoising data`.
2. Perform one render.
3. In the compositing tab, activate `Use nodes`.
4. Add a Denoise node, plug in `Noisy Image`, `Denoising Normal` adn `Denoising Albedo` from the `Render layer` node, connect `Image` output to the `Composite` node.

Voilà!

### Evee


### Cycles


## Blender usage

### Camera

To see where the camera focuses (depth of field), activate `limits` option in Camera's `Viewport Display` settings.


### Managing files

### Shortcuts

### Interface customization

