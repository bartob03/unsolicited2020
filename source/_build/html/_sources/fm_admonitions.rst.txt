Formatting admonitions in unstructured FrameMaker
===============================================================

.. contents:: Table of Contents
   :depth: 3

Admonition text are sections of a document that add/explain details about a particular chapter or part. They are generally formatted as a separate block of text and categorized as either Note, Important, Caution, Warning and Tip, although the captions/conventions vary according to the author and publication style guide. They generally break the flow of text and can be distracting when used too often, though they are indispensable for highly complex work such as documentation for developers and engineering specifications. Admonition blocks/lists can include a colorful customized icon like those found in the excellent `Fedora Project documentation <http://www.getfedora.org>`_, or a black and white icon such as those found in Wiley books.

Document generators such as **Asciidoc** and **XML/XSLT** tool chains using **Docbook, xsltproc, SAX** and **DITA** take care of formatting and adding the icon but in unstructured **Adobe FrameMaker**, writers will have to create a paragraph or table style specifically for admonition paragraphs, blocks, or lists. Creating admonitions in WYSIWYG applications such as **Adobe InDesign** and **CorelDraw** is easy since all you need is to **Place** the icon image next to a resized text frame. However, unless you anchor the icon to a text frame (which isn't really recommended for image-intensive documentations), managing the flow of text in **InDesign** can be tricky. **InDesign**, in contrast, relies on anchored objects for managing text and images, though users who are accustomed to **InDesign**'s click and drag approach may find **InDesign**'s roundabout approach frustrating at first.

Admonition paragraphs
-------------------------

Admonition paragraphs are nothing more than text formatted/positioned differently from the main text flow. Admonition paragraphs focus on one technical point only and shouldn't be too long. To create an admonition paragraph with a caption:

1.  With your insertion point in the paragraph you want to format, click the **Commands** button and then **New Format** in **Paragraph Designer**.

2. In the **New Format** window, enter a **Tag name** and click **Create**.

3. Click the **Basic** button and enter ``0.5"`` on **Left indent**. Most writers prefer text blocks to be flush to the right like most of the text but if you prefer to isolate the paragraph completely, add ``0.5"`` on the **Right indent** also.

4. Enter a point value in the **Above Pgf** and **Below Pgf** items. This adds white space between the note and the rest of the text and breaks up long narratives.

5. Click **Update All** or **Apply**.

If you prefer to add formatting to the Note/Important/Warning/Caution caption, create a separate **Character** tag using the **Character Designer**.

Admonition paragraphs with icons
-----------------------------------

Small icons highlight the section and attract the reader's attention. However, they are often unnecessary in more serious documents. They are acceptable for consumer user manuals, however, since they make the documentation friendlier to readers and more colorful.

.. figure:: images/fm_ad1.png
    :align: center

    Admonition example from the Samsung S4 manual.

To add an icon to an admonition paragraph:

1. Place the insertion point at the beginning of the paragraph.

2. Click **File > Import**. Navigate to the image file and select either **Import By Reference** or **Copy Into Document**.

3. Click **Import**.

4. Using your mouse pointer, select the image frame.

5. Click **Special > Anchored Frame**.

6. In the **Anchored Frame** pod, change the **Anchoring Position** to **Run into Paragraph**. Change **Alignment** to **Left**.

.. image:: images/fm_ad2.png
    :align: center

7. Using your mouse pointer, select the image inside the frame. Hold down **SHIFT** and drag the handles to resize the icon. Select the frame and resize the frame as well.

8. If you want to retain the paragraph's alignment, resize the image frame so the text aligns as before. Since the text runs around the image, adjusting the tabs won't help so adjusting the image frame is a good workaround to achieve an aligned text.

.. tip::

	To reuse the icon and the resized image frame, just select the image frame using the mouse pointer, copy, and then paste on to the next admonition paragraph.

.. image:: images/fm_ad3.png
    :align: center

Admonition blocks/lists
-----------------------------

Admonition blocks/lists work the same way as any bulleted list in **FrameMaker** - just add the left and right indents to separate them from the flow of the text. The text for "Notes:" should have its own **Character** tag while the bulleted list would have its own **Paragraph** tag. Use **Tabs** to keep the bulleted list aligned.

If there's already an instance of the icon for the admonition, just copy and paste it on the insertion point. Again, you might have to resize the image frame to retain the list's alignment.

Admonition blocks separated by upper and bottom lines
----------------------------------------------------------

Some manuals and documentation use lines or boxes to separate the text from the flow. This is extremely easy to set up in **InDesign** or **Microsoft Word** using **Paragraph Rules**, an option missing in **Framemaker 10**.

.. figure:: images/fm_ad4.png
    :align: center

    Screenshot from a Netopia modem manual.

You can draw lines using the **Graphics Toolbar** in **FrameMaker** but it won't be anchored with the text. As a workaround, you can use the **Table Designer** instead to create the "box" for your admonition.

To create a **Table** tag specifically for admonition blocks:

1. Click **Table** and then **Insert Table.**

2. In the **Insert Table** window, input ``1`` for **Columns** and ``1`` for **Body Rows**. Remove any **Heading Rows**. Click **Insert**.

.. image:: images/fm_ad6.png
    :align: center

3. Place the insertion point inside the table cell.

4. In **Table Designer**, click the **Commands > New Format**. Input a name for your admonitions table tag. Click **Create**.

5. Click the **Basic** button in **Table Designer**. Input **Left** and **Right Indents**.

6. In the **Title** item, select **No Title**.

7. Click the **Ruling button** in **Table Designer**. In the **Outside Ruling** section, select ``None`` for **Left** and **Right Ruling**. Click **Update All** or **Apply**.

8. Click the **Table** menu and select **Format > Resize Columns**.

.. image:: images/fm_ad7.png
    :align: center

9. In the **Resize Selected Columns** window, input a value in the **To Width** box.

10. Type the text or list inside the table. You can also add an icon if needed, customize the shading, or lines of the table.

The newly created table tag will now appear as an option whenever you need to insert a table for admonitions.

The screenshot below displays the PDF result of the different ways of formatting admonition blocks with or without icons or lines.

.. image:: images/fm_ad8.png
    :align: center
