Logic blocks
============

Version 23
----------

.. _logic-blocks-1:

1 Logic Blocks
--------------

1.1 The Logic Block System
~~~~~~~~~~~~~~~~~~~~~~~~~~

The Logic Block System has been developed for the construction program:

▪ Logic Blocks are compound entities consisting of 3D Objects,
processes, 2D drawing objects, dimension lines, text and labels, which
are connected by logic functions and conditions.

▪ Once inserted, Logic Blocks can be re-calculated in order to adjust to
changes in the building. Re- calculating offers the same options as
inserting the Logic Blocks from scratch.

▪ When they are edited, moved, deleted, etc. Logic Blocks behave like
one entity. On top of that it is also possible to edit individual items
inside the Logic Block with standard features.

▪ The re-calculation feature of Logic Blocks may be overcome by
disbanding the Logic block.

▪ Logic Blocks are used to develop custom solutions for individual
clients without extensive programming skills. With the correct module
configuration you will be able to edit existing Logic Blocks or to
develop your own.

▪ Standard design routines and tasks can be automated and streamlined by
the use of Logic Blocks.

**1.1.1 Authorizations for Logic Blocks**

::

   ▪ In order to use, insert, existing Logic Blocks in most cases it is sufficient to have access to the
   relevant program modules. E.g. users who have access to the module 'ground plan' can use
   the furniture Logic Blocks that come with the standard release.
   ▪ In order to use Logic Blocks in D-CAM (7- 8 - 1) 'at point, object', D-CAM Pro is minimum
   requirement.
   ▪ To create new or adjust existing Logic Blocks D-CAM Premium is required. Contact your
   Dietrich’s representative to find out how Logic Blocks may apply to your design needs.

::

   ▪ Users with D-CAM Premium can adjust existing LB to their own need or develop new LB from
   scratch.

10.
^^^

::

   Contact your Dietrich’s representative to find out how Logic Blocks may apply to your design
   needs.

.. _section-1:

10.
^^^

::

   Special Notes:

::

   Generally Logic Blocks will only apply if the required module configuration is available:
   ▪ D-CAM Professional for profiled cross section beams. D-CAM the logic block will create a beam
   with a circumscribing rectangular cross section instead.
   ▪ D-CAM Professional or Metal Connector Catalogue for Metal Connectors
   ▪ Users without the access to wall design (D-Wall Pro) cannot create beams inside a wall
   (position of the beam’s axis is relevant)

::

   ▪ This limitation applies independent of the function you use to insert it: along wall, in plan
   or at doors/ windows.
   ▪ This limitation applies independent of object type (beam, sheathing ...).

.. _section-2:

10.
^^^

::

   ▪ You will be able to use Logic Blocks for furniture, sanitary object and electric installation
   without having access to D-Wall Pro though.

::

   User to User Applications:
   ▪ Users with D-CAM Premium can adjust existing LB to their own needs or develop new LB from
   scratch.
   ▪ Logic Block that have be created or edited like this can be forwarded to other users for their
   own purposes.
   ▪ If a Logic Block requires certain module configuration in order to be used properly these
   conditions will still apply after the Logic Block has been edited.

.. _section-3:

11.
^^^

1.2 Logic Blocks in Superordinate Functions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

   Logic Blocks will be moved, copied and mirrored with building parts. They will also be saved with
   building library elements. The following rules and conditions apply:
   ▪ Affected Logic Blocks may belong to storeys, walls, wall openings (windows, doors)
   ▪ If a Logic Block is defined by prompting the user to select objects, all prompted objects have
   to be part of the selection, otherwise the Logic Block will not be affected.
   ▪ After a mirroring process, Logic Block will be recalculated. They need to be checked
   afterwards, since the alignment of objects and the orientation of doors and windows may
   have changed.

::

   ▪ Logic Blocks cannot be edited with the D-CAM 2-Edit menu functions. These functions will only
   apply to individual objects. Once the Logic Block is recalculated the changes will be reset.
   Copies and mirrored objects contain no Logic Block information any more. This also applies if
   a Logic Block created a component or has been taken from a library.

.. _section-4:

11.
^^^

**1.2.1 Logic Blocks at Windows and Doors**

::

   Logic blocks at windows and doors can be recalculated, edited and deleted. The opening
   definition does not have to be edited any more to achieve this. Logic block can be edited from
   ground plan or wall design.
   ▪ Direct recalculation with 7- 9 - 1 e.g. after a wall guideline has been applied and objects at
   windows have to be recalculated.

::

   ▪ Direct edit with 7- 9 - 4 e.g. you want to change the window blinds etc.
   ▪ Direct delete with 7- 9 - 7 will also delete LB from windows and doors

.. _section-5:

11.
^^^

2 Logic Blocks: Basic Technologies
----------------------------------

2.1 Building Parts (BP), Basic-Building Part, Additional Building Parts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The **Basic Building Part** is determined by combination of current
program module and logic block type. E.g. if a Logic Block is defined in
the wall design module the current wall is the Basic Building Part.
Nevertheless, the same logic block can also be used in order to insert
objects into other building parts. If, apart from the basic building
part, other building parts are used, they are the “Additional building
parts”. Additional building parts can be identified while adding
Objects, Library Parts, Drawing Sections, Dimension Lines, Labels and
Text.

**2.1.1 Basic-Building Parts**

Module Function Basic-BP

Ground Plan in ground current storey along wall edge selected wall along
truss edge selected truss

Wall Design Front side current wall reverse side current wall at points,
objects current wall

Ceiling Area in ground current storey

Ceiling Design in ground current ceiling area at points, objects current
ceiling area

Roof Calculation in ground current roof along truss edge selected truss
in roof surface selected roof surface

Roof Design in ground current roof along truss edge selected truss in
roof surface selected roof surface at points, objects current roof

Truss Design Front side current truss reverse side current truss at
points, objects current truss

D-CAM free design at point, object D-CAM free design

**2.1.2 Additional Building Parts (BP)**

Objects may be assigned to additional building parts by inserting them
into a:

::

   1 storey
   2 roof
   3 wall
   4 adjacent wall
   5 current/ lower ceiling
   6 upper ceiling
   7 roof surface
   8 Truss Design
   9 D-CAM free design

If the desired building part is not the basic building part, then it is
an additional building part that has to be determined first. To do this
several routines have been developed which depend on the combination of
program module, basic building part and LB-type.

For LBs inserted ‘at point, object’ the routine is different from other
LB types and is explained at the end of this section.

2.1.2.1 Additional building parts: Storeys

▪ The current storey is precisely defined in the modules ground plan,
wall design, ceiling areas and ceiling design.

▪ If the basic building part is a truss which belongs to a storey, the
storey is an additional building part, independent from the program
module.

▪ In the program modules roof calculation and roof design: The current
storey from program module floor plan

▪ In the program modules roof calculation and roof design, LB is
inserted ‘in roof surface’, the next lower storey below the point of
insertion will represent an additional BP. The bottom edge of the storey
is relevant to determine the next lower storey.

▪ If a truss which belongs to the roof is the basic BP, the next lower
storey below the point of insertion will represent an additional BP. The
bottom edge of the storey is relevant to determine the next lower
storey.

2.1.2.2 Additional Building Part: Roof

▪ At the moment the roof is precisely defined since there can be only
one roof.

2.1.2.3 Additional Building Part: Wall

▪ A wall can be an additional BP only for LBs that are inserted ‘at
point, object’. Rules: See below

2.1.2.4 Additional Building Part: Adjacent Wall

▪ An adjacent wall will be identified automatically, only if the basic
BP is a Wall. This means only if you insert along an edge of a wall or
in wall design.

▪ The routine will look for an adjacent wall in a plan view.

::

   ▪ It will take all walls of the current storey into consideration.
   ▪ The walls don't necessarily need to be connected with a corner or T-joint.
   ▪ Starting from the insertion coordinate system it will look for the next closest wall.

::

   ▪ The routine will identify walls in corner and t-joint like situations. It will also detect walls parallel to
   the current one.

▪ There are a number of system variables regarding walls and adjacent
walls:

::

   SP00X The distance of the insertion-CS to the intersection of the 0-slices of the two walls taken in
   X direction. Depending on where the LB is inserted (front side or reverse side) the front or
   the back of slice 0 of the current wall will be taken into regard. On the adjacent wall it will
   always take the front of slice 0.

::

   WWXY Angle between the X axes of the two walls in plan view (XoY). The result will be between
   0° and 180° counter clock wise and 0° to -180° clockwise. If the LB is inserted on the
   reverse side of the wall the coordinate system of the wall will change accordingly and the
   X-axis will run opposite to the front side CS.
   WELR Indicates which end of the wall is closer to the Insertion-CS: -1 (left end) wall origin is
   closer, +1 (right end) wall end is closer. If you insert on the reverse side, the rotated CS of
   the wall becomes relevant: -1 (left end) wall end is closer, +1 (right end) wall origin is
   closer
   A_SP00X The distance in the adjacent wall between the projection of the insertion coordinate system
   to the intersection of the 0-slices of the two walls taken in X direction. Depending on where
   the LB is inserted (front side or reverse side) the front or the back of slice 0 of the current
   wall will be taken into regard. On the adjacent wall it will always take the front of slice 0.
   A_WELR Indicates which end of the wall is closer to the Insertion-CS: -1 = left end, +1 = right end.
   In the adjacent wall, this will always look at the front side of the wall.

▪ When inserted ‘at point, objects’ in D-CAM, you can prompt the user to
select an object to identify a wall as an additional BP. Rules and
conditions see further down.

2.1.2.5 Additional Building Part: Ceiling (current, below)

▪ ‘Current’ means that the current ceiling is the Basic BP. If a ceiling
should be identified as an Additional BP, it will be the next lower
ceiling (below).

▪ In order to find the next lower ceiling the routine will look for a
ceiling area close to the Insertion-CS according to certain rules. When
inserting in plan it will look for a ceiling at the origin of the
Insertion- CS. When inserting in wall or truss it will look for a
ceiling within close limits in front of, or behind the building part.
This means that if you insert on the front side of the wall (front) it
will ignore any ceiling areas that end on the reverse side or inside the
wall.

▪ Modules ground plan, wall design, roof calculation, roof design and
truss: If there are ceiling areas the routine will identify them as
follows: In an area of +/- 1m from the bottom edge of the storey at the

::

   insertion point it will identify the top ceiling area. Height reference is the top edge of the ceiling. This
   routine will detect all ceiling areas independent of the storey they belong to.

▪ Module ceiling area: Only ceiling areas of the current storey will be
considered. It will identify the top ceiling area at the insertion
point.

▪ There are system variables regarding ceilings (current, below):

::

   LDp0Z In the origin of the insertion-CS the top edge of slice 0 of the ceiling (current, bottom) will
   be detected. This is the Z value (height) of the top edge.

2.1.2.6 Additional Building Part: Ceiling Top

▪ Similar to the bottom ceiling, the top ceiling will be identified at
the origin of the insertion coordinate system. When inserting in plan it
will look for a ceiling at the origin of the Insertion-CS. When
inserting in wall or truss it will look for a ceiling within close
limits in front of, or behind the building part. This means that if you
insert on the front side of the wall (front) it will ignore any ceiling
areas that end on the reverse side or inside the wall.

▪ Modules ground plan, wall design, roof calculation, roof design and
truss: If there are ceiling areas the routine will identify them as
follows: In an area of +1m or more from the bottom edge of the storey at
the insertion point it will identify the bottom ceiling area. Height
reference is the top edge of the ceiling. This routine will detect all
ceiling areas independent of the storey they belong to.

▪ Module ceiling area, ceiling design: Top ceiling areas will not be
identified!

▪ There are system variables regarding top ceilings:

::

   LOp0Z In the origin of the insertion-CS the top edge of slice 0 of the top ceiling will be detected.
   This is the Z value (height) of the top edge.

2.1.2.7 Additional Building Part: Roof Surface

▪ Similar to the top ceiling, the roof surface will be identified at the
origin of the insertion coordinate system. When inserting in plan it
will look for a ceiling at the origin of the Insertion-CS. When
inserting in wall or truss it will look for a ceiling within close
limits in front of, or behind the building part. This means that if you
insert on the front side of the wall (front) it will ignore any roof
surface areas that ends on the reverse side or inside the wall.

▪ Modules ground plan, wall design, roof calculation, roof design and
truss: If there are roof surfaces the routine will identify them as
follows: At the insertion point it will identify the bottom most roof
surface.

▪ There are system variables regarding roof surfaces:

::

   LFp0Z In the origin of the insertion-CS the top edge of slice 0 of the roof surface will be detected.
   This is the Z value (height) of the top edge.

2.1.2.8 Additional Building Part: Truss

