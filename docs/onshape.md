# Using the models in Onshape

English | [日本語](onshape.ja.md)

## Import

1. In an Onshape document, click **+** in the tab bar at the bottom left, choose **Import…**, and select the STEP file
   (`<MODEL>.step`, for example `BCAP091207G.step`).
2. Import options:
   - Do **not** flatten the assembly into a single Part Studio. Keeping the assembly keeps one part per component,
     with its name.
   - Do **not** check **Y Axis is up**. The models use +Z up.
   - The STEP file is in millimeters. If Onshape asks for units, choose millimeters.
3. Onshape creates a Part Studio (the geometry) and an Assembly (the placement). Parts are named `<MODEL>_<Role>`,
   for example `BCAP091207G_Base`, `BCAP091207G_TopCover`, `BCAP091207G_Gasket`, `BCAP091207G_Latch`.
   When a role appears more than once, `_1`, `_2`, … is added (for example `BCAP091207G_InsertNutM4_1`).
   All parts are already in the closed position, so you can check fit and interference right away.
4. In the Assembly, **Fix** the base (`<MODEL>_Base`). Fasten the gasket and the insert nuts to the base, and the latch
   (closed position) to the base or the cover, with **Fastened** mates.
5. Clear-cover variants carry the cover color and transparency in the STEP file. If the cover does not look
   transparent, set its **Appearance** in the Assembly (the colors are listed in `manifest.json`).
6. To add holes, connectors or glands, edit the imported parts in the Part Studio, or model the cutting shapes in a new
   Part Studio and remove them with **Boolean → Subtract**.

The screws supplied with the box are not modeled. Use Onshape standard content instead.

## Coordinate system

- Origin: center of the bottom outer face of the base (feet not included)
- +Z: up (toward the cover)
- +X: along the long side of the box
- +Y: toward the hinge (the latch is on the −Y side)
- Units: mm

Each model's README lists the catalog dimensions (W × D × H) and the overall size including ears, hinge, latch and
feet, with the model axis of each dimension.

## Hinge (revolute mate)

The hinge axis and the maximum opening angle of each model are in [`manifest.json`](../manifest.json), under
`models.<BASE>.hinge`:

- `point_mm`: a point on the axis (mm)
- `axis`: the direction of the axis
- `max_open_deg`: the maximum opening angle in degrees (0° = closed)

To make the cover open and close:

1. In the Assembly, fix the base.
2. Place a **Mate connector** on the circular edge of the hinge pin hole in a base knuckle. Its origin must lie on the
   hinge axis and its Z axis must point along the axis direction; use **Flip primary axis** if needed.
3. Place a Mate connector the same way on the circular edge of the pin hole in a cover knuckle.
4. Select both Mate connectors and create a **Revolute** mate. Under **Limits**, set 0° to `max_open_deg`.
5. The latch is modeled in its closed position. Suppress (or delete) the latch's Fastened mate before you open the
   cover.
