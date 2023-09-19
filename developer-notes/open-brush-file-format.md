# Open Brush File Format

The .tilt file format can also be parsed by the [Open Brush Toolkit](https://github.com/icosa-foundation/open-brush-toolkit).

A .tilt is a zip-format file with a prepended header:

```
uint32 sentinel ('tilT')
uint16 header_size (currently 16)
uint16 header_version (currently 1)
uint32 reserved
uint32 reserved
```

Inside the zip, the strokes are stored in a custom binary format in a file, "data.sketch":

```
uint32 sentinel
uint32 version
uint32 reserved (must be 0)
[ uint32 size + <size> bytes of additional header data ]
int32 num_strokes
num_strokes * {
    int32 brush_index
    float32x4 brush_color
    float32 brush_size
    uint32 stroke_extension_mask
    uint32 controlpoint_extension_mask
    [ int32/float32 for each set bit in stroke_extension_mask & ffff ]
    [ uint32 size + <size> bytes for each set bit in stroke_extension_mask & ~ffff ]
    int32 num_control_points
    num_control_points * {
        float32x3 position
        float32x4 orientation (quat)
        [ int32/float32 for each set bit in controlpoint_extension_mask ]
    }
}
```

The orientation is that of the controller. Curve and surface frames must be reconstructed.

Stroke extensions:

| 0 | <p>uint32 bitfield.<br>Bit 0: IsGroupContinue</p> |
| - | ------------------------------------------------- |

Control point extensions:

| 0 | float pressure, in \[0,1]         |
| - | --------------------------------- |
| 1 | uint32 timestamp, in milliseconds |

###

Also inside the zip is "metadata.json", the metadata for the sketch in json format. Here are some of the fields that can be found there:

* "Authors": an array of author names.
* "SceneTransformInRoomSpace": the transform of the scene relative to the room.
* "ThumbnailCameraTransformInRoomSpace": the transform used to generate the sketch as an array of:
  * translation (array of 3 floats)
  * rotation quaternion (array of 4 floats)
  * scale (single float)
* "ModelIndex": an array of models imported into the sketch. Each model can have the following:
  * "FilePath": location of the model
  * "PinStates": an array to indicate whether each instance of the model should initially be pinned.
  * "RawTransforms": an array of transforms for each instance of the model.
