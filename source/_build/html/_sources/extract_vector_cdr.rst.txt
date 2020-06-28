Extracting vector objects from a PDF using CorelDraw
===========================================================

CorelDraw, like Adobe Illustrator, can extract and edit objects directly from PDFs. Even if the document was produced from open source software such as **Inkscape** or a commercial product such as InDesign, CorelDraw can import the PDF and extract vector objects.

.. note::

	Screenshots are from CorelDraw X3. The PDF sample was produced using Adobe InDesign CS4 and Adobe Illustrator CS4.

To import and edit the vector objects from a PDF using CorelDraw:

1. On an empty page, click **File > Import**. Navigate to the PDF file and then click **Import**.

2. On the **Import PDF** window, select **Text** if you intend to reuse text from the PDF or **Curves** if you want to focus on working with vector objects only. Specify the PDF page where the vector object is located if needed.

.. figure:: images/cdr-pdf-vec1.png
    :align: center

3. Position the mouse pointer on the page and press **Enter**. The PDF page will be displayed as an object.

4. Ungroup the PDF object like any CorelDraw object. Using the **Pick Tool**, select and delete any unnecessary objects or remove fills and color if needed.

.. figure:: images/cdr-pdf-vec2.png
    :align: center

.. note::

	 Note that tables and some objects may not retain the vector nodes from the original vector drawing, particularly if the vector object was designed in Illustrator.

.. figure:: images/cdr-pdf-vec3.png
    :align: center
