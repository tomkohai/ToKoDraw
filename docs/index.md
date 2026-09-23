---
layout: default
title: ToKoDraw
---

![Animation](/assets/gifs/AnimSkull_Sign.gif)


# Presentation

  ToKoDraw is a Blender addon designed to extend and streamline the Texture Paint workflow. It is particularly suited for artists working in stylized NPR emission, but it also allows painting stylized normal maps directly, providing depth through BSDF. It includes a dedicated normal map palette and offers a simple switch between emission and BSDF through the Render Switch, making it easy to move from flat stylized rendering to a relief‑based look.



  It aims to bring into Blender a drawing and animation workflow inspired by traditional 2D tools such as Krita. The goal is to offer a familiar, painter‑friendly environment inside Blender, so artists accustomed to classic 2D software can feel at home with a workflow that matches the way they naturally draw and animate. It acts as a bridge between 2D and 3D practices, expanding Blender’s accessibility without replacing existing tools like Grease Pencil.



  It is under active development and aims to bring Blender closer to a Krita / Photoshop‑like workflow, while remaining 100% native to Blender. It works in both Layout and Texture Paint Mode, and its internal architecture relies on node groups (NG) that separate and organize layers, providing a clean and non-destructive layer stack with advanced masking tools.



  fully compatible with Blender versions <strong>4.5 through 5.2</strong>.



## Support & Downloads

<p>
  ToKoDraw is a free addon developed by <strong>ToKohai</strong> within 
  <strong>Enjoy Graphix</strong>. You can download the addon from the official platforms,
  and support the project if you wish to help its development and future features.
</p>

<p><strong>Download the addon:</strong></p>
<div>
  <a class="download-btn" href="https://tomkohai.github.io/ToKoDraw/download.html" target="_blank"> 
    Download Page
  </a>
</div>

<p><strong>How you can contribute to Tokodraw’s development</strong></p>
<div>
  <a class="support-btn" href="https://tomkohai.github.io/ToKoDraw/support.html" target="_blank">
    Support Tokodraw
  </a>
</div>

<p><strong>You can also contribute your ideas here</strong></p>
<div>
  <a class="discord-btn" href="https://discord.gg/HAfbG6YKQ5" target="_blank">
    Join the Community
  </a>
</div>




## Working Modes
This addon provides several modes to adapt to the artist’s workflow:

### Standard 3D Painting
Direct painting on 3D objects in the viewport, similar to Texture Paint, but with a full layer system.

### LineArt CamView
A dedicated mode for painting a 3D object with its line art oriented correctly, unlike the standard 3D view where line art always faces the camera. This mode allows stylized painting without losing contours, with a control panel to orient the object.

### Canvas Mode (2D)
Painting on a 2D canvas integrated into Blender.  
When creating a canvas, the user can choose:
- Horizontal  
- Vertical  
- Custom Size  

This mode is ideal for creating 2D elements (FX, backgrounds, props) directly inside Blender, then integrating them into the 3D scene.

## Dynamic Layer System
Layer system inspired by 2D software:
- add or remove layers anywhere in the stack,  
- choose the canvas size at creation,  
- freely reorder layers,  
- each layer includes: Hide/Show, Alpha Lock, Layer Lock, Rename, Duplicate and UV Transform (animatable).

Layers are stored inside **node groups**, which ensures:
- full compatibility with the Shader Editor,  
- the ability to add custom nodes,  
- a non‑destructive workflow,  
- a clean separation between layers and the final shader.

**Normal Layer**  
When adding a new layer, the user can choose to create a normal map layer. After assigning the image to the normal texture node through the BSDF normal map settings, they can paint normals directly on the visible layer to control the colors used or benefit from real‑time rendering.

## Merge 
Merging system based on checkbox selection.
This mode allows you to merge any layers, even when they are not consecutive. This system makes it easy to finalize a painting while keeping the file lightweight and maintaining a clear layer hierarchy. Improvements to the selective merge system are currently under development to further optimize rendering and eliminate artifacts.

**Image Source**  
Manages the layer’s image directly without opening the Image Editor or Shader Editor. Users can create, import, replace, rename, or remove images, and also supports image sequences for animated workflows. The goal is to centralize texture management inside the layer panel.


**Transform**  
Moves, scales, or rotates a layer by modifying its UV mapping. Instead of editing the object or its UVs, apply transformations directly to the layer, making it easy to reposition painted elements or adjust stylized details. Since these transformations can be animated, they provide a simple way to add motion to a layer while remaining fully integrated into the shader.


## Dynamic Animation of Settings
All layer parameters can be animated directly from the panel. A simple right‑click on any setting — opacity or transformations — inserts a **keyframe** just like any native Blender property.


A dedicated frame‑by‑frame animation mode is planned for future development, designed to deliver perfect 2D rendering directly inside Blender.
Its goal is to let artists combine stylized painting, animated layers, and NPR rendering within a coherent, fluid, fully native workflow.

## Development & Support
ToKoDraw is evolving constantly. **Upcoming updates** aim to expand **drawing, painting, and selection tools**, including line, rectangle, ellipse, lasso, and **pixel selection movement**.  
The **layer system** will also grow with **grouping, clipping masks, and filter masks**, bringing it closer to full 2D software capabilities.  
A **frame‑by‑frame animation mode** is planned, along with **improved transform tools** for animating layers, line art, and stylized elements more smoothly.

**Developed by Thomas Chauveau (To Kohai)**. The addon is free and intends to remain free.  
**A support link will be added soon for users wishing to contribute through donations.**
