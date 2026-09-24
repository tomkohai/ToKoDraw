# ToKoDraw Roadmap — Upcoming Features & Future Versions

The following roadmap outlines the planned evolution of ToKoDraw after the v1.0 release. It follows the approximate order in which features are expected to be developed, starting with incremental v1.x updates and gradually moving toward the long-term v2 vision.

*Last updated: September 2026*

## v1.1 — Layer controls & image source improvements

- **Per-layer opacity slider** — the opacity slider will remain in the ToolList, but an additional per-layer slider will be added inside each layer's Settings panel. This local slider is intended specifically for keyframe animation, preventing the current issue where the shared global slider becomes locked once a keyframe is added. The same approach will be applied to Hard Alpha.

- **Save button in Image Source** — a dedicated Save Image button will be added to the Image Source panel for quick export of painted textures.

- **Right-click settings menu for layers** — continuation of the floating settings menu accessible via right-click on a layer. A dedicated button in the Tools panel will also open this menu.

## v1.2 — Filters & transform enhancements

- **Tone / color filters & blur/sharpen** — introduction of a per-layer filter system: tone, color correction, blur, sharpen, and other basic FX.

- **Right-click transform tools** — transform options via right-click, and exploration of improved transform nodes beyond the standard Mapping node.

- **Pixel-based transform system (early work)** — initial groundwork for a system that moves painted pixels directly, without relying on UVs or image projection. This will eventually allow drag-and-drop pixel movement, copy/paste between layers, and keyframe animation of pixel transforms.

## v1.3 — Blending & FX pipeline

- **Blending node (experimental)** — investigation of a blending system between layers despite the stacked architecture, requiring careful design to avoid breaking the NBAdd chain and the straight-alpha pipeline.

- **FX effects (glow, blur, etc.)** — basic FX nodes applicable per layer or globally.

## v1.4 — Drawing & selection tools

A new **Drawing Toolbar** will be added, containing:

- **Drawing tools** — line, rectangle, circle, and other basic shapes.
- **Selection tools** — rectangle, ellipse, free selection, plus fill tools with painted-pixel edge detection.
- **Pixel movement tools** — drag-and-drop pixel displacement inside a layer, copy/paste to another layer, and pixel transforms without touching UVs. Potential support for keyframed pixel movement.

## v1.5 — Animation tools & line art

- **Line Art Animation panel** — a dedicated panel for animating Grease Pencil line art, including noise, motion and timing controls.

## v1.6 — Brush engine

- **Brush engine improvements** — creation of optimized brush packs (pencil, paint, texture brushes) and refinement of brush behavior.

## v1.7–1.9 — Layer masks & layer groups (long-term work)

- **Layer masks** — clipping, color masks, transform masks, filter masks, etc. This requires deep changes to the internal pipeline.
- **Layer groups** — create groups inside the layer stack, reorder them, and move layers in and out. A heavy feature, developed over a longer period to ensure stability.

## v2 — Advanced animation & the integrated 2D studio vision

The long-term goal is to transform ToKoDraw into a **full 2D animation studio inside Blender**, combining 2D painting, 3D scenes, camera work and animation tools.

Planned features include:

- **Frame-by-frame drawing panel** — timeline, onion skin, simple animation tools, and a dedicated frame-by-frame workflow.
- **Scene animation integration** — animate objects, layers, lights, cameras and scene elements directly from the Canvas workflow.
- **Gamepad camera controller** — already in prototype: real-time camera control using a gamepad for cinematic shots.

### The long-term vision

ToKoDraw aims to become a hybrid 2D/3D animation environment inside Blender. Artists will be able to paint 3D objects for backgrounds or props, animate planes or layers as dynamic backgrounds, create camera shots inside Blender, add a Canvas on top of the shot and paint a 2D character, then animate that character frame-by-frame while the canvas moves with the camera.

ToKoDraw is not meant to replace Blender's existing 2D tools such as Grease Pencil, but to complement them with a workflow inspired by traditional 2D animation software like Krita, OpenToonz and TVPaint — a natural bridge between 2D and 3D practices.

## FAQ

### Is ToKoDraw still in active development?
Yes — the public roadmap is updated regularly, with incremental v1.x releases planned before the larger v2 milestone.

### When will layer groups and masks be added?
Layer masks and layer groups are planned for the v1.7–1.9 range, as they require deep changes to the internal pipeline.

### Will there be a frame-by-frame animation mode?
Yes — frame-by-frame animation with a timeline and onion skin is part of the long-term v2 vision.