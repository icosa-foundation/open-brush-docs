# Exporting to Unreal Engine 5

How to Import OpenBrush FBX files & edit Materials to appear correctly



![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FkRkVXx2MkXIuOloJuTV7%2FScreenshot%202023-05-05%20222604.jpg?alt=media\&token=f08a5e37-af5a-4481-8e3a-e1a6cc192160)

This example uses models that are best viewed without lighting. In UE5's scene view, change the scene lighting to "UNLIT" (top left of window).

* Drag the FBX from Windows Explorer into the UE5 scene
*   An FBX Import Option menu will come up:\


    ![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FFebVYMEpHhxOchxxG7Yj%2FScreenshot%202023-05-05%20215751.jpg?alt=media\&token=347c89bd-9b4d-4c8e-a338-70807f90a656)

    Make sure to select: **Advanced > Vertex Color Import Option \[REPLACE]**

### **Organize Materials, Textures, Mesh Files** <a href="#organize-materials-textures-mesh-files" id="organize-materials-textures-mesh-files"></a>

* Upon importing the FBX, the _Content Drawer_ will include the meshes and materials
* Create a subfolder for _MATERIALS_ and _TEXTURES_
*   Select the imported materials, drag and drop them into the newly created _MATERIALS folder_\


    ![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FST98BqelmVs2ygQ6Y7n6%2FScreenshot%202023-05-05%20215933.jpg?alt=media\&token=988b40d5-9ac2-4b56-ae0a-5ae45d9ac916)
*   The materials are pretty terribly named. I highly recommend renaming them. The brush material names are at the end of the filename:\


    ![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FWub9i586PvNyNN1sWLDQ%2FScreenshot%202023-05-05%20220129.jpg?alt=media\&token=b5fa9c66-c197-4fca-8c5b-c3ffa248a564)
*   From Windows Explorer, drag optimized PNG brush textures into the UE5 _TEXTURES_ folder:\


    ![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2F9bWgd6txMPp3SuHGhkLl%2FScreenshot%202023-05-05%20220218.jpg?alt=media\&token=2321168b-56de-4167-ad08-a147ba1968af)
*   From the _CONTENT DRAWER_, drag and drop the meshes into the scene. I recommend creating a folder in the _OUTLINER_ window and drag all the mesh objects into there:\


    ![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FFMsxcrCeMilX7gJOLZ4r%2FScreenshot%202023-05-05%20220354.jpg?alt=media\&token=48f409bc-cf39-458c-9077-72ebcb494b99)

    Selecting all the model mesh objects, it may help to update these DETAILS:

    Location: 0,0,0 Scale: 0.5,0.5,0.5
*   I also recommend turning off visibility of all the other non-mesh objects in the OUTLINER tab (e.g. Atmospheric Fog, Floor, etc.)\


    ![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FNPC8emFoPDSDcaTQyZdX%2FScreenshot%202023-05-05%20225156.jpg?alt=media\&token=93ef74b7-be01-43a8-82c5-7c27aba61833)

### Associate Vertex Colors, Textures, Opacity to Materials <a href="#associate-vertex-colors-textures-opacity-to-materials" id="associate-vertex-colors-textures-opacity-to-materials"></a>

**Edit Vertex Colors to Materials that&#x20;**_**only**_**&#x20;need Vertex Colors:**

| Material Name | NODE: Vertex Color | NODE: Texture Sample | Material Details               |
| ------------- | ------------------ | -------------------- | ------------------------------ |
| **Flat**      | ✓                  | No                   | Blend Mode: MASKED ☑ Two Sided |
| **MatteHull** | ✓                  | No                   | Blend Mode: MASKED ☑ Two Sided |
| **UnlitHull** | ✓                  | No                   | Blend Mode: MASKED ☑ Two Sided |
| **Wire**      | ✓                  | No                   | Blend Mode: MASKED ☑ Two Sided |

* In CONTENT DRAWER > _MATERIALS,_ double click the "Flat" material file. The Material Graph window will popup
* Right click on the empty grid, type in _VERTEX COLOR_ to add the node

![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FP7tT78fJ5mzKgFQZWM0J%2FScreenshot%202023-05-05%20220633.jpg?alt=media\&token=2fcf371d-53d9-4203-89d6-aca96c20a014)

Connect the top white dot to _BASE COLOR_ in the "_FLAT"_ window.

* Click on "FLAT" so you can see its _DETAILS_ on the left menu
* Update: **BLEND MODE** - MASKED **Two Sided** - \[checked]​