▪ A truss can be an additional BP only for LBs that are inserted ‘at
point, object’. Rules: See below

2.1.2.9 Additional Building Part: D-CAM free design

▪ D-CAM free design is precisely defined and always available as
additional BP.

2.1.2.10 Additional Building Parts: LB type ‘at point, object’

▪ Also for this LB type it is possible to identify the additional BPs
wall, ceiling (current, bottom), roof surface, storey and roof.

▪ The top priority in identifying additional BPs have objects the user
is prompted to select:

::

   ▪ The first user prompt object that belongs to a wall identifies the wall. The second user prompt
   object that belongs to a wall identifies the adjacent wall.
   ▪ The first user prompt object that belongs to a ceiling area, truss or roof surface identifies the
   ceiling (current, bottom), truss or roof surface. A ceiling (top) cannot be identified.
   ▪ The first user prompt object that belongs to a roof surface will also identify the roof.

::

   ▪ The first user prompt object that belongs to a wall, ceiling area or truss will also identify the storey.
   Trusses can only be used to identify the storey if the truss belongs to a storey.
   ▪ Like this, user prompt objects that have to be selected anyways to insert the LB can be used to
   define additional BPs. It can also make sense to use user prompt objects in such logic blocks, that
   identify additional building BPs only. To do this the user may also select wall or roof/ ceiling slice
   volumes.

▪ Building parts that have not been identified by user prompt objects
can be defined by the current building MOS settings: ▪ If the current
building MOS is a wall, this wall defines the wall and storey as
additional BPs. ▪ This rule also applies accordingly to ceiling areas
and trusses that belong to a storey. ▪ It is not possible to identify a
storey by a roof surface or by trusses that don’t belong to a storey!

2.2 Coordinate Systems (CS)
~~~~~~~~~~~~~~~~~~~~~~~~~~~

While inserting a LB a couple of relevant CS are being used in sequence,
the properties and dependency of these CS are fundamental for the design
of the LB.

**2.2.1 Basic CS and Insertion CS, general process**

The Basic-CS is defined by the combination of program module and LB
type, e.g. in ground plan the Basic-CS is the CS of the storey, in wall
design it is the wall CS. Listing of Basic-CS see table below.

The definition of the Insertion-CS is based on the Basic-CS. There are
generally 2 ways:

1. Positioning Point

::

   ▪ The origin of the Insertion-CS will be at the positioning point of the LB. The orientation will be
   parallel to the Basic-CS.
   ▪ If you position the LB with Positioning Point = Choice and don't select the shown origin, but move
   the positioning point, the Insertion-CS will be moved accordingly. E.g. a 2.0m long object has its
   origin at the shown origin. To position the LB a point at its end is selected. Once you chose the
   positioning point now, the Insertion-CS will be 2.0 m away from the positioning point.
   ▪ The Z-position (height) of the origin depends on the option used to define the 'height level' of the
   LB.
   ▪ While inserting you can define a rotation against the Basic-CS (ground angle XoY). In addition to
   that you can rotate the preview in 90°increments by setting 'Positioning Point = choice'.
   ▪ Positioning points cannot be used with LB type 'at point, objects'

2. Insertion CS via 3 points

::

   ▪ The Insertion-CS can be defined with 3 points:

1. Origin

   2. Orientation of X-axis
   3. Point in positive ZoX plane. ▪ You can use direct numbers or
      calculations. Variables, coordinates of user prompt points and
      objects are available.

::

   ▪ The coordinates of the three points are defined in the Basic-CS. Consider this within the formulas.
   All further definitions inside the LB refer to the Insertion-CS.
   ▪ The definition with 3 points can be used for LB type 'at point, object' and all other LBs if the
   Positioning Point is set to 'no request'.

All further definitions inside the LB refer to the Insertion-CS!.

**2.2.2 Basic-Coordinate Systems**

Module Function global CS

Ground Plan in ground global CS along wall edge > front side wall CS >
reverse side reverse wall CS (*) along truss edge > front side truss CS
> reverse side reverse truss CS (*)

Wall Design Front side wall CS reverse side reverse wall CS (*) at
points, objects wall CS

Ceiling Area in ground global CS

Ceiling Design in ground ceiling CS at points, objects ceiling CS

Roof Calculation in ground global CS along truss edge > front side truss
CS > reverse side reverse truss CS (*) in roof surface roof surface CS

Roof Design in ground global CS along truss edge > front side truss CS >
reverse side reverse truss CS (*) in roof surface roof surface CS at
points, objects global CS

Truss Design Front side truss CS reverse side reverse truss CS (*) at
points, objects truss CS

D-CAM free design at point, objects global CS

\*) On the reverse side of walls and trusses an alternate coordinate
system is used: Looking at the reverse side, the X-axis runs from the
end of the wall to the origin of the wall, opposite the X-axis of the
normal wall CS. The Y-axis runs from the reverse side to the front side,
so it also runs opposite to the Y-Axis of the front side CS. The Z-axis
remains the same, indicating heights in the wall. While you insert on
the reverse side objects will also reference to the reverse side of
slices. The values of the Variable WELR indicate the left or right end
of the wall. Looking on the front side the origin of the wall is on the
left hand side, which means that WLER = -1, on the reverse side the end
of the wall is on the left hand side, WLER = - 1

Wall CS: Looking at the front side of the wall (front side), the X-Axis
runs from left to right, the Z-axis from bottom to top, and the Y-axis
away from the front. The bottom-left-front corner of the wall object is
at the origin of the wall CS

for windows and doors: Initially the insertion-CS will be identical to
the wall CS (basic-CS). The following parameters will affect the initial
location. For more info see Logic Blocks - Insertion - at Door, Window.

Ceiling CS: Z-axis runs globally from bottom to top. The CS is
orientated, so that all ceiling slice objects are located in the 1st
octant (+X/+Y/+Z). This means, that the CS is at the bottom of the
ceiling slice panels. The Y-direction (span direction) is defined by
clicking 2 points while the ceiling area is defined.

Roof Surface CS: The X-axis runs horizontally along the eave of the roof
surface, parallel to the XoY plane. The Y-axis runs parallel to the line
of greatest slope of the roof surface. The Z-axis runs upwards
perpendicular to the roof surface. The coordinate system is located Z =
0 at the roof calculation polygon (top edge slice 0) and all roof lines
are inside the 1st octant (+X/+Y/+Z).

Truss CS: In a default view of the truss (from front), the X-axis runs
from left to right, the Z-axis from bottom to top and the Y-axis away
from the front. The left bottom corner of the truss outline is at X = 0;
Z = 0; The truss thickness starts at Y = 0, the truss outline is at Y =
(truss thickness)/2.

**2.2.3 Calculation of Coordinates for Insertion CS**

Depending on the situation, complex calculations for the coordinates of
the insertion coordinate system may be necessary. It is helpful to be
able to use intermediate values. This is possible by the following
procedure when inserting a logic block. The systematics of the procedure
must be taken into account when creating the logic block:

::

   1.1 All coordinates of user prompt points, user prompt objects, slice outlines etc. are determined
   in the main coordinate system.
   1.2 Calculations are calculated and, if necessary, take into account these coordinates with
   reference to the main coordinate system.
   1.3 Generating the insertion coordinate system; optionally using calculations.
   1.4 All coordinates of user prompt points, user prompt objects, slice outlines etc. are determined
   in the insertion coordinate system.
   1.5 Calculations are calculated again and, if necessary, take into account these coordinates with
   reference to the insertion coordinate system.
   1.6 Further execution of the logic block.

(17.01) If automatically searched user prompt objects (see Automatically
searched user prompt objects) are used in the logic block, additional
steps are performed. This is necessary in order to be able to calculate
the coordinates of the reference point with calculations and to be able
to use the user prompt objects for the definition of the insertion
coordinate system:

::

   1.1 All coordinates of user prompt points, user prompt objects, slice outlines etc. are determined
   in the main coordinate system.
   1.2 Calculations are calculated and, if necessary, take into account these coordinates with
   reference to the main coordinate system. Values of automatically searched user prompt
   objects are still missing.
   1.2a Determining the reference points; optionally using the calculations. The reference points are
   used to search the user prompt objects.
   1.2b Calculations are recalculated and continue to take into account coordinates relative to the
   main coordinate system. Now, the values of automatically searched user prompt objects are
   also available.
   1.3 Generating the insertion coordinate system; optionally using the calculations.
   1.4 All coordinates of user prompt points, user prompt objects, slice outlines etc. are determined
   in the insertion coordinate system.
   1.5 Calculations are calculated again and, if necessary, take into account these coordinates with
   reference to the insertion coordinate system.
   1.6 Further execution of the logic block.

**2.2.4 Offset and Projected Insertion CS**

Positioning Objects:

▪ The position points of an object are always defined in the
Insertion-CS.

▪ If objects are positioned in a slice running parallel to the BP, the
positioning points of the object are projected onto the front face of
the slice.

▪ After that the object is created from point to point; Offsets and
rotations refer to the projected points. This has to be taken into
account especially for the tilt angle.

▪ If the object is inserted at the reverse side of the wall or truss,
the points will be projected onto the back face of the slice. Like above
the Basic-CS of the reverse side is different from the one on the front
side.

▪ If the wall or truss is an additional BP, reference will always be the
front side, all points will be projected to the front of the slice.

Positioning Library Objects:

▪ Offsets and rotations of library objects refer to the Insertion-CS if
the option orientation is set to ‘Orientation = free’.

▪ If library objects are positioned in a slice, parallel to the BP, a
projected CS is created first:

::

   ▪ The insertion point of the library object is projected onto the front face of the slice as origin of the
   projected Insertion-CS.
   ▪ Storey, roof and D-CAM free design: The X-axis will be projected into the XoY plane. The Z-axis of
   the projected Insertion-CS will be parallel to the Z-axis of the BP. This automatically determines
   the Y-axis. If the X-axis of the Insertion-CS is parallel to the Z-axis of the BP, the Y-axis will be
   used instead.

::

   ▪ Walls and trusses: The Z-axis of the Insertion-CS is projected onto the slice. The Y-axis of the
   projected Insertion-CS is parallel to the Y-axis of the BP. This automatically determines the X-axis.
   If the Z-axis of the Insertion-CS is parallel to the Y-axis of the BP, the X-axis will be used instead.
   ▪ Ceilings and roof surfaces: The X-axis of the Insertion-CS is projected onto the slice. The Z-axis of
   the projected Insertion-CS will be parallel to the Z-axis of the BP. This automatically determines
   the Y-axis.
   If the X-axis of the Insertion-CS is parallel to the Z-axis of the BP, the Y-axis will be used instead.

▪ The library object will be inserted at the origin of the projected
Insertion-CS and moved, rotated according to the defined offsets and
rotation angles. Movements and rotations refer to the projected
Insertion-CS (!)

▪ If the library part is inserted on the reverse side of a wall or
truss, the back face of the slice and the reverse CS apply accordingly.

▪ If the wall or truss is an additional BP, reference will always be the
front side.

Positioning Drawing Objects, Dimensions and Labels:

▪ Points for dimensions are projected onto the relevant drawing plane.

▪ Position and reference points of texts and labels are projected onto
the relevant drawing plane.

▪ The X-axis of the Insertion-CS is projected onto the drawing plane and
defines the X-orientation of drawing objects. This automatically defines
the Y-axis in the drawing plane.

▪ Movements and rotations refer to the projected axes.

2.3 Temporary objects in logic blocks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

During execution of a logic block objects can be positioned that are
only used for the purpose of the logic block and will not be needed
afterwards. This may e.g. be the case it the object carries a Type4
process that will be applied to other objects or if it is used as a
subtraction solid in a Boolean operation.

▪ If you give such an object the item# TEMPORARY, it will automatically
be deleted after the logic block has been executed; the resulting Type5
processes remain as Type0 processes.

▪ The item# TEMPORARY can be used in the library object, but you can
also assign it in the logic block. Newly created objects can have this
item# as well. Newly generated objects can have this item# as well.

▪ If you re-calculate the logic block, the temporary object will also be
re-positioned, transfer its processes and will be deleted afterwards.

▪ Note: The item# TEMPORARY does not have to be part of the material
database.

2.4 Variables und calculations of logic blocks in openings (doors, windows
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

and niches)
~~~~~~~~~~~

(Version 18.01) In doors and windows, the first logic block
significantly determines the properties and construction. Therefore, its
variables and calculations are passed on to the following logic blocks.
These variables and calculations can now also be processed in the areas
of jamb, air gap and reveal and passed on to wall guidelines.

Typical use is the “bottom air gap”: This is specified in the default
values for all windows. The first logic block also takes this as an
external variable. There, the variable can be overwritten on the
individual window in order to define a special air gap only for this
window. The setting for the “bottom air gap” does not need to be
changed; there is now also the variable, which now automatically assumes
the value from the logic block.

::

   In order to use a variable or a calculation of the logic block, the variable or the calculation must be
   defined as a variable in the default values of the building. So also acalculation must be defined in
   the default values as a variable.

Wall guidelines: In formulas of opening settings and calculations of the
wall guideline, the variables and calculations of the opening are used.
When used, the HRB interpreter takes exactly the values for this opening
at each opening. This allows a very precise control of each individual
window. This is suitable e.g. for transferring information about belt
winders or type of bottom connection for floor to ceiling windows
(balcony, terrace, facade).

In order to use a variable or acalculation of the logic block, the
variable or the calculation must be defined as an external variable in
the variables of the wall guideline.

Special possibilities arise here when using IFC-Premium: The assignments
can be used to directly address the variables of the first logic block.
A special value for e.g. “bottom air gap” can thus be controlled via
IFC, the requirement from the shop planning can thus be transferred to
the wall guideline.

3 Create and Edit Logic Blocks
------------------------------

3.1 Logic Blocks: Design, File Structure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The entire structure of a Logic Block is laid down in the LB file (
\*\ **.ksz** ). This file contains:

▪ Variable definitions, user prompts, calculations, etc.

▪ Cross references to images, 3D library objects, smart tags and 2D
drawing objects.

▪ The file is encrypted and can be edited with the function ‘7-7 Manage
Logic Blocks’.

The LB file cross references to a number of other files. The content of
these files is not saved inside the LB file:

▪ Images: Help pictures for the LB and for variable prompts. Images can
also be used for documentation of the LB.

▪ 3D library objects that will be inserted

▪ 2D drawing objects that will be inserted

▪ Smart Tags that will be applied

The cross reference consist of the file path, the file name and, if
necessary, the name of the element. A part of the file path may be
replaced by environment variables, if the LB recognizes a default
directory. In project administration default paths can be defined under
5 Settings -3 Paths. E.g. if the variable DHPKOLis set to ’
**C::raw-latex:`\Dietrichs`:raw-latex:`\KOL*`\* ’ the path
‘C::raw-latex:`\Dietrichs`:raw-latex:`\KOL`:raw-latex:`\Test`:raw-latex:`\Image`1.bmp’
will be replaced by
’**\ %DHPKOL%:raw-latex:`\Test`:raw-latex:`\Image`1.bmp*\* ’ and saved
with like this in the LB file. This makes it possible to use the same LB
in a different environment by copying all relevant files and
subdirectories to the location defined by the variable **DHPKOL**.

We highly recommend keeping all files that are referenced in one LB file
in the same subdirectory under DHPKOL. This would be images, 3D
libraries, 2D drawing objects, smart tags. Only by doing this you can
easily exchange LBs with other users, simply by giving them the entire
subdirectory and inserting it into their **DHPKOL** directory.

As of Version 13.01 the path info of elements, that are located in the
same directory as the Logic Block file, will be reduced to “."
(point-backslash) within the Logic Block references. This makes it
possible to copy the Logic Block file with all its dependencies into any
directory, and still keep the path references valid. Warning! Logic
Blocks that have been inserted into a project file can only be
re-calculated if the files are still in the same location they were in,
when the Logic Block was inserted. The new path feature is useful to
copy existing Logic Block files into a new directory and use them there
as a template for a new Logic Block. A once finalized Logic Block should
always remain in the same sub-directory within **%dhpkol%.**

**3.1.1 Logic Block: Help Pictures**

Help pictures are used to make selection of a LB easier and to assist
users in entering values for variables. On top of that they can be used
for documentation of the LB, e.g. by adding explanatory images to
calculations. For more information on help pictures refer to the
document \**Variables_Ud*.doc**.

▪ Possible file formats are: *.bmp,*.png, *.wmf,*.emf, \*.jpg.

