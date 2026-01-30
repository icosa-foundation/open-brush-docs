# Merging Sketches

Merging sketches allows you to combine multiple Open Brush sketches into a single scene, enabling you to build complex compositions from separate components or collaborate by combining work from different artists.

## What does it do?

The merge sketches feature lets you:

* Load additional sketches into your current scene without closing the current sketch
* Combine elements from multiple sketches into one composition
* Build complex scenes by importing pre-made components
* Collaborate by merging sketches created by different artists
* Create libraries of reusable elements that can be merged into new sketches

## How to merge sketches

### Using the Sketch Browser

1. Open your base sketch (the one you want to merge content into)
2. Open the **Sketch Browser** (from the main menu panel)
3. Find the sketch you want to merge
4. Look for the **Merge** option or button next to the sketch
5. Select **Merge** to add the sketch's contents to your current scene

The merged sketch's strokes, models, images, and other elements will be added to your current sketch at their original positions.

## What gets merged?

When you merge a sketch, the following elements are imported:

* **Brush strokes** - All painted strokes from the source sketch
* **Imported media** - Images, videos, and 3D models
* **Lights** - Custom lights placed in the scene
* **Guides** - Any guides that were saved with the sketch

The following are NOT merged (your current sketch's settings are preserved):

* Environment settings
* Background images/panoramas
* Camera paths
* Layer organization (merged content may go to the active layer)

## Tips and best practices

* **Save before merging** - Always save your current sketch before merging, in case you want to undo the merge
* **Check scale** - Merged sketches retain their original scale, which might differ from your current sketch
* **Layer organization** - Consider creating a new layer before merging to keep merged content separate
* **Performance** - Merging very complex sketches can impact performance; monitor your frame rate
* **Position adjustment** - You may need to reposition merged elements to fit your composition

## Use cases

* **Component libraries** - Create a library of trees, buildings, or other elements to merge into new scenes
* **Collaboration** - Multiple artists can work on different parts of a scene and merge them together
* **Iterative composition** - Build complex scenes by merging together simpler sketches
* **Reference elements** - Merge in template sketches with guides, grids, or reference objects

## Alternative methods

* **Copy and paste between sketches** - Use selection tools to copy elements, though this requires switching between sketches
* **[Saved Stroke Gallery](importing-images-videos-3d-models.md)** - Save selections as reusable stroke groups (v2.13+)
* **Import as 3D model** - Export a sketch as GLB/GLTF and import it as a 3D model (loses editability)

## See also

* [Saving and sharing your Open Brush sketches](saving-and-sharing-your-open-brush-sketches.md)
* [Saved Stroke Gallery](importing-images-videos-3d-models.md)
* [Layers Panel](using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/layers-panel.md)
