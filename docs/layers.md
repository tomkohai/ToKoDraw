![Layers](/assets/tuto/layer/shaderedit.gif)

## **Introduction to Layers**

In ToKoDraw, each layer is represented inside the material as an individual node group, stacked one above another.
These node groups do not mix colors together during the layer stage: each layer preserves its own pixel data, opacity, and blending parameters independently.

The actual color mixing only happens later in the shader, where the stacked node groups are combined to produce the final material output.

This architecture ensures:

- precise control over each layer,

- non‑destructive editing,

- predictable blending behavior,

- and a clean separation between layer compositing and shader rendering.

  
## **Layer List**

![Layers](/assets/tuto/layer/list.png)



**Slider**
![Layers](/assets/tuto/layer/opalpha.png)

*Opacity*
Controls the opacity of the active layer.

*Hard Alpha*
Controls the hardness of the alpha edges of painted pixels.
Helps produce cleaner edges when the canvas is hidden.

![Layers](/assets/tuto/layer/alpha.gif)


## Global controls

![Layers](/assets/tuto/layer/layertools.png)

- **Add Layer**  
Creates a new layer in the stack, based on the current active layer position, with an optional custom pixel size.

- **Trash / Remove Layer**  
Deletes the active layer from the stack.

- **Reorder Layers**  
Allows changing the order of layers in the stack.
The layer order directly affects how pixels are blended.

![Layers](/assets/tuto/layer/reorder.gif)


- **Merge Selected Layers**  
Merges the layers that have their Merge checkbox enabled, whether they are consecutive or not.

![Layers](/assets/tuto/layer/merge.gif)

## Each layer displays:

![Layers](/assets/tuto/layer/layer.png)

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

![Layers](/assets/tuto/layer/settings.png)

  - *Image source*
    
The Image Source panel provides full control over the image assigned to the layer. It includes the complete list of available images, along with options to create a new image, remove the current one, rename it, or import an external image or an image sequence. The panel also exposes all relevant texture settings, such as interpolation, projection, extension, color, and alpha handling. Additional Source Settings allow switching between file‑based images and generated images, with the ability to resize the image’s pixel dimensions when needed. However, some of these parameters—especially those affecting projection, extension, or image generation—can lead to loss of painted pixels if modified after painting has already been done, so they should be adjusted with care.

![Layers](/assets/tuto/layer/source.png)
      
  - *Transform*
    
The Transform panel allows you to adjust the UV mapping of the layer’s image, including location, rotation, and scale. These operations modify how the image is projected onto the canvas, without altering the underlying pixels themselves. UV transforms are useful for repositioning or orienting a texture, but they remain limited to UV-space manipulation. A dedicated system for true pixel‑based transformations (moving the painted pixels directly, without relying on UVs or image projection) is currently in development and will provide more intuitive control for hand‑painted layers.
    
![Layers](/assets/tuto/layer/transform.png)

![Layers](/assets/tuto/layer/transform.gif)

For better accuracy when using Transform on a layer, consider adjusting Blender’s Unit Scale to 0.5.

![Layers](/assets/tuto/layer/unit.gif)



## **Normal Map**

![Layers](/assets/tuto/layer/normal.png)

*Inactive when the material is first created.*

**Normal Map Handpaint in ToKoDraw**
The Normal Map Handpaint mode activates automatically when creating a normal map layer. From that moment, the normal depth painting palette becomes available in the palette (brush tools → palette), allowing you to paint relief information directly on the canvas. The generated normal map image is immediately assigned to the Normal Map node in the shader, ensuring correct OpenGL interpretation, while remaining active inside the layer so you can paint on it directly and in real time.

![Layers](/assets/tuto/layer/process.gif)

## Normal Settings (via the layer arrow)

**Image settings**

- Delete the image

- Rename the image

- Import an image

- Select an existing image

This panel becomes active only when the normal map layer is selected.

**UV Mapping**
Allows you to transform the normal map image directly on the canvas:

- Translate

- Rotate

- Scale

These transformations let you adjust the position of the painted relief without modifying the painting itself.


**Normal Map Node**

- Controls the strength

- Controls the Tangent/Object space

- Allows stylization of the relief interpretation

**Normal Mapping Node**

- Controls how the light reacts to the relief

- Enables dynamic shading even in a 2D workflow

**BSDF Shader (Metallic / Roughness / IOR)**

The BSDF completes the pipeline by allowing refinement of:

- Metallic

- Roughness

- IOR

These parameters influence the physical or stylized behavior of the final material, complementing the painted relief.

![Layers](/assets/tuto/tools/normal1.gif)
