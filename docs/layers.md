![Layers](/assets/tuto/layer/editor.png)

## **Introduction to Layers**

In LayerForge Canvas, each layer is represented inside the material as an individual node group, stacked one above another.
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

  - Image source 

![Layers](/assets/tuto/layer/source.png)
      
  - Transform
    
![Layers](/assets/tuto/layer/transform.png)

![Layers](/assets/tuto/layer/transform.gif)

For better accuracy when using Transform on a layer, consider adjusting Blender’s Unit Scale to 0.5.

![Layers](/assets/tuto/layer/unit.gif)



## **Normal Map**

![Layers](/assets/tuto/layer/normal.png)

Inactive when the material is first created.
Automatically becomes active when a Normal Map layer is added, enabling hand‑painted normal map workflows.
