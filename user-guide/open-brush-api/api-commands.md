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

Example:[ http://localhost:40074/api/v1?brush.turn.y=45&brush.draw=1](http://localhost:40074/api/v1?brush.turn.y=45&brush.draw=1)

If you want to send a lot of commands or especially long commands (complex paths etc) then you can just http POST instead of GET. The commands should be form-encoded in the body of the request (exactly as if you submitted a html form with the form name as the command name and the form value as the command parameters)

You can also send multiple requests although because of the nature of http, these can sometimes arrive in a different order to how yousent them. We will soon support websockets which should be a better way to send realtime streams of commands.

### Command List

{% hint style="info" %}
Correct for beta version as of Oct 21 2025)
{% endhint %}

**listenfor.strokes** (string url) [Try it](http://localhost:40074/api/v1?/api/v1?listenfor.strokes=http://localhost:8000/)

Adds the url of an app that wants to receive the data for a stroke as each one is finished  
  

**showfolder.scripts** [Try it](http://localhost:40074/api/v1?/api/v1?showfolder.scripts)

Opens the user's Scripts folder on the desktop  
  

**showfolder.exports** [Try it](http://localhost:40074/api/v1?/api/v1?showfolder.exports)

Opens the user's Exports folder on the desktop  
  

**spectator.move.to** (Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.move.to=1,1,1)

Moves the spectator camera to the given position  
  

**spectator.move.by** (Vector3 amount) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.move.by=1,1,1)

Moves the spectator camera by the given amount  
  

**user.move.to** (Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?user.move.to=1,1,1)

Moves the user to the given position  
  

**user.move.by** (Vector3 amount) [Try it](http://localhost:40074/api/v1?/api/v1?user.move.by=1,1,1)

Moves the user by the given amount  
  

**spectator.turn.y** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.turn.y=45)

Rotates the spectator camera left or right.  
  

**spectator.turn.x** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.turn.x=45)

Rotates the spectator camera up or down.  
  

**spectator.turn.z** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.turn.z=45)

Tilts the angle of the spectator camera clockwise or anticlockwise.  
  

**user.turn.y** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?user.turn.y=45)

Rotates the user camera left or right.  
  

**user.turn.x** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?user.turn.x=45)

Rotates the user camera up or down. (monoscopic mode only)  
  

**user.turn.z** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?user.turn.z=45)

Tilts the angle of the user camera clockwise or anticlockwise. (monoscopic mode only)  
  

