# Open Brush AsCanvas Notes

AsCanvas\[pointer.transform] = foo _(where foo is in Canvas space)_:

Sets pointer transform to foo

RHS convert transform to canvas space TrTransform:

* TrTransform xf\_CS = Coords.AsCanvas\[transform]; // Get transform in canvas space, and write to scene.
* TrTransform rAttachPoint\_CS = App.Scene.ActiveCanvas.AsCanvas\[InputManager.Brush.Geometry.ToolAttachPoint];
* m\_xfLocal = m\_canvas.AsCanvas\[transform];
* TrTransform xf\_CS = canvas.AsCanvas\[p.m\_Script.transform];
* m\_Pointers\[i].m\_StraightEdgeXf\_CS = Coords.AsCanvas\[m\_Pointers\[i].m\_Script.transform];
* var xfPointer\_CS = canvas.AsCanvas\[script.transform];
* TrTransform xf\_CS = Coords.AsCanvas\[TransformForStroke(stroke)];
* return Coords.AsCanvas\[InputManager.m\_Instance.GetBrushControllerAttachPoint()].translation;
* m\_vOriginalPos\_CS = Coords.AsCanvas\[transform].translation;
* var xf\_CS = Coords.AsCanvas\[transform];

LHS convert canvas space TrTransform to transform:

* m\_canvas.AsCanvas\[transform] = m\_xfLocal;
* canvas.AsCanvas\[m\_MainPointerData.m\_Script.transform] = mainPointerXf\_CS;
* Coords.AsCanvas\[transform] = xf\_CS;
* return ChangeBasis(App.Scene.AsScene\[xfInput], basis, basisInverse)
* m\_Rotation\_SS = App.Scene.AsScene\[transform].rotation;
* CanvasTransformInSceneSpace = App.Scene.AsScene\[App.Instance.m\_CanvasTransform],
* m\_Transform\_SS = App.Scene.AsScene\[m\_Owner];
* Vector3 vOwnerEulers\_SS = App.Scene.AsScene\[m\_Owner].rotation.eulerAngles;
* App.Scene.AsScene\[transform] = m\_Transform\_SS;