![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2F5av9FwwAHqyXxO72CNgw%2FScreenshot%202023-05-05%20220705.jpg?alt=media\&token=d3bfb309-a40b-42ce-bf34-311315300702)

That's it! Be sure to save these edits or CTRL + S. The edits won't show up on the main scene window until these Material changes are saved.

* Repeat for the other three materials listed above that only need Vertex Colors associated to the materials.

**Edit Materials that need Vertex Colors and Texture Sample:**

| Material Name           | NODE: Vertex Color | NODE: Texture Sample            | Material Details               |
| ----------------------- | ------------------ | ------------------------------- | ------------------------------ |
| **DiamondHull**         | ✓                  | ✓ RGBA connects to Opacity Mask | Blend Mode: MASKED ☑ Two Sided |
| **Dots**                | ✓                  | ✓ RGBA connects to Opacity Mask | Blend Mode: MASKED ☑ Two Sided |
| **DoubleTaperedMarker** | ✓                  | ✓ RGBA connects to Opacity Mask | Blend Mode: MASKED ☑ Two Sided |
| **Embers**              | ✓                  | ✓ RGBA connects to Opacity Mask | Blend Mode: MASKED ☑ Two Sided |
| **Marker**              | ✓                  | ✓ RGBA connects to Opacity Mask | Blend Mode: MASKED ☑ Two Sided |

* Do the same steps above to add VERTEX COLOR to the BASE COLOR
* Do the same steps above to update the Material Details to (same as before): **BLEND MODE** - MASKED **Two Sided** - \[checked]
*   Right click the empty grid space and type in _TEXTURE SAMPLE_ to bring up a node where you'll associate the texture png files

    ![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FY9aKjPnA0vJEtSLE075K%2FScreenshot%202023-05-05%20221053.jpg?alt=media\&token=2ec21675-c44a-4750-88dd-4bf506f68a2c)

    * Click on the _TEXTURE SAMPLE_ node window so you can edit the _DETAILS_
    * In the section for "Material Expression Texture Base" click on the dropdown to select the texture name that matches with the material name.
      * _NOTE_: The DoubleTaperedMarker material can use the "Marker" texture
    * Connect the _TEXTURE SAMPLE_ node's "RGBA" dot to the Material's "Opacity Mask" dot
* REPEAT for the other materials with same properties

**Edit Materials that need Vertex Colors, Texture Sample, and Transparency:**

| Material Name       | NODE: Vertex Color | NODE: Texture Sample       | Material Details                 |
| ------------------- | ------------------ | -------------------------- | -------------------------------- |
| **Highlighter**     | ✓                  | ✓ RGBA connects to Opacity | Blend Mode: ADDITIVE ☑ Two Sided |
| **Smoke**           | ✓                  | ✓ RGBA connects to Opacity | Blend Mode: ADDITIVE ☑ Two Sided |
| **SoftHighlighter** | ✓                  | ✓ RGBA connects to Opacity | Blend Mode: ADDITIVE ☑ Two Sided |

* Do the same steps above to add VERTEX COLOR to the BASE COLOR
* Update the Material Details: **BLEND MODE** - ADDITIVE **Two Sided** - \[checked] "Additive" will allow these brushes to appear semi-transparent, foggy, smokey.
* Do the same steps as above to associate textures to _TEXTURE SAMPLE_ node



![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2FTCcrdBSQBMXdwdldCZB9%2FScreenshot%202023-05-05%20212407.jpg?alt=media\&token=246a4126-6918-4135-90d1-553dad9b84b4)

* Connect the _TEXTURE SAMPLE_ node's "RGBA" dot to the Material's **"Opacity"** \[not Opacity Mask as previous materials]
* REPEAT for the other materials with same properties

Make sure to save all of your Material window edits!

![](https://1248961711-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F6yJRiXJ9mfWMFMmMQFtp%2Fuploads%2Fvasxa7HekBGRzRpnfI2w%2FScreenshot%202023-05-05%20212146.jpg?alt=media\&token=eac53147-8515-4b30-8dd7-cc1f0aa9e1dc)

Make sure to view this in "unlit" mode.

Also hide the Light Source, etc to prevent any shadows from showing up in the scene.

Reward yourself with ice cream.

_Docs contributed by_ [_Estella Tse_](https://www.estellatse.com/)_. Additional thanks to_ [_Steve Bowler_](https://www.linkedin.com/in/stevebowler/)&#x20;
