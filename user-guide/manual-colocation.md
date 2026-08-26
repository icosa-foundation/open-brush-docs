---
description: Align a multiplayer scene for several headsets sharing the same physical room.
---

# Manual Colocation

Manual colocation aligns the Open Brush scene for multiplayer participants who are in the same physical room. Each person measures the same two real-world points, allowing Open Brush to calculate how their tracked play spaces relate to one another.

{% hint style="warning" %}
Choose a reference that everyone can reach safely without colliding with another person, furniture or a wall. Continue to follow each headset's boundary and safety guidance after alignment.
{% endhint %}

## Choose a shared reference

Choose two recognizable endpoints on a stable, mostly horizontal real-world object, such as the corners of a table edge.

1. The endpoints must be at least `0.1` metres apart.
2. Use points with enough horizontal separation for Open Brush to determine the room's direction reliably.
3. Everyone must measure the same endpoints in the same **A-to-B** order.

## Set the shared alignment

The owner of the multiplayer room creates the reference:

1. Join the same [multiplayer room](multiplayer.md) as the other participants.
2. On the Multiplayer panel, select **Set Shared Alignment**.
3. Place the tip of the brush controller at endpoint A and pull the trigger.
4. Place the controller tip at endpoint B and pull the trigger.
5. Check that the displayed arrow points from A to B.
6. Pull the brush-controller trigger to confirm. Pull the other controller's trigger to swap A and B, or cancel and repeat the measurement.

The Multiplayer panel reports **Shared alignment ready** when the reference has been sent to the room.

## Align each participant

Each other participant then measures the reference from their own tracked play space:

1. On the Multiplayer panel, select **Align Play Space**.
2. Record endpoints A and B in the same order used by the room owner.
3. Check the arrow and confirm the measurement.
4. Confirm that the Multiplayer panel reports **Play space aligned**.

Open Brush moves the participant's virtual scene to match the shared reference. It does not change the headset's guardian or boundary.

## Realign or reset

Select **Realign Play Space** if tracking changes or the scene no longer matches the physical reference. If the room owner replaces the reference, other participants see **Alignment changed — realign** and must repeat their measurement.

The room owner can select **Reset Shared Alignment** to remove the current reference. Moving or scaling the scene invalidates an existing alignment and may require the owner to set it again.

Manual colocation data applies only to the current multiplayer room and is cleared when the room session ends.
