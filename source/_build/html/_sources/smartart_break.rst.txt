Breaking apart SmartArt in PowerPoint 2007
==============================================

**Office 2007**'s version of **PowerPoint** has a known issue regarding **SmartArt**.  As useful as SmartArt is, a known bug corrected by **Office 2007 SP1**, prevents users from modifying SmartArt objects and text individually.  Even resizing the SmartArt (which is contained in its bounding box) will result in destroying the nicely laid out text and shapes.  Even adding another box or arrow that doesn't follow the general direction of the preset design is near impossible (adding a shape before and after any object in the preset SmartArt will only follow the "flow" of the preset layout).

.. figure:: images/smartart.png
    :align: center

Smart Art's preset designs are extremely useful, but modifying it can be time consuming.  For instance, in the image above, adding another box linked to Mac OSX doesn't work.  Instead, it will add another shape following the flow (i.e. the **[Text]** box).

.. figure:: images/smart1.png
    :align: center

Moving objects out of the border is impossible as the Smart Art was designed to remain within the bounding box.  Resizing will often ruin the structure too.

.. figure:: images/smart2.png
    :align: center

To be able to modify each object and text within the bounding box, users would have to select all the objects within the box, cut them out, and paste them outside the bounding box.

.. figure:: images/smart3.png
    :align: center

Cutting and pasting objects outside the bounding box won't work if users don't select ALL the objects inside.  Occasionally, **CTRL+A** (select all) even fails.  After pasting the objects outside the box, the bounding box can be deleted.

.. figure:: images/smart4.png
    :align: center


Individual text and objects can now be duplicated, edited, and changed once outside the bounding box.
The solution can be found in Office online and involves selecting all the objects within the SmartArt bounding box, using the **Cut** command, deleting the bounding box, and pasting the objects on the PowerPoint slide.  The procedure allows users to now individually select arrows, objects, lines, text, and shapes individually and modify each separately.

**Office 2010** doesn't suffer from this problem and upgrading to Office 2007 SP1 via an online update corrects this issue.
