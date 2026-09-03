---
layout: default
title: Presentation
---



Presentation
LayerForge Canvas is a Blender addon designed to extend and streamline the Texture Paint workflow. It is particularly suited for artists working in stylized NPR emission, but it also allows painting stylized normal maps directly, providing depth through BSDF. LFC includes a dedicated normal map palette and offers a simple switch between emission and BSDF through the Render Switch, making it easy to move from flat stylized rendering to a relief‑based look.
LFC is under active development and aims to bring Blender closer to a Krita / Photoshop‑like workflow, while remaining 100% native to Blender. It works in both Layout and Texture Paint Mode, and its internal architecture relies on node groups (NG) that separate and organize layers.
Working Modes
LayerForge Canvas provides several modes to adapt to the artist’s workflow:
Standard 3D Painting
Direct painting on 3D objects in the viewport, similar to Texture Paint, but with a full layer system.
LineArt CamView
A dedicated mode for painting a 3D object with its line art oriented correctly, unlike the standard 3D view where line art always faces the camera. This mode allows stylized painting without losing contours, with a control panel to orient the object.
Canvas Mode (2D)
Painting on a 2D canvas integrated into Blender.
When creating a canvas, the user can choose:
·	Horizontal
·	Vertical
·	Custom Size
This mode is ideal for creating 2D elements (FX, backgrounds, props) directly inside Blender, then integrating them into the 3D scene.
Dynamic Layer System
LFC offers a layer system inspired by 2D software:
·	add or remove layers anywhere in the stack,
·	choose the canvas size at creation,
·	freely reorder layers,
·	each layer includes: Hide/Show, Solo, Alpha Lock, Rename, Duplicate, Blend Mode, and Transform (animatable).
Layers are stored inside node groups, which ensures:
·	full compatibility with the Shader Editor,
·	the ability to add custom nodes,
·	a non‑destructive workflow,
·	a clean separation between layers and the final shader.
Normal Layer: When adding a new layer, the user can choose to create a normal map layer. After assigning the image to the normal texture node through the BSDF normal map settings, they can paint normals directly on the visible layer to control the colors used or benefit from real‑time rendering.
Image Source manages the layer’s image directly without opening the Image Editor or Shader Editor. Users can create, import, replace, rename, or remove images, and LFC also supports image sequences for animated workflows. The goal is to centralize texture management inside the layer panel so the artist can stay focused on painting.
Blending adjusts how a layer mixes with a chosen color via the picker. It allows softening or strengthening the result through blend modes, modifying the layer’s brightness, or controlling alpha hardness when working with transparent rendering using Canvas Hide. It’s a quick way to correct areas, refine transitions, or enhance stylized elements without repainting.
Transform moves, scales, or rotates a layer by modifying its UV mapping. Instead of editing the object or its UVs, LFC applies transformations directly to the layer, making it easy to reposition painted elements or adjust stylized details. Since these transformations are animatable, they provide a simple way to add motion to a layer while remaining fully integrated into the shader.
Merge & Optimization
LFC provides two fusion systems:
·	Merge visible layer images (show only) → combines only the active layer images. The merged image can then be assigned to a layer through Image Source.
·	Full merge with new material creation → generates a single texture, preserves alpha, and creates an optimized material.
This system allows finalizing a painting while keeping a clean, lightweight result and preserving the material for future edits. A selective layer merge system is under development to improve layer panel organization and management.
Dynamic Animation of Settings
In LayerForge Canvas, all layer parameters can be animated directly from the panel. A simple right‑click on any setting — opacity, brightness, blend mode, visibility, or transformations — inserts a keyframe just like any native Blender property.
Once keyframes are added, the animation can be edited in the Graph Editor, benefiting from all curve tools (interpolation, easing, cycles, etc.). This makes it possible to animate a layer like a graphic element: fading it in or out, brightening it progressively, creating pulsation effects, or moving and deforming it over time.
A dedicated frame‑by‑frame animation mode is also planned, designed to achieve perfect 2D rendering directly inside Blender. The goal is to let artists combine stylized painting, animated layers, and NPR rendering in a coherent, fluid, fully native workflow.
Development & Support
LayerForge Canvas is evolving constantly. Upcoming updates aim to expand drawing, painting, and selection tools, including line, rectangle, ellipse, lasso, and pixel selection movement. The layer system will also grow with grouping, merging, clipping masks, and filter masks, bringing it closer to full 2D software capabilities. A frame‑by‑frame animation mode is planned, along with improved transform tools for animating layers, line art, and stylized elements more smoothly.
LayerForge Canvas is developed solo by Thomas Chauveau (To Kohai). The addon is free and intends to remain free. A support link will be added soon for users wishing to contribute through donations.
