# Open Brush Beta Docs

### Jitter <a href="#_lnka1z4mzei7" id="_lnka1z4mzei7"></a>

Randomize color, size, position both while painting and applied to existing strokes.

<img  src="../.gitbook/assets/0" width="500"/>

### Repaint <a href="#_3vhyqt3524ll" id="_3vhyqt3524ll"></a>

Modifying existing stroke size, color, brush.

<img src="../.gitbook/assets/1 (1)" width="400"/>

### Guide settings <a href="#_8pqxozpy6zng" id="_8pqxozpy6zng"></a>

Control the appearance and behaviour of guides.

<img src="../.gitbook/assets/2" width="300"/>

<img src="../.gitbook/assets/3" width="500"/>

Change the attract distance, grid size, line and frame widths.

### Hiding Brushes with Brush Tags <a href="#_yzlb2bab7mx9" id="_yzlb2bab7mx9"></a>

Assign tags to brushes in the config file and choose which groups of brushes to hide or show

See [here for more information](../alternate-and-experimental-builds/upcoming-beta-release/hiding-brushes-with-brush-tags.md)

<img src="../.gitbook/assets/4" width="500"/>

### Selection/Erase Filter <a href="#_yv25takdqgzd" id="_yv25takdqgzd"></a>

If you hold down your Wand trigger (the left hand if you're using Open Brush right-handed) when you first select a stroke with the Selection Tool, only brushstrokes that use that brush will be added to the selection as you continue to select strokes. You only have to be careful with the first stroke you select, and then after that, you can just wave the selector tool with reckless abandon and it will only select other strokes with the same brush.

This also works with the Erase Tool.

(Note that "same brush" is a bit of a simplification. Internally it selects strokes that belong to the same "batch". This is always the same brush type but

### View Axis Unlocking <a href="#_la31jnra3xq0" id="_la31jnra3xq0"></a>

This feature makes it possible to freely re-orient your workspace to match the sweep of your arm.

You can toggle it by pressing the button marked with a padlock while squeezing both controller grips.

{% embed url="https://www.youtube.com/watch?v=_d34eBiTtGA" %}

### Lazy Input <a href="#_ddz4xs77xmp9" id="_ddz4xs77xmp9"></a>

VR controllers can sometimes be a little too accurate and responsive, making it difficult to create smooth curves at low movement speeds. The Lazy Input feature will exchange responsiveness for control by applying real-time input averaging.

Toggle it by HOLDING your off-hand trigger and TAPPING the button marked with the rabbit/turtle.

{% embed url="https://www.youtube.com/watch?v=2CEyUrv3IZk" %}

### Wand Stroke Guide <a href="#_496rvkdaqngj" id="_496rvkdaqngj"></a>

This is a 3D-version of bimanual tape drawing sometimes used in automotive drafting.

Holding the off-hand trigger down will constrain the brush to move in a straight line towards the off-hand controller.

You can curve the line by using your off-hand controller to control the stroke's direction while using your main-hand controller to move the cursor closer to the off-hand controller and control the stroke's orientation.

{% embed url="https://www.youtube.com/watch?v=ufGpqmul4Rc" %}

### Wand Guide Revolver <a href="#_4u7pybbggg1h" id="_4u7pybbggg1h"></a>

The Revolver adds a lathe function to the Wand Stroke Guide. Activate the Revolver by tapping the button marked with a bulls-eye icon while the Wand Stroke Guide is active.

The radius of the revolving arc constraint is dependent on the distance between the main hand controller and the Wand Stroke Guide Axis. You can tap the bulls-eye button to adjust the radius.

The revolver can also be made to automatically sweep around the axis by using the joystick.

{% embed url="https://www.youtube.com/watch?v=Wtx5uAF0GXs" %}

### Snapping <a href="#_nswr7i93typ5" id="_nswr7i93typ5"></a>

Grid snapping for new brush strokes and when cloning/moving selections. Angle snapping when cloning/moving selections)

<img src="../.gitbook/assets/5" width="500"/>

### Merging Sketches <a href="#_u3ptgwey7elf" id="_u3ptgwey7elf"></a>

Import strokes from saved sketches into the current sketch.

<img src="../.gitbook/assets/6" width="500"/>

### Scripting API <a href="#_656cnqqjniaf" id="_656cnqqjniaf"></a>

<img src="../.gitbook/assets/7" width="350"/>

Control almost every aspect of Open Brush from an external source. Draw complex shapes and create content procedurally. Modify the current content., Import, export, move the spectator camera, change modes.

## GLB/GLTF Export Improvements

A small change that might be significant for people who export sketches to other software. GLTF export is probably the best format for preserving our more exotic brushes especially if your target platform is a web browser. Previously textures for built-in brushes were links to textures stored on the Google's servers. In this release we now copy the textures when exporting to GLB/GLTF and they should be included in the exported file.
