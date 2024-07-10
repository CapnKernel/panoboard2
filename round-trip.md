# A KiCad/FreeCAD board outline round trip.

In KiCad:

 - Mave board edges on `Edge.Cuts`, and slots on `User.Drawings`.
 - Modify these layers as desired.
 - Align top corner board to some well-defined point, such as (50, 30).
 - Set origin (`S`) to this point.

In FreeCAD:

 - Select KiCadStepUp workbench
 - ksu PushPull > Pull sketch from PCB
   - Edge cuts
   - replace PCB and Sketch in current document
   - Select `.kicad_pcb` file.
   - Set Z=1
 - Drill down into loaded PCB, find `PCB_Sketch_\n+` file.
 - File > Import
   - Choose original board picture.  Transform to align with imported outline.  Z=-1
 - Create 3D model of board using sketches, pads and pockets.
 - Click on final operation, and choose Draft workbench.
   - Modification > Shape 2D view
   - Modification > Draft to sketch
 - Choose KiCadStepUp workbench
 - Click on resultant sketch
 - ksu PushPull > Push sketch to PCB
   - Edge.Cuts
   - Select `.kicad_pcb` file.
 - Hide all visible objects
 - ksu PushPull > Pull sketch from PCB
   - Dwgs.User
   - import Layer in active document
   - Select `.kicad_pcb` file.
 - Part workbench
 - Click on `Dwgs.User` object
 - Part > 2D offset
   - Offset 0.5mm
   - Intersection
 - Expand Offset2D object, and deselect Dwgs.User object
 - Click on Offset2D layer
 - Choose Draft workbench.
 - Modification > Draft to sketch
 - Click on resultant sketch
 - Choose KiCadStepUp workbench
 - Push sketch to PCB
   - Eco1.User
   - Select `.kicad_pcb` file.

In KiCad:
 - Turn off all layers, turn on User.Eco1 layer
 - Select slot strokes from User.Eco1 layer
 - Change layer in Properties Manager to Edge.Cuts
 - Turn on all layers and verify appearance
 - Examine board in 3D viewer to confirm valid shape

