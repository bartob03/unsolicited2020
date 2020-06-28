PDF bookmarks and TOC in Lyx
===============================

Most of Adobe's popular products, such as **Adobe FrameMaker, RoboHelp, InDesign**, and **Acrobat**, support the creation of PDF bookmarks and table of contents when exporting to PDF.

Users of the open source **Lyx** can do this using easily by visiting the **Document Properties** settings.

To enable automatic creation of bookmarks/table of contents in a Lyx document:

1. Click **Document > Settings**.

2. On the left panel, click **Numbering and TOC**.  Drag the **Numbering** and **List in Table of Contents** slider as needed.  Dragging the **Numbering** slider changes the **Example Element** as numbered or unnumbered.  Dragging the **List in Table of Contents** slider allows the **Example Element** to be included in the Table of Contents.

.. figure:: images/lyx_toc3.png
    :align: center


3. On the left panel, click **PDF properties**.  Check **Use hyperref support**.  Click the **Bookmarks** tab and check **Generate Bookmarks, Numbered bookmarks and Open bookmarks**.  Type the number of levels included in the bookmarks (i.e. multiple nested bookmarks).

.. figure:: images/lyx_toc4.png
    :align: center


4. Click **Apply > OK**.

5. Use the **Numbered Elements** to create a list or document sections.  Once exported to PDF, these will constitute the Table of Content headings and subheadings.

.. figure:: images/lyx_toc5.png
    :align: center

    Use the preset numbered Elements to format text.


6. Once finished numbering and writing the document, export the Lyx document by clicking on **File > Export**.  Select **PDF (ps2pdf)**.  The document will be exported as a PDF with the same filename as the Lyx document.

7. Open the document in a PDF viewer that supports bookmarks such as **Adobe Reader, Evince**, or **Okular**.  The bookmarks panel will display the created Table of Contents.

.. figure:: images/lyx_toc7.png
    :align: center