**scene.scale.to** (float scale) [Try it](http://localhost:40074/api/v1?/api/v1?scene.scale.to=0.5)

Sets the scene scale to the given value  
  

**scene.scale.by** (float amount) [Try it](http://localhost:40074/api/v1?/api/v1?scene.scale.by=1.5)

Scales the scene by the given amount  
  

**spectator.direction** (Vector3 direction) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.direction=45,45,0)

Points the spectator camera to look in the specified direction. Angles are given in x,y,z degrees  
  

**user.direction** (Vector3 direction) [Try it](http://localhost:40074/api/v1?/api/v1?user.direction=45,45,0)

Points the user camera to look in the specified direction. Angles are given in x,y,z degrees. (Monoscopic mode only)  
  

**spectator.look.at** (Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.look.at=1,2,3)

Points the spectator camera towards a specific point  
  

**user.look.at** (Vector3 direction) [Try it](http://localhost:40074/api/v1?/api/v1?user.look.at=1,2,3)

Points the user camera towards a specific point (In VR this only changes the y axis. In monoscopic mode it changes all 3 axes)  
  

**spectator.mode** (string mode) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.mode=stationary)

Sets the spectator camera mode to one of stationary, slowFollow, wobble, circular  
  

**spectator.hide** (string thing) [Try it](http://localhost:40074/api/v1?/api/v1?spectator.hide=panels)

Hides the chosen type of elements from the spectator camera (widgets, strokes, selection, headset, panels, ui  
  

**brush.move.to** (Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?brush.move.to=widgets)

Moves the brush to the given coordinates  
  

**brush.move.to.hand** (string hand, Boolean alsoRotate) [Try it](http://localhost:40074/api/v1?/api/v1?brush.move.to.hand=r)

Moves the brush to the given hand (l or r  
  

**brush.move.by** (Vector3 offset) [Try it](http://localhost:40074/api/v1?/api/v1?brush.move.by=1,1,1)

Moves the brush by the given amount  
  

**brush.move** (float distance) [Try it](http://localhost:40074/api/v1?/api/v1?brush.move=1)

Moves the brush forward by 'distance' without drawing a line  
  

**brush.draw** (float distance) [Try it](http://localhost:40074/api/v1?/api/v1?brush.draw=2)

Moves the brush forward by 'distance' and draws a line  
  

**brush.turn.y** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?brush.turn.y=45)

Changes the brush direction to the left or right. Angle is measured in degrees  
  

**brush.turn.x** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?brush.turn.x=45)

Changes the brush direction up or down. Angle is measured in degrees  
  

**brush.turn.z** (float angle) [Try it](http://localhost:40074/api/v1?/api/v1?brush.turn.z=45)

Rotates the brush clockwise or anticlockwise. Angle is measured in degrees  
  

**brush.look.at** (Vector3 direction) [Try it](http://localhost:40074/api/v1?/api/v1?brush.look.at=1,2,3)

Changes the brush direction to look at the specified point  
  

**brush.look.forwards** [Try it](http://localhost:40074/api/v1?/api/v1?brush.look.forwards)

Changes the brush direction to look forwards  
  

**brush.look.up** [Try it](http://localhost:40074/api/v1?/api/v1?brush.look.up)

Changes the brush direction to look upwards  
  

**brush.look.down** [Try it](http://localhost:40074/api/v1?/api/v1?brush.look.down)

Changes the brush direction to look downwards  
  

**brush.look.left** [Try it](http://localhost:40074/api/v1?/api/v1?brush.look.left)

Changes the brush direction to look to the left  
  

**brush.look.right** [Try it](http://localhost:40074/api/v1?/api/v1?brush.look.right)

Changes the brush direction to look to the right  
  

**brush.look.backwards** [Try it](http://localhost:40074/api/v1?/api/v1?brush.look.backwards)

Changes the brush direction to look backwards  
  

**brush.home.reset** [Try it](http://localhost:40074/api/v1?/api/v1?brush.home.reset)

Resets the brush position and direction  
  

**brush.home.set** [Try it](http://localhost:40074/api/v1?/api/v1?brush.home.set)

Sets the current brush position and direction as the new home. This persists in new sketches  
  

**brush.transform.push** [Try it](http://localhost:40074/api/v1?/api/v1?brush.transform.push)

Stores the current brush position and direction on to a stack  
  

**brush.transform.pop** [Try it](http://localhost:40074/api/v1?/api/v1?brush.transform.pop)

Pops the most recent current brush position and direction from the stack  
  

**debug.brush** [Try it](http://localhost:40074/api/v1?/api/v1?debug.brush)

Logs some info about the brush  
  

**text.add** (string text) [Try it](http://localhost:40074/api/v1?/api/v1?text.add=Hello%20world!)

Adds a text widget to the sketch  
  

**video.import** (string location) [Try it](http://localhost:40074/api/v1?/api/v1?video.import=animated-logo.mp4)

Imports a video given a url or a filename in Media Library\\Videos  
  

**skybox.import** (string location) [Try it](http://localhost:40074/api/v1?/api/v1?skybox.import=panorama.jpg)

Sets the skybox from either a url or a filename in Media Library\\BackgroundImages (Images loaded from a url are saved locally first)  
  

**image.import** (string location) [Try it](http://localhost:40074/api/v1?/api/v1?image.import=OpenBrushLogo.png)

Imports an image given a url or a filename in Media Library\\Images (Images loaded from a url are saved locally first)  
  

**environment.type** (string name) [Try it](http://localhost:40074/api/v1?/api/v1?environment.type=pistachio)

Sets the current environment  
  

**panel.open** (string name, float x, float y, float z) [Try it](http://localhost:40074/api/v1?/api/v1?panel.open=scripts,4,12,4)

Opens a given panel at the given position  
  

**panel.close** (string name) [Try it](http://localhost:40074/api/v1?/api/v1?panel.close=scripts)

Closes a given panel  
  

**panel.position** (string name, Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?panel.position=4,12,4)

Sets position of a given panel  
  

**panel.rotation** (string name, Vector3 rotation) [Try it](http://localhost:40074/api/v1?/api/v1?panel.rotation=4,12,4)

Sets rotation of a given panel  
  

**strokes.debug** [Try it](http://localhost:40074/api/v1?/api/v1?strokes.debug)

Logs some debug info about the strokes  
  

**panel.attach** (string name) [Try it](http://localhost:40074/api/v1?/api/v1?panel.attach=scripts)

Attaches the given panel to the user's wand  
  

**panel.detach** (string name, Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?panel.detach=scripts)

Detaches the given panel from the user's wand  
  

**layer.add** [Try it](http://localhost:40074/api/v1?/api/v1?layer.add)

Adds a new layer  
  

**layer.clear** (int layer) [Try it](http://localhost:40074/api/v1?/api/v1?layer.clear=2)

Clears the contents of a layer  
  

**debug.ram** (Boolean active) [Try it](http://localhost:40074/api/v1?/api/v1?debug.ram)

Enable/Disable logging of RAM usage to the in-app console (Android only)  
  

**layer.delete** (int layer) [Try it](http://localhost:40074/api/v1?/api/v1?layer.delete=1)

Deletes a layer  
  

**layer.squash** (int squashedLayer, int destinationLayer) [Try it](http://localhost:40074/api/v1?/api/v1?layer.squash=1,0)

Move everything from one layer to another then removes the empty layer  
  

**layer.activate** (int layer) [Try it](http://localhost:40074/api/v1?/api/v1?layer.activate=2)

Make a layer the active layer  
  

**layer.show** (int layer) [Try it](http://localhost:40074/api/v1?/api/v1?layer.show=2)

Make a layer visible  
  

**layer.hide** (int layer) [Try it](http://localhost:40074/api/v1?/api/v1?layer.hide=2)

Hide a layer  
  

**layer.toggle** (int layer) [Try it](http://localhost:40074/api/v1?/api/v1?layer.toggle=2)

Toggles a layer between visible and hidden  
  

**model.select** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?model.select=2)

Selects a 3d model by index.  
  

**model.position** (int index, Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?model.position=2,6,8)

Move a 3d model to the given coordinates  
  

**model.rotation** (int index, Vector3 rotation) [Try it](http://localhost:40074/api/v1?/api/v1?model.rotation)

Set a model's rotation to the given angles  
  

**model.scale** (int index, float scale) [Try it](http://localhost:40074/api/v1?/api/v1?model.scale)

Set a model's scale to the amount  
  

**symmetry.position** (Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.position=2,6,8)

Move the symmetry widget to the given coordinates  
  

**symmetry.set.rotation** (Vector3 rotation) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.set.rotation=45,30,0)

Sets the symmetry widget rotation  
  

**symmetry.set.transform** (Vector3 position, Vector3 rotation) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.set.transform=2,6,8,45,30,0)

Sets the position and rotation of the symmetry widget  
  

**brush.force.painting.on** (Boolean active) [Try it](http://localhost:40074/api/v1?/api/v1?brush.force.painting.on=true)

Turns on or off an override that paints even if the trigger is not pressed.  
  

**brush.force.painting.off** (Boolean active) [Try it](http://localhost:40074/api/v1?/api/v1?brush.force.painting.off=false)

Turns on or off an override that stops the user painting even if the trigger is pressed.  
  

**brush.new.stroke** [Try it](http://localhost:40074/api/v1?/api/v1?brush.new.stroke)

Ends the current stroke and starts a new one next frame  
  

**image.select** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?image.select=2)

Selects an image by index.  
  

**image.delete** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?image.delete=2)

Deletes an image by index.  
  

**video.delete** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?video.delete=2)

Deletes a video by index.  
  

**model.delete** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?model.delete=2,6,8)

Deletes a 3d model by index.  
  

**guide.delete** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?guide.delete=2)

Deletes a guide by index.  
  

**image.position** (int index, Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?image.position=2,1,6,8)

Move an image to the given coordinates  
  

**image.rotation** (int index, Vector3 rotation) [Try it](http://localhost:40074/api/v1?/api/v1?image.rotation)

Set a images rotation to the given angles  
  

**image.scale** (int index, float scale) [Try it](http://localhost:40074/api/v1?/api/v1?image.scale)

Set a images scale to the amount  
  

**light.position** (int index, Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?light.position)

Move a light to the given coordinates  
  

**light.rotation** (int index, Vector3 rotation) [Try it](http://localhost:40074/api/v1?/api/v1?light.rotation)

Set a light's rotation to the given angles  
  

**image.formEncode** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?image.formEncode=2)

Converts an image to a string suitable for use in a form  
  

**image.base64Decode** (string base64, string filename) [Try it](http://localhost:40074/api/v1?/api/v1?image.base64Decode)

Saves an image based on a base64 encoded string  
  

**scripts.initPluginScripting** [Try it](http://localhost:40074/api/v1?/api/v1?scripts.initPluginScripting=)

Call this before using any HTTP endpoint that accesses plugins (including html pages that list plugins)  
  

**scripts.toolscript.activate** (string scriptName) [Try it](http://localhost:40074/api/v1?/api/v1?scripts.toolscript.activate=Spiral)

Activate the given tool script  
  

**scripts.toolscript.deactivate** [Try it](http://localhost:40074/api/v1?/api/v1?scripts.toolscript.deactivate=Spiral)

Dectivate the tool script  
  

**scripts.symmetryscript.activate** (string scriptName) [Try it](http://localhost:40074/api/v1?/api/v1?scripts.symmetryscript.activate=Boids)

Activate the given symmetry script  
  

**scripts.symmetryscript.deactivate** [Try it](http://localhost:40074/api/v1?/api/v1?scripts.symmetryscript.deactivate=Boids)

Dectivate the symmetry script  
  

**scripts.pointerscript.activate** (string scriptName) [Try it](http://localhost:40074/api/v1?/api/v1?scripts.pointerscript.activate=Loops)

Activate the given pointer script  
  

**scripts.pointerscript.deactivate** [Try it](http://localhost:40074/api/v1?/api/v1?scripts.pointerscript.deactivate=Loops)

Dectivate the pointer script  
  

**scripts.backgroundscript.activate** (string scriptName) [Try it](http://localhost:40074/api/v1?/api/v1?scripts.backgroundscript.activate=Lines)

Activate the given background script  
  

**scripts.backgroundscript.deactivate** (string scriptName) [Try it](http://localhost:40074/api/v1?/api/v1?scripts.backgroundscript.deactivate=Lines)

Dectivate the given background script  
  

**scripts.backgroundscript.activateall** [Try it](http://localhost:40074/api/v1?/api/v1?scripts.backgroundscript.activateall)

Dectivate all background scripts  
  

**scripts.backgroundscript.deactivateall** [Try it](http://localhost:40074/api/v1?/api/v1?scripts.backgroundscript.deactivateall)

Dectivate all background scripts  
  

**guide.add** (string type) [Try it](http://localhost:40074/api/v1?/api/v1?guide.add=cube)

Adds a guide to the scene (cube, sphere, capsule, cone, ellipsoid)  
  

**guide.select** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?guide.select=2)

Selects a guide by index.  
  

**guide.position** (int index, Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?guide.position=2,4,10,-4)

Move a guide to the given coordinates  
  

**guide.scale** (int index, Vector3 scale) [Try it](http://localhost:40074/api/v1?/api/v1?guide.scale=2,1.5,1,1.5)

Sets the (non-uniform) scale of a guide  
  

**draw.paths** (string jsonString) [Try it](http://localhost:40074/api/v1?/api/v1?draw.paths=[[0,0,0],[1,0,0],[1,1,0]],[[0,0,-1],[-1,0,-1],[-1,1,-1]])

Draws a series of paths at the current brush position \[\[\[x1,y1,z1\],\[x2,y2,z2\], etc...\]\]. Does not move the brush position  
  

**brush.pathsmoothing** (float amount) [Try it](http://localhost:40074/api/v1?/api/v1?brush.pathsmoothing=0.1)

Sets the amount of smoothing applied to brush paths at corners. Default is 0.10 turns off smoothing and you'll have to ensure you create enough points or else the path may end up smoothed to nothing.  
  

**draw.path** (string jsonString) [Try it](http://localhost:40074/api/v1?/api/v1?draw.path=[0,0,0],[1,0,0],[1,1,0],[0,1,0])

Draws a path at the current brush position \[x1,y1,z1\],\[x2,y2,z2\], etc.... Does not move the brush position  
  

**draw.stroke** (string jsonString) [Try it](http://localhost:40074/api/v1?/api/v1?draw.stroke=[0,0,0,0,180,90,.75],[1,0,0,0,180,90,.75],[1,1,0,0,180,90,.75],[0,1,0,0,180,90,.75])

Draws an exact brush stroke including orientation and pressure  
  

**draw.polygon** (int sides, float radius, float angle) [Try it](http://localhost:40074/api/v1?/api/v1?draw.polygon=5,2.5,45)

Draws a polygon at the current brush position. Does not move the brush position  
  

**draw.text** (string text) [Try it](http://localhost:40074/api/v1?/api/v1?draw.text=hello%20world)

Draws the characters supplied at the current brush position  
  

**draw.opentypetext** (string text, string fontPath) [Try it](http://localhost:40074/api/v1?/api/v1?draw.opentypetext=hello%20world,hello%20world,calibri.ttf)

Same as draw text but uses an opentype font (the font should be in a Fonts folder in your Open Brush folder)  
  

**draw.svg** (string svg) [Try it](http://localhost:40074/api/v1?/api/v1?draw.svg)

Draws an entire SVG document  
  

**draw.svg.path** (string svgPath) [Try it](http://localhost:40074/api/v1?/api/v1?draw.svg.path=M%20184,199%20116,170%2053,209.6%2060,136.2%204.3,88)

Draws the path supplied as an SVG Path string at the current brush position  
  

**brush.type** (string brushType) [Try it](http://localhost:40074/api/v1?/api/v1?brush.type=ink)

Changes the brush. brushType can either be the brush name or it's guid. brushes are listed in the /help screen  
  

**color.add.hsv** (Vector3 hsv) [Try it](http://localhost:40074/api/v1?/api/v1?color.add.hsv=0.1,0.2,0.3)

Adds the supplied values to the current color. Values are hue, saturation and value  
  

**color.add.rgb** (Vector3 rgb) [Try it](http://localhost:40074/api/v1?/api/v1?color.add.rgb=0.1,0.2,0.3)

Adds the supplied values to the current color. Values are red green and blue  
  

**color.set.rgb** (Vector3 rgb) [Try it](http://localhost:40074/api/v1?/api/v1?color.set.rgb=0.1,0.2,0.3)

Sets the current color. Values are red, green and blue  
  

**color.set.hsv** (Vector3 hsv) [Try it](http://localhost:40074/api/v1?/api/v1?color.set.hsv=0.1,0.2,0.3)

Sets the current color. Values are hue, saturation and value  
  

**color.set.html** (string color) [Try it](http://localhost:40074/api/v1?/api/v1?color.set.html=darkblue)

Sets the current color. colorString can either be a hex value or a css color name.  
  

**brush.size.set** (float size) [Try it](http://localhost:40074/api/v1?/api/v1?brush.size.set=0.5)

Sets the current brush size  
  

**brush.size.add** (float amount) [Try it](http://localhost:40074/api/v1?/api/v1?brush.size.add=0.1)

Changes the current brush size by the given amount  
  

**draw.camerapath** (int index, float step) [Try it](http://localhost:40074/api/v1?/api/v1?draw.camerapath=0)

Draws along a camera path with the current brush settings  
  

**model.webimport** (string url) [Try it](http://localhost:40074/api/v1?/api/v1?model.webimport=Andy\Andy.obj)

Imports a model given a url or a filename in Media Library\\Models (Models loaded from a url are saved locally first)  
  

**import.webmodel** (string url) [Try it](http://localhost:40074/api/v1?/api/v1?import.webmodel=Andy\Andy.obj)

Same as model.webimport (backwards compatibility for poly.pizza)  
  

**model.icosaimport** (string modelId) [Try it](http://localhost:40074/api/v1?/api/v1?model.icosaimport=9L2Lt-sxzdp)

Imports a model from the Icosa Gallery given a model id  
  

**model.import** (string location) [Try it](http://localhost:40074/api/v1?/api/v1?model.import=Andy.glb)

Imports a model given a filename in Media Library\\Models (Models loaded from a url are saved locally first)  
  

**model.breakapart** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?model.breakapart=0)

Breaks apart a model  
  

**save.overwrite** [Try it](http://localhost:40074/api/v1?/api/v1?save.overwrite)

Save the current scene overwriting the last save if it exists  
  

**save.as** (string filename) [Try it](http://localhost:40074/api/v1?/api/v1?save.as=newSketch)

Saves the current scene under a new name. (No need to include the .tilt suffix)  
  

**save.new** [Try it](http://localhost:40074/api/v1?/api/v1?save.new)

Saves the current scene in a new slot  
  

**save.selected** [Try it](http://localhost:40074/api/v1?/api/v1?save.selected)

Saves the current selected strokes in a new slot  
  

**icosa.devicelogin** (string code) [Try it](http://localhost:40074/api/v1?/api/v1?icosa.devicelogin)

Login to the Icosa Gallery using a device code  
  

**icosa.logout** [Try it](http://localhost:40074/api/v1?/api/v1?icosa.logout)

Logout of the Icosa Gallery  
  

**icosa.upload** [Try it](http://localhost:40074/api/v1?/api/v1?icosa.upload)

Uploads it to the Icosa Gallery  
  

**export.all** [Try it](http://localhost:40074/api/v1?/api/v1?export.all)

Exports all the scenes in the users's sketch folder  
  

**drafting.visible** [Try it](http://localhost:40074/api/v1?/api/v1?drafting.visible)

Shows all strokes made with the drafting brush fully opaque  
  

**drafting.transparent** [Try it](http://localhost:40074/api/v1?/api/v1?drafting.transparent)

Shows all strokes made with the drafting brush semi-transparent  
  

**drafting.hidden** [Try it](http://localhost:40074/api/v1?/api/v1?drafting.hidden)

Hides all strokes made with the drafting brush  
  

**load.user** (int slot) [Try it](http://localhost:40074/api/v1?/api/v1?load.user=2)

Loads the sketch from the user's sketch folder given an index (0 being most recent)  
  

**load.featured** (int slot) [Try it](http://localhost:40074/api/v1?/api/v1?load.featured=2)

Loads the sketch in the given slot number from the featured sketch list  
  

**load.liked** (int slot) [Try it](http://localhost:40074/api/v1?/api/v1?load.liked=2)

Loads the sketch in the given slot number from the user's liked sketches  
  

**load.drive** (int slot) [Try it](http://localhost:40074/api/v1?/api/v1?load.drive=2)

Loads the sketch in the given slot number from the user's Google Drive  
  

**load.named** (string filename) [Try it](http://localhost:40074/api/v1?/api/v1?load.named=Untitled_1)

Loads the sketch with the given name from the user's sketch folder  
  

**merge.named** (string filename) [Try it](http://localhost:40074/api/v1?/api/v1?merge.named=Untitled_1)

Loads the sketch with the given name from the user's sketch folder  
  

**new** [Try it](http://localhost:40074/api/v1?/api/v1?new)

Clears the current sketch  
  

**symmetry.mirror** [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.mirror)

Sets the symmetry mode to 'mirror'  
  

**symmetry.multimirror** [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.multimirror)

Sets the symmetry mode to 'multimirror'  
  

**twohandeded.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?twohandeded.toggle)

Toggles painting with both hands at once  
  

**straightedge.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?straightedge.toggle)

Toggles the straight edge tool on or off  
  

**autoorient.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?autoorient.toggle)

Toggles autoorientate on or off  
  

**undo** [Try it](http://localhost:40074/api/v1?/api/v1?undo)

Undoes the last action  
  

**redo** [Try it](http://localhost:40074/api/v1?/api/v1?redo)

Redo the last action  
  

**panels.reset** [Try it](http://localhost:40074/api/v1?/api/v1?panels.reset)

Reset the position of all panels  
  

**sketch.origin** [Try it](http://localhost:40074/api/v1?/api/v1?sketch.origin)

Enables the sketch origin tool  
  

**viewonly.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?viewonly.toggle)

Toggles 'view only' mode on or off  
  

**spectator.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?spectator.toggle)

Toggles the spectator camera  
  

**spectator.on** [Try it](http://localhost:40074/api/v1?/api/v1?spectator.on)

Turns the spectator camera on  
  

**spectator.off** [Try it](http://localhost:40074/api/v1?/api/v1?spectator.off)

Turns the spectator camera off  
  

**autosimplify.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?autosimplify.toggle)

Toggles 'auto-simplify' mode on or off  
  

**export.current** [Try it](http://localhost:40074/api/v1?/api/v1?export.current)

Exports the current sketch to the user's Exports folder  
  

**showfolder.sketch** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?showfolder.sketch)

Opens the user's Sketches folder on the desktop  
  

**guides.disable** [Try it](http://localhost:40074/api/v1?/api/v1?guides.disable)

Toggles guides on and off  
  

**disco** [Try it](http://localhost:40074/api/v1?/api/v1?disco)

Starts a party  
  

**selection.duplicate** [Try it](http://localhost:40074/api/v1?/api/v1?selection.duplicate)

Create a duplicate of the current selection (uses symmetry mirrors if active  
  

**selection.delete** [Try it](http://localhost:40074/api/v1?/api/v1?selection.delete)

Deletes the current selection  
  

**selection.group** [Try it](http://localhost:40074/api/v1?/api/v1?selection.group)

Groups (or ungroups) the current selection  
  

**export.selected** [Try it](http://localhost:40074/api/v1?/api/v1?export.selected)

Exports the selected strokes to the user's Media Library  
  

**camerapath.render** [Try it](http://localhost:40074/api/v1?/api/v1?camerapath.render)

Renders the current camera path to a video  
  

**profiling.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?profiling.toggle)

Toggles profiling mode on or off  
  

**settings.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?settings.toggle)

Toggles the settings panel on or off  
  

**mirror.summon** [Try it](http://localhost:40074/api/v1?/api/v1?mirror.summon)

Summons the mirror origin to the user's position  
  

**selection.invert** [Try it](http://localhost:40074/api/v1?/api/v1?selection.invert)

Inverts the current selection  
  

**select.all** [Try it](http://localhost:40074/api/v1?/api/v1?select.all)

Selects all strokes and widgets on the current layer  
  

**select.none** [Try it](http://localhost:40074/api/v1?/api/v1?select.none)

Deselects all strokes and widgets on the current layer  
  

**selection.flip** [Try it](http://localhost:40074/api/v1?/api/v1?selection.flip)

Mirrors the current selection  
  

**postprocessing.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?postprocessing.toggle)

Toggles post-processing effects on or off  
  

**watermark.toggle** [Try it](http://localhost:40074/api/v1?/api/v1?watermark.toggle)

Toggles the watermark on or off  
  

**camerapath.togglevisuals** [Try it](http://localhost:40074/api/v1?/api/v1?camerapath.togglevisuals)

Toggles the camera path visuals on or off  
  

**camerapath.togglepreview** [Try it](http://localhost:40074/api/v1?/api/v1?camerapath.togglepreview)

Toggles the camera path preview on or off  
  

**camerapath.delete** [Try it](http://localhost:40074/api/v1?/api/v1?camerapath.delete)

Deletes the current camera path  
  

**camerapath.record** [Try it](http://localhost:40074/api/v1?/api/v1?camerapath.record)

Starts recording a camera path  
  

**camerapath.setactive** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?camerapath.setactive)

Sets the active camera path  
  

**stroke.delete** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?stroke.delete=2)

Delete a stroke by index  
  

**stroke.select** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?stroke.select=2)

Select a stroke by index.  
  

**strokes.select** (int from, int to) [Try it](http://localhost:40074/api/v1?/api/v1?strokes.select=1,4)

Select multiple strokes by index.  
  

**selection.recolor** (Boolean jitter) [Try it](http://localhost:40074/api/v1?/api/v1?selection.recolor)

Recolors the currently selected strokes  
  

**strokes.move.to** (int start, int end, Vector3 position) [Try it](http://localhost:40074/api/v1?/api/v1?strokes.move.to=1,2,5,12,-4)

Moves several strokes to the given position  
  

**strokes.move.by** (int start, int end, Vector3 translation) [Try it](http://localhost:40074/api/v1?/api/v1?strokes.move.by=1,2,5,12,-4)

Moves several strokes to the given coordinates  
  

**strokes.rotate.by** (int start, int end, float angle) [Try it](http://localhost:40074/api/v1?/api/v1?strokes.rotate.by=1,2,5,12,-4)

Rotates multiple brushstrokes around the current brush position  
  

**strokes.scale.by** (int start, int end, float scale) [Try it](http://localhost:40074/api/v1?/api/v1?strokes.scale.by=1,2,0.5)

Scales multiple brushstrokes around the current brush position  
  

**selection.rebrush** (Boolean jitter) [Try it](http://localhost:40074/api/v1?/api/v1?selection.rebrush=true)

Rebrushes the currently selected strokes  
  

**selection.resize** (Boolean jitter) [Try it](http://localhost:40074/api/v1?/api/v1?selection.resize)

Changes the brush size the currently selected strokes  
  

**selection.trim** (int count) [Try it](http://localhost:40074/api/v1?/api/v1?selection.trim=4)

Removes a number of points from the currently selected strokes  
  

**selection.points.perlin** (string axis, Vector3 scale) [Try it](http://localhost:40074/api/v1?/api/v1?selection.points.perlin=y,0.5,2,0.5)

Moves the position of all control points in the selection using a noise function  
  

**stroke.points.quantize** (Vector3 grid) [Try it](http://localhost:40074/api/v1?/api/v1?stroke.points.quantize=2,2,2)

Snaps all the points in selected strokes to a grid (buggy)  
  

**stroke.join** [Try it](http://localhost:40074/api/v1?/api/v1?stroke.join)

Joins a stroke with the previous one  
  

**strokes.join** (int from, int to) [Try it](http://localhost:40074/api/v1?/api/v1?strokes.join=1,4)

Joins all strokes between the two indices (inclusive)  
  

**stroke.add** (int index) [Try it](http://localhost:40074/api/v1?/api/v1?stroke.add=2)

Adds a point at the current brush position to the specified stroke  
  

**symmetry.type** (string type) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.type=wallpaper)

Sets the custom symmetry type (Currently either 'point' or 'wallpaper'  
  

**symmetry.pointfamily** (string family) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.pointfamily=C4v)

Sets the custom point symmetry family (Any of Cn, Cnv, Cnh, Sn, Dn, Dnh, Dnd, T, Th, Td, O, Oh, I, Ih) Replace n with a number to also set the order.  
  

**symmetry.wallpapergroup** (string group) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.wallpapergroup=p6m)

Sets the custom wallpaper symmetry group (Any of p1, pg, cm, pm, p6, p6m, p3, p3m1, p31m, p4, p4m, p4g, p2, pgg, pmg, pmm, cmm)  
  

**symmetry.pointorder** (int order) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.pointorder=5)

Sets the custom point symmetry order  
  

**symmetry.wallpaperrepeats** (int x, int y) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.wallpaperrepeats=4,4)

Sets the custom wallpaper symmetry repeats  
  

**symmetry.wallpaperscale** (float x, float y) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.wallpaperscale=0.5,1)

Sets the custom wallpaper symmetry scale  
  

**symmetry.wallpaperskew** (float x, float y) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.wallpaperskew=1,0.5)

Sets the custom wallpaper symmetry skew  
  

**symmetry.colorshift.hue** (string mode, float amplitude, float frequency) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.colorshift.hue=Noise,1,2)

Sets the custom wallpaper color shift hue (mode is one of SineWave, SquareWave, SawtoothWave, TriangleWave, Noise)  
  

**symmetry.colorshift.saturation** (string mode, float amplitude, float frequency) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.colorshift.saturation=SineWave,0.1,1)

Sets the custom wallpaper color shift saturation (mode is one of SineWave, SquareWave, SawtoothWave, TriangleWave, Noise)  
  

**symmetry.colorshift.brightness** (string mode, float amplitude, float frequency) [Try it](http://localhost:40074/api/v1?/api/v1?symmetry.colorshift.brightness=SquareWave,0.5,6)

Sets the custom wallpaper color shift brightness (mode is one of SineWave, SquareWave, SawtoothWave, TriangleWave, Noise)  
  

**multiplayer.join** (string nickname, string roomName, Boolean isPrivate, int maxPlayers, Boolean silentRoom, Boolean viewOnlyRoom) [Try it](http://localhost:40074/api/v1?/api/v1?multiplayer.join)

Joins a multiplayer room  
  

**multiplayer.leave** [Try it](http://localhost:40074/api/v1?/api/v1?multiplayer.leave)

Leaves a multiplayer room  
  

**tool.sketchsurface** [Try it](http://localhost:40074/api/v1?/api/v1?tool.sketchsurface)

Activates the SketchSurface  
  

**tool.selection** [Try it](http://localhost:40074/api/v1?/api/v1?tool.selection)

Activates the Selection Tool  
  

**tool.colorpicker** [Try it](http://localhost:40074/api/v1?/api/v1?tool.colorpicker)

Activates the Color Picker  
  

**tool.brushpicker** [Try it](http://localhost:40074/api/v1?/api/v1?tool.brushpicker)

Activates the Brush Picker  
  

**tool.brushandcolorpicker** [Try it](http://localhost:40074/api/v1?/api/v1?tool.brushandcolorpicker)

Activates the Brush And Color Picker  
  

**tool.sketchorigin** [Try it](http://localhost:40074/api/v1?/api/v1?tool.sketchorigin)

Activates the SketchOrigin Tool  
  

**tool.autogif** [Try it](http://localhost:40074/api/v1?/api/v1?tool.autogif)

Activates the AutoGif Tool  
  

**tool.canvas** [Try it](http://localhost:40074/api/v1?/api/v1?tool.canvas)

Activates the Canvas Tool  
  

**tool.transform** [Try it](http://localhost:40074/api/v1?/api/v1?tool.transform)

Activates the Transform Tool  
  

**tool.stamp** [Try it](http://localhost:40074/api/v1?/api/v1?tool.stamp)

Activates the Stamp Tool  
  

**tool.freepaint** [Try it](http://localhost:40074/api/v1?/api/v1?tool.freepaint)

Activates the FreePaint Tool  
  

**tool.eraser** [Try it](http://localhost:40074/api/v1?/api/v1?tool.eraser)

Activates the Eraser Tool  
  

**tool.screenshot** [Try it](http://localhost:40074/api/v1?/api/v1?tool.screenshot)

Activates the Screenshot Tool  
  

**tool.dropper** [Try it](http://localhost:40074/api/v1?/api/v1?tool.dropper)

Activates the Dropper Tool  
  

**tool.saveicon** [Try it](http://localhost:40074/api/v1?/api/v1?tool.saveicon)

Activates the SaveIcon Tool  
  

**tool.threedofviewing** [Try it](http://localhost:40074/api/v1?/api/v1?tool.threedofviewing)

Activates the ThreeDofViewing Tool  
  

**tool.multicam** [Try it](http://localhost:40074/api/v1?/api/v1?tool.multicam)

Activates the MultiCam Tool  
  

**tool.teleport** [Try it](http://localhost:40074/api/v1?/api/v1?tool.teleport)

Activates the Teleport Tool  
  

**tool.repaint** [Try it](http://localhost:40074/api/v1?/api/v1?tool.repaint)

Activates the Repaint Tool  
  

**tool.recolor** [Try it](http://localhost:40074/api/v1?/api/v1?tool.recolor)

Activates the Recolor Tool  
  

**tool.rebrush** [Try it](http://localhost:40074/api/v1?/api/v1?tool.rebrush)

Activates the Rebrush Tool  
  

**tool.pin** [Try it](http://localhost:40074/api/v1?/api/v1?tool.pin)

Activates the Pin Tool  
  

**tool.camerapath** [Try it](http://localhost:40074/api/v1?/api/v1?tool.camerapath)

Activates the CameraPath Tool  
  

**tool.fly** [Try it](http://localhost:40074/api/v1?/api/v1?tool.fly)

Activates the Fly Tool  
  

**snap.angle** (string angle) [Try it](http://localhost:40074/api/v1?/api/v1?snap.angle=15)

Sets the current snapping angle. Angle must be a supported value (15, 30, 45, 60, 75 or 90)  
  

**snap.grid** (string size) [Try it](http://localhost:40074/api/v1?/api/v1?snap.grid=5)

Sets the current snapping grid. Size must be a supported value (0.1, 0.25, 0.5 ,1, 2, 3, 5  
  

**selection.snap.angles** [Try it](http://localhost:40074/api/v1?/api/v1?selection.snap.angles)

Applies the current snap angle to all selected objects  
  

**selection.snap.positions** [Try it](http://localhost:40074/api/v1?/api/v1?selection.snap.positions)

Applies the current snap grid to all selected objects  
  

**selection.align** (string axis, string alignBy) [Try it](http://localhost:40074/api/v1?/api/v1?selection.align=x,center)

Aligns all selected objects to the given axis using their minimum, center or maximum points

