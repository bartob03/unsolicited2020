Docbook and EPUB
===================

For would-be **Docbook** writers and veteran Docbook users who are interested in using EPUB rather than PDF as their final output, the XSL stylesheets provided by the Docbook team can be `downloaded from Sourceforge <http://docbook.sourceforge.net/>`_ and provide a pretty good output for use with ebook readers. Used in conjunction with **Sigil**, you can easily create exceptional and well-supported EPUBs for a variety of devices.

This brief tutorial reviews the basics of creating an EPUB from Docbook XML using the stylesheets and basic editing via Sigil.

This article discusses the following:

- Docbook Setup
- XSLTPROC
- EPUB Images
- Mimetype
- Compressing and renaming
- Editing in Sigil
- Testing in **Okular, Calibre, EPUBReader** for **Mozilla Firefox**

Docbook Setup
---------------

OpenSUSE and Fedora users may already have the basic packages for working with Docbook including **xsltproc**, **Docbook 5**, and **fo**. Although users can download the latest stylesheets for Docbook through Sourceforge, Linux users can also install the software packages using their software manager.

Before exporting to EPUB, go through the normal steps to validate your Docbook XML file. For this article, the pre-tasks involved the following:

1. Wrote a fictional technical document using **Bluefish Editor**.
2. Validated the document using **xmllint** in **Konsole**.
3. Placed PNG, SVG, and other image files in the same folder as the **Docbook XML** file.

XSLTPROC
-----------

Take note that this example uses **Docbook 5.0** though the steps using earlier versions are the same. In a terminal such as **Yakuake** or **Konsole**, input:

``xsltproc <path and filename of the epub stylesheet> <xml filename>``

With *914b.xml* as the Docbook XML file and the Docbook XML stylesheets stored in the default openSUSE ``/usr`` folder, run the following command in a terminal:

``xsltproc /usr/share/xml/docbook/stylesheet/nwalsh5/1.76.1/epub/docbook.xsl 914b.xml``

The command will produce two folders:

1. ``META-INF``
2. ``OEBPS``

EPUB images
-------------

Move your images into the ``OEBPS`` folder. If you placed the images in a folder, make sure your XML markup accurately points to the correct source folder.

Mimetype
-------------

Although this is an optional step, create a mimetype file using a plain text editor. To create a mimetype for your EPUB file:

1. Launch **KWrite** (or any text editor).
2. Type ``application/epub+zip``.
3. Save the mimetype file in the same parent folder as ``META-INF`` and ``OEBPS`` with the filename *mimetype* (the file extension .txt is unnecessary). This ensures that an operating system/application recognizes the final EPUB as an EPUB or Zip file and will be associated with the correct application or service.

.. figure:: images/epub-docbook1.png
    :align: center

Compressing and renaming
----------------------------

EPUB is nothing more than a zipped file with the file extension changed to EPUB. The XSLT stylesheet creates the ``META-INF`` and ``OEBPS`` folders and the necessary toc, XHTML, and ``content.opf`` files, but it won't compress the files automatically into a zip. However, there are advantages to manually zipping the files, such as making sure all the images are in the ``OEBPS`` folder and adding a mimetype.

To zip the necessary files into an EPUB in KDE:

1. Select the ``META-INF``, ``OEBPS`` folders and the mimetype file. Do not include the original Docbook **.xml** file.
2. Right-click and click **Compress > As ZIP Archive**.
3. To rename the file, right-click, then select **Rename**. Input an ebook name with an **.epub** file extension.

Editing in Sigil
------------------

It's always a good idea to validate and test the EPUB using a variety of devices and another EPUB application. The developers of Sigil knew what they were doing when they wrote the excellent ebook editor, which can examine the contents of an EPUB file and validate the EPUB for compatibility.

Open the newly created EPUB file using Sigil and use the **Book Browser** pane to preview the individual **.xhtml** files stored in the **Text** folder.

If the images aren't displayed when viewed using an EPUB Viewer, check the following:

1. Check if the **Images** folder contains all the necessary images of the document. If they aren't, manually add the images using Sigil.
2. Double-click the XHTML files in the **Text** folder and correct the path of the images if needed.

To check if your EPUB is valid, click **Tools** on the toolbar then **Validate With EPUB FlightCrew**.

.. note::
	   Unlike the EPUB I created using **Calligra** and **LyX**, the EPUB produced from the Docbook XML EPUB stylesheets had only one error regarding the format of the date (the metadata required the ``yyyy-mm-dd`` format).

.. figure:: images/docbook-epub2.png
    :align: center

Testing in Okular and Calibre
-------------------------------------

Open the EPUB file using an ebook reader to check if the images and formatting are consistent. The Docbook XML document converted to EPUB in this example opened properly in Calibre E-Book Viewer and EPUBViewer for Mozilla Firefox, complete with an accurate Table of Comments and proper Docbook formatting. Okular, KDE's document viewer, isn't a dedicated ebook viewer so the application added unnecessary bullet points in the Package Contents section. However, issues didn't appear when viewed in iOS iBooks and using Android apps.
