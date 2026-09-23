## Tools 


**Blender Mode Selector**

![Tools](/assets/tuto/tools/blendmode.png)

The panel includes a synchronized list of Blender modes, allowing fast switching between Object Mode, Edit Mode, Sculpt Mode, Texture Paint, and others. Changing the mode from the Tools panel updates Blender instantly, ensuring seamless workflow transitions without navigating Blender’s default mode selector.



![Tools](/assets/tuto/tools/toolbar.png)
<img src="/assets/tuto/tools/Backicon.png" class="picto-inline" alt="Backicon">
**Backface Culling**
Backface Culling can be enabled directly from the panel. While primarily used as a viewport optimization, it also helps clarify the visible painting surface by hiding back‑facing polygons, which can be useful when painting or outlining complex meshes.

![Tools](/assets/tuto/tools/rendericon.png)
**Render Switch**
The Render Switch toggles the material between BSDF shading and Emission shading with a single click. This is especially useful when previewing painted textures, isolating color information, or working in 2D canvas mode where lighting can interfere with the final look.

![Tools](/assets/tuto/tools/outlineicon.png)
## Outline System

The Outline tool automatically adds a clean outline mesh to the painted object and opens the floating Outline Settings panel. Once the outline has been created, pressing the button again simply reopens the settings instead of generating a new outline.

*Outline Settings include:*

- Thickness

- Offset

- Flip Normal

- Alpha Slide

- Hide / Show

- Delete
![Tools](/assets/tuto/tools/outline.gif)


![Tools](/assets/tuto/tools/lineicon.png)
## Line Art System

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

![Tools](/assets/tuto/tools/camicon.png)
**CamView** — switches to the dedicated 2D camera view used for painting.

![Tools](/assets/tuto/tools/transpicon.png)
**Transform Panel** — opens the object transform controls (move, rotate, scale).

![Tools](/assets/tuto/tools/frameicon.png)
**Frame Selected** — centers the view on the selected object in the scene.


## Animating Settings and Layer Parameters

All settings in the Tools panel, as well as layer parameters and other controls, can be animated directly through right‑click keyframing. Any slider, toggle, or numeric field supports keyframe insertion via Right‑Click → Insert Keyframe. Once keyframes are added, the animation curves can be edited in Blender’s Graph Editor, allowing full control over timing, interpolation, and transitions. This makes it possible to animate opacity changes, outline thickness, line‑art parameters, camera transforms, and even layer operations, enabling advanced animated workflows directly inside ToKoDraw.

**Anim Object from panel ToKoDraw**

![Tools](/assets/tuto/tools/animobj.gif)

**Anim Layers from panel TDK**
![Tools](/assets/tuto/tools/animeyes.gif)

![Tools](/assets/tuto/tools/animlayer.gif)
