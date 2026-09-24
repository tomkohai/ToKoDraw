---
title: Layers
description: Learn how ToKoDraw layers work in Blender texture painting: create, organize, blend and merge non-destructive layers, inspired by Krita.
---

# ToKoDraw Layer System

ToKoDraw brings a full **layer system to Blender's Texture Paint mode**, inspired by Krita and Photoshop. Each layer stays non-destructive, independently editable, and stackable — with smart merging and direct normal map painting.


![ToKoDraw layer stack shown as node groups in the Shader Editor](/assets/tuto/layer/shaderedit.gif)

## How layers work

In ToKoDraw, each layer is represented inside the material as an individual **node group**, stacked one above another. These node groups do not mix colors together during the layer stage: each layer preserves its own pixel data, opacity, and blending parameters independently.

The actual color mixing only happens later in the shader, where the stacked node groups are combined to produce the final material output.

This architecture ensures:

- precise control over each layer,
- non-destructive editing,
- predictable blending behavior,
- and a clean separation between layer compositing and shader rendering.

## The Layer List

![The ToKoDraw layer list panel with opacity slider](/assets/tuto/layer/list.png)


### Opacity & Hard Alpha

![HardAlpha and opacity slide in the ToKoDraw sider panel](/assets/tuto/layer/opalpha.png)

*Opacity* controls the opacity of the active layer.

*Hard Alpha* controls the hardness of the alpha edges of painted pixels. It helps produce cleaner edges when the canvas is hidden.

![Hard Alpha producing cleaner edges on painted pixels](/assets/tuto/layer/alpha.gif)


## Layer stack controls

![Add, remove, reorder and merge buttons of the ToKoDraw layer panel](/assets/tuto/layer/layertools.png)

- **Add Layer**  
Creates a new layer in the stack, based on the current active layer position, with an optional custom pixel size.

- **Trash / Remove Layer**  
Deletes the active layer from the stack.

- **Reorder Layers**  
Allows changing the order of layers in the stack.
The layer order directly affects how pixels are blended.

![Reordering layers in the ToKoDraw stack](/assets/tuto/layer/reorder.gif)


- **Merge Selected Layers**  
Merges the layers that have their Merge checkbox enabled, whether they are consecutive or not.

![Merging non-consecutive layers with the merge checkbox](/assets/tuto/layer/merge.gif)

## Per-layer buttons

Each layer in the list displays:

- **Merge Checkbox**
Allows selecting layers to merge (whether consecutive or not).

- **Hide / Show**
Shows or hides the layer while preserving its defined opacity.

- **Lock Alpha**
Enables or disables alpha protection.
Prevents brushes from painting outside the pixels already present on the active layer.

- **Lock Layer**
Prevents the layer from being selected in the list, avoiding accidental modifications.

- **Duplicate Layer**
Duplicates the active layer and its pixels into a new layer.

- **Rename Layer**
Renames the layer’s label.

- **Right Arrow**
Opens the layer Settings.

### Layer Settings

![The ToKoDraw layer settings panel](/assets/tuto/layer/settings.png)

#### Image source
    
The Image Source panel provides full control over the image assigned to the layer: the complete list of available images, options to create, remove, rename, or import an image or an image sequence, and all relevant texture settings — interpolation, projection, extension, color and alpha handling. Source Settings also allow switching between file-based and generated images, with the ability to resize the image's pixel dimensions.

⚠️ Some parameters — especially projection, extension or image generation — can lead to loss of painted pixels if modified after painting. Adjust them with care.


![The Image Source panel for a ToKoDraw layer](/assets/tuto/layer/source.png)
      
#### Transform
    
The Transform panel adjusts the UV mapping of the layer's image — location, rotation and scale. These operations modify how the image is projected onto the canvas, without altering the underlying pixels themselves.

A dedicated system for true pixel-based transformations (moving painted pixels directly, without UVs or image projection) is in development.
    
![The Transform panel for layer UV mapping](/assets/tuto/layer/transform.png)

![Animating a layer transform in real time](/assets/tuto/layer/transform.gif)

💡 For better accuracy when using Transform on a layer, consider adjusting Blender's Unit Scale to 0.5.

![Adjusting Blender Unit Scale for accurate layer transforms](/assets/tuto/layer/unit.gif)



## Normal Map
*Inactive when the material is first created.*

![Inactive normal map button](/assets/tuto/layer/normal.png)


### Normal Map Handpaint in ToKoDraw

The Normal Map Handpaint mode activates automatically when creating a normal map layer. From that moment, the normal depth painting palette becomes available in the palette (brush tools → palette), allowing you to paint relief information directly on the canvas. The generated normal map image is immediately assigned to the Normal Map node in the shader, ensuring correct OpenGL interpretation, while remaining active inside the layer so you can paint on it directly and in real time.

![Painting a stylized normal map in real time](/assets/tuto/layer/process.gif)

### Normal Settings

Open the layer arrow to access the normal map settings.

**Image settings** (active only when the normal map layer is selected): delete, rename, import or select an existing image.

**UV Mapping** — translate, rotate and scale the normal map image directly on the canvas. These transformations adjust the position of the painted relief without modifying the painting itself.

**Normal Map Node** — controls the strength, the Tangent/Object space, and the stylization of the relief interpretation.

**Normal Mapping Node** — controls how the light reacts to the relief and enables dynamic shading even in a 2D workflow.

**BSDF Shader (Metallic / Roughness / IOR)** — completes the pipeline by refining the physical or stylized behavior of the final material, complementing the painted relief.

![Normal map settings controlling strength, space and BSDF response](/assets/tuto/tools/normal1.gif)

## Next steps

- See how to merge layers non-destructively
- Discover the painting tools and palettes
- Change your working mode: 3D, LineArt CamView or Canvas

## FAQ

### Can I merge non-consecutive layers in ToKoDraw?
Yes — enable the Merge checkbox on any layers in the stack and click Merge Selected Layers, even if they are not adjacent.

### Does ToKoDraw modify my painted pixels?
No — transforms like move, rotate and scale adjust the layer's UV mapping without altering the underlying pixels.

### How do I paint a normal map in ToKoDraw?
Create a normal map layer: the Normal Map Handpaint mode activates automatically, the depth palette appears, and the image is assigned to the shader's Normal Map node in real time.