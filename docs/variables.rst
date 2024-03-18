Variables
=========

Version 23
~~~~~~~~~~

.. _variables-1:

1 Variables
===========

1.1 Variable System
-------------------

In dialogues definitions are made by entering fixed values. A lot of
time it would be beneficial to be able to manipulate such definitions
‘from outside’ or to specify values with dependency on other settings.
These requirements can be met by a system to define and use variables.
Instead of giving a fixed value to e.g. the height of a beam you enter a
variable. This variable is entered in a central location e.g. in the
‘default values’ of a building file. This default value will now be
entered in all dialogue boxes where the variable has been used to define
the height of a beam without having to open each box and make manual
adjustments. Other variables, such as the thickness of slices, are
automatically provided by the system.

▪ The ‘System of Variables’ is used in ‘Default Values’, ‘SmartTags’,
‘Wall Guideline Editor’ and ‘Logic Blocks’.

▪ In every editor it is possible to define the specifications of
variables in the **variable definition dialog**. Once the user is
prompted to specify default values or a Smart Tag or Logic Block is
positioned, the user will be prompted to enter or edit the values of the
defined variables. The dialog box is the **user variable prompt**.

**1.1.1 User Variables**

▪ ▪The variable that can be defined by the user are called **User
Variables**. There are also variables that provide values and
information about objects and building parts. These are called **system
variables (SV)** , they are hard wired in the system and cannot be
edited or defined.

▪ The UV can be freely defined.

::

   ▪ The variable name has to start with a capital 'V', as to set them apart from the SV. The naming
   makes UV easy to recognize and handle. e.g. 'VdBm' as Variable depth Bird's mouth
   ▪ Variable names are alpha numeric and may be structured with underscores. Spaces, Operations (+,

-  , \*, /), punctuation, brackets or other special characters are not
   allowed. ▪ ▪Names are case sensitive; **Vab** is different from VAB.
   It is not advisable to use upper and lower case to keep different
   variable names apart.

▪ Variables can be arranged in groups. If there are more than one group
in a variable prompt, they will be shown in separate sub sections. Each
sub section can be opened by clicking the respective button. Each
variable group automatically generates a button in the dialogue box.

▪ You can add descriptive text and help pictures to each variable. The
text and picture show up in the variable prompt and when you insert a
variable in a function or calculation.

▪ Sets of variables can be saved and managed with the usual routine. A
variable set contains definitions of a number of variables. A set of
variables can be saved and reused for other purposes. Sets of variables
can be shared with other users via ‘data exchange’, e-mail attachment
etc. When you load a variable set you have a choice of replacing
existing variables or just adding new ones.

**1.1.2 Dietrich’s Default Variables**

Dietrich’s provides a comprehensive set definitions based on user
defined variables. This is the Dietrich’s default set of user variables.
Like user variables, they can be edited freely. To avoid naming
conflicts and overwriting of variables please observe the following
rules:

1) Dietrich’s default variables also start with V followed by an
   underscore ‘V\_’. Avoid naming your own user variables using ‘V\_’
   and you will not run into conflicts with the default set.

2) You are free to use Dietrich’s default variables in prompts and
   settings. Doing that, please don’t change the intention of the
   variable itself.

1.1.2.1 Dietrich’s Default Values

Together with the update we provide a comprehensive and coherent
collection of default values and prepared settings for the program
modules Roof, Wall, Ceiling, Truss and the related processes. The
default values used are called ‘Dietrich’s Default Values’. They are
based on the ‘Dietrich’s Default Variables’ mentioned above.

In order for the prepared settings to work properly, the ‘Dietrich’s
Default Values’ have to be available. If you load the under 1-6 Default
values, you can use them and change the values. If you don’t include all
variables, some values are not available and some settings might not
work. In order to have all settings with working reasonable values, the
missing variables will be made available from a separate list. In the
formula editor, you will find this list in the tree element under
‘Dietrich’s Default Values’. The default values you specify under 1-6
Default Values are in the list of ‘User Defined Variables’.

**1.1.3 System Variables**

System variables offer values that come from the system directly. They
make information about building parts and objects available for use in
calculations, conditions and functions, e.g. slice thicknesses, point
coordinates, etc.

System variables are available through the formula editor. They come
with description text and help pictures.

**1.1.4 Ranking of Variables**

▪ Generally, the variable system is continuous over all levels. A
variable that has been defined on a project level can be used in
positions, SmartTags, Logic Blocks and wall guidelines.

▪ Variables that serve as default values will be linked through to the
next level, always keeping the value that has been defined last: ▪ E.g.
you define a post width of 0,06m on a project level. Each file within
this project can access this variable and all posts will be generated
with a width of 0,06m. If the default values of one building file
(position level) of this project redefines the same variable with a post
width of 0,08m the posts in this file will be 0,08m wide, whereas the
post width in all other files will remain 0,06m. ▪ A wall guideline that
is applied in the same building file will also use the 0,08m post width.
If the variable is defined inside the wall guideline with a width of
0,10m the guideline will use this value in the same building file.

▪ The tag ‘external’ will reverse this ranking.

::

   ▪ E.g. the variable for post width is defined with 0,06m on a building file level; the 'external' tag is
   set. All posts generated in the building file will be 0,06m wide. If the same variable is defined on
   project level (one level up) with 0,12m, the posts generated in the building file will be 0,12m wide.
   The external value coming from project level will have higher priority than the value on position
   level.
   ▪ The same variable used in a wall guideline with the 'external' flag set will now also generate 0,12m
   wide posts coming from the building file or directly from project level.
   ▪ Externally defined variables can be used to initiate a value for a variable. The variable will receive
   this value if not otherwise defined on a higher level. Like this you can make sure that the variable
   in e.g. a wall guideline has a value, even if it has not been defined for the building file or project
   level.

1.2 Definition of Variables
---------------------------

**1.2.1 Variable Definition, Properties of Variables**

Variables can be edited in the variable list or the variable definition
dialog box. In the list you can quickly define variables, edit values
and sort them. The dialog offers a more elaborate definition of
variables. The following describes the columns of the list of variables;
the further explanations describe functions to be found in the variable
definition dialog.

▪ Using the dialog box is recommended to add description text and to
enter a list of possible values for an ‘ENUM’ type variable (enumeration
= list)

▪ The sequence of appearance inside the variable list can be changed by
moving variables up or down. Un-used variables can be deleted; new ones
can be added any time. See the buttons on the right hand side under the
list.

Column F / Fixed Value: If this box is ticked, the variable cannot be
changed in the user prompt (14.03) (In former versions the variable was
not even visible in this case). Fixed values are used to define values
the designer of the LB might want to change later on, but should not be
open to the general user.

Column E / External: This tag reverses the priority that defines the
value of the variable: If the variable is defined on a higher level this
value will be used instead.

::

   Example: The same variable is defined in a building file and in a Logic Block. Normally, the
   Logic Block would use the value given inside the Logic Block. Now we define the variable to
   receive its value externally:
   ▪ If the variable exists in the building file, its value will now be used in the Logic Block. The
   variable prompt of the Logic Block will show the variable with the value coming from the
   building file. The value can be erased.

::

   ▪ If the value for the variable is taken from external, the input field is green. If the
   external value is altered, the change is adopted in the field.
   ▪ If you overwrite the default value, the input field becomes red. The manually entered
   value is kept also if you change the default value.
   ▪ If you highlight the manually entered value and delete it with "DEL", the default value
   appears again and the field is highlighted with green color.
   ▪ If the variable does not exist in the building file, the value from inside the Logic Block will
   be used. The variable prompt of the Logic Block will show the variable with the value
   coming from the Logic Block. Its value can be edited.
   ▪ If the variable should not appear in the prompt, you can put a check mark in the H-
   column. (In former versions, the column F (fixed value) was used in this case).
   If you want to use a variable in a Logic Block, Smart Tag or wall guideline, you have to define
   it there in order to make it appear in the formula editor.

Column H / Hidden (14.03) By default, all variables are represented at
input now, no matter if they are “fixed values” or “external”. If you do
not want a variable to be represented at input, check the box
“H”(hidden). Existing definitions of fixed values from older version are
automatically set to “invisible” so that the behavior is the same as
before.

Column Variable/ Variable Name: Name of the variable to be used in
functions and calculations. The browser button next to the name can be
used to load variable sets. You can select a single variable from any
variable set and add it to the list.

Column Variable Prompt / Variable Prompt: This is the text that will
show up in the ‘variable prompt’ dialog box when the LB is inserted. The
user will be asked to enter a value according to this description. In
the formula editor this text will also appear as a short description of
the variable.

Column Default Value / Default Value: This is the initial value of the
variable, the first time the user prompt appears. Once a value is
changed the dialog box will remember the last settings used. With the
button ‘Default Values’ they can be reset to the initial values.

Column Unit / Unit: This defines the unit of the variable value. The
unit controls the available options of the user prompt and show browser
buttons etc. Available units see further down.

Picture / Help Picture: The selected picture is shown in the user prompt
for this variable. The help picture should

::

   assist the user in entering the correct information. Most of the time a picture explains more
   that words ever will. The picture will also assist the designer of the LB or someone who will
   try and adjust it for their purposes. The last help picture will also be shown for the next
   variables unless they have their own picture attached.
   For more information on help pictures refer to the respective section.

Variable Group: Variable can be organized in groups. The groups will
structure the visual appearance in the variable prompt dialogue and in
the selection dialogues of the formula editor. If no group is specified,
the variable belongs to the group ‘general’. In variable definition,
specific groups of variables can be accessed by the group buttons. The
list of variables remains visible; the variables of the current group
are shown in blue, the other groups are shown in grey. The list will
jump to the first variable of the selected group. All variables remain
editable. If there is more than one group in a variable prompt, they
will be shown in separate sub sections. Each sub section can be opened
by clicking the respective button. Each variable group automatically
generates a button in the dialogue box.

Variable Display: In den mehrzeiligen Texten der Planelemente können
Variablen eingefügt werden. Intern wird der Variablenname gespeichert,
der jedoch für das Lesen teils ungeeignet ist. Wird der Text editiert,
wird für die Variable die Variablenanzeige angezeigt, wenn sie vorhanden
ist. Beispiel: Für die Eingabe des Lieferdatums in den Vorgabewerten
wird die Variable **V_LDat** verwendet. Definiert man die
Variablenanzeige als **Lieferdatum** , so wird beim Editieren des Textes
die Variable als **#Lieferdatum#** (und nicht als **#V_LDat#** )
angezeigt.

Variable Condition: (V20.02) The variable condition can be used to hide
variables in the variable query of building default values and logic
blocks. The queries can therefore be adapted to the input situation.
This is used to e.g. query only certain variables in a window in an
input situation A (architecture), additional variables in the input
situation C (construction). For control purposes, the standard variable
**V_VarSit** is set in the default values of the project or the building
position and queried in the variable conditions. ▪ **V_VarSit** must be
set before calling the logic block, i.e. in the default values of the
project or the structure position. To use it in the building default
values, it must also be set beforehand, i.e. in the project default
values. ▪ **V_VarSit** should preferably be an enum with, for example,
the values **A: Architectur; C: Construction; X: Administrator**.

::

   ▪ In the conditions, it is advisable to query the values with wildcards so that texts can also
   be adjusted in the default values. The condition (V_VarSit = {A *}) works for the term
   Architecture as well as for Architectural design as well as A: Design department
   etc.
   ▪ For a variable that is only to be queried in the architecture situation (planning phase), the
   condition is then: (V_VarSit={A*}).

::

   ▪ For a variable that is only to be queried in the situations (planning phase) architecture and
   construction, the condition is then: (V_VarSit={A*~c*}).

::

   Variables with the identifier I (invisible) are never queried; the condition is only effective for
   variables for which I is not set.
   If the variable V_VarSit was not set in the default values, then all conditions would be false
   and no conditional variables would be displayed. In this case, the system sets the V_VarSit
   variable to "_" (an underscore). This can be used as follows:
   ▪ The variable is placed at the beginning of the variable queries for building default values
   and logic blocks V_VarSit_NotExist.

. It gets the variable condition: \**(V_VarSit=_)*\* , only appears in
this case. . The following text can be used to query the variables:
**The input situation is not** **defined!**.

. **%DHPABB%:raw-latex:`\DVARSITX`.bmp** should be used here as an
auxiliary image, which provides corresponding information. ▪ So that all
conditional variables are displayed in the case of \**V_VarSit = \_,*\*
it is recommended to include the underscore in the selection. For a
variable that should normally only be queried in the architecture input
situation, the condition is then: \**(V_VarSit = {A \* ~ \_}*\* ). For a
variable that should only be queried in the architecture and
construction input situations, the condition is then: \**(V_VarSit = {A
\* ~ C \* ~ \_}).*\*

::

   Input situation V_Varsit in the current dialog: The variable condition in a dialog (example
   default values building) is usually controlled by the value of V_Varsit that was set externally
   (example default values project). If V_Varsit is now also set in the current dialog, this value
   applies because the variables are read in first and then the display is set up. If you now
   change the value of V_Varsit in the dialog (i.e. in the default values for the building), this
   change only takes effect the next time the dialog is called. V_Varsit is created in the variable
   logic blocks so that it can be used in the formula editor. So that the value is taken over from
   the outside, you simply have to set V_Varsit to external.

Further Values: This list is only available for ENUM type variables.
Here you can specify the options that will appear in a drop down list in
the variable prompt. In the variable definition dialog there is one
value per line. The first value of the list automatically is the
default. In the variable list the values can be written into the
‘default value’ column, separated by semi colons.

Variable Description: Additional explanatory text for each variable.
This text will show up in the variable prompt and in the formula editor
when you pick a variable.

**1.2.2 Available Variable Units:**

Separator In the user prompt the text in column variable prompt will
appear as a headline for the next section. The user cannot enter a value
here. A default value has to be defined but is irrelevant (e.g. enter
‘0’).

Number Numeric value. Integer. This can be used e.g. to specify a number
of elements.

m, cm, mm, in, ft: length units. Meter, centimeter, millimeter, inches,
feet-inches

° Angle in degrees. 306° full circle

A-B Reference faces of objects A or B. A origin, B end. They can only be
used in Smart Tags.

C-F Reference faces of objects C through F (length faces without origin
and end). They can only be used in Smart Tags.

A-F Reference faces of objects A through F (length faces, origin and
end). They can only be used in Smart Tags.

txt Text

Y/N Yes/No: They can only be used in Smart Tags.

Enum Enumeration: List of texts the user can select from. The user
prompt will offer a drop down list and the user can select from a fixed
list of options. The first value of the list automatically is the
default. Use the variable definition dialog box to easily enter the list
items. Enum are used a lot to define conditions, but they can also be
used in texts.

Item#fixt Item number of fixtures. In the user prompt a browser button
allows to access the material dbase. The dbase will only show fixture
objects. This unit is used in Smart Tags primarily.

Item#Np Item number, no profile. In the user prompt a browser button
allows to access the material dbase. The dbase will only show object
types beam, sheet material, mold, auxiliary that do not have a profile
description attached. This unit is used to give 3D library objects a new
item#. Since the library objects can have any shape and form it does not
make sense to give them an item# of an object with a fixed section
profile.

Item#Obj Item number for objects. In the user prompt a browser button
allows to access the material dbase. The dbase will show object types
beam, sheet material, mold, auxiliary. This unit is used to give objects
that are created by the LB an item# and if required a profile
description, to enter I-beams etc.

BeamT Beam type. It can only be used in Smart Tags.

S/C Deliver to Shop or Construction site. It can only be used in Smart
Tags.

Texture SetTexture set for objects or 3D library objects. In the user
prompt a browser button allows to access to the texture sets.

ColTexture Additional color for texture sets. This color will be mixed
with the texture set of objects. In the user prompt a browser button
allows to access to the color selection.

**1.2.3 Variables: Help Pictures**

Help pictures are used to assist users in entering values for variables.

▪ ▪Possible file formats are: \*\*\ *.bmp,*.png, *.wmf,*.emf, \*.jpg**.

