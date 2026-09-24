---
title: ToKoDraw | Tools
description: ToKoDraw tools panel for Blender: mode selector, Render Switch, Outline system, Line Art, CamView access, Transform panel and right-click keyframe animation of any setting.
---


# ToKoDraw Tools Panel

The ToKoDraw **Tools panel** gathers the essential **painting tools for Blender** in one place: mode switching, render shading toggle, outline and line art generation, and keyframe animation of any setting. It works in every working mode, alongside the layer system.

![The ToKoDraw Tools panel](/assets/tuto/tools/toolbar.png)


## Blender mode selector

![The Blender mode list in the ToKoDraw panel](/assets/tuto/tools/blendmode.png)

The panel includes a synchronized list of Blender modes, allowing fast switching between Object Mode, Edit Mode, Sculpt Mode, Texture Paint, and others. Changing the mode from the Tools panel updates Blender instantly, ensuring seamless workflow transitions without navigating Blender’s default mode selector.


### Backface Culling

![Backface Culling icon in the ToKoDraw toolbar](/assets/tuto/tools/Backicon.png){: .picto-inline }

Backface Culling can be enabled directly from the panel. While primarily used as a viewport optimization, it also helps clarify the visible painting surface by hiding back‑facing polygons, which can be useful when painting or outlining complex meshes.

### Render Switch (Emission ↔ BSDF)

![Render Switch icon in the ToKoDraw toolbar](/assets/tuto/tools/rendericon.png){: .picto-inline }

The Render Switch toggles the material between **BSDF shading and Emission shading** with a single click. This is especially useful when previewing painted textures, isolating color information, or working in Canvas 2D mode where lighting can interfere with the final look.

## Outline System

![Outline tool icon in the ToKoDraw toolbar](/assets/tuto/tools/outlineicon.png){: .picto-inline }

The Outline tool automatically adds a **clean outline mesh** to the painted object and opens the floating Outline Settings panel. Once the outline has been created, pressing the button again simply reopens the settings instead of generating a new outline.

*Outline Settings include:* Thickness, Offset, Flip Normal, Alpha Slide, Hide / Show, Delete.

![Generating an automatic outline mesh around a painted object](/assets/tuto/tools/outline.gif)

## Line Art System

![Line Art tool icon in the ToKoDraw toolbar](/assets/tuto/tools/lineicon.png){: .picto-inline }

The Line Art tool automatically adds a **Grease Pencil Line Art object** linked to the painted mesh and opens the floating Line Art Settings panel. As with the outline system, pressing the button again only reopens the settings without creating additional line-art objects.

*Line Art Settings include:* Source / Target, Radius, Opacity Threshold, Edge Mark, Intersection, Crease, Delete.

![Generating a Grease Pencil line art overlay on a painted mesh](/assets/tuto/tools/lineart.gif)

## Quick access helpers

The Tools panel also provides quick access to workflow helpers:

- **CamView** — switches to the dedicated 2D camera view used for painting
- **Transform Panel** — opens the object transform controls (move, rotate, scale)
- **Frame Selected** — centers the view on the selected object in the scene

## Animating settings and layer parameters

All settings in the Tools panel — as well as layer parameters and other controls — can be animated through **right-click keyframing**. Any slider, toggle or numeric field supports keyframe insertion via Right-Click → Insert Keyframe.

Once keyframes are added, the animation curves can be edited in Blender's Graph Editor, giving full control over timing, interpolation and transitions. This makes it possible to animate opacity changes, outline thickness, line-art parameters, camera transforms and even layer operations — enabling advanced animated workflows directly inside ToKoDraw.

**Animating an object from the ToKoDraw panel**

![Keyframe animating an object from the ToKoDraw panel](/assets/tuto/tools/animobj.gif)

**Animating layers from the ToKoDraw panel**

![Keyframe animating layers from the ToKoDraw panel](/assets/tuto/tools/animeyes.gif)

![Animated layer parameters in the ToKoDraw panel](/assets/tuto/tools/animlayer.gif)

## Next steps

- Learn the layer system: opacity, merge, normal layers
- See the painting modes: 3D, CamView, Canvas 2D
- Follow the roadmap for upcoming tools

## FAQ

### Can I animate ToKoDraw settings?
Yes — right-click any slider, toggle or numeric field and choose Insert Keyframe, then edit the curves in the Graph Editor.

### Does the Outline tool create a new outline every time?
No — once the outline exists, pressing the button again only reopens the Outline Settings panel.

### What does the Render Switch do?
It toggles the material between Emission shading (flat, 2D-like) and BSDF shading (relief and lighting) with a single click.