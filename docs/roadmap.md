---
title: Roadmap
description: ToKoDraw development roadmap: upcoming features, planned improvements and future releases of the Blender texture painting addon.
---


## Roadmap — Post‑V1 Development Path 
The following roadmap outlines the planned evolution of ToKoDraw after the V1.0 release.
It follows the approximate order in which features are expected to be developed, starting with incremental V1.x updates and gradually moving toward the long‑term V2 vision.

**V1.1 — Layer Controls & Image Source Improvements**
- Per‑Layer Opacity Slider  
The opacity slider will remain in the ToolList, but an additional per‑layer slider will be added inside each layer’s Settings panel.
This local slider is intended specifically for keyframe animation, preventing the current issue where the shared global slider becomes locked once a keyframe is added (forcing Replace instead of Insert when switching layers).
The same approach will be applied to Hard Alpha, which will also be available inside the layer Settings for animation purposes.

- Save Button in Image Source  
In addition to the file path, a dedicated Save Image button will be added to the Image Source panel for quick export of painted textures.

- Right‑Click Settings Menu for Layers  
Continuation of the floating settings menu accessible via right‑click on a layer.
A dedicated button in the Tools panel will also open this menu without requiring a right‑click.

**V1.2 — Filters & Transform Enhancements**

- Tone / Color Filters & Blur/Sharpen  
Introduction of a filter system for per‑layer adjustments:
tone, color correction, blur, sharpen, and other basic FX.

- Right‑Click Transform Tools  
Adding transform options directly via right‑click.
Exploration of improved transform nodes beyond the standard Mapping node to achieve more intuitive control.

- Pixel‑Based Transform System (Early Work)  
Initial groundwork for a system that moves painted pixels directly, without relying on UVs or image projection.
This will eventually allow drag‑and‑drop pixel movement, copy/paste between layers, and keyframe animation of pixel transforms.

**V1.3 — Blending & FX Pipeline**

- Blending Node (Experimental)  
Investigation of a blending system between layers despite the stacked architecture.
This requires careful design to avoid breaking the NBAdd chain and the straight‑alpha pipeline.

- FX Effects (Glow, Blur, etc.)  
Introduction of basic FX nodes that can be applied per layer or globally.

**V1.4 — Drawing & Selection Tools**

A new Drawing Toolbar will be added, containing:

- Drawing Tools  
Line, rectangle, circle, and other basic shapes.

- Selection Tools  
Rectangle, ellipse, free selection, plus fill tools with painted‑pixel edge detection.

- Pixel Movement Tools  
Drag‑and‑drop pixel displacement inside a layer,
copy/paste to another layer or a new layer,
and transform pixels without touching UVs or the image source.
Potential support for keyframed pixel movement.

**V1.5 — Animation Tools & Brush Engine**

- Line Art Animation Panel  
A small dedicated panel for animating Grease Pencil line art, including noise, motion, and timing controls.

**V1.6**
- Brush Engine Improvements  
Creation of optimized brush packs (pencil, paint, texture brushes) and refinement of brush behavior.

**V1.7 to 9 — Layer Masks & Layer Groups (Long‑Term Work)**

- Layer Masks  
Clipping, color masks, transform masks, filter masks, etc.
This requires deep changes to the internal pipeline.

- Layer Groups  
Ability to create groups inside the layer stack, reorder them, and move layers inside/outside groups.
Internally, this may involve generating a node group that combines selected layers and reintegrates the output into the NBAdd chain.
This is a heavy feature and will be developed over a longer period to ensure stability.

## V2 — Advanced Animation & Integrated 2D Studio Vision

The long‑term goal is to transform ToKoDraw into a full 2D animation studio inside Blender, combining 2D painting, 3D scenes, camera work, and animation tools.

*Planned features include:*

- Frame‑by‑Frame Drawing Panel  
Timeline, onion skin, simple animation tools, and a dedicated frame‑by‑frame workflow.

- Scene Animation Integration  
Animation of objects, layers, lights, cameras, and scene elements directly from the Canvas workflow.

- Gamepad Camera Controller  
Already in prototype: real‑time camera control using a gamepad for cinematic shots.

## Long‑Term Vision
ToKoDraw aims to become a hybrid 2D/3D animation environment inside Blender.
Artists will be able to:

paint 3D objects for backgrounds or props,

animate planes or layers as dynamic backgrounds,

create camera shots directly inside Blender,

add a Canvas on top of the shot and paint a character in 2D,

animate that character frame‑by‑frame while the canvas moves with the camera.

ToKoDraw is not meant to replace Blender’s existing 2D tools such as Grease Pencil, but to complement them with a workflow inspired by traditional 2D drawing and animation software like Krita, OpenToonz, and TVPaint. The goal is to bring a familiar, painter‑friendly environment directly inside Blender, so artists coming from classic 2D pipelines can work the way they are used to while gradually discovering Blender’s 3D environment through TKD. This creates a natural bridge between 2D and 3D practices, making Blender more accessible to illustrators and animators who prefer traditional 2D workflows, without reinventing what already exists.