▪ Default size of help pictures is 340x340 pixel (used to be 300x300).
If the image file is bigger than that, it will automatically shrink to
fit. To save memory, bigger images (e.g. photos) should be edited with
appropriate software tools (e.g. http://www.irfanview.net/ ,
http://www.getpaint.net/, http://www.gimp.org/ ) to reduce size and
number of colors.

▪ Dietrich’s provides a comprehensive set of help pictures for different
applications. They can be found in the system directory for help
pictures **%dhpabb%** ,
e.g. C::raw-latex:`\Dietrichs12`:raw-latex:`\abb`. These pictures are
generally available for all users with a current release version. If you
share files using these pictures, you don’t have to share the linked
images as well. That’s why variable sets and default value definitions
only contain links to images, not the images themselves.

▪ If a saved set of variables contains links to images in %dhpabb% only
the reference links will be saved. If you link to images from a
different location, the image will be saved in-line with the variables.
If you share your definitions all images will be included either as
references or in-line.

▪ SmartTags only save references to images. If you share a LogicBlock
you will also have to include the images that have not been taken from
**%dhpabb%**

▪ Logic Blocks only save references to images. If you share a LogicBlock
you will also have to include the images that have not been taken from
**%dhpabb%**

▪ Wall guidelines save all help images in-line. If you share your wall
guidelines all images will be included either as references or in-line.

▪ ▪If a default values of projects, building files and roof profiles
contain links to images in **%dhpabb%** only the reference links will be
saved. If you link to images from a different location, the image will
be saved in-line with the default values. If you share a project or
individual files, all images will be included either as references or
in-line.

**1.2.4 Saving Variables in Variable Sets**

▪ Sets of variables can be saved and managed with the usual routine. You
can load entire sets or individual variables in a variable definition.

Single variables can be loaded by clicking the browser button next to
the variable name. Entire sets of variables can be loaded by selecting
the set in the pull down list at the top of the dialogue box.

▪ By loading saved variable you can make sure that you are always using
the same variable for the same purpose.

▪ Descriptive text and help pictures are automatically defined
appropriately.

▪ You can use saved variables in default values, SmartTags, Logic Blocks
and wall guidelines alike. They can be used as default values on project
level, building files and roof profiles.

▪ If you load an entire set, you have a choice of:

-  adding new variables only,
-  overwriting existing ones and adding new ones
-  clearing all variables and loading the entire set.

**1.2.5 Auxiliary functions for entering variables**

1.2.5.1 Variable Search

(V20.01) When creating and editing formulas, it often happens that you
have to look for the definition of the variable or colculations. In all
dialogs for the definition of variables and calculations (default
values, smart tags, logic blocks, HRB Editor) there is now a function to
search for variables or calculations. This is called up via the
corresponding button and the search term is entered:

▪ The exact text (e.g. **V_abc123** ) or with wildcards the text part,
e.g. **V_A**\ \* for all variables that begin with **V_A, \* abc**\ \*
for all that contain abc.

▪ The function searches both in the variable names and in the variable
query. You can also search for the text displayed if you do not know the
variable name.

▪ If you start the function again and enter a new search text, the
search starts automatically at the beginning of the variable list.

▪ With the button “continue” the most recently used search text is
searched for and the user jumps from the current position to the next
position that contains the text.

1.2.5.2 Variable Editor file

(V20.01) Variable Editor file: For editing calculations, it has proven
useful to be able to store them in a text file and edit them with a
conventional text editor. There are many helpful functions such as
searching, replacing, copying etc. available. Now, in all dialogs for
variable definition (default values, samrt tags, logic blocks and HRB
editor), the variables can also be swapped out and put back into a text
file. The files are located as for the calculations in **%DHPTMP%**
(z.B. **C::raw-latex:`\Dietrichs19`:raw-latex:`\wintmp*`\* ) ans the
filenames are**\ VAEditor.txt*\* bzw. **VAEditorHRB.txt**.

1.2.5.3 log-files for variables and calculations

When executing logic blocks and when working with wal guidelines we can
generate log files. These contain a list of the variables and
calculations with the corresponding values in the respective situation.
The log files are created in the **%DHPTMP%** directory (for example,
\**c::raw-latex:`\Dietrichs20`:raw-latex:`\wintmp*`\* ). They are
extremely helpful for the control, but these files are not necessary for
the application of logic blocks and wall guidelines The generation is
controlled in the project administration in the function ” *5 - 02 - 1
Log functions* ” via the checkbox ” *Create log files for variables* “.
If it is set, the log files are generated. By default, the checkbox is
not set, the files are not created. This saves time in the process.

2 Formulas and Text
===================

2.1 Formulas
------------

Functions that can be used in calculations:

-  

   -  

      -  / Mathematical operations

() Brackets

sin, cos, tan Angle functions. Sin, cousin, tangent. Angle in degrees
(0-360°)

asin, acos, atan Angle functions. Arcus sinus, arcus cosinus, arcus
tangens. To determine an angle from the relationship between 2 sides of
a triangle. (Result in degrees 0-360°)

sqrt Square root ( sqrt(25) = 5)

^ Powers. (5^2 = 25)

Pi Math constant Pi (approx. 3.14159). Circumference of a circle with a
diameter of 2.5 = 2.5*Pi. etc.

round Rounding of numerical value. The rounding mode is round half up
(e.g. round(2.4) = 2; round(2.5)=3) If you want to round up you have to
add 0.5 to the value. (e.g. round(VAB+0.5); VAB=2,4 -> round(2.4+0.5) =
3 Important function to calculate distributions.

abs Absolute value. Turns positive and negative values into positive
values only. abs(25) is 25, abs(-25) is 25. Important function to
calculate distances between points independent of the sequence they are
selected in.

2.1.1.1 Formula editor

The formula editor shows a list of variables in the bottom left corner
that are used in a formula. Behind the variable names is description
text. If you select a variable, it will open in the tree element next to
it and where applicable, a help picture will be displayed. The content
of the formula will become more transparent.

(V20.01) HRB-Editor: Display of current values in the formula editor: If
a formula is opened in the formula editor, the current values of the
variables are also displayed in the variable list after the texts. At
the top of the dialog you can see the result of the whole formula. These
displays are very helpful in checking the formulas; it is easier to see
whether it is due to the current formula or whether there is an
unexpected value for a variable. The values can only be displayed in the
HRB editor, since only here are the system variables assigned.

2.1.1.2 All variables available in the formula editor

(15.01) Conditions can be defined for all types of formula. In
conditions, not only numeric values can be used. It is possible to use
all types of variables, e.g. texts. Therefore, not only variables for
numeric values are offered in the formula editor, but all types of
variables.

**2.1.2 Formulas with conditions, conditions**

Formulas may contain conditions. With conditions you can define formulas
that will react differently in certain situations. E.g. this should
reduce the number of required SmartTags dramatically.

A formula with condition consists of three parts, which are separated by
semicolons:

**(IF);(THEN);(ELSE)**

(14.03) Conditions can be interlaced, in order to cover more than 2
situations within one formula.

Examples:

**(condition 1);((condition 2);(2 true);(2 false));(1 un true) (** —————
*1 true————————* **)**

**(condition 1);(1 true);((condition 2);(2 true);(2 false)) (** - ————-
*1 false———–* **)**

The interlacing can be continued in ‘true’ and ‘false’ at the same time.

On the next level, the interlacing of conditions can go on. Example:

**(con. 1);(1 erf.);((con. 2);(2 true.);((con. 3);(3 true.);(3 false.)))
(** ——— *1 false———————————-* **) (** ——— *2 false————–* **)**

2.1.2.1 Comparisons, that can be used in LBs:

= Equal to. True if compared values are equal. E.g.: VAB = 4 is true if
VAB is exactly 4

!= Not equal to. True if compared values are not equal. It does not say
that one is greater than the other, or even that they can be compared in
size. e.g.: VAB != 4 is true if VAB is less or greater than 4.

   Greater than. True if the value in front of the sign is greater than
   the other. These relations are known as strict inequalities. e.g.:
   VAB>4 is true if VAB is bigger than 4

..

   = Greater than or equal to. True if value in front of the sign is
   greater than or equal to the other. e.g.: VAB>=4 is true if VAB is
   greater than or equal to 4

< Less than. True if the value in front of the sign is less than the
other. These relations are known as strict inequalities. e.g.: VAB<4 is
true if VAB is less than 4

<= Less than or equal to. True if value in front of the sign is less
than or equal to the other. e.g.: VAB<=4 is true if VAB is less than or
equal to 4

& AND. Multiple conditions can be linked with &. All linked comparisons
have to be true to make the entire inequality true. e.g. (VAB>4)&(VAB<8)

2.1.2.2 Linked conditions, logical links

Several conditions can be logically linked:

& logic **and**. All conditions associated with **and** must be met. So
if VAB must be greater than 4 and less than 8, the whole expression is:

(VAB> 4) & (VAB <8)

| logic **or**. (V20.01) At least one of the conditions must be met:

. As an **or** character (as in C ++) the \| used. You get this on the
keyboard with AltGr + “<”. . We use the normal **or** here: If at least
one of the two sub-conditions is met, the whole **or** expression is
met. Both partial conditions may also be met. (with the exclusive **or**
only one of the two should be met).

The logical links and **and** or **or** can also be used in combination.
Here are examples of conditional formulas:

Example: **((V_abc=a)|(V_abc=b));(0.04);(0.16)**

If the variable V_abc has the value a **or** b, the value is 0.04. In
all other cases the value is 0.16.

Example: **((V_aa=a)|(V_bb=b));(0.04);(0.16)**

If the variable V_aa has the value a **or** V_bb the value b, then the
value is 0.04. The overall condition is also met if both parts apply
(V_aa = a and V_bb = b). In all other cases the value is 0.16.

Example: **V_a1=0)&(V_a2!=0))|((V_a1!=0)&(V_a2=0)));(0.04);(0.16)**

