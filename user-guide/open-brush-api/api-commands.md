# API Commands List

[API Docs](./)

{% hint style="info" %}
_This page was generated from the output directly from Open Brush API server. It's not always totally up to date. When you're running Open Brush then use the live commands list you get from_ [_http://localhost:40074/help/commands_](http://localhost:40074/help/commands) _as that will always be current._
{% endhint %}

{% hint style="info" %}
_The "Try It" links assume that a version of Open Brush with API support is currently running on this computer. They won't work if Open Brush isn't running. You can run a_ [_monoscopic_ ](../../developer-notes/github-wiki/monoscopicmode.md)_version if you don't have a VR headset attached._
{% endhint %}

To run commands just send a request to this url with [http://localhost:40074/api/v1?](http://localhost:40074/api/v1?)

Commands are query string parameters. Like this: command.name=parameters

Separate multiple commands with: **&**&#x20;

Example:[ http://localhost:40074/api/v1?brush.turn.y=45\&brush.draw=1](http://localhost:40074/api/v1?brush.turn.y=45\&brush.draw=1)

If you want to send a lot of commands or especially long commands (complex paths etc) then you can just http POST instead of GET. The commands should be form-encoded in the body of the request (exactly as if you submitted a html form with the form name as the command name and the form value as the command parameters)

You can also send multiple requests although because of the nature of http, these can sometimes arrive in a different order to how yousent them. We will soon support websockets which should be a better way to send realtime streams of commands.

### Command List

{% hint style="info" %}
Correct for beta version as of Oct 21 2025)
{% endhint %}

**listenfor.strokes** (string url) Try it

Adds the url of an app that wants to receive the data for a stroke as each one is finished

**showfolder.scripts** Try it

Opens the user's Scripts folder on the desktop

**showfolder.exports** Try it

Opens the user's Exports folder on the desktop

**spectator.move.to** (Vector3 position) Try it

Moves the spectator camera to the given position

**spectator.move.by** (Vector3 amount) Try it

Moves the spectator camera by the given amount

**user.move.to** (Vector3 position) Try it

Moves the user to the given position

**user.move.by** (Vector3 amount) Try it

Moves the user by the given amount

**spectator.turn.y** (float angle) Try it

Rotates the spectator camera left or right.

**spectator.turn.x** (float angle) Try it

Rotates the spectator camera up or down.

**spectator.turn.z** (float angle) Try it

Tilts the angle of the spectator camera clockwise or anticlockwise.

**user.turn.y** (float angle) Try it

Rotates the user camera left or right.

**user.turn.x** (float angle) Try it

Rotates the user camera up or down. (monoscopic mode only)

**user.turn.z** (float angle) Try it

Tilts the angle of the user camera clockwise or anticlockwise. (monoscopic mode only)

**scene.scale.to** (float scale) Try it

Sets the scene scale to the given value

**scene.scale.by** (float amount) Try it

Scales the scene by the given amount

**spectator.direction** (Vector3 direction) Try it

Points the spectator camera to look in the specified direction. Angles are given in x,y,z degrees

**user.direction** (Vector3 direction) Try it

Points the user camera to look in the specified direction. Angles are given in x,y,z degrees. (Monoscopic mode only)

**spectator.look.at** (Vector3 position) Try it

Points the spectator camera towards a specific point

**user.look.at** (Vector3 direction) Try it

Points the user camera towards a specific point (In VR this only changes the y axis. In monoscopic mode it changes all 3 axes)

**spectator.mode** (string mode) Try it

Sets the spectator camera mode to one of stationary, slowFollow, wobble, circular

**spectator.hide** (string thing) Try it

Hides the chosen type of elements from the spectator camera (widgets, strokes, selection, headset, panels, ui

**brush.move.to** (Vector3 position) Try it

Moves the brush to the given coordinates

**brush.move.to.hand** (string hand, Boolean alsoRotate) Try it

Moves the brush to the given hand (l or r

**brush.move.by** (Vector3 offset) Try it

Moves the brush by the given amount

**brush.move** (float distance) Try it

Moves the brush forward by 'distance' without drawing a line

**brush.draw** (float distance) Try it

Moves the brush forward by 'distance' and draws a line

**brush.turn.y** (float angle) Try it

Changes the brush direction to the left or right. Angle is measured in degrees

**brush.turn.x** (float angle) Try it

Changes the brush direction up or down. Angle is measured in degrees

**brush.turn.z** (float angle) Try it

Rotates the brush clockwise or anticlockwise. Angle is measured in degrees

**brush.look.at** (Vector3 direction) Try it

Changes the brush direction to look at the specified point

**brush.look.forwards** Try it

Changes the brush direction to look forwards

**brush.look.up** Try it

Changes the brush direction to look upwards

**brush.look.down** Try it

Changes the brush direction to look downwards

**brush.look.left** Try it

Changes the brush direction to look to the left

**brush.look.right** Try it

Changes the brush direction to look to the right

**brush.look.backwards** Try it

Changes the brush direction to look backwards

**brush.home.reset** Try it

Resets the brush position and direction

**brush.home.set** Try it

Sets the current brush position and direction as the new home. This persists in new sketches

**brush.transform.push** Try it

Stores the current brush position and direction on to a stack

**brush.transform.pop** Try it

Pops the most recent current brush position and direction from the stack

**debug.brush** Try it

Logs some info about the brush

**text.add** (string text) \[Try it]\(/api/v1?text.add=Hello world!)

Adds a text widget to the sketch

**video.import** (string location) Try it

Imports a video given a url or a filename in Media Library\Videos

**skybox.import** (string location) Try it

Sets the skybox from either a url or a filename in Media Library\BackgroundImages (Images loaded from a url are saved locally first)

**image.import** (string location) Try it

Imports an image given a url or a filename in Media Library\Images (Images loaded from a url are saved locally first)

**environment.type** (string name) Try it

Sets the current environment

**panel.open** (string name, float x, float y, float z) Try it

Opens a given panel at the given position

**panel.close** (string name) Try it

Closes a given panel

**panel.position** (string name, Vector3 position) Try it

Sets position of a given panel

**panel.rotation** (string name, Vector3 rotation) Try it

Sets rotation of a given panel

**strokes.debug** Try it

Logs some debug info about the strokes

**panel.attach** (string name) Try it

Attaches the given panel to the user's wand

**panel.detach** (string name, Vector3 position) Try it

Detaches the given panel from the user's wand

**layer.add** Try it

Adds a new layer

**layer.clear** (int layer) Try it

Clears the contents of a layer

**debug.ram** (Boolean active) Try it

Enable/Disable logging of RAM usage to the in-app console (Android only)

**layer.delete** (int layer) Try it

Deletes a layer

**layer.squash** (int squashedLayer, int destinationLayer) Try it

Move everything from one layer to another then removes the empty layer

**layer.activate** (int layer) Try it

Make a layer the active layer

**layer.show** (int layer) Try it

Make a layer visible

**layer.hide** (int layer) Try it

Hide a layer

**layer.toggle** (int layer) Try it

Toggles a layer between visible and hidden

**model.select** (int index) Try it

Selects a 3d model by index.

**model.position** (int index, Vector3 position) Try it

Move a 3d model to the given coordinates

**model.rotation** (int index, Vector3 rotation) Try it

Set a model's rotation to the given angles

**model.scale** (int index, float scale) Try it

Set a model's scale to the amount

**symmetry.position** (Vector3 position) Try it

Move the symmetry widget to the given coordinates

**symmetry.set.rotation** (Vector3 rotation) Try it

Sets the symmetry widget rotation

**symmetry.set.transform** (Vector3 position, Vector3 rotation) Try it

Sets the position and rotation of the symmetry widget

**brush.force.painting.on** (Boolean active) Try it

Turns on or off an override that paints even if the trigger is not pressed.

**brush.force.painting.off** (Boolean active) Try it

Turns on or off an override that stops the user painting even if the trigger is pressed.

**brush.new.stroke** Try it

Ends the current stroke and starts a new one next frame

**image.select** (int index) Try it

Selects an image by index.

**image.delete** (int index) Try it

Deletes an image by index.

**video.delete** (int index) Try it

Deletes a video by index.

**model.delete** (int index) Try it

Deletes a 3d model by index.

**guide.delete** (int index) Try it

Deletes a guide by index.

**image.position** (int index, Vector3 position) Try it

Move an image to the given coordinates

**image.rotation** (int index, Vector3 rotation) Try it

Set a images rotation to the given angles

**image.scale** (int index, float scale) Try it

Set a images scale to the amount

**light.position** (int index, Vector3 position) Try it

Move a light to the given coordinates

**light.rotation** (int index, Vector3 rotation) Try it

Set a light's rotation to the given angles

**image.formEncode** (int index) Try it

Converts an image to a string suitable for use in a form

**image.base64Decode** (string base64, string filename) Try it

Saves an image based on a base64 encoded string

**scripts.initPluginScripting** Try it

Call this before using any HTTP endpoint that accesses plugins (including html pages that list plugins)

**scripts.toolscript.activate** (string scriptName) Try it

Activate the given tool script

**scripts.toolscript.deactivate** Try it

Dectivate the tool script

**scripts.symmetryscript.activate** (string scriptName) Try it

Activate the given symmetry script

**scripts.symmetryscript.deactivate** Try it

Dectivate the symmetry script

**scripts.pointerscript.activate** (string scriptName) Try it

Activate the given pointer script

**scripts.pointerscript.deactivate** Try it

Dectivate the pointer script

**scripts.backgroundscript.activate** (string scriptName) Try it

Activate the given background script

**scripts.backgroundscript.deactivate** (string scriptName) Try it

Dectivate the given background script

**scripts.backgroundscript.activateall** Try it

Dectivate all background scripts

**scripts.backgroundscript.deactivateall** Try it

Dectivate all background scripts

**guide.add** (string type) Try it

Adds a guide to the scene (cube, sphere, capsule, cone, ellipsoid)

**guide.select** (int index) Try it

Selects a guide by index.

**guide.position** (int index, Vector3 position) Try it

Move a guide to the given coordinates

**guide.scale** (int index, Vector3 scale) Try it

Sets the (non-uniform) scale of a guide

**draw.paths** (string jsonString) Try it

Draws a series of paths at the current brush position \[\[\[x1,y1,z1],\[x2,y2,z2], etc...]]. Does not move the brush position

**brush.pathsmoothing** (float amount) Try it

Sets the amount of smoothing applied to brush paths at corners. Default is 0.10 turns off smoothing and you'll have to ensure you create enough points or else the path may end up smoothed to nothing.

**draw.path** (string jsonString) Try it

Draws a path at the current brush position \[x1,y1,z1],\[x2,y2,z2], etc.... Does not move the brush position

**draw.stroke** (string jsonString) Try it

Draws an exact brush stroke including orientation and pressure

**draw.polygon** (int sides, float radius, float angle) Try it

Draws a polygon at the current brush position. Does not move the brush position

**draw.text** (string text) \[Try it]\(/api/v1?draw.text=hello world)

Draws the characters supplied at the current brush position

**draw.opentypetext** (string text, string fontPath) \[Try it]\(/api/v1?draw.opentypetext=hello world,hello world,calibri.ttf)

Same as draw text but uses an opentype font (the font should be in a Fonts folder in your Open Brush folder)

**draw.svg** (string svg) Try it

Draws an entire SVG document

**draw.svg.path** (string svgPath) \[Try it]\(/api/v1?draw.svg.path=M 184,199 116,170 53,209.6 60,136.2 4.3,88)

Draws the path supplied as an SVG Path string at the current brush position

**brush.type** (string brushType) Try it

Changes the brush. brushType can either be the brush name or it's guid. brushes are listed in the /help screen

**color.add.hsv** (Vector3 hsv) Try it

Adds the supplied values to the current color. Values are hue, saturation and value

**color.add.rgb** (Vector3 rgb) Try it

Adds the supplied values to the current color. Values are red green and blue

**color.set.rgb** (Vector3 rgb) Try it

Sets the current color. Values are red, green and blue

**color.set.hsv** (Vector3 hsv) Try it

Sets the current color. Values are hue, saturation and value

**color.set.html** (string color) Try it

Sets the current color. colorString can either be a hex value or a css color name.

**brush.size.set** (float size) Try it

Sets the current brush size

**brush.size.add** (float amount) Try it

Changes the current brush size by the given amount

**draw.camerapath** (int index, float step) Try it

Draws along a camera path with the current brush settings

**model.webimport** (string url) Try it

Imports a model given a url or a filename in Media Library\Models (Models loaded from a url are saved locally first)

**import.webmodel** (string url) Try it

Same as model.webimport (backwards compatibility for poly.pizza)

**model.icosaimport** (string modelId) Try it

Imports a model from the Icosa Gallery given a model id

**model.import** (string location) Try it

Imports a model given a filename in Media Library\Models (Models loaded from a url are saved locally first)

**model.breakapart** (int index) Try it

Breaks apart a model

**save.overwrite** Try it

Save the current scene overwriting the last save if it exists

**save.as** (string filename) Try it

Saves the current scene under a new name. (No need to include the .tilt suffix)

**save.new** Try it

Saves the current scene in a new slot

**save.selected** Try it

Saves the current selected strokes in a new slot

**icosa.devicelogin** (string code) Try it

Login to the Icosa Gallery using a device code

**icosa.logout** Try it

Logout of the Icosa Gallery

**icosa.upload** Try it

Uploads it to the Icosa Gallery

**export.all** Try it

Exports all the scenes in the users's sketch folder

**drafting.visible** Try it

Shows all strokes made with the drafting brush fully opaque

**drafting.transparent** Try it

Shows all strokes made with the drafting brush semi-transparent

**drafting.hidden** Try it

Hides all strokes made with the drafting brush

**load.user** (int slot) Try it

Loads the sketch from the user's sketch folder given an index (0 being most recent)

**load.featured** (int slot) Try it

Loads the sketch in the given slot number from the featured sketch list

**load.liked** (int slot) Try it

Loads the sketch in the given slot number from the user's liked sketches

**load.drive** (int slot) Try it

Loads the sketch in the given slot number from the user's Google Drive

**load.named** (string filename) Try it

Loads the sketch with the given name from the user's sketch folder

**merge.named** (string filename) Try it

Loads the sketch with the given name from the user's sketch folder

**new** Try it

Clears the current sketch

**symmetry.mirror** Try it

Sets the symmetry mode to 'mirror'

**symmetry.multimirror** Try it

Sets the symmetry mode to 'multimirror'

**twohandeded.toggle** Try it

Toggles painting with both hands at once

**straightedge.toggle** Try it

Toggles the straight edge tool on or off

**autoorient.toggle** Try it

Toggles autoorientate on or off

**undo** Try it

Undoes the last action

**redo** Try it

Redo the last action

**panels.reset** Try it

Reset the position of all panels

**sketch.origin** Try it

Enables the sketch origin tool

**viewonly.toggle** Try it

Toggles 'view only' mode on or off

**spectator.toggle** Try it

Toggles the spectator camera

**spectator.on** Try it

Turns the spectator camera on

**spectator.off** Try it

Turns the spectator camera off

**autosimplify.toggle** Try it

Toggles 'auto-simplify' mode on or off

**export.current** Try it

Exports the current sketch to the user's Exports folder

**showfolder.sketch** (int index) Try it

Opens the user's Sketches folder on the desktop

**guides.disable** Try it

Toggles guides on and off

**disco** Try it

Starts a party

**selection.duplicate** Try it

Create a duplicate of the current selection (uses symmetry mirrors if active

**selection.delete** Try it

Deletes the current selection

**selection.group** Try it

Groups (or ungroups) the current selection

**export.selected** Try it

Exports the selected strokes to the user's Media Library

**camerapath.render** Try it

Renders the current camera path to a video

**profiling.toggle** Try it

Toggles profiling mode on or off

**settings.toggle** Try it

Toggles the settings panel on or off

**mirror.summon** Try it

Summons the mirror origin to the user's position

**selection.invert** Try it

Inverts the current selection

**select.all** Try it

Selects all strokes and widgets on the current layer

**select.none** Try it

Deselects all strokes and widgets on the current layer

**selection.flip** Try it

Mirrors the current selection

**postprocessing.toggle** Try it

Toggles post-processing effects on or off

**watermark.toggle** Try it

Toggles the watermark on or off

**camerapath.togglevisuals** Try it

Toggles the camera path visuals on or off

**camerapath.togglepreview** Try it

Toggles the camera path preview on or off

**camerapath.delete** Try it

Deletes the current camera path

**camerapath.record** Try it

Starts recording a camera path

**camerapath.setactive** (int index) Try it

Sets the active camera path

**stroke.delete** (int index) Try it

Delete a stroke by index

**stroke.select** (int index) Try it

Select a stroke by index.

**strokes.select** (int from, int to) Try it

Select multiple strokes by index.

**selection.recolor** (Boolean jitter) Try it

Recolors the currently selected strokes

**strokes.move.to** (int start, int end, Vector3 position) Try it

Moves several strokes to the given position

**strokes.move.by** (int start, int end, Vector3 translation) Try it

Moves several strokes to the given coordinates

**strokes.rotate.by** (int start, int end, float angle) Try it

Rotates multiple brushstrokes around the current brush position

**strokes.scale.by** (int start, int end, float scale) Try it

Scales multiple brushstrokes around the current brush position

**selection.rebrush** (Boolean jitter) Try it

Rebrushes the currently selected strokes

**selection.resize** (Boolean jitter) Try it

Changes the brush size the currently selected strokes

**selection.trim** (int count) Try it

Removes a number of points from the currently selected strokes

**selection.points.perlin** (string axis, Vector3 scale) Try it

Moves the position of all control points in the selection using a noise function

**stroke.points.quantize** (Vector3 grid) Try it

Snaps all the points in selected strokes to a grid (buggy)

**stroke.join** Try it

Joins a stroke with the previous one

**strokes.join** (int from, int to) Try it

Joins all strokes between the two indices (inclusive)

**stroke.add** (int index) Try it

Adds a point at the current brush position to the specified stroke

**symmetry.type** (string type) Try it

Sets the custom symmetry type (Currently either 'point' or 'wallpaper'

**symmetry.pointfamily** (string family) Try it

Sets the custom point symmetry family (Any of Cn, Cnv, Cnh, Sn, Dn, Dnh, Dnd, T, Th, Td, O, Oh, I, Ih) Replace n with a number to also set the order.

**symmetry.wallpapergroup** (string group) Try it

Sets the custom wallpaper symmetry group (Any of p1, pg, cm, pm, p6, p6m, p3, p3m1, p31m, p4, p4m, p4g, p2, pgg, pmg, pmm, cmm)

**symmetry.pointorder** (int order) Try it

Sets the custom point symmetry order

**symmetry.wallpaperrepeats** (int x, int y) Try it

Sets the custom wallpaper symmetry repeats

**symmetry.wallpaperscale** (float x, float y) Try it

Sets the custom wallpaper symmetry scale

**symmetry.wallpaperskew** (float x, float y) Try it

Sets the custom wallpaper symmetry skew

**symmetry.colorshift.hue** (string mode, float amplitude, float frequency) Try it

Sets the custom wallpaper color shift hue (mode is one of SineWave, SquareWave, SawtoothWave, TriangleWave, Noise)

**symmetry.colorshift.saturation** (string mode, float amplitude, float frequency) Try it

Sets the custom wallpaper color shift saturation (mode is one of SineWave, SquareWave, SawtoothWave, TriangleWave, Noise)

**symmetry.colorshift.brightness** (string mode, float amplitude, float frequency) Try it

Sets the custom wallpaper color shift brightness (mode is one of SineWave, SquareWave, SawtoothWave, TriangleWave, Noise)

**multiplayer.join** (string nickname, string roomName, Boolean isPrivate, int maxPlayers, Boolean silentRoom, Boolean viewOnlyRoom) Try it

Joins a multiplayer room

**multiplayer.leave** Try it

Leaves a multiplayer room

**tool.sketchsurface** Try it

Activates the SketchSurface

**tool.selection** Try it

Activates the Selection Tool

**tool.colorpicker** Try it

Activates the Color Picker

**tool.brushpicker** Try it

Activates the Brush Picker

**tool.brushandcolorpicker** Try it

Activates the Brush And Color Picker

**tool.sketchorigin** Try it

Activates the SketchOrigin Tool

**tool.autogif** Try it

Activates the AutoGif Tool

**tool.canvas** Try it

Activates the Canvas Tool

**tool.transform** Try it

Activates the Transform Tool

**tool.stamp** Try it

Activates the Stamp Tool

**tool.freepaint** Try it

Activates the FreePaint Tool

**tool.eraser** Try it

Activates the Eraser Tool

**tool.screenshot** Try it

Activates the Screenshot Tool

**tool.dropper** Try it

Activates the Dropper Tool

**tool.saveicon** Try it

Activates the SaveIcon Tool

**tool.threedofviewing** Try it

Activates the ThreeDofViewing Tool

**tool.multicam** Try it

Activates the MultiCam Tool

**tool.teleport** Try it

Activates the Teleport Tool

**tool.repaint** Try it

Activates the Repaint Tool

**tool.recolor** Try it

Activates the Recolor Tool

**tool.rebrush** Try it

Activates the Rebrush Tool

**tool.pin** Try it

Activates the Pin Tool

**tool.camerapath** Try it

Activates the CameraPath Tool

**tool.fly** Try it

Activates the Fly Tool

**snap.angle** (string angle) Try it

Sets the current snapping angle. Angle must be a supported value (15, 30, 45, 60, 75 or 90)

**snap.grid** (string size) Try it

Sets the current snapping grid. Size must be a supported value (0.1, 0.25, 0.5 ,1, 2, 3, 5

**selection.snap.angles** Try it

Applies the current snap angle to all selected objects

**selection.snap.positions** Try it

Applies the current snap grid to all selected objects

**selection.align** (string axis, string alignBy) Try it

Aligns all selected objects to the given axis using their minimum, center or maximum points
