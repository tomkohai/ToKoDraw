<<<<<<< HEAD
# ToKoDraw 

All rights reserved.  
© 2026 – To Kohai / ToKoDraw
=======
# ToKoDraw

## Official Documentation
ToKoDraw is an advanced layer system for texture painting in Blender, inspired by workflows from 2D software such as Krita.
It allows you to create, organize, and blend non‑destructive layers, with a clear and fast workflow designed for stylized art, hand‑painted textures, creative shading, and FX pipelines.

### Main Features
Non‑destructive layers — paint directly on your 3D meshes, edit, reorganize, and refine your work without ever losing progress.
>>>>>>> ac6e57891944d6bd02cd59c64111faedc76c8c3f


## ToKoDraw Canvas 
Is an advanced multi‑material layer management system for Blender, designed for compositing, painting, 2D FX and stylized artistic workflows.

It provides a non‑destructive layer stack that can be reordered, merged, and fully synchronized with the Shader Editor.

Image Texture‑Based Workflow:

ToKoDraw is built on Blender’s Image Texture system, ensuring full compatibility with Cycles, Eevee, and all custom shaders.

<<<<<<< HEAD
Painting occurs before shading, making the workflow stable and predictable.
=======
### Roadmap & V1 Features
Implemented Features
Create ToKoDraw material
>>>>>>> ac6e57891944d6bd02cd59c64111faedc76c8c3f

---



<<<<<<< HEAD


- Non‑destructive layer stack

- Add, remove, reorder, merge, and clean layers

- Per‑layer opacity and Hard Alpha control

- Per‑layer rendering mode (Emission / BSDF)

- Automatic material creation and removal

- Fully synchronized and stable Layer ↔ NBAdd pipeline



- Emission mode for NPR, cel‑shading, and stylized rendering

- BSDF mode for stylized painting with depth

- Render Switch for instant toggling

- Automatic Normal Map injection when painting in BSDF

- Dedicated palette for stylized normal painting



- Paint directly from the camera view

- Dedicated transform panel to orient the object while keeping Line Art aligned

- Ideal for stylized, anime, comic, NPR workflows



- Automatic add/remove of Line Art or Outline on the mesh

Perfect for stylized rendering, cel‑shading, anime, comics


ToKoDraw includes a complete 2D canvas, similar to a painting software:

- Create a 2D canvas (horizontal, vertical, custom)

- Paint directly on a flat surface

- Canvas can be hidden in Emission mode (PNG rendering)

- Ideal for backgrounds, FX, masks, stylized textures


ToKoDraw is actively developed. Planned features include:

- Vector painting tools (line, rectangle, ellipse, fill, lasso, pixel move)

- Advanced stylized filters

- 2D frame‑by‑frame animation pipeline (Krita‑like)

- Texture animation tools for Line Art and stylized FX

- New blend modes and painting tools



1. Download the add‑on ZIP file  
2. Blender → **Edit → Preferences → Add‑ons**  
3. Click **Install…**  
4. Select the ZIP  
5. Enable **ToKoDraw**

---


- **Create Mat or Canvas**: automatically creates the material and assigns it to the 3D object.
- **Remove Mat**: removes the material and all its content (node groups, layers, images…).
- **Mode**: changes Blender’s mode directly from the panel.
- **Add Layer**: adds a layer anywhere in the stack (also allows adding a normal map layer and automatically enables BSDF normal map mode).
- **Remove Layer**: removes the selected layer  
- **Reorder Layer**: moves a layer within the stack  
- **Merge Layers**: merges the layers checked in the Merge Map  
- **Radio Button**: selects the active layer in the stack.
- **Opacity Slider**: adjusts the opacity of the selected layer.
- **Hard Alpha Slider**: softens or hardens the alpha of the selected layer.
- **Settings (arrow)**: available on the active layer — manages the source image (layer images) and UV transformations.
- **Backface Culling**: disables painting on internal faces.
- **Render Switch**: automatically toggles between Emission and BSDF shaders.
- **Outline & Settings**: adds an outline mesh linked to the 3D object and provides access to its parameters.
- **Line Art & Settings**: adds a Grease Pencil Line Art and provides access to its parameters.
- **Set Camera View**: enables camera‑view painting mode and the object transform panel (editable in Texture Paint).
- **Set Object Transform Panel**: enables or disables the object transform panel independently of camera view.
- **Frame Selected**: frames the camera on the selected object.

---



- Blender **4.x**  
- Cycles / Eevee  
- Custom Node Groups  
- Complex materials  
- Multi‑material setups

---



### Version: 1.0.0 — First stable release

See the **CHANGELOG.md** file.

---

ToKoDraw is distributed under a **free proprietary license with source access** (*Free Proprietary, Source‑Available License*).

You may:
- use the extension for free in personal and professional projects;
- modify the source code strictly for your private use.

You may not:
- redistribute the extension or its source code, whether modified or not;
- publish or share a modified version;
- create derivative works, forks, or extensions based on this code;
- reuse any part of the code in another project.

See the `LICENSE` file for more details.

---



For any question, suggestion, or bug:  

- GitHub Issues: https://github.com/tomkohai/ToKoDraw/issues/

- Website: https://tomkohai.github.io/ToKoDraw/

- Social networks:  
  https://www.instagram.com/tomkohai/  
  https://www.tiktok.com/@tom.kohai  
  https://www.linkedin.com/in/thomas-chauveau-eg/

- Developer contact: tomkohai@gmail.com 

- Community: https://discord.gg/YHYVpDFUY5

- Support: https://tomkohai.github.io/ToKoDraw/support/



=======
### v0.1 — Layer system, opacity, UI panels…

#### Support
For any questions: tomkohai@gmail.com
>>>>>>> ac6e57891944d6bd02cd59c64111faedc76c8c3f