Only one of the variables V_a1 and V_a2 may have the value 0, then the
value is 0.04. In all other cases the value is 0.16.

2.1.2.3 Possibilities of nesting conditions

In conditional formulas, the conditions can be very nested, e.g.:

::

   (((V_a1=0)&(V_a2!=0))|((V_a1!=0)&(V_a2=0)));(0.04);(0.16)

In conditional formulas, the conditions can also contain formulas, for
example:

::

   (V_a1=(1+2+V_a2));(0.04);(0.16)

In conditional formulas, complete conditional formulas can also be
placed in the true/false parts (after the first or second semicolon) and
thus be further nested, e.g.:

::

   (V_a1=0);((V_a2=0);(0.04);(0.16));(0.16)

However, no complete conditional formula may be used within a condition.

So the following is not allowed:

::

   (0.3<((0.4<0.5);(0.6);(0.1));(0.04);(0.10)

As said above, conditions may be nested arbitrarily and the individual
parts (left and right of the comparison sign) may also contain formulas.
But the condition must not contain a complete conditional formula. So no
semicolons may appear there.

Logically, these cases can be covered by rearranging the formula or, for
a better overview, can be broken down into several calculations.

2.1.2.4 Tolerances in comparisons:

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
‘abs’ for an absolute value (0.01>(abs(VA - 1.0)))

▪ In other cases it might be enough to compare a value with a safe
enough number. E.g. in a distribution function you would normally
calculate the number of pieces (VNumP). If the condition is now, that
there should be more than 3 pieces, you don’t compare with greater than
3, but with greater than 2.5 (VNumP>2.5). By doing that it does not
matter if VNumP is 2.99999 or 3.00001.

2.1.2.5 Texts in coditonal formulas

(21.01) This chapter from version 18.01 has been completely deleted.

2.1.2.6 Comparing texts:

Texts can be used for comparisons as well. Basically, you can use
variables with all units that contain no numerical value: txt, Idnr.,
Enum, A-F, …

The comparison value is written directly as a text without additional
tags. Example: If the variable ’ **V_Textvariable** ’ is supposed to be
equal ’ *Test* ’, the comparison is: **(V_Textvariable=Test)**

Texts are sorted alphabetically. So they can also be compared with ‘>’
and ‘<’. Texts coming first in the sorting are ‘smaller’ than texts
coming last in the sorting: So ’ **Aluminum** ’ is ’ *smaller* ’ than ’
**Brick** ’.

If the condition is, that teh variable contains empty text, the value of
the variable has to bigger ’ ’ (space character) **(V_Textvariable> )**.
There is no formula for empty text, so we have to compare with the
smallest possible value. The ’ ’ (space character) is one of the first
characters in the fonts. Only the control characters are on top. We have
to use one of the characters before ’ **#** ‘, because item numbers
begin with’ **#** ’.

2.1.2.7 Texts in conditions: Special case oa1 file (IFC Premium)

In the conditions of the oa1 files, comparisons are made with system
variables. Dabei ist folgendes zu beachten:

::

   If the system variable is a number, it is written directly; Example:
   Condition=(OH=1.23)
   If it is a text that starts with a number (only then), it must be written in quotes. Example:
   Condition=(IFCNAME="1.23")

2.1.2.8 Lists and wild cards in conditions

To now, it was only possible to compare with one single value in the
conditions. The new possibility of interrogating the storey (SWAKT) or
the property (AUSF) leads us to using lists and wild cards.

Lists: If a condition is only valid for GF, type (SWAKT=GF). If it is
valid for GF, IF and TF, type (SWAKT= **{GF\ UF\ AG})**. The list is put
into curly brackets, use tilde ‘~’ as a separator.

Wild card: If a condition is valid only for the property “E Stick Frame
R13”, type ( **AUSF=E Stick Frame R13)**. If it is valid for all
properties starting with “E”, type ( \**AUSF={E*})**. The expression is
put into curly brackets. Use asterisk ’*’ as a wild card. The following
arrangements can be used:

::

   ABC* Starts with ABC , arbitrary end

::

   *ABC Starts arbitrarily, ends on ABC

::

   *ABC* Contains ABC at any position

Listings and wildcards: Both possibilities can be combined as well. If
it is valid for all properties starting with ‘E’ or ‘I’, type
**(AUSF={E\ ~I}** ).

**2.1.3 Arrays in formulas**

Only Logic Blocks: Where you define coordinates in order to position
objects, library items and reference points of SmartTags, you can define
arrays.

▪ In every coordinate field you can enter an array as follows (
**ORIGIN\ SPACING\ QUANTITY** ). A quantity of

::

   1 means, you get only 1 object in origin.

▪ If you specify an array, you have to do so in X, Y and Z.

::

   X(1.0~0.1~5)Y(0.0~0.0~1)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step size 0.

::

   X(1.0~0.1~5)Y(0.0~0.2~4)Z(0.0~0.0~1) Row along X with 5 objects, origin at 1.0 step size 0.1,
   this row 4 times along Y step size 0.2.

▪ With arrays, you can define rows, grids and 3 dimensional grids in one
go.

**2.1.4 Error message, reporting incorrect formulas**

(V20.01) With the introduction of the new formula system, the error
messages have also been revised:

▪ The display of formula errors has been expanded:

::

   ▫ Formulas are checked when files are opened (HRB, logic blocks, settings). If desired, the
   corresponding checkbox is set beforehand in the project administration in function 5- 02 - 1 log
   functions. The building must be restarted to take this into account.
   ▫ As far as possible, the type of formula error and the affected formula are displayed. This message
   can be copied to the clipboard and then used in the search function of editors.
   ▫ The display of further errors can be prevented by pressing the button in the message. This applies
   until the building (or HRB editor) is restarted. However, the error message of a division by 0 cannot
   be prevented.

2.2 Variables in Text, Item Numbers
-----------------------------------

Text is used in dimensions, texts and labels. In those cases, text can
be entered directly or via variables.

▪ In texts it is possible to mix any number of text strings and
variables. In order to use a variable in text the variable name has to
be between ‘#’ signs. Z.B. **‘’Length: #VL[m,3]#, Width: #VW[cm,1]#,
Height: #VH[cm,1]’**

▪ You can ask the user to enter text in the variable prompt for ’
**txt** ’ and **Enum** variables.

::

   ▪ Variables with item# or Beam Type are also text strings and can be used in text.
   ▪ Numeric values can be used in text. You have to define the format they should appear in. (see
   below)
   ▪ In addition to that it is possible to add the values of system variables.

▪ Formatting of numeric values in text:

::

   ▪ In order to show numeric values in different units and decimal places the unit and precision info is
   added to the Variable name in square brackets. e.g.: #V23[cm, 1]# will show the value of 'V23' in
   centimeter and 1 decimal place.
   ▪ For the units m (meter), cm (centimeter), mm (millimeter) and in (inches) you define the number
   of decimal places. For the unit ft (feet) you define the fraction you want to show. e.g. #VL[ft,16]#
   will show the value of VL in feet-inches and 16th (10'-0 3/16")
   ▪ ▪The unit of angles is '°' e.g. #Valpha[°,1]# is 45,3°

::

   ▪ For numeric values that are neither lengths nor angles you don't have to specify a unit, but you
   have to add the comma and number of decimals. e.g. #VNumP[,1]# .; #VNumP[,0]# number of
   pieces no decimals (3).
   (V20.02) There is an additional formatting option for the output of variables in texts. For this
   purpose, a filler character and the total number of characters are added after the decimal places.

::

    Example variable V _Num=34.34676. The formatting #V_Num[m,2] # outputs in m with rounding
   to 2 decimal places: 34.35. Now you can extend the formatting to #V_Zahl[m,2,x,8]#; this fills
   the text with x to a total of 8 digits: xxx34.35. The decimal separator also counts as one digit.

::

   If you do not need fill characters, the formatting can still be written with units and decimal
   places: #V_Num[m,2]#.

::

    If a text variable is formatted longer, no unit or rounding is required. For the variable V_Text =
   abcde , the formatting #V_Text[,,-,8]# fills the text with - to a total of 8 characters: ---abcde.
   The first two commas must be specified in the formatting, even if there is no unit and rounding.
    This formatting is used e.g. for right-aligned lists or for the formation of file names.

In the same way, text variables can be used to carry item numbers. Using
text and variables you can put together an item# that can be used for 3D
library objects and objects. This can be used to add a size to an item
number. E.g. you want to compare an item# with the text **‘rod’** and
the diameter ‘Vdia’ in full mm. The expression for the item# would be
‘rod#Vdia[mm,0]#’.

You can also use the calculations to compose text and have the result in
a variable. In calculations you also have the option to compose text
differently depending on conditions that you define. For further
information refer to the chapter: ‘Logic blocks - calculations’

**2.2.1 Special rules in formulas for caltculations of type text**

If a calculation has the type Text (unit txt), you can directly assign
plaintext, all kinds of variables or both mixed, and enter it in the
formula. There are the following rules to consider:

::

   ▪ If the calculation should directly take on the value of a variable of type text, then this variable can
   be written directly into the formula without special characters. If the calculation V_ZW_Text1 should
   get the value oft he variable V_Var_Text , sthe formula is simply: V_Var_Text

::

   Attention: The program first checks whether the whole text of the formula matches the name of a
   variable (system variables, user variables, calculations). Ist dies der Fall, so wird der Text
   bevorzugt als Variable interpretiert und ihr Wert übernommen.
   So you can not directly assign the text V_Var_Text in our case; it would be replaced by the content
   of the variable. The same applies to system variables: If a formula consists only of the word SWAKT ,
   this word will always be replaced by the content of the system variable SWAKT (current storey).

::

   If the text, which consists only of the name of a variable (system variables, user variables,
   calculations), is needed, a character must be prefixed or appended. The space can also be set
   ahead. Operators (- + * / ~ <> = etc.) are not allowed here. For our examples would be possible
   e.g.: _SWAKT or SWAKT_.

::

   ▪ If variables (system variables, user variables, calculations) are combined with plain text, the
   variable names must be enclosed in #: plain text #SWAKT#

::

   ▪ (17.01) These rules also apply to formulas that are part of a conditional formula.
   (18.01) It should be noted here that plaintext in conditional formulas must always be written in
   apostrophes.
   Example: The value of SWAKT is GF.

::

   The conditional formula ( condition );(#SWAKT#);(SWAKT) results:

::

   Condition met: GF (#SWAKT# is replaced by value)

::

   Condition not met: GF (SWAKT is recognized as a variable because it stands
   alone, so it is also replaced by value)
   The conditional formula ( condition );("Klartext" #SWAKT#);("Klartext" SWAKT) results

::

   Condition met: Klartext GF (#SWAKT# is replaced by value)

::

   Condition not met: Klartext SWAKT (SWAKT is recognized as a variable because it stands
   alone)

2.2.1.1 Conditional formulas for calculations of type text (unit txt)

(21.01) For calculations of type decimal (unit m) conditions may contain
mathematical formulas as well as text comparisons. However, the formulas
of intermediate values of type text (unit txt) are treated completely as
texts only; thus, conditions are performed with text comparison.
Conditions for intermediate calculations of type text may not contain
mathematical formulas.

::

   Example of a calculations of type text:
   The following conditional formula is possible, because the condition compares texts: The
   name of the execution must contain AW, then C24 is taken, otherwise KVH-Si:
   Possible formula: (AUSF={AW*});(C24);(KVH-Si)

::

   The following conditional formula is not possible because the condition contains mathematical
   formulas. The program would recognize the variable V_width and compare its value with the
   text "2.0" after alphabetical sorting: And this has confusing results:
   Faulty formula: (V_Width>2.0));(C24);(KVH-Si)

::

   Attention! If V_width has the value 3.00, then the texts "3.00" and "2.00" would be
   compared and the result C24 looks correct. Because the 3 comes more alphabetically
   after the 2 and is thus larger. However, if V_width has the value 10.00, the result is
   KVH-Si. The "10.00" is therefore not larger than "2.00", since the 1 comes
   alphabetically before the 2 and is therefore smaller.

Recommendation for conditions for calculations of type text (unit txt):

If you want to condition calculations of text type (txt unit) with
mathematical formulas, you must enter them in the Variable condition
field. Then the conditions are not in a conditional formula, but
independent conditions and are analyzed accordingly. Mathematical
formulas as well as text comparisons are possible here.

3 Editable settings files
=========================

(18.02) Some functions of the program require editable settings that are
not to burden the dialogues and are particularly effective to edit in a
conventional text editor. For this purpose, the editable settings files
were introduced. Examples of the application:

::

   ▪ Project administration: new project – from IFC
   ▪ Free design 1 - 4 - 9 Check building
   ▪ Wall design 1 - 4 - 2 Center of gravity, auto. mounting
   (Editable setting only available via special module)
   ▪ Floor plan, floor decks and roof calculation: 1 - 8 - 5 sheating – enter designation
   (Editable setting only available via special module)

All these files are structured according to the same rules and can be
edited accordingly. The uniformity ensures the most effective
workability of the files.

There are 2 ways to edit the contents of these files:

-  In special dialogue for these files: *Change settings* for editable
   settings files
-  or in a general text editor, e.g. Notepad. In any case, incorrect
   entries are possible that can not be intercepted by the program.
   **Therefore, only savvy users should edit these files.**

For these files, the benefits of ” *manage settings* ” to data exchange
can be used.

3.1 Select and manage settings for editable settings files
----------------------------------------------------------

In dialogs with access to editable settings files, there is an item from
*select settings* and *change settings* :

**3.1.1 Settings Selection for editable settings files**

Several settings can be stored in the settings file. By clicking in the
element *select settings* a tree element with the available settings and
the option no *settings opens*. Here you can quickly switch between the
settings.

**3.1.2 Change settings for editable settings files**

When changing settings, a dialog for editing the editable settings files
is called up. This allows a comfortable and yet free editing of the
files:

::

   The header of the dialog shows the path and file name of the edited file. So you can find the file
   even if it should be opened with a general text editor.
   At the top left there are hints about the purpose and content of the settings file.

::

   Underneath are the usual elements for settings: select, save, and manage. In the selection is
   therefore the setting that is currently being edited. It is not possible to reduce the dialog.
   Each setting contains different data sections, so-called "sections", depending on the file. In the
   drop-list, the data area to be edited is selected.
   Information about the purpose and content of the data area is displayed below for the current
   data area. On the right there is a picture for further explanation.

::

   The lower part of the dialog is taken by the actual editor. There, the content of the data area, ie
   the data lines, is edited with usual functions. It is also possible to make incorrect entries that can
   not be intercepted by the program. Therefore, only savvy users should edit these files.
   Common editing functions are available here such as marking (with mouse), copying (Ctrl +
   C), cutting (Ctrl + X) and pasting (Ctrl + V). Ctrl + Z takes a step back.

3.1.2.1 Data lines

Within the data area (section), each line consists of keyword - equals
sign - value. After that, a comment can follow separated by a double
slash.

::

   Kennwort = Wert
   Kennwort = Wert // Kommentar

The possibilities and meanings for the keywords and values depend on the
function that processes this data. The corresponding instructions can be
found in the descriptions that are displayed further up in the dialog.

The comment is often used for given keywords for a definition of the
keyword. For self-defined keywords or user variables, the comment should
also be used for a description, as it facilitates later processing
considerably.

3.2 Structure of editable settings files, editing in the general text editor
----------------------------------------------------------------------------

The editing of the files can also take place outside the program system
in a standard text editor. Changes are not automatically loaded in the
project administration or in the building position. Therefore, the
following procedures are to be followed:

::

   To edit the file, the calling function should be left in project administrarion or the building position.
   When calling the function that uses the editable settings file, it is also reloaded.
   Standard functions from Manage Settings are only to be used if the settings file is not opened in a
   text editor.
   Note: Unfortunately, it is not always possible to determine that a file is currently open, as e.g.
   Notepad ++ automatically opens just a copy of the file.

Here are any incorrect entries possible that can not be intercepted by
the program. The file can become unusable. **Therefore, only savvy users
should edit these files with a general text editor.**

**3.2.1 Structure and contents of editable settings files**

In editable settings files are structures and areas that can be changed
in the editor and those that should not be changed. Many of these files
contain notes on the purpose and content of the file in corresponding
entries and comments.

If the text is a reference in the form # 123 (crossbar with number),
then this is the reference to the line number in Editdsi1.frg.

The files are divided into data sections called sections. Each section
begins with an entry in square brackets and ends with the same entry
supplemented by the word **ENDSEC** :

::

   [ SECTION NAME ]
   ...
   [ SECTION NAME ENDSEC]

Within the section, each line consists of keyword - equals sign - value.
After that, a comment can follow separated by a double slash.

::

   Kennwort = Wert
   Kennwort = Wert // Kommentar

**3.2.2 Structure version of the file, [VERSION]**

Editability: Do not change!

The **VERSION** section contains the identifier for the structure
version of the file. The program needs this information to process the
file correctly. This is not the version of their data. This section must
not be changed.

ExMPLE:

::

   [VERSION]
   Version=1.
   [VERSION ENDSEC]

**3.2.3 Groups, [CATEGORY]**

Editability: Preferably, edit with *Manage Settings*.

The **CATEGORY** section contains the names and order of the groups. The
keywords end with a number

that corresponds to the order. After the equal sign, the name of the
group follows:

Example:

::

   [CATEGORY]
   CategoryName1= group abc
   CategoryName2= group 123
   [CATEGORY ENDSEC]

**3.2.4 File information,** [FILE INFO]

The section **FILE INFO** contains information about the file and the
data defined in it. Here are valuable

hints about the data and rules in the file.

If the text is a reference in the form # 123 (crossbar with number),
then this is the reference to the line number in **Editdsi1.frg.** The
texts from the frg (language file) are displayed in the dialog for
editing the editable settings files.

The keywords **FileDescription_1** to **FileDescription_5** can be
assigned up to 5 lines of text..

Example:

::

   [FILE INFO]
   FileDescription_1= Beschreibung der Datei
   FileDescription_2= max. 5 lines
   FileDescription_ 3 = #
   [FILE INFO ENDSEC]

**3.2.5 Section information, [SECTION INFORMATION]**

Editability: Information must be available for each section! Observe
notes in the individual entries!

All settings of the file contain the same sections. System information
is the same for all these sections, regardless of their setting.
Therefore, this information is recorded in this upstream section.
Settings do not have to contain all of these sections, but can only
contain sections that have been defined here.

::

   The SECTION INFORMATION section contains all the sections that can be used in the settings. For
   each section there are information texts, the SectionsType and the reference
   to a help picture:
   Line1 .. Line5 Up to five lines of explanation text on the content of the section. Here are
   valuable hints for editing the file. If the text is a reference in the form # 123
   (crossbar with number), then this is the reference to the line number in
   Editdsi1.frg. The texts from the frg (language file) are displayed in the
   dialog for editing the editable settings files.

::

   SectionType There are 3 types of sections : FILTER, FREE, FIX

::

   FILTER The keyword in front of the equal sign describes a selection of
   properties (wall, ceiling, roof surface) or a selection of item
   numbers.
   The following selection descriptions are possible:
   ABC123 the whole name is ABC
   ABC * the name starts with ABC
   * ABC the name ends with ABC
   * ABC * ABC is somewhere in the name.

::

   Any number of entries can be made in this section. The parent
   function determines if all applicable entries, only the first one or
   only the last one is used.
   FREE The keyword before the equal sign can be freely assigned. This
   can e.g. be user variables.
   Any number of entries can be made in this section.
   FIX The keywords before the equals sign and their number are set. In
   these sections, the possible keywords are already entered. No
   further supplements can be added. Keywords that are not used
   should simply stop with no assigned value.

::

   ReferenceImagePath Reference to a help picture. This is displayed in the dialog for editing the
   editable settings files.

Example:

[SECTION INFORMATION]
~~~~~~~~~~~~~~~~~~~~~

[ SECTION A ]
~~~~~~~~~~~~~

::

   Line1=Text for section A
   Line2=max. 5 lines
   Line3=#
   SectionType=FILTER
   ReferenceImagePath=%DHPABB%\GWE___04.bmp
   [ SECTION A ENDSEC]

::

   [ SECTION B ]
   ..
   [ SECTION B ENDSEC]

::

   ..

::

   [SECTION INFORMATION ENDSEC]

**3.2.6 Settings [DATASET EDITDSI]**

The actual settings are defined in the sections **DATASET EDITDSI.**

::

   ▪ There is one such section for each shot. The section name is always the same, so it does not
   contain a sequential number or the name of the setting.
   ▪ The display order of the settings corresponds to the order in the file.

[DATASET EDITDSI]
~~~~~~~~~~~~~~~~~

…
~

[DATASET EDITDSI ENDSEC]
~~~~~~~~~~~~~~~~~~~~~~~~

.. _dataset-editdsi-1:

[DATASET EDITDSI]
~~~~~~~~~~~~~~~~~

.. _section-1:

…
~

.. _dataset-editdsi-endsec-1:

[DATASET EDITDSI ENDSEC]
~~~~~~~~~~~~~~~~~~~~~~~~

Each of the settings first contains the information about the setting:

::

   Name The name of the setting used to display it in select settings. The names of
   the settings in a file must be unique, no name can be assigned twice.
   CategoryName Group to which the setting belongs. Possible groups are listed in section
   CATEGORY.

::

   ReferenceImagePath Reference to a help picture. This is displayed in select settings and can be
   very helpful to the operator.

::

   The assignment of the help picture should be done in manage settings , since
   the possible references in the paths are entered automatically here.

This is followed by the actual data *sections*. These were defined
earlier in section **[SECTION INFORMATION].**

The comment on the setting is recorded in the last *section* in this
setting: **[DATASET EDITDSI MULTILINE_STRING]** With the keywords
**Line1** to **Line5** up to 5 lines of comment text can be specified..
This is displayed in *select settings* and can be very helpful to the
operator. The comment can also be entered in *Manage Settings*.

Example:

.. _dataset-editdsi-2:

[DATASET EDITDSI]
~~~~~~~~~~~~~~~~~

::

   Name= Dataset one
   CategoryName= group abc
   ReferenceImagePath=%DHPABB%\DietrichsLogo.png

::

   [ SECTION A ]
   AW*=(WL<12.0[m]) //use double slash for commentary
   [ SECTION A ENDSEC]

::

   [ SECTION B ]
   ..
   [ SECTION B ENDSEC]

::

   ..

::

   [DATASET EDITDSI MULTILINE_STRING]
   Line1= Text for setting Dataset one
   Line2= max. 5 lines
   [DATASET EDITDSI MULTILINE_STRING ENDSEC]

::

   [DATASET EDITDSI ENDSEC]

**3.2.7 Data lines**

Within the data section, each line consists of keyword - equals sign -
value. After that, a comment can follow separated by a double slash.

::

   Kennwort = Wert
   Kennwort = Wert // Kommentar

The possibilities and meanings for the keywords and values depend on the
function that processes this data. The file contains corresponding notes
in the sections **[FILE INFO]** and **[SECTION INFORMATION].**

The comment is often used for given keywords for a definition of the
keyword. For self-defined keywords or user variables, the comment should
also be used for a description, as it facilitates later processing
considerably.

4 Log
=====

::

   Date Chapter Remark
   11.10.12 Variable definition Description 'column E, external'^

::

   13.11.12 Dietrich's Default Values Added chapter: Dietrich's Default Values^
   13.08.13 Variable Definition, Properties of
   Variables

::

   Added text describing variable group

::

   13.08.13 Formulas with conditions, conditions New chapter: Formulas with conditions^

::

   19.08.13 Arrays in formulas New chapter:^ Arrays in formulas^

::

   27.10.14 Formula editor New chapter: Innovations in the formula editor^
   (general description not yet available)

::

   30.10.14 Comparisons, that can be used in
   LBs:
   Tolerances in comparisons:

::

   Added chapter, adopted from Logic
   blocks_Ud15_1501.doc.

::

   17.11.14 Comparing texts: Added chapter^
   02.02.15 Formulas with conditions, conditions Interlaced conditions^

::

   02.02.15 Variable Definition, Properties of
   Variables

::

   Overwrite external variables

::

   13.04.15 Variable Definition, Properties of
   Variables

::

   'Hidden' tag for variables

::

   06.07.15 Lists and wild cards in conditions Added chapter^

::

   06.07.15 All variables available in the formula
   editor

::

   Added chapter

::

   18.01.18 Special rules in formulas for
   caltculations of type text

::

   Added chapter

::

   18 .01.18 Texts in conditional formulas Added chapter^

::

   1 8.01.18 Texts in conditions: Special case
   oa1 file (IFC Premium)

::

   Added chapter, especially for oa1 files

::

   22.01.1 9 Editable settings files
   New chapter

::

   15.01.20 (various) Extensions to update V20.01 are marked with V20.^

::

   15.01.20 Variable Definition, Properties of
   Variables

::

   Adjustment in the sections Variable display and
   Variable condition

::

   15.01.20 Variables in texts, Item numbers Formatting option for variables^

26.01.21 Variable definition, properties of variables; section Variable
condition

::

   The original sentence at the end of the section has
   been removed; it started with Variable condition for
   external...

26.01.21 Possibilities of nesting conditions Possibilities of nesting
conditions^

26.01. Texts in conditional formulas (chapter deleted)

::

   Chapter deleted

26.01.21 Conditional formulas for calculations of type text (unit txt)

::

   New chapter
