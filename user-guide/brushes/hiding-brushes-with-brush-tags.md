# Hiding Brushes with Brush Tags

Currently the brush panel is cluttered with a large number of brushes and is likely to grow larger in the future. As a first step toward better organizing them, this feature serves to classify each brush with a list of tags and a couple of filtering options.

Via OpenBrush.cfg (UserConfig), the brushes that show up in the panel can be limited by using the following options:

1. IncludeTags - specifies all of the brushes that may be included included in the panel
2. ExcludeTags - specifies all of the brush that must be excluded (even if they are also in "include").

To test, try the following:

* Declare include\
  `{ "User": { }, "Brushes": { "IncludeTags": ["classroom"], }, "Video": { }, "Flags": { }, "Export": { }, }`\
  Result should be only a single page of brushes that have been tagged with "classroom".
* Add a new tag called "test" to a few brush descriptors that also have "classroom" and then declare inlude and exclude\
  `{ "User": { }, "Brushes": { "IncludeTags": ["classroom"], "ExcludeTags": ["test"] }, "Video": { }, "Flags": { }, "Export": { }, }`\
  Result should be only a single page of brushes that have been tagged with "classroom" minus the brush tagged with "test".
* Exclude only case\
  `{ "User": { }, "Brushes": { "ExcludeTags": ["classroom"] }, "Video": { }, "Flags": { }, "Export": { }, }`\
  Result should be all of the brushes minus those tagged with classroom.

In addition, tags can be added and removed. Here is an example that includes this usage:

```
{
	"User": {
	},
	"Brushes": {
		"AddTagsToBrushes": {
			"Rainbow": ["classroom", "bedazzling"],
			"Plasma": ["classroom", "bedazzling"],
			"testBrushNotFound": ["classroom"]
		},
		"RemoveTagsFromBrushes": {
			"Rainbow": ["default", "test"],
			"Plasma": ["default", "test"],
			"testBrushNotFound": ["classroom"]
		},
		"IncludeTags": ["classroom"],
		"ExcludeTags": ["test"] 
	},
	"Video": {
	},
	"Flags": {
	},
	"Export": {
	},
}
```