▪ Default size of help pictures is 300x300 pixels. If the image file is
bigger than that, it will automatically shrink to fit. To save memory,
bigger images (e.g. photos) should be edited with appropriate software
tools (e.g. http://www.irfanview.net/ , http://www.getpaint.net/ ,
http://www.gimp.org/ ) to reduce size and number of colors.

▪ The LB only contains a cross reference to the image file. It does not
contain the image itself (!) See explanations in the previous section.

3.2 Variables, Formulas, Calculations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**3.2.1 Variable System**

The new system to define and manage variables is used in the same way in
Smart Tag Editor, Wall Guideline Editor and Logic Blocks. For a detailed
description please refer to the document Variables_Ud*.doc.

**3.2.2 Calculations**

In Logic Blocks you can use Calculations. Calculations are variables
where you can enter a formula to calculate the value. Main purpose is to
split calculations up into a number of steps to make it more
comprehensive. In addition to that the result can be use in a number of
places. You don’t have to enter the formula every time.

Further explanations see section: Logic Blocks – Calculations

**3.2.3 Conditions**

With conditions you can control if an object in a LB is created in a
certain situation or not. Like that a LB can cover a variety of
different situations, which normally would require a number of
individual LBs.

Freely defined conditions are also used in calculations in LB’s. See
section Calculations. For more information see section ‘Calculations’.

Conditions ‘to insert LB in’:

Besides freely defined conditions there are special conditions under ‘to
insert Logic Block in’. The options you can select here are ‘wall (front
face only)’, ‘wall (back face only)’, ‘truss (front face only)’,‘truss
(back face only)’. These options derive from applied design requirements
and cannot be replaced by freely defined conditions. The condition
refers to the insertion of the entire LB, not of the individual object.

Comparisons, that can be used in LBs:

= Equal to. True if compared values are equal e.g.: VAB = 4 is true if
VAB is exactly 4

!= Not equal to. True if compared values are not equal. It does not say
that one is greater than the other, or even that they can be compared in
size. e.g.: VAB != 4 is true if VAB is less or greater than 4.

   Greater than. True if the value in front of the sign is greater than
   the other. These relations are known as strict inequalities. e.g.:
   VAB>4 is true if VAB is bigger than 4

..

   = Greater than or equal to. True if the value in front of the sign is
   bigger than or equal to the other. e.g.: VAB>=4 is true if VAB is
   greater than or equal to 4

< Less than. True if the value in front of the sign is less than the
other. These relations are known as strict inequalities. e.g.: VAB<4 is
true if VAB is less than 4

<= Less than or equal to. True if the value in front of the sign is less
than or equal to the other. e.g.: VAB<=4 is true if VAB is less than or
equal to 4

& AND. Multiple conditions can be linked with &. All linked comparisons
have to be true to make the entire inequality true. e.g. (VAB>4)&(VAB<8)

3.2.3.1 Tolerances in comparisons:

If you compare calculated values, you have to observe, that internally
numbers are handled with a lot of decimal places. Instead of 1.0 the
result of a calculation could be 0.99999999999 or 1.00000000001. If you
compare for equality now (VA=1), the result may be false, even though
technically the result should be true.

▪ You can compare 2 values within a given tolerance range. To do that
you compare the difference to the desired value: e.g. VA = 1.0 shall be
true within a range of +/- 0.01. The difference has to be between -0.01
and +0.01. The condition can be defined as ((0.01>(VA - 1.0))&(-0.01<(VA
- 1.0))) To eliminate the negative part you can also use the function
‘abs’ for an absolute value. (0.01>(abs(VA - 1.0)))

▪ In other cases it might be enough to compare a value with a safe
enough number. E.g. in a distribution function you would normally
calculate the number of pieces (VNumP). If the condition is now, that
there should be more than 3 pieces, you don’t compare with greater than
3, but with greater than 2.5 (VNumP>2.5). By doing that it does not
matter if VNumP is 2.99999 or 3.00001.

**3.2.4 Variable Log File**

Every time you insert a LB the system writes a log file, to
%DHPTMP%:raw-latex:`\KOLVariablen`.log. This file lists all user and
system variables and the values they had, the last time the LB has been
used. This file also includes all values of calculations.

Please note that coordinates relate to the Insertion-CS.

This file is an important tool when you design LB. Here you can verify
calculations and conditions and find out where possible errors occur.

3.3 Logic Blocks – Save Settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In many dialogs in a LB you can save and manage settings. You can use
this feature in many ways:

▪ Save settings you want to use frequently, also in other LB, giving
them a significant name. Saved settings can be organized in groups. You
can build yourself a library of templates for standard applications.

▪ In a lot of dialogs some values will be the same (e.g. 0.0°). Even if
you don’t want to save a specific setting it makes sense to save one
setting with default values as a blank template.

▪ You can also use the save settings feature as a clip board. Save
settings (e.g. save as ‘tmp001’) which you keep overwriting. In the next
dialog you can load the settings, edit and move on.

3.4 Logic Blocks - Name
~~~~~~~~~~~~~~~~~~~~~~~

::

   The Logic Block is selected by name. Since a Logic Block File may contain more than one LB, the
   name has to be unique within the file.
   The name of a LB can be changed at any time.

::

   After you copy a LB you have to change the name first. If you don't change the name, an error
   message appears when you leave the input field: "A Logic Block with the same name already
   exists".

.. _section-6:

10.
^^^

3.5 Logic Blocks - Info
~~~~~~~~~~~~~~~~~~~~~~~

::

   Help pictures for LBs are highly recommended. The help find the right LB for a particular
   application.

.. _section-7:

10.
^^^

::

   In order to help the user find the right LB, you can add descriptive text. Please limit the text to
   no more than 5 lines. 5 lines is the number of lines that are shown without scrolling. If
   necessary, the text can be longer than that.

.. _section-8:

10.
^^^

**3.5.1 Logic Blocks - Info- Logic Block Type**

The LB type defines in what program modules and with which functions a
LB can be inserted.

::

   Insert in plan
   ▪ modules ground plan, ceiling areas, ceiling design, roof calculation, roof design
   ▪ This type is also used if you insert a LB into a roof surface or ceiling area. The positioning
   points will be projected vertically onto the roof surface.

.. _section-9:

10.
^^^

::

   Insert in wall
   ▪ along wall in module ground plan

.. _section-10:

10.
^^^

::

   ▪ insert on front face or back face in module wall design

::

   Insert in wall elevation
   ▪ insert on front face or back face in module wall design
   ▪ for LB that require the user to select points in an elevation the input in ground plan is not
   useful.

.. _section-11:

12.
^^^

::

   Insert at door/ window
   ▪ the LB can be specified in the wall/ window dialog box.

.. _section-12:

10.
^^^

::

   Insert in roof surface
   ▪ modules roof calculation and roof design
   ▪ positioning points are projected perpendicular onto the roof surface.
   ▪ since 2D (X/Y) coordinates are not sufficient here the program will automatically switch to a
   3D view.
   ▪ in order to insert LB into a roof surface, the surface has to be identified. If you have not
   selected one roof surface yet (2-3), you will be asked to select one.

.. _section-13:

12.
^^^

::

   Insert in truss
   ▪ insert along truss in modules ground plan, roof calculation and roof design.
   ▪ insert on front face or back face in module truss design

.. _section-14:

12.
^^^

::

   Insert in truss elevation
   ▪ insert on front face or back face in module truss design
   ▪ for LB that require the user to select points in an elevation the input in ground plan is not
   useful.

.. _section-15:

12.
^^^

::

   at point, object
   ▪ Insert function in module D-CAM – free design
   ▪ The Insertion-CS always has to be defined by user prompt points or objects.

.. _section-16:

12.
^^^

::

   for ceiling openings and niches.
   As for wall openings and niches, logic blocks can also be produced in the ceiling openings and
   niches. For this purpose, the logic block type "for ceiling openings and niches" was developed.
   ▪ The system points of the opening can be accessed with the variables ORnX and ORnY (n = 1-
   12). Instead of ORnZ of the wall openings ORnY is used here.

▪ The openings in the ceiling can be rotated. The X-direction of the opening is indicated by OAR
================================================================================================

::

   (0 ° to 360 °) relative to the X-direction of the ceiling.

::

   ▪ The depth of a niche is recorded in ONT; it is always measured from the opening side.

.. _section-17:

17.
^^^

**3.5.2 Logic Blocks – Info - Components**

::

   Logic Blocks can create components:

::

   ▪ all objects that have been created or inserted by the LB are grouped to one component.
   ▪ The CS of the component can be defined with formulae. The coordinates refer to the
   Insertion-CS.
   ▪ In the views dialog you can define views for the component drawing. The coordinates for the
   view direction can be defined with formulas. The coordinates refer to the component CS,
   which makes the easy to handle, since they have fixed coordinates most of the time.

.. _section-18:

11.
^^^

::

   ▪ The components can be edited with the component edit function in 'D-CAM 7-06'. Once you
   recalculate the LB these changes will be lost (!).

::

   ▪ You can create component drawings of these components.

::

   Objects of the logic block can also be assigned to an existing component. An existing component
   can therefore be supplemented with logic blocks whose objects in turn belong to this module.
   Thus, logic blocks can be divided into various structural parts and combined as desired and still
   form a component at the end.
   ▪ In Create component from logic block use the 3rd option Attach objects to component K.
   ▪ For this purpose, the component of the first user prompt object (which belongs to a
   component) is used.

::

   ▪ The first component can already be formed by a logic block. Even if this logic block is
   recalculated, the reference (user prompt object) for the second logic block remains: It is
   noted that the user prompt object was e.g. the 3rd generated object of the first logic block.

.. _section-19:

17.
^^^

**3.5.3 Logic blocks - info - Logic Blocks at Windows and Doors**

::

   For 3D graphic representation of doors and windows, a new technology based on logic blocks has
   been implemented. The following parameters in "info" control the selection. They are available
   only for logic block type "for windows/ doors " only:
   ▪ Object mode: You can choose between the technologies "Templates" or "logic block (default)"
   when you insert a window. Not all logic blocks can be used for both object modes. Select, for
   which of the object modes the logic block should be available.
   ▪ All: The logic block is suitable for all object modes.

::

   ▪ Logic block (default): The logic block is suitable only for the object mode "Logic block".
   ▪ Are sizes and dimensions editable: Constructions, e.g. of doors, with fixed dimensions may
   not be altered by the window/door dialogue. If this parameter is set to "No", the input of
   dimensions is deactivated in the corresponding dialogues.
   ▪ Opening type: For which opening types should the logic block be available: All / doors /
   windows/ doors and windows / CON reference.

::

   ▪ Shape: The logic block should be available for which shape: Rectangular / slanting / pointed /
   diamond / curve / circular.

.. _section-20:

14.
^^^

3.6 Logic Blocks – User Prompt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

   User prompt points: Here you can ask the user to graphically select points you require for
   calculations or positioning. The specified text will be used.
   ▪ The coordinates of these points can be used to position objects in the LB. The points are
   named in order of appearance P1, P2, P3, etc. The X coordinate of P1 can be found under
   system variables named P1X etc.

.. _section-21:

11.
^^^

::

   User prompt objects: here you can ask the user to graphically select objects you require for
   calculations or positioning.

::

   ▪ The user prompt objects are named in order of appearance K1, K2, K3, etc.

.. _section-22:

11.
^^^

▪ The coordinates of corner and axis points can be used in formulas and
to position objects. They can be found under system variables named
e.g. K1E4X for object 1 corner 1 X-value etc. For further explanation
refer to the help pictures in the formula editor.

▪ The dimensions of objects can be used in formulas. They can be found
under system variables named e.g. K1B for the width of object 1 For
further explanation refer to the help pictures in the formula editor.

▪ The item# of objects can be used to give newly created objects the
same item#.

▪ You can apply Smart Tags to user prompt objects.

Prompted Objects: System variable for selected objects:

The application of the Logic Block may depend on which end of the object
(Origin or End) is affected. The user can be prompted to select the
object at the desired end. It is sufficient to click the respective half
of the object. Internally the Logic Block will handle the system
variable KnAAE: If the value is -1 the object has been selected at the
origin. If the value is 1 the end has been selected. If the user
selected the end of the third prompted object, the value of K3AAE=-1.

.. _section-23:

12.
^^^

Logic Blocks: Flexible number of user prompt points and user prompt
objects

While using a Logic Block, it is no more necessary to pick all user
prompt points and user prompt objects defined in the Logic Block file.
Example: If a Logic Block contains up to 8 user prompt points, the
selection can be quit with a right mouse click after picking the third
point and the Logic Block is executed. Old Logic Blocks cannot handle a
flexible/ reduced number of user prompt points or user prompt objects.
If you do not pick all defined user prompt points or user prompt
objects, they will still be cancelled.

Furthermore it is possible to cancel the execution of the Logic Block by
rejecting the first user prompt point or user prompt object with a right
mouse click.

By using appropriate conditions you have to make sure that that rejected
user prompt points and user prompt objects do not lead to problems.

▪ A user prompt point has not been selected, if its coordinates have the
value 999999 e.g. P3X=999999.

▪ A user prompt object has not been selected if its lenght has a value
of 0.0, e.g. K3L=0.

.. _section-24:

16.
^^^

Logic Blocks – Automatic searched user prompt objects

User prompt objects often require information such as item numbers or
dimensions. User prompt objects can be selected by the user or searched
automatically via a reference point.

▪ Below the list of user prompt objects are parameters of the currently
selected user prompt object. In the definition of the user prompt
object, you can select whether the user prompt object be selected by the
user or searched by the program via a reference point.

▪ The possibly required reference point is defined in the next 3 fields.
It should be noted that the coordinates must be specified in the main
coordinate system. Calculations can be used to calculate the
coordinates.

▪ If the reference point touches an object, it is selected as the user
prompt object. After that, its information can be accessed as with a
normal user prompt object. When searching with the reference point, wall
volumes, floor slice panels and roof slice panels are ignored.

▪ An automatically searched user prompt object can be combined with
selected user prompt objects. It retains its number, even if not all
previous prompt objects have been selected. ▫ It is possible to cancel a
logic block by mouse right at the first user prompt objects. Therefore,
when mixing selected and automatically searched user prompt objects, the
first user prompt object should be a selected one.

▪ (19.03) An automatically user prompt object keeps its number, even if
not all previous automatically searched user prompt objects were found.

.. _section-25:

17.
^^^

Now user prompt objects can also be assigned to the component. For
example, if one chooses an existing steel beam to attach a top plate to
a component, these can together form a component.

.. _section-26:

17.
^^^

::

   ▪ To do this, the 2nd option Yes is selected in the add preliminary object to component setting.

3.7 Logic Blocks - Variables
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

(from Version 13.01 on) This dialogue has been separated from the user
prompt.

::

   Definition of Variables: here you define the variables the user will be prompted to provide
   information for later on. See section on Variables

.. _section-27:

10.
^^^

::

   In variable definition, specific groups of variables can be accessed by the group buttons.
   The list of variables remains visible; the variables of the current group are shown in blue, the
   other groups are shown in grey. The list will jump to the first variable of the selected group. All
   variables remain editable.

.. _section-28:

13.
^^^

3.8 Logic Blocks - Insertion
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The basic environment for insertion is defined by the coordinate
systems. See section 2 Basic Technologies.

**3.8.1 Logic Blocks - Insertion – Positioning Point**

During insertion of a LB the user can be asked to define a positioning
point. This point will be the locator of the Insertion-CS in which will
all further definitions are made. The height reference ( Z coordinate )
of the Insertion-CS can be determined in a number of automatic ways via
‘Height Level’ settings.

::

   Positioning Point - Choice
   ▪ Inserting in plan you can define a ground angle. The Insertion-CS of the LB will be rotated by
   this angle.

::

   ▪ Inserting in plan you can select the positioning point in a preview of the LB. The bounding box
   and the center of the LB are offered as options. With a right mouse click you can rotate the LB
   in 90° increments.
   ▪ Inserting along a wall or truss edge and in wall or truss design the LB can be positioned at
   points along the X-axis: left aligned, right aligned, centered and as defined in LB if this varies
   from the 3 options above.

.. _section-29:

10.
^^^

::

   Positioning Point – no request
   ▪ the LB is inserted directly at the point of insertion, as defined in the LB
   ▪ the orientation of the Insertion-CS is parallel to the Basic-CS. For more information see
   section 'Coordinate Systems'.

.. _section-30:

10.
^^^

::

   Positioning Point – no request
   ▪ This setting may be very useful if you are using user prompt points. You can use these to
   position the LB. Further user definitions may not be necessary.

::

   ▪ If you don't define a Insertion-CS, the Basic-CS will be used.
   ▪ In this case it is also not possible to define a 'Height Level'; this option will be greyed out.

.. _section-31:

11.
^^^

**3.8.2 Logic Blocks- Insertion – Height of Insertion Point**

The height reference (Z coordinate) of the Insertion-CS can be
determined in a number of automatic ways via ‘Height Level’ settings.

▪ There are a number of options to define the Z-position (height level)
of the Insertion-CS

▪ These options are not available for LB types = at Window, Door

▪ These options are not available for positioning point = no request

::

   Insertion point height – according to LB type
   ▪ The Z= 0 coordinate of the Basic-CS will be used.

.. _section-32:

12.
^^^

::

   Insertion point height – by request
   ▪ When the LB is inserted the Z-level of the Insertion-CS can be defined during user variable
   prompt, via a combination of 3 values:
   ▪ The 'Height Bottom Edge of Storey US' is the absolute height of the bottom edge of the
   current storey. If the is no current storey available, the option will offer global 0.
   ▪ 'TE Finished Floor Level to BE Storey DS' is the distance from the bottom edge of the storey to
   the top edge of the floor (finished floor level). To determine global Z this value will be added
   to the height level of BE storey.
   If there are ceiling areas, a default value will be determined: In an area of Z +/- 1m from the
   BE of the current storey, the TE of the bottom most ceiling will be detected. The distance of
   this point from the BE storey will be calculated and entered. This routine will detect all ceiling
   areas independent of the storey they belong to.

::

   ▪ Finally 'Height of destination point over Finished Floor Level ED' will show the distance of the
   insertion point from the just determined TE of finished floor level. To calculate the final Z-level
   this value will also be added.

.. _section-33:

10.
^^^

::

   Insertion point height – automatically TE Ceiling

::

   ▪ When the LB is inserted, the insertion point will automatically be on the TE of a detected
   ceiling.
   ▪ The ceiling, following certain rules, will be detected at the point selected by mouse click.
   Inserting in plan this will be directly at the cursor. Inserting in wall or truss, an area in front of
   or behind the BP will be considered. This means that if you insert on the front side of the wall
   (front) it will ignore any ceiling areas that end on the reverse side or inside the wall.

::

   ▪ Modules ground plan, wall design, roof calculation, roof design, truss: If there are ceiling
   areas the routine will identify them as follows: In an area of +/- 1m from the bottom edge of
   the storey at the insertion point it will identify the top ceiling area. Height reference is the top
   edge of the ceiling. This routine will detect all ceiling areas independent of the storey they
   belong to. If no suitable ceiling can be detected, the BE of the current storey will be used.
   ▪ Module ceiling area: Only ceiling areas of the current storey will be considered. It will identify
   the top ceiling area at the insertion point. If no suitable ceiling can be detected, the BE of the
   current storey will be used.
   ▪ Module ceiling design: The current ceiling will be selected.

.. _section-34:

10.
^^^

::

   Insertion point height – automatically BE storey

::

   ▪ The Insertion-CS will automatically at the height level of BE of the current storey.
   ▪ If there is no current storey available, global 0 will be used.

.. _section-35:

10.
^^^

::

   Insertion point height – automatically BE wall, truss

::

   ▪ The Insertion-CS is automatically at the height level of the bottom edge of the current wall/
   truss.
   ▪ This option only makes sense for LB types 'insert in wall', '... wall elevation', '... truss' or '...
   truss elevation'.

.. _section-36:

10.
^^^

::

   Insertion point height – global 0.
   ▪ The Insertion-CS is at global Z= 0.

.. _section-37:

12.
^^^

**3.8.3 Logic Blocks – Insertion – Insertion CS**

::

   The Insertion-CS is defined in the Basic-CS with 3 points. The coordinates of the points are
   calculated with reference to the Basic-CS. All further coordinates in the LB refer to the Insertion-
   CS.

::

   The Insertion-CS can be defined with 3 points:
   1st point Origin
   2nd point on X-axis

3. Point in positive ZoX plane.

::

   If an insertion-CS is defined using user prompt points, the variables P1X, P1Y etc. can be used.
   For the definition of the insertion-CS these coordinates still refer to the basic-CS. After the
   insertion-CS is defined the variables will be re-calculated to refer to the insertion-CS. That
   means that if you use variable P1X later on in the LB, its value refer to the insertion CS.

.. _section-38:

12.
^^^

**3.8.4 Logic Blocks - Insertion - at Door, Window**

In the lower area of the dialog box you will find entries that are used
for LB-types ‘at Door, Window’ only. For these LB the insertion-CS will
automatically be determined at the door or window opening. Initially the
insertion-CS will be identical to the wall CS (basic-CS). The following
parameters will affect the initial location.

The same principal features apply for insertion of library objects at
door or window openings in the wall guideline editor.

::

   additional text for window description:
   ▪ This text will be added to the window description. It will also appear in list documents as
   description text.

.. _section-39:

10.
^^^

::

   Slice, Y-Offset
   ▪ The insertion-CS will be moved to this slice with an additional offset in Y. A positive offset will
   move into the slice.
   ▪ Slices -8 through +8 are available. -8 and +8 will be flush outside of the wall

.. _section-40:

10.
^^^

::

   Reference Edge, Offset

::

   ▪ To define the Z-level, a reference edge has to be defined first. You can pick the top and
   bottom edge of the wall, or the top and bottom edge of the opening.
   ▪ From there you can give an additional offset in Z. The principles opposite to the wall
   guidelines apply: A positive offset enlarges the opening size. This results in the following
   offsets:
   Reference Edge negative Offset positive Offset
   Top Wall Edge upwards (+Z) downwards (-Z)

::

   Bottom Wall Edge downwards (-Z) upwards (+Z)
   Top Opening Edge downwards (-Z) upwards (+Z)
   Bottom Opening Edge upwards (+Z) downwards (-Z)

.. _section-41:

10.
^^^

::

   Insertion and Opening Side, X-Offset
   ▪ The insertion-CS will be positioned optionally at the left or right edge of the opening

.. _section-42:

10.
^^^

::

   ▪ Afterwards you can move it in X by giving it an additional X-offset. The principles opposite to
   the wall guideline s apply: A positive offset enlarges the opening size. This results in the
   following offsets:
   Reference Edge negative Offset positive Offset
   Left opening edge to the right (+X) to the left (-X)
   Right opening edge to the left (-X) to the right (+X)
   ▪

::

   Rotation angle about Z
   ▪ The insertion-CS will be rotated around its Z-axis.
   ▪ Different from wall guidelines you are not limited to 90° increments though.

.. _section-43:

10.
^^^

3.9 Logic Blocks - Calculations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In Logic Blocks you can use Calculations. Calculations are variables
where you can enter a formula to calculate the value. Main purpose is to
split calculations up into a number of steps to make it more
comprehensive. In addition to that the result can be use in a number of
places. You don’t have to enter the formula every time.

▪ Calculation can also be used in formulas like regular variables. The
variable name starts with ‘V’ and has to be unique among the variables
of the LB.

▪ Calculations are variables with a value that’s being calculated using
other variables and informations. The value of a calculation can be used
in following calculations.

▪ Calculations can be documented like variables with text and pictures.
This documentation is important for the designer of the LB.

▪ Calculations can be saved and managed as a set of variables.

▪ Possible units of calculations are m and txt. ‘m’ does not necessarily
mean that this is limited to meters. It stands for any number with or
without decimal places. Default unit of calculations is ‘m’; in the
variable definition dialog you can change it to ‘txt’. ▪ Calculations
with ‘m’ unit can be used in conjunction with the usual mathematical
operations. ▪ Calculations with the unit ‘txt’ are text strings. Here
you have the text functions and formatting options as described in
‘Variables in Text, Item Numbers’. The formula editor cannot be used
here.

▪ For every calculation you can define a condition. If the condition is
true the calculation receives the result of the formula as a value. If
the condition is false the value of the calculation will be 0.0 if the
unit is ‘m’ or it will remain empty (not even a space sign) if the unit
is ‘txt’.

Examples:

▪ A number of library objects have the same value, e.g. length. Without
calculations the full formula that calculates the length has to be
entered in every library object. With calculations you calculate the
value of the length once and enter the name of the calculation in every
library object. If you change the formula in the calculation now, the
change will automatically apply to all affected library objects.

▪ An angle you calculate has to be used in a number of formulas. Without
calculations you would have to enter the formula to determine the angle
in each further formula. Now you calculate the angle once in a
calculation variable, and insert the variable in every formula where you
need the angle.

**3.9.1 Calculations - Import, edit with text editor**

(from Version 13.01 on) Calculations may become very involved. Editing
individual calculations may become complex and confusing. There is an
option to copy calculations to a text file, which can be edited in an
editor and be imported back into the calculations.

▪ With Export, all calculations are written into individual lines of the
file %dhptmp%:raw-latex:`\ZWEditor`.txt.

▪ The file %dhptmp%:raw-latex:`\ZWEditor`.txtcan now be opened with any
text editor (e.g. Notepad). Set up the default tab-size (e.g. 40). You
can use all editing features (copy, paste, search and replace, …). All
calculations, conditions and formulas are visible at the same time.

▪ Save the file and import it in the dialogue. All existing calculations
will be deleted, only the imported ones will remain.

▪ The file %dhptmp%:raw-latex:`\ZWEditor`.txt:

::

   ▪ All calculations are in individual lines.
   ▪ The data sets are separated by tab-stops, text format is UTF8 (take special care when using Excel
   to edit!)
   ▪ The data sets within one line are:
   Variable Name Name of the calculation variable.

::

   Variable Prompt Additional explanatory text for each variable.
   Conditions Conditions
   Formula Formula
   Unit Unit: meter or text.

::

   Variable Description detailed description
   Help Picture Help picture
   Variable Group Group

::

   Fixed Value invalid, defaults to 0
   External invalid, defaults to 0
   Variable Display invalid, defaults to empty
   Enum List invalid, defaults to empty
   ▪ Every line must include all data sets and the right number of tab-stops, even if they are empty.

**3.9.2 Calculations with conditions**

Numeric calculations with conditions:

This is an important method in order to perform calculations under
certain conditions.

▪ For every calculation you can define a condition. If the condition is
true the calculation receives the result of the formula as a value. If
the condition is false, the value of the calculation will be 0.0.

▪ Multiple conditions can be linked with &. If VAB has to be greater
than 4 and less than 8, the entire expression is: **(VAB>4)&(VAB<8)**.

▪ First you have to make a calculation for each condition. They are
named e.g. **VBZ1, VBZ2,** etc. If the

::

   condition is true, the value of the calculation is the result of the formula, else the value is 0.0.

▪ ▪The final result according to the multiple conditions is the sum of
the individual calculations: **VBZ = VBZ1 + VBZ2 +..** .. Since the
false **VBZ is 0 ,** only the values of the true condition are the
result of VBZ.

▪ The calculation **VBZ** can now be used in all instances where it is
needed. Without calculations with conditions you would possible have to
make individual LBs for different situations.

String calculations with conditions:

This way you can also arrange texts, which have to have different
content depending on certain conditions. This text strings can also be
used to make item numbers. Without this method you would have to prepare
an individual object, library part etc. for every text variation you
want to have.

▪ For every calculation you can define a condition. If the condition is
true, the value of the calculations is the arranged text. If the
condition is false, the value of the calculation is EMPTY (not even a
space sign).

▪ Multiple conditions can be linked with &. If VAB has to be greater
than 4 and less than 8, the entire expression is: **(VAB>4)&(VAB<8)**.

▪ First you define a text variable for each condition. They are named
e.g. **VBT1, VBT2,** etc. If the condition is true, the value of the
calculation variable is the defined text, else it is empty.

▪ ▪The actual text will be arranged in a calculation variable by
combination of the individual calculations with conditions: **VBT =
#VBT1##VBT2#..** .. Since the values of the false conditions VBT? are
empty only the true condition text is entered into **VBT**.

▪ The calculation **VBT** can now be used in all instances where it is
needed, e.g. in a text, label, item# or a library object. Without this
option you would have to prepare individual library objects with
conditions for every text variation.

3.10 Logic Blocks - Objects
~~~~~~~~~~~~~~~~~~~~~~~~~~~

In LB you can directly create objects. Basically this uses the features
of D-CAM function ‘2- 1 - 1 constant section’ with the positioning
option ‘Point to Point’.

::

   As soon as an object is defined, it is given an object number: B1, B2 etc.
   ▪ This object number is shown in the tree element on the left hand side.
   ▪ Smart Tags directly be assigned to objects. To do that, the object number is entered in the
   Smart Tag: B1, B2 etc.
   ▪ Bottom right under the picture you can enter descriptive text. This is for better
   documentation. The first line of the text will also be shown in the tree element on the left,
   next to the number. This makes it easier to identify objects and their function.

.. _section-44:

11.01
^^^^^

::

   'to insert LB in' and Conditions:
   ▪ Here you can define under which conditions the object should be created. For more
   information refer to the section 'Conditions'.

.. _section-45:

11.01
^^^^^

::

   Item number can be defined with fixed item# or by using a variable.
   ▪ The variable can be part of the user prompt. With the browser button in the user prompt you
   have access to the material dbase.
   ▪ Item number can be prompted via variables. Variable unit has to be 'Item#Np' (without
   profile description) or 'Item#Obj' (general object). Alternatively you can use lists of options
   (Enum) or text variables (txt).

::

   ▪ The item number can also be taken from a user prompt object.
   ▪ Item numbers can be arranged from a number of text strings. This can be used to add a size
   to an item number. e.g. You want to compare an item# with the text 'rod' and the diameter
   'Vdia'in full mm. The expression for the item# would be 'rod#Vdia[mm,0]#'.

.. _section-46:

11.01
^^^^^

::

   Item numbers can be defined wit fixed values or you can use variables.
   ▪ In the user prompt a browser button will open the texture browser. Textures are shown in
   preview. Accordingly the additional colors can be selected.

.. _section-47:

11.01
^^^^^

::

   Insert in Group / Building Part:
   ▪ The generated object will be assigned to a group MOS.
   ▪ The generated object will be assigned to a building part (MOS).
   ▪ The group MOS can be assigned with variables as well. Possible variable units are Number, txt
   (Text) or Enum (list). To enter the variable value in 'Group' the Variable has to be in '#':
   #VGroup#.

.. _section-48:

11.01
^^^^^

Insert in Slice (empty = outside) / Orientation:

▪ Orientation = free: The object will be positioned directly at the
defined points. It will belong to the specified building part, but the
orientation will be defined by the insertion-CS.

▪ Orientation = parallel Building Part: Now you can also specify a
slice. The specified points will be projected perpendicular onto the
slice The object will be generated at the projected points. Further
alignments refer to the basic-CS of the building part.

▪ Slice = empty the points will be projected onto the outside surface of
the building part. For walls and trusses this may be the front or back
face depending on the orientation of the insertion-CS. For ceilings and
roof surfaces this is always the top face.

▪ For insertion in storey, roof or D-CAM free design the orientation
defaults to ‘free’.

▪ The slice can be assigned with variables as well. Possible variable
units are Number, txt (Text) or Enum (list). To enter the variable value
in ‘Slice’ the Variable has to be in ‘#’: #VSlice#.

.. _section-49:

12.01
^^^^^

After generating an object, it can be assigned to any number of
user-defined MOS.

▪ The name of the user-defined MOS is simply entered as a text. Use
tilde ~ in order to separate several user-defined MOS.

.. _section-50:

16.01
^^^^^

▪ Length and section sizes can be defined with a fixed value or by using
variables or even formulas.

▪ Additional length at origin and end can be defined accordingly.

.. _section-51:

11.01
^^^^^

▪ To position the object precisely you can define what point of the
object (corner, axis) will be located at the specified points.

▪ In addition to that you can add offsets or tilt angle.

▪ The coordinates of the positioning points are entered in pairs (point
to point insertion). For every pair you specify an object will be
created. Please note that you have to observe the CS you are working in
while you specify point coordinates; see section ‘Coordinate Systems’.

.. _section-52:

11.01
^^^^^

Distribution of objects

Where you define coordinates in order to position objects, you can
define arrays.

● In every coordinate field you can enter an array as follows (
**ORIGIN\ SPACING\ QUANTITY** ). A

::

   quantity of 1 means that you get only 1 object in origin.

● If you specify an array, you have to do so in X, Y and Z.

::

   X(1.0~0.1~5)Y(0.0~0.0~1)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step
   size 0.1
   X(1.0~0.1~5)Y(0.0~0.2~4)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step
   size 0.1, this row 4 times along Y step size
   0.2.

● With arrays, you can define rows, grids and 3 dimensional grids of
objects in one go.

● Objects have an origin and an end. For objects, the first origin point
will be connected to the first end point, the second origin to the
second end, etc.

● If you reference to an object (B1, B2, …), e.g. in connection
settings, this will affect all objects that have been generated as an
array.

.. _section-53:

13.01
^^^^^

Connection Origin, End:

▪ For the connection at the origin and end of the object you can select
from the usual settings (e.g. tenon, step joint, etc.).

▪ These connections will be applied after the object is positioned; this
means also, that they are added after the object has been intersected
with a slice. Intersection with a slice can also be used to trim the
object to a certain length before connections are applied.

The connections will also find all other objects that have been created
by the LB. If a further object has the suitable length, a previously
created object will also connect to it. Since the

.. _section-54:

12.01
^^^^^

::

   length of an object changes with the connection, the sequence of insertion may still affect the
   result.

::

   ▪ The connections look for other objects to connect to, starting from the ends of the object. The
   will extend by a maximum length defined in D-CAM 1- 7 - 7. This applies independently from
   the current program module.
   ▪ Objects will not connect to objects they run through entirely. The object has to end either in
   front of or inside the other object in order to connect to it.
   ▪ The connections generally are defined with fixed dimensions in the saved settings. If the
   settings have been prepared using variables, they can be specified in the LB as well. The
   values will be transferred to the connection settings. See also 'external' tag in section
   'Variable Definition, Properties'.

::

   Intersect with Slice, Offset E/I:
   ▪ Every object can be intersected (punched out) with the outline of a slice. The object does not
   have to be located in the slice or be assigned to it. It can even be located somewhere outside
   the building. Intersection is independent of object type (e.g. beam, sheet material, etc.)
   ▪ To intersect, the outline of the slice can be edited with offsets E/I: offset E will affect the
   external, offset I the internal polygon (e.g. windows). A positive offset value enlarges the
   material section (extends outside polygon, reduces opening size).
   ▪ The adjusted outline will then be used to punch out the objects perpendicular to the building
   part.

.. _section-55:

12.01
^^^^^

3.11 Logic Blocks - Extruded objects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In a logic block you can create objects now by extruding an outline.

::

   ▪ You can define the object coordinate system with point coordinates. The CS is orientated, so
   that all objects are located in the 1st octant (+X/+Y/+Z).
   ▪ Two further points define the origin and the end of the extruded object. These define the
   orientation of the extrusion and the length of the final object.

::

   ▪ Outside and inside polygons are defined with an arbitrary number of segments:
   ▪ Every segment is defined with two points. They don't have to be the endpoints of the final
   segment.
   ▪ The sequence of the points is arbitrary as well.
   ▪ You only have to consider, that the sequence of the first segment and the second point
   of the second segment define the sense of rotation of the polygon. This sense of rotation
   determines the orientation of the positive radius for arcs.
   ▪ A radius of 0.0 defines a linear segment. If you specify a radius, the segment will be an
   arc. You can enter positive or negative values. Observe the rotation sense to achieve
   convex or concave segments. The arc is positioned through both of these points.
   ▪ All segments will automatically be connected to form a closed outline.
   ▪ The segments are connected according to the sequence.

::

   ▪ The segments can overlap and they can be far away from each other. The function
   works as if you use the D-CAD function " fillet ", picking the segment in its midpoint
   ▪ If the " fillet radius " is equal 0.0, a corner is generated. If the radius is greater than 0.0,
   the segments will be connected tangentially at the fillet.
   ▪ The tag "END" is assigned at the last segment of the polygon. The next segment starts a
   new polygon. The first polygon defines the outline; all further polygons are internal shapes
   and will generate holes in the extruded object.

::

   ▪ The extruded objects can be intersected with slice outlines just like other regular objects.

.. _section-56:

14.01
^^^^^

::

   ▪ Extruded objects can also be used and edited with connections, smart tags and special
   processes. They are labelled with a capital E at the beginning; E1 is the first extruded
   object.

::

   ▪ After generating an extruded object, it can be assigned to any number of user-defined MOS.

::

   ▪ The name of the user-defined MOS is simply entered as a text. Use tilde ~ in order to
   separate several user-defined MOS.

.. _section-57:

16.01
^^^^^

3.12 Logic Block - Connections
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

   Connections: Objects can be created with connective processes.
   ▪ Select the connection setting you want to use. Possible processes:
   ▪ Post and Beam Connections: Shoulder, Tenon, Dove Tail Tenon, Step Joint, Shouldered
   Tenon, Butt Joint, T-Joint, Profiled Connection, Fork Joint, Ornamental Lap Joint,
   Connection T-Joint, Closed Housing, Dove Tail End Lap
   ▪ Corner Connections : End Lap Joint
   ▪ Crosswise Connections: Half Lap Joint, Dovetail Lap Joint, Ornamental Half Lap, Drilling at
   Junction, Connection at Junction, Free Marker
   ▪ End-to-end Connections: End-to-end Joint, Gerber Joint, Scarf Joint, End-to-End Tenon,
   End-to-end Dovetail Tenon.
   ▪ There may be certain geometric requirements for individual joints to apply.

::

   ▪ Now you can specify beam 1 and beam 2 in a list of objects. The list of objects contains
   objects from within the LB and objects selected by the user.
   ▪ With this list you can precisely define, which object should be connected to what other object.
   You avoid random connections with stray objects.
   ▪ For the second beam you can also use the options ‘search at origin’ and search at end. The
   second beam is not specified, but the Logic Block will search for available objects. The partner
   object can be searched for starting from the origin or the end of the specified beam. This
   function will only extend and not shorten the beam.
   ▪ If the type of connection is subject to certain conditions, previously you had to define
   separate objects for each type of connection. Now you define the objects once and only the
   connection is subject to conditions.

.. _section-58:

12.01
^^^^^

::

   The Miter Cut function has been established as a new connective process. This new function
   connects beams and sheet material at corners and edges with different options

.. _section-59:

14.01
^^^^^

3.13 Logic Blocks - Library Objects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

With LBs you can insert library objects from 3D libraries. 3D libraries
are created in D-CAM 1- 5 - 1.

To insert library objects, the features of ‘Ref. Library Object’ from
the Smart Tag editor are used:

::

   ▪ A library object has its own coordinate system. The position of this CS is defined by the current CS
   at the time the object was put into the library.
   ▪ If a library object is inserted its CS will initially match the insertion-CS (or projected insertion-CS).
   ▪ The library object will be moved together with its CS according to the offsets in X-, Y- and Z-
   direction.

::

   ▪ Finally the object will be rotated around the moved origin of its CS observing the following
   sequence:

-  1st ground angle in XoY plane,

-  2nd inclination angle to XoY plane,

-  3rd tilt angle around the now rotated X-axis of the library object
   CS.

As soon as a library object is defined, it is given an object number: 1,
2 etc.

▪ This number is shown in the tree element on the left hand side.

▪ A preview of the library object is shown on the right hand side.

▪ Bottom right under the picture you can enter descriptive text. This is
for better documentation. The first line of the text will also be shown
in the tree element on the left, next to the number. This makes it
easier to identify library objects and their function.

.. _section-60:

10.01
^^^^^

Library Object:

▪ You can select as many library objects as you want to. In order to
make the LB available on other systems, it is advisable to keep the
necessary libraries in the same directory as the LB files.. For more
information see section ‘Logic Blocks: Design, File Structure’.

▪ As of Version 13.01, library objects can be inserted as variables. You
can use variable with the unit Text or Enum as well as calculations with
the unit Text. Library objects that are inserted in the same way, with
the same long/ short information, can be managed with one entry. The
decision which library objects to insert can be made in a calculation.

.. _section-61:

10.01
^^^^^

.. _section-62:

13.01
^^^^^

‘to insert LB in’ and Conditions:

▪ Here you can define under which conditions the library objects should
be inserted. For more information refer to the section ‘Conditions’.

.. _section-63:

10.01
^^^^^

You can assign item number to inserted library objects. The item number
will apply to all parts of the library object. If objects should have
different item numbers, they have to be kept in a separate library
object. If the item# field is empty, the original item numbers of the
library parts remain.

▪ The shape of library objects remains the same, only the item# will
change; accordingly item numbers with profile description cannot be
selected.

▪ The variable can be part of the user prompt. With the browser button
in the user prompt you have access to the material dbase.

▪ Item number can be prompted via variables. Variable unit has to be
‘Item#Np’ (without profile description). Alternatively you can use lists
of options (Enum) or text variables (txt).

▪ The item number can also be taken from a user prompt object.

▪ Like this objects can receive item numbers for bills of materials and
other evaluations. It is not necessary to provide separate library
objects for each item number.

▪ Item numbers can be arranged from a number of text strings. This can
be used to add a size to an item number. e.g. You want to compare an
item# with the text **‘rod’** and the diameter ‘Vdia’ in full mm. The
expression for the item# would be ‘rod#Vdia[mm,0]#’. For more
information refer to section ‘Variables in Text, Item Numbers’.

.. _section-64:

11.01
^^^^^

Item numbers can be defined wit fixed values or you can use variables.
The item number will apply to all parts of the library object. If
objects have to be different, they have to be kept in a separate library
object. If the respective field is empty, the original properties of the
library parts remain.

▪ In the user prompt a browser button will open the texture browser.
Textures are shown in preview. Accordingly the additional colors can be
selected.

▪ Like this, objects can receive individual visual appearance. It is not
necessary to provide separate library objects for each item number.

.. _section-65:

11.01
^^^^^

Insert in Group / Building Part:

▪ The inserted library object will be assigned to a group MOS. If the
group field is empty, the original group assignments of the library
parts remain.

▪ The inserted library object will be assigned to the specified building
part (MOS).

.. _section-66:

11.01
^^^^^

::

   Insert in Slice (empty = outside) / Orientation:
   ▪ Orientation = free: The library object will be positioned directly at the insertion-CS. It will
   belong to the specified building part, but the orientation will be defined by the insertion-CS.
   ▪ Orientation = parallel Building Part: Now you can also specify a slice. The origin of the
   insertion-CS will be projected perpendicular onto the slice. Depending on the type of building
   part a projected insertion-CS will be calculated. Afterwards offsets and orientation will refer to
   this CS. For a detailed description of these processes please refer to section: Offsets and
   Projected Insertion-CS.

::

   ▪ Slice = empty the origin will be projected onto the outside surface of the building part. For
   walls and trusses this may be the front or back face depending on the orientation of the
   insertion-CS. For ceilings and roof surfaces this is always the top face.
   ▪ For insertion in storey, roof or D-CAM free design the orientation defaults to 'free'.

.. _section-67:

12.01
^^^^^

::

   ▪ After generating a 3D library object, it can be assigned to any number of user-defined MOS.
   ▪ The name of the user-defined MOS is simply entered as a text. Use tilde ~ in order to
   separate several user-defined MOS.

.. _section-68:

16.01
^^^^^

::

   X-, Y-, Z-Offsets, Ground-, Inclination- and Tilt Angles:
   ▪ These are translation offsets and rotations that are applied according to the sequence
   described above.

.. _section-69:

10.01
^^^^^

::

   Distribution of library objects
   Where you define coordinates in order to position library objects, you can define arrays.
   ● In every coordinate field you can enter an array as follows ( ORIGIN~SPACING~QUANTITY ). A
   quantity of 1 means that you get only 1 object in origin.
   ● If you specify an array, you have to do so in X, Y and Z.
   X(1.0~0.1~5)Y(0.0~0.0~1)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step
   size 0.1

::

   X(1.0~0.1~5)Y(0.0~0.2~4)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step
   size 0.1, this row 4 times along Y step size
   0.2.
   ● With arrays, you can define rows, grids and 3 dimensional grids of library objects in one go.

.. _section-70:

13.01
^^^^^

::

   List of resizing definitions: When you save a library object, you can define sections, where you
   want to be able to lengthen or shorten the library objects.
   ▪ No. and Resize describe the length adjustments, e.g. in what direction the change will apply.
   ▪ Actual Length shows the actual length of the library object before it is resized. The actual
   length is taken in the direction of the length adjustment at the maximum extent of the library
   object.
   ▪ Theoretical Length: Here you can enter the required length as fixed value or with a formula.
   The length of library objects will be adjusted by the difference between actual and theoretical
   length at the point specified.

.. _section-71:

10.01
^^^^^

3.14 Logic Blocks - Smart Tags
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Smart Tags can be part of a Logic Block. The values for the variables of
the Smart Tag can be specified with fixed values or formulas. The Smart
Tag will be applied with the function ‘at Point’. Starting from this
point the Smart Tag will look for objects to apply to. They can apply to
objects and library objects of the LB, but also to objects already
existing in the building. With a special filter function it is possible
to define in detail what objects should affected. Objects created with
the LB can be addressed specifically.

Smart Tag:

▪ You can select as many Smart Tags as you want to. In order to make the
LB available on other systems, it is advisable to keep the necessary
Smart Tags in the same directory as the LB files. For more information
see section ‘Logic Blocks: Design, File Structure’.

.. _section-72:

10.01
^^^^^

List of Smart Tag variables:

▪ No. and ‘Variable Name’ describe the variable of the Smart Tag.

▪ Default value shows the initial default value of the variable.

▪ Desired Value: Here you can enter the required value a fixed value or
as formula.

.. _section-73:

10.01
^^^^^

Reference for ‘at Point’:

▪ With the X-, Y- and Z-offsets you define a point in the insertion-CS.

▪ The Smart Tag will be applied at this point, similar to manually
selecting a point when applying a Smart Tag ‘at Point’ ▪ The point will
be projected perpendicular onto the specified reference side. The X-
coordinate of the projected point in the CS of the reference side can be
used as length position, the Y-coordinate for the cross dimension.
(Access cross dimension ‘from the left’). ▪ The X- and Y-position of the
reference point have to be used for calculations inside the Smart Tag.
They cannot be used in formulas inside the LB.

.. _section-74:

10.01
^^^^^

Distribution of SmartTags

Where you define coordinates in order to position SmartTags, you can
define arrays.

● In every coordinate field you can enter an array as follows (
**ORIGIN\ SPACING\ QUANTITY** ). A quantity of 1 means that you get only
1 object in origin.

● If you specify an array, you have to do so in X, Y and Z.

::

   X(1.0~0.1~5)Y(0.0~0.0~1)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step
   size 0.1

::

   X(1.0~0.1~5)Y(0.0~0.2~4)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step
   size 0.1, this row 4 times along Y step size
   0.2.

● With arrays, you can define rows, grids and 3 dimensional grids of
SmartTag processes in one go.

.. _section-75:

13.01
^^^^^

‘to insert LB in’ and Conditions:

▪ Here you can define under which conditions the Smart Tag should be
applied. For more information refer to the section ‘Conditions’.

.. _section-76:

10.01
^^^^^

Affected Objects: Here you can set up the filter to define what objects
the Smart Tag should apply to. The individual conditions are ‘AND’
conditions. They all have to be true in order for the Smart Tag to
apply.

▪ Object Type: Here you define what object types are affected
(e.g. beam, sheet material, etc.)

▪ Objects belong to: Here you can limit the Smart Tag to objects that
belong to e.g. a wall, roof, truss, etc. Additionally you define whether
the objects belong to the current BP (e.g. wall) or an arbitrary BP
(e.g. wall).

▪ Groups: Limit the ST to objects of certain groups. You can specify
individual groups separated with a forward slash (-2/1/3) or consecutive
areas indicated by points (3..6). You can mix individual groups and
areas of groups (-6..-4/1/3/6..8)

▪ Beam Types: Limit the ST to certain types of beams. You can specify
individual beam types separated by a forward slash (211/221/321) or
consecutive areas indicated by points

.. _section-77:

10.01
^^^^^

::

   (210..216). You can mix individual beam types and areas of beam types
   (110..129/321/333/621..628).

::

   ▪ Item#: Limit the ST to certain item numbers. You can enter a certain item# or use wildcards.
   Use an asterisk (*) as wildcard. e.g. 'C*' would apply to 'C24', 'C26', 'C30' etc.
   ▪ Max. distance to Ref. Point: Limits the ST to all objects that are within this limit in X-Y- or Z-
   direction. This means that the affected objects make contact with a virtual box that's formed
   around the reference point with an edge length of 2x this limit.
   ▪ You can either use the filter or specify actual objects in the field on the bottom.

::

   Object / Object /..: Here you can specify objects created by the LB or user prompt objects to
   assign ST to them.

::

   ▪ Individual objects are separated with forward slashes (K1/K2/B1/B2)
   ▪ User prompt objects are named 'K' with a consecutive number.
   ▪ Objects created by the LB are named 'B' with a consecutive number.
   ▪ If you specify explicit objects here, the 'affected objects' filter above will be disabled.

.. _section-78:

11.01
^^^^^

3.15 Logic Blocks - Special processes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

   A group of special processes is available now. This includes Boolean operations to work on solids
   (without machine processes) and a free cut-off.

::

   ▪ General Cut:
   ▪ In many cases it is a lot easier to cut an object with a general cut rather than with a smart
   tag.
   ▪ Similar to the general cut in D-CAM you define a cutting plane via 3 points. With a 4th
   point you define the location of the plane, the 5th point selects the end of the beam that
   you want to cut off.
   ▪ In addition to that you can offset the cutting plane from its location.

::

   ▪ All objects of the first group will be cut.
   ▪ The result is processes. These can be cut-offs and hip-cuts.
   ▪ Intersect
   ▪ The objects of the first group are male, the second group of objects are female. All male
   objects will be subtracted from the female ones. Both object groups remain.
   ▪ If you don't need the male object after it has been subtracted, use the item# TEMPORARY
   for the object. See also temporary objects in logic blocks.
   ▪ Unite
   ▪ All objects of the first group will be united to one object.
   ▪ Object information and the object coordinate system are taken from the first object in the
   group.
   ▪ Combine
   ▪ The object of the first group will be combined with the object of the second group. The first
   object of the first group will be combined with the first object of the second group, etc.
   ▪ Combine: The part both objects have in common will remain.

.. _section-79:

14.01
^^^^^

::

   Logic Blocks - Special Processes - Assign Information: With this special process,information can
   be assigned user prompt objects:
   ▪ It can be assigned: Item number, Beam type / designation, Texture set / Colorize texture,
   Group of objects and User-defined MOS.

.. _section-80:

17.01
^^^^^

::

   ▪ The original information of the object will be kept. If the logic block is deleted, it is reset to
   the original information.

::

   ▪ The information can be assigned to user prompt objects. These are entered in objects / male / 1st
   objects. Accordingly, only K n, K1 , K2 , etc., can be used.

3.16 Logic Blocks - Views
~~~~~~~~~~~~~~~~~~~~~~~~~

::

   Under 'Views' you can define viewpoints of components. They will apply only if the LB creates a
   component. See setting under Logic Block 'Information'.
   The views are defined similar to the general component definitions, but here you can also enter
   formulas to calculate coordinates. For a more detailed description on viewpoints please refer to
   the general program documentation.
   The coordinates refer to the Component-CS:
   ▪ That's why the use of formulas and calculations should not be necessary. You can also use
   the pre-set definitions of default views (front, top, etc...).
   ▪ Coordinates of user prompt points or objects cannot be used directly. They have to be re-
   calculated to the Component-CS.

.. _section-81:

11.01
^^^^^

3.17 Logic Blocks - 2D Drawing Objects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

With LBs you can insert previously saved 2D drawing sections. You can
save drawing sections in D-CAD 2D with function ‘1- 5 - 1 drawing
section’ or in the construction modules (module 1 through 8) with
function ‘1- 5 - 4 drawing section’.

Inserting drawing sections with a LB automates the manual insertion
process:

::

   ▪ A drawing section is saved with its own CS. The position of this CS is defined by the current CS at
   the time the drawing section was saved.
   ▪ If a drawing section is inserted its CS will initially match the insertion-CS (or projected insertion-
   CS).
   ▪ Then the drawing section will be moved together with its CS according to the offsets in X-, Y- and
   Z-direction.

::

   ▪ Finally the drawing section will be rotated around the moved origin of its CS in the drawing plane.
   ▪ The available offsets and rotations depend on the situation, especially on the LB type and the BP
   the drawing section has been inserted in.
   ▪ A more detailed description on the process you can find in section: Offset and Projected Insertion
   CS

::

   As soon as a drawing section is defined, it is given a number: 1, 2 etc.
   ▪ This number is shown in the tree element on the left hand side.
   ▪ A preview of the drawing section object is shown on the right hand side.

::

   ▪ Bottom right under the picture you can enter descriptive text. This is for better
   documentation. The first line of the text will also be shown in the tree element on the left,
   next to the number. This makes it easier to identify drawing sections and their function.

.. _section-82:

10.01
^^^^^

::

   2D Drawing Section: 10.01

::

   ▪ You can select as many drawing sections as you want to. In order to make the LB available on
   other systems, it is advisable to keep the necessary drawing sections in the same directory as
   the LB files. For more information see section 'Logic Blocks: Design, File Structure'.
   ▪ As of Version 13.01, drawing sections can be inserted as variables. You can use variable with
   the unit Text or Enum as well as calculations with the unit Text. Drawing sections that are
   inserted in the same way, with the same long/ short information, can be managed with one
   entry. The decision which library objects to insert can be made in a calculation.

.. _section-83:

13.01
^^^^^

::

   'to insert LB in' and Conditions:
   ▪ Here you can define under which conditions the drawing section should be inserted. For more
   information refer to the section 'Conditions'.

.. _section-84:

10.01
^^^^^

::

   Insert in:
   ▪ The drawing section will be inserted into the drawing area of the selected building part.

.. _section-85:

10.01
^^^^^

::

   X-, Y-, Z-Offsets, Ground Angle:
   ▪ These are translation offsets and rotations that are applied according to the sequence
   described above.

.. _section-86:

10.01
^^^^^

::

   List of resizing definitions: When you save a drawing section, you can define sections, where you
   want to be able to lengthen or shorten the drawing objects.
   ▪ No. and Resize describe the length adjustments, e.g. in what direction the change will apply.
   ▪ Actual Length shows the actual length of the drawing section before it is resized. The actual
   length is taken in the direction of the length adjustment at the maximum extent of the library
   object. This will only affect lines, circles, etc... Dimension lines or text will not change.

::

   ▪ Theoretical Length: Here you can enter the required length as fixed value or with a formula.
   The length of drawing section will be adjusted by the difference between actual and
   theoretical length at the point specified.

.. _section-87:

10.01
^^^^^

3.18 Logic Blocks - Dimensions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In LB you can create dimension lines.

▪ These dimension lines can be part of the current BP but may also
belong to other building parts. E.g. you can insert a LB into a wall and
add a dimension line in ground plan (storey).

▪ The points to be dimensioned are defined via coordinates with all
options of formulas. Any arbitrary points of the LB can be dimensioned.
Additionally certain points of the BP are available, e.g. left end of
wall.

▪ Dimensions from various LB can be combined in one dimension line. E.g.
you have inserted a number of objects in a wall and want to add one
dimension line to dimension their location. You can define the
dimensions in the LBs such, that they will be combined in one continuous
dimension line. Also if you edit the dimension line manually it will
react accordingly.

The orientation of the dimension line and the dimensioned points depend
on different coordinate systems:

::

   ▪ The orientation of the dimension lines is based on the insertion-CS if they are created in the basic-
   BP; else they will base on the projected insertion-CS. For more information see; Offset and
   Projected Insertion Coordinate Systems.
   ▪ The dimension points are based on the insertion-CS. They are projected perpendicularly onto the
   drawing plane. This is the drawing plane of the BP the dimension line should be inserted in.
   ▪ Since the points are projected into a plane, one coordinate will automatically be 0. In most cases
   this coordinate will already be blocked for the input.

As soon as a dimension is defined, it is given a number: 1, 2 etc.

▪ This number is shown in the tree element on the left hand side.

▪ Bottom right under the picture you can enter descriptive text. This is
for better documentation. The first line of the text will also be shown
in the tree element on the left, next to the number. This makes it
easier to identify the dimension lines and their function.

.. _section-88:

10.01
^^^^^

Dimension Style: Style of the dimension line.

▪ Select the name of the dimension style. The list shows the saved
settings, not the ones currently available in the project.

▪ Only the name of the dimension style will be saved.

▪ Once the LB is inserted and a dimension style with this name exists in
the project, these settings will be applied.

::

   ▪ If the style does not exist in the project, but in the saved settings, the style will be added
   to the project settings.
   ▪ If the dimension style is not available at all, the dimension line will not be created, and an
   error message will appear.

.. _section-89:

10.01
^^^^^

Layer: The layer where the dimension line will be put on.

▪ Select the name of the Layer. Both drop list and browser button will
show a list of the currently available layers of the project.

▪ Only the name of the layer will be saved.

▪ Once the LB is inserted, a layer with the same name is searched within
the building. If the layer is found, its settings will be applied. ▪ If
the layer does not exist yet, it will be generated with default
settings: line type = continuous, line weight = default thickness from
‘D-CAM 1- 7 - 2’, color set = black, Scale = 1:50.

▪ In order for the dimension line to appear properly you need to define
a scale. The scale is defined with the layer in the construction
modules. The dimension line will then be shown in the proper relation
with the other objects. ▪ If the scale of the layer where the dimension
line is inserted is 1:1, the dimension line will be hardly readable. If
this is the case, a dialog box will appear automatically, which allows
you to adjust the scale of the layer.

.. _section-90:

10.01
^^^^^

Dimension type: Type of dimension line (e.g. base line, distance, …).
10.01

Additional info, position of additional text:

▪ Dimension lines may, as in manual, input include additional text. The
additional text may be composed of direct strings and variables. For
more info see ‘Variables in texts, Item Numbers’.

▪ Position of additional text as in manual dimension line input.

.. _section-91:

10.01
^^^^^

Dim Line Tag: Dimension lines with identical tags will be united to one
dimension line.

▪ The tag can be alphanumerical (text and numbers). It should resemble
the function of the dim line. e.g. ‘Sanitary’.

▪ Dim lines without tag will not be combined with other ones.

▪ In order for dim lines to be combined, the following settings have to
match: ▪ Dim Line Tag ▪ Orientation in drawing plane ▪ Dimension Type

.. _section-92:

10.01
^^^^^

::

   ▪ Building Part they belong to
   ▪ Building part they refer to, see further down
   ▪ Layer

‘to insert LB in’ and Conditions:

▪ Here you can define under which conditions the dim line should be
inserted. For more information refer to the section ‘Conditions’.

.. _section-93:

10.01
^^^^^

Position in: The dim line will be created in the specified BP

▪ Only building parts that actually exist at this time can be used.

.. _section-94:

10.01
^^^^^

Orientation: For the general orientation of the dim line you can select
from the following options: ‘horizontal (along X)’ and ‘vertical (along
Y or Z)’

▪ The orientation of the dimension lines is based on the insertion-CS if
they are created in the basic-BP; else they will base on the projected
insertion-CS. For a more information see Offset and Projected Insertion
Coordinate Systems.

.. _section-95:

10.01
^^^^^

Dim. Line Offset: Distance of the dim line to the axis of the projected
insertion-CS.

▪ For horizontal (along X) this is the distance to the Y- or Z-axis. For
vertical (along Y, or Z) this is the distance to the X-axis.

▪ e.g. you insert a LB into a wall and generate a dim line in the storey
parallel to the wall (=horizontal). A negative distance will move the
dim line away from the wall.

▪ If the dim line is moved manually later on, the new distance value
will be entered into the inserted LB. If you re-calculated the inserted
LB the moved dim line will remain at its position.

.. _section-96:

10.01
^^^^^

Building Part to refer to, Edge to refer to, Building Part - Reference
Slice: You can include certain points of existing BP in the dimension
line.

▪ At the moment you can use slice outlines of walls.

▪ The slices outline which shall be taken into regard is defined under ’
Building Part - Reference Slice’.

▪ In ‘Edge to refer to’ you define what edge of the slice outline should
be dimensioned in the dim line. This depends on the orientation of the
dim line:

::

   ▪ For horizontal dim lines you can select the left, the right, left and right or the next closest
   vertical edge. The next closest vertical edges are normally edges of door and window
   openings.
   ▪ For vertical dim lines you can select the bottom, top or both slice edges. The routine will
   look for edges at the origin of the insertion-CS. This has to be observed especially for walls
   with slanting top edges.

.. _section-97:

10.01
^^^^^

Dimension points, X-, Y-, Z-Distance: enter coordinates of as many
points as you like to dimension them.

▪ Observe coordinate systems as you specify points; see description at
the beginning of this section. Depending on the orientation of the dim
line the irrelevant coordinate will be set to 0 and locked.

▪ There have to be at least 2 points, or one point and a reference to a
slice outline defined.

▪ A distribution formula can be used to generate equally distributed
dimensioned points within one step. If structural objects, library
elements or SmartTags have been generated with a distribution formula in
the same Logic Block, it is often convenient to use the same values
again for the distributed dimensions: \**Variables_Ud16_*.doc\ **,
Chapter ” Arrays in formulas “. If you use e.g. the
formula**\ (1.20\ :sub:`0.33`\ 5)*\* for the X-coordinate, 5 points will
be dimensioned with a distance of 0,33m, starting at 1.20m.

.. _section-98:

10.01
^^^^^

3.19 Logic Blocks - Text, Labels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In LB you can create single line text and single line labels. For labels
you can define the position of the text and the reference point for the
leader line.

▪ Text and labels can be part of the current BP but may also belong to
other building parts. E.g. you can insert a LB into a wall and add a
dimension line in ground plan (storey).

▪ The text may be composed of direct strings and variables. For more
info see ‘Variables in texts, Item Numbers’.

The orientation of the text and the position of reference points depend
on different coordinate systems:

::

   ▪ The orientation is based on the insertion-CS if they are created in the basic-BP; else they will base
   on the projected insertion-CS. For a more information see Offset and Projected Insertion
   Coordinate Systems.
   ▪ Generally the orientation is parallel to the X-axis and the rotation angle rotates in mathematical
   positive sense (counter clockwise)
   ▪ The points for position and reference point are defined in the insertion CS. Then they are projected
   onto the drawing plane. This is the drawing plane of the BP the text should be inserted in.
   ▪ Since the points are projected into a plane, one coordinate will automatically be 0. In most cases
   this coordinate will already be blocked for the input.

::

   As soon as a text or label is defined, it is given a number: 1, 2 etc.
   ▪ This number is shown in the tree element on the left hand side.
   ▪ Bottom right under the picture you can enter descriptive text. This is for better
   documentation. The first line of the text will also be shown in the tree element on the left,
   next to the number. This makes it easier to identify the dimension lines and their function.

.. _section-99:

10.01
^^^^^

::

   Text style: Text Style to be used.

::

   ▪ Select the name of the text style. The list shows the saved settings, not the ones currently
   available in the project.
   ▪ Only the name of the text style will be saved.
   ▪ Once the LB is inserted and a text style with this name exists in the project, these settings
   will be applied.
   ▪ If the style does not exist in the project, but in the saved settings, the style will be added
   to the project settings.

::

   ▪ If the text style is not available at all, the text will not be created, and an error message
   will appear.

.. _section-100:

10.01
^^^^^

::

   Layer: The layer where the text will be put on.
   ▪ Select the name of the Layer. Both drop list and browser button will show a list of the
   currently available layers of the project.
   ▪ Only the name of the layer will be saved.
   ▪ Once the LB is inserted and a layer with this name will be searched for in the project. If the
   layer exists, its settings will be used.

::

   ▪ If the layer does not exist yet, it will be generated with default settings: line type =
   continuous, line weight = default thickness from 'D-CAM 1- 7 - 2', color set = black, Scale =
   1:50.

.. _section-101:

10.01
^^^^^

▪ In order for the text to appear with proper height you need to define
a scale. The scale is defined with the layer in the construction
modules. The text will then be shown in the proper relation with the
other objects. ▪ If the scale of the layer where the text is inserted is
1:1, the text will be hardly readable. If this is the case, a dialog box
will appear automatically, which allows you to adjust the scale of the
layer.

Text: The text may be composed of direct strings and variables. For more
info see ‘Variables in texts, Item Numbers’.

.. _section-102:

10.01
^^^^^

Text type: Here you differentiate between single line text and single
line label.

▪ For single line text the settings for the reference point are greyed
out.

.. _section-103:

10.01
^^^^^

Text to Destination Point: Here you can define the alignment of the text
left or right aligned to the reference point.

.. _section-104:

10.01
^^^^^

‘to insert LB in’ and Conditions:

▪ Here you can define under which conditions the text or label should be
inserted. For more information refer to the section ‘Conditions’.

.. _section-105:

10.01
^^^^^

Position in: The text or label will be created in the specified BP

▪ Only building parts that actually exist at this time can be used.

.. _section-106:

10.01
^^^^^

Rotation Angle:

▪ The orientation is based on the insertion-CS if they are created in
the basic-BP; else they will base on the projected insertion-CS. For a
more information see Offset and Projected Insertion Coordinate Systems.

▪ Generally the orientation is parallel to the X-axis and the rotation
angle rotates in mathematical positive sense (counter clockwise)

.. _section-107:

10.01
^^^^^

Text Reference Point, X-, Y-, Z-Distance: Enter the coordinates of the
point the text should be positioned at:

▪ Observe coordinate systems as you specify points; see description at
the beginning of this section. Depending on the BP of the text the
irrelevant coordinate will be set to 0 and locked.

▪ e.g. you insert a LB into a wall and generate a text in the storey. A
negative Y-distance will move the text away from the wall.

▪ If the text is moved manually later on, the new distance value will be
entered into the inserted LB. If you re-calculate the inserted LB the
moved text will remain at its position.

Label Reference Point, X-, Y-, Z-Distance: Enter the coordinates of the
point the leader line should be positioned at:

▪ Observe coordinate systems as you specify points; see description at
the beginning of this section. Depending on the BP of the text the
irrelevant coordinate will be set to 0 and locked.

4 Subsequent editing of inserted logic blocks
---------------------------------------------

4.1 Recalculating logic blocks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Logic blocks can be recalculated: Generally by calling the function 7- 9
- 1, for doors with 4-5, for windows and niches with 4-04.

**4.1.1 Recalculation not possible, missing components**

(22.01) If it is not possible to change or execute the logic block due
to missing libraries, partial drawings or smart tags, a message appears.
In this dialog now also the first, not found file is displayed. This way
the missing files can be added step by step if necessary.

**4.1.1 Rereading and calculating logic blocks**

(22.01) Many logic blocks have already been entered in projects; mainly
in windows but also in any other form. One or more of these logic blocks
were changed. In order to be able to use the new version of the logic
blocks, it was now necessary to reselect the logic blocks in the windows
(doors and niches). For other types of logic blocks the already inserted
logic block had to be removed and the changed one had to be entered
completely new. With the function *7 - 9 - 8 Read and calculate logic
blocks again* , any number of logic blocks already inserted can now be
selected directly. The corresponding modified logic block is read in
again, whereby the input values of the variables, selected points and
objects, etc. are retained. The newly read logic blocks are then
recalculated.

The prerequisites for this are:

▪ The logic block is still in the same directory. The system directory
%DHPKOL% can be changed; it depends on the underlying directories.

▪ File name of the logic block file and name of the logic block must
still match exactly.

▫ For logic blocks supplied by Dietrichs, note that directory names,
file names and logic block names are partially translated. Internally,
not the plain texts but the language-neutral identifier is stored,
e.g. #203 for “window”.

▪ The type of the logic block must match: A logic block for basic
insertion can only be replaced with one of this type.

▪ The following procedure is used with variables:

▫ of already existing variables the value is kept

▫ newly added variables are given the default value

▫ variables that no longer exist are simply removed.

▪ The number of User prompt points and the number of User prompt objects
must match exactly.

▪ The smart tags and libraries used in the modified logic block must
also be present.

If prerequisites are not met:

▪ the existing logic block is retained.

▪ A corresponding message appears describing the reason for this.

▪ In the message, the directory, file name and combination element name
are displayed both in plain text and in the internal form with
language-neutral identifiers. This makes it easy to find the file even
with Explorer or TotalCommander.

This function saves a lot of input work when changing logic blocks.
Errors and loss of information due to re-entry are avoided. The function
also supports the development of logic blocks very well: Often you can
check the changes made without having to re-enter the logic block.

5 Log
-----

::

   Date Chapter Remark
   05.10.12 Additional Building Parts:
   LB type 'at point, object'

::

   Revised sentence: The first prompt object that belongs
   to a roof or roof surface defines the roof.

::

   13.08.13 Logic Blocks - Objects
   Logic Blocks - Library
   Objects

::

   Logic Blocks - Smart Tags

::

   Distribution of objects, library items and SmartTags

::

   13.08.13 Calculations - Import, edit
   with text editor

::

   Edit calculations with an external text editor.

::

   13.08.13 Logic Blocks – User Prompt Separate dialogues for user prompt and variables. Refer to the
   following chapter.
   13.08.13 Logic Block - Connections Connections^

::

   19.08.13 Basic-Coordinate Systems Paragraph added in "for windows and doors"^
   21.10.13 Logic Blocks: Design, File
   Structure

::

   Bottom paragraph "As of Version 13..." added.

::

   21.1.13 Logic Block - Library
   Objects Logic Block-
   Drawing Sections

::

   Library objects and drawing sections via variables

::

   07.07.14 Temporary objects in logic
   blocks

::

   New chapter temporary volumes

::

   07.07.14 Logic blocks - Special
   processes

::

   New chapter special processes

::

   22.09.14 Logic blocks - connections Miter^ cut now available^
   22.10.14 Logic blocks - Extruded
   objects

::

   Extruded objects

::

   22.10.14 Logic blocks - info - Logic
   Blocks at Windows and
   Doors

::

   Info: logic blocks at windows and doors

::

   17.09.15 Logic Blocks - Insertion - at
   Door, Window

::

   Correction: Orientation of Z and X offset as implemented:
   Opposite to timber frame guidelines

::

   08.08.16 Diverse chapters Entries are flagged with 16.01^

::

   14.06.17 Calculation of Coordinates
   for Insertion CS

::

   New chapter

::

   14.06.17 Various chapters Entries are marked with 17.01^

::

   14.06.17 Logic Blocks - Insertion –
   Positioning Point

::

   Line removed

::

   22.01.19 Variables und calculations
   of logic blocks in openings
   (doors, windows and
   niches)

::

   Chapter added

::

   15.01.20 Logic Blocks - Queries Logic Blocks –^ Automatic searched user prompt objects^

26.01.21 Basic-Building Parts

::

   Basic-Coordinate Systems

::

   Addition of base coordinate system at points, objects for other
   program modules

03.01.22 Subsequent editing of inserted logic blocks

::

   Additions for 22.01
