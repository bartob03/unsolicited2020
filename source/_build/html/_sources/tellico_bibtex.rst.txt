Using Tellico citations/Bibtex in LyX
===========================================

KDE's database manager **Tellico** and document processor **LyX** can be used together to write long documents with numerous citations and a bibliography. Any book database created in Tellico can be converted to a **Bibtex** file and then inserted into a LyX document.

.. note::

	This article uses LyX 2.0.3 and Tellico 2.3.5 installed on openSUSE 12.2 KDE.


To use a Tellico book collection for inserting citations in a LyX document, the Tellico file needs to be exported as a Bibtex file. A book collection created in Tellico, however, cannot be exported to Bibtex immediately and must be converted to a Bibliography first.

To convert a book collection to a bibliography in Tellico:

1. With the book collection file open, click **Collection > Bibliography**.
2. Click **Convert to Bibliography**.
3. Save the file using a different name to avoid losing the original book collection.

Before using a book collection as a source for citations for a thesis, proposal, or literary work, check that the necessary fields are completed for every entry.

If needed, customize the Bibtex key for each entry. The Bibtex key is used to insert citations in a document. The system will actually generate a Bibtex key for each book automatically but some writers prefer to customize the key for easy reading.

The Bibtex key item is not found in the **Entry Editor** window when working with a standard book collection so if the Tellico book collection was converted to a bibliography, the Bibtex key field is empty and a key is automatically created once the Tellico file is exported as a Bibtex file.

To edit book entries in Tellico and customize a Bibtex key:

1. Click **Settings > Show Entry View**. Entry details will be displayed for each book entry on the main window.
2. To edit a book entry, double-click an item from the left pane.
3. On the **General** tab, enter a Bibtex Key.

.. figure:: images/tellico-lyx41.png
    :align: center

4. Click **Save Entry**. Any edited information will now be updated for that book.

The book collection/bibliography can now be exported to the Bibtex file format for use in LyX or any other Bibtex supported application.

To export to Bibtex in Tellico:

1. Click **File > Export**.
2. Click **Export to Bibtex**.
3. On the **Export Options** window, make any necessary changes and click **OK**.
4. Enter a filename and then click **Save**.

Working with Bibliography in LyX
-------------------------------------

Using the Bibtex file exported from Tellico, a bibliography can now be added to a LyX document.

To add a bibliography list to a LyX document:

1. Position the insertion point in the section where the bibliography will be added.
2. Click **Insert > List/TOC**.
2. Click **BibTeX Bibliography.**
3. In the **LyX: BibTeX Bibliography** window, click **Add.**
4. In the **LyX: Add Bibliography** window, click **Browse.**

.. figure:: images/tellico-lyx2.png
    :align: center

5. Navigate to the Bibtex file exported from Tellico, and then click **Open**.
6. Click **Add**. The Bibtex file will be displayed on the list of Databases.
7. Click **OK**.

The text *BibTeX Generated Bibliography* will be displayed as placeholder. If no citations have been added using the Bibtex file, previewing the PDF will display an empty area where the bibliography should be.

Working with Citations in LyX
----------------------------------

With the bibliography inserted into the document, citations can now be added using two ways.

To add citations from within LyX:

1. Place the insertion point to where the citation should be marked.
2. Click **Insert > Citation**.
3. Use the **Search** field to look for a specific book or manually select a Bibtex key on the left pane. Click **Add**.

.. figure:: images/tellico-lyx3.png
    :align: center

4. Click **OK**. The Bibtex key will be displayed as placeholder for the citation.

If Tellico and LyX is set up properly on the system, citations can be inserted directly from Tellico, which is especially useful if the Bibtex keys are vague, the book doesn't come up in the search results, or the writer is unsure of which book is referenced.

To insert a citation from Tellico:

1. Place the insertion point to where the citation should be marked in the LyX document.
2. Open the Tellico file and select the book entry from the left pane.
3. Click **Collection > Bibliography**.
3. Click **Cite Entry** in LyX.

.. figure:: images/tellico-lyx4.png
    :align: center

Before previewing the PDF version of the LyX document, save the LyX document first or the citations and bibliography list will not be displayed.
