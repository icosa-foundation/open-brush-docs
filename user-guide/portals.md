---
description: Add a portal widget that links the current sketch to an Icosa Gallery sketch.
---

# Portals Between Sketches

A portal is a spherical widget that links the current sketch to another sketch on the Icosa Gallery. Its surface displays the destination sketch's thumbnail; activating it loads that sketch.

## Requirements

1. The destination must appear in the **Curated** or **Liked** section of the Sketchbook. Local sketches cannot currently be used as portal destinations.
2. Open Brush needs an internet connection to retrieve the destination from Icosa Gallery.
3. Save changes to the current sketch before testing a portal. Activating it loads another sketch and may show the normal unsaved-changes confirmation.

## Add a portal

1. Open the Sketchbook.
2. Open **Curated** or **Liked**.
3. Open the options menu for the destination sketch.
4. Select **Drop Portal**.
5. Move and scale the portal like another widget. Pin it if you do not want it to be moved accidentally.
6. Save the current sketch to store the portal and its destination.

## Use a portal

Point the brush controller at the portal and pull the trigger. Open Brush downloads the destination if necessary and then loads it. The portal changes appearance while loading is in progress.

Portal links use the destination's Icosa asset ID. A portal will stop working if that asset is removed or can no longer be downloaded.

## API

The HTTP API can add a portal at the current brush position with an Icosa asset ID:

```text
http://localhost:40074/api/v1?portal.add=dLHpzNdygsg
```

See [Open Brush API](open-brush-api/) for API setup and security guidance.
