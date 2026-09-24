---
title: Tools
description: Overview of ToKoDraw painting tools for Blender: brushes, smart merge, stylized normal map tools and layer management utilities.
---


## Tools 


**Blender Mode Selector**

![Tools](/assets/tuto/tools/blendmode.png)

The panel includes a synchronized list of Blender modes, allowing fast switching between Object Mode, Edit Mode, Sculpt Mode, Texture Paint, and others. Changing the mode from the Tools panel updates Blender instantly, ensuring seamless workflow transitions without navigating Blender’s default mode selector.



![Tools](/assets/tuto/tools/toolbar.png)

**Backface Culling** ![Backicon](/assets/tuto/tools/Backicon.png){: .picto-inline } 

Backface Culling can be enabled directly from the panel. While primarily used as a viewport optimization, it also helps clarify the visible painting surface by hiding back‑facing polygons, which can be useful when painting or outlining complex meshes.

 **Render Switch** ![Tools](/assets/tuto/tools/rendericon.png){: .picto-inline }

The Render Switch toggles the material between BSDF shading and Emission shading with a single click. This is especially useful when previewing painted textures, isolating color information, or working in 2D canvas mode where lighting can interfere with the final look.

## Outline System ![Tools](/assets/tuto/tools/outlineicon.png){: .picto-inline }

The Outline tool automatically adds a clean outline mesh to the painted object and opens the floating Outline Settings panel. Once the outline has been created, pressing the button again simply reopens the settings instead of generating a new outline.

*Outline Settings include:*

- Thickness

- Offset

- Flip Normal

- Alpha Slide

- Hide / Show

- Delete

![Tools](/assets/tuto/tools/outline.gif)


## Line Art System ![Tools](/assets/tuto/tools/lineicon.png){: .picto-inline }

The Line Art tool automatically adds a Grease Pencil Line Art object linked to the painted mesh and opens the floating Line Art Settings panel. As with the outline system, pressing the button again only reopens the settings without creating additional line‑art objects.

*Line Art Settings include:*

- Source / Target

- Radius

- Opacity Threshold

- Edge Mark

- Intersection

- Crease

- Delete

![Tools](/assets/tuto/tools/lineart.gif)


The Tools panel also provides quick access to several workflow helpers:

**CamView** ![Tools](/assets/tuto/tools/camicon.png){: .picto-inline }

 — switches to the dedicated 2D camera view used for painting.

**Transform Panel** ![Tools](/assets/tuto/tools/transpicon.png){: .picto-inline }

 — opens the object transform controls (move, rotate, scale).

**Frame Selected** ![Tools](/assets/tuto/tools/frameicon.png){: .picto-inline }

 — centers the view on the selected object in the scene.


## Animating Settings and Layer Parameters

All settings in the Tools panel, as well as layer parameters and other controls, can be animated directly through right‑click keyframing. Any slider, toggle, or numeric field supports keyframe insertion via Right‑Click → Insert Keyframe. Once keyframes are added, the animation curves can be edited in Blender’s Graph Editor, allowing full control over timing, interpolation, and transitions. This makes it possible to animate opacity changes, outline thickness, line‑art parameters, camera transforms, and even layer operations, enabling advanced animated workflows directly inside ToKoDraw.

**Anim Object from panel ToKoDraw**

![Tools](/assets/tuto/tools/animobj.gif)

**Anim Layers from panel TDK**

![Tools](/assets/tuto/tools/animeyes.gif)

![Tools](/assets/tuto/tools/animlayer.gif)
