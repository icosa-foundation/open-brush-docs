# PseudoCode

## Creation of rendering data from input

* Input comes in from a user, makes its way to a pointer.
  * A modal painting tool \(e.g. `FreePaintTool`\) processes user input and feeds it to the pointer.
  * There may be multiple pointers depending on the drawing mode, e.g. symmetry.
* The pointer deals with creating/finalizing `BaseBrushScript` instances. 
  * The pointer also deals with remembering which control points were used. This is a little gross though; see `UpdateLineFromObject`. The pointer assumes that the BBS will use a piece of input, and it's up to the BBS to tell it "I used new input to over-write the last quad/whatever" or "I used your input to create an all-new quad", which has implications for which control points the pointer keeps around. Lots of potential for off-by-one errors and so on.
* Eventually the user lets go of the trigger, the `PointerScript` terminates the line, deals with off-by-one issues in its control point array, arranges for the geometry in the brush to be finalized into a `GameObject`/batch, for the control points to be finalized into a stroke, puts the stroke into the memory, and so on.

## Loading Data

Or we could be loading from a file, in which case the work is substantially similar:

* We reuse `PointerScript` to load from files and kind of trick it into thinking that it's being driven from a user;
  * but there are hacks to ensure that the `BaseBrushScript` doesn't reject any control points coming in.
  * And there are some other hacks to allow brushes to try to process a whole batch of control point input at once instead of one-at-a-time. This was one of the main motivations for `GeometryBrush`; a brush should:
    1. not do O\(n\) work for each new control point, 
    2. be able to process a group of control points at once instead of doing O\(n\) updates. Updating "stretch" UVs is obviously always going to be O\(n\) so there are some other hacks to defer that generation until "update visuals" gets called. Maybe some other things. Anyway, there are mechanisms to prevent O\(n^2\) behaviour on load. Similarly, you wouldn't want your hull brush to compute a hull N times when loading. Something to think about when writing a geometry generator.

