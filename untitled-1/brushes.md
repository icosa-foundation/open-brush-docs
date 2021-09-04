# Brushes

## Hierarchy

* `BaseBrushScript`
  * `BlocksBrushScript` purely exists to provide a vertex layout.
  * `EnvironmentBrushScript` purely exists to provide a vertex layout.
  * `PbrBrushScript` purely exists to provide a vertex layout.
  * `GeometryBrush`
    * `FlatGeometryBrush`
    * `HullBrush`
    * `MidpointPlusLifetimeSprayBrush`
    * `GeniusParticlesBrush` - camera aligned particles. Particle brush V2.
    * `PrintableBrush`
    * `SliceBrush` gives each control point a quad whose normal is the direction of motion.
    * `SprayBrush`
    * `Square3DPrintBrush` generates a manifold, 3D printable "tube" with a rounded 

      square cross section.

    * `SquareBrush`
    * `TetraBrush`
    * `ThickGeometryBrush`
    * `TubeBrush`
      * `BubbleWandBrush`
  * `QuadStripBrush` - base class of brushes that draw flat ribbons of connected quads.

    This is the first brush that existed.

    * `QuadStripBrushDistanceUV`
    * `QuadStripBrushStretchUV`
    * `QuadStripUnitizedUVBrush`

  * `ParentBrush`  
    * `CandyCane`
    * `HolidayTree`
    * `PlaitBrush`
    * `SnowflakeBrush` illustrates 6-fold symmetry.
* `MasterBrush` holds geometry in progress.  It's used for both active stroke and the

  preview stroke, and handles decay of preview brush for certain brush types.  Typical

  use would push the geometry here down to the Unity mesh every frame. `ActiveStroke` 

  would be a better name.

## History

From notes by Paul Du Bois:

Things started with `QuadStripBrush`, with a couple variants based on how UVs were generated. It just generates strips, 6 unique verts per tri \(3 for top, 3 for bottom, backface culled\). Then there was a variant that produced isolated quads \(for brushes like "leaves"\) instead of strips. `QuadStripBrush` uses a class called `MasterBrush` to temporarily store and work on the geometry before it's finalized into a mesh / batch.

Then `GeometryBrush` to "reboot" geometry generation and enable other kinds of topology. The intent was that `QuadStripBrush`-based brushes would migrate to `FlatGeometryBrush`, but the way that `QuadStripBrush` did its smoothing was not easy to replicate \(the details aren't important but the incremental algorithm QSB uses means that each knot doesn't have "local support" in the technical sense, and `GeometryBrush` in part was written to force people to use knots with local or at least bounded support for efficiency reasons\). So `FlatGeometryBrush` isn't used much. Most other brushes are derived from `GeometryBrush`.

`GeometryBrush` is notable for using a different storage scheme for intermediate geometry called "`GeometryPool`". This is used all over the place, wherever we want to process mesh data in C\# \(eg: geometry generation, multiplying geometry by a `TrTransform`, export\). Some of these manipulations have native-code versions that MachWerx wrote in C++; I think we ship that DLL in the repo.

The `GeometryBrush` variant of the old "isolated quad" brushes is `SprayBrush`, and I think the old version of that doesn't exist in the code any more.

`GeniusParticlesBrush` is I think Xap's very first work on the project and replaced an older less genius way of particle brushes.

`TubeBrush` was our first volumetric brush; it's also slightly notable for using a different method of curve framing. Instead of `BaseBrushScript.ComputeSurfaceFrameNew`, it uses parallel transport.

Dark Jeremy wrote `HullBrush` and that made the concept of "Knot" kind of weird. `ParentBrush` was an experiment

The `BatchManager` was written because "1 `GameObject` per stroke" is obvs not scalable. So it's a way of taking a bunch of tiny meshes, all of the same material, and grouping them into larger meshes. The tiny meshes become a "`BatchSubset`" within a larger mesh "Batch", and a single material \("`BatchPool`"\) will have multiple meshes \("Batches"\) and the whole thing is orchestrated by `BatchManager`.

## Coordinate Systems

From `BaseBrushScript`:

```text
// COORDINATE SYSTEMS
//
// Compared to the rest of Tilt Brush, BaseBrushScript and its subclasses
// use a simplified set of coordinate systems. Instead of Scene, Canvas,
// and Room, brushes only need to worry about their parent's local coordinate
// system and the coordinate system of the Pointer (the tool which is drawing
// the stroke). tldr: Local ~= Canvas and Pointer ~= Room.
//
// POINTER COORDINATES
//
// Brushes only care about the Pointer coordinate system for scale-invariance: a
// stroke drawn on a shrunk-down canvas should generate the same geometry as that
// same stroke drawn on an unscaled canvas. This is easy -- do everything in
// local space. However, we also want a way to independently alter the geometry
// density:
//
// - A long stroke drawn on a very scaled-down canvas would generate an
//   unnecessarily dense amount of geometry. Practically speaking, we want
//   geometry density to be specified in room space, not canvas space.
//
// - We want to be able to move strokes between canvases of different scales
//   without regenerating geometry. Or put another way, when redrawn in its new
//   canvas, the stroke should generate the same geometry.
//
// We do this by paying attention to the relative scale between Room (ie Pointer)
// and Canvas (ie Local).  If the user is a dinosaur relative to the canvas, the
// line density is lowered; if they are a mouse, the line density is increased.
//
// The suffix "_PS" indicates a distance or velocity measured in the pointer
// coordinate system. Lack of suffix implies the local coordinate system.
//
// TODO: we could probably simplify this so everything is in Canvas, by
// replacing everything relating to Pointer space with a "density" parameter.
// That's essentially how things work now, except "density" is encoded as
// 1/m_LastSpawnXf.scale -- which we assume never changes, even though the
// translation and rotation do change.
```

## User Brushes

In your Open Brush folder there will be a folder called 'Brushes'. You can create subfolders in that folder for your own user brushes. There is a `Brush.cfg` jspn file in which you have to specify a name, a guid, and the brush it is a variant of. You can then also add in a new main and normal texture if you want.

