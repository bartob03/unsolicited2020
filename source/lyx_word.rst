LyX and Microsoft Word 2007/2010
===================================

Users who are introduced to **LyX** may balk at the lack of support for the ubiquitous **Microsoft Word**. LyX is dependable with exporting to LaTeX, DVI, and PDF, but does not directly export to common file formats such as .rtf and .doc, which can be somewhat disconcerting for those who may want to use their well-written LyX documents in Microsoft Office.

For very simple documents that are focused mainly on structured writing with minimal links and images, writers can export their documents to Plain Text.

To export a LyX document to Plain Text:

1. Click **File > Export**.
2. Click **Plain text**.

A .txt file will be saved in the same folder as the source LyX file. The .txt file will retain unformatted headings and sections but not images. The disadvantage of exporting to plain text becomes apparent with links and bibliographies. Bibtex keys appear as placeholders but the Bibtex bibliography will not be retained.

A somewhat more laborious workaround is to export the LyX file to PDF and convert the PDF to Word or .odt using various applications or by manually copying and pasting the content to a new Word document. A more effective solution is to export the LyX document to LyXHTML, which can then be opened in Microsoft Word for editing.

To exporting a LyX document to LyXHTML for Microsoft Word:

1. Place the BibTeX file (if one was used for the document) and the LyX document in the same folder.
2. With the LyX document open, click **File > Export**.
3. Click **LyXHTML**. LyX will extract the image files included on the document and then create an XHTML file on the same folder.

Preparing Microsoft Word for LyXHTML
---------------------------------------

Before importing the XHTML exported from LyX, you will have to enable file format confirmation in Word.

To enable file format conversion in **Microsoft Word 2007**:

1. Click the Microsoft Word Orb.
2. Click **Word Options > Advanced**.
3. On the **General** section, select **Confirm file format conversion on open**.
4. Click **Apply > OK**.

To enable file format file conversion in **Microsoft Word 2010**:

1. Click **File > Options > Advanced**.
2. On the **General** section, select **Confirm file format conversion on open**.
3. Click **OK**.

To open LyXHTML in **Microsoft Word 2007/2010**:

1. Click **File > Open**. If the XHTML file from LyX isn't displayed, click the filter list and select **All Files**.
2. In the **Convert File** window, select **HTML Document**.
3. Click **OK**.

Since the document imported is XHTML, text and images are best viewed using the **Web Layout** option in the **View** ribbon.

Once the LyXHTML is imported to Word, the Word document retains the hyperlinks, citation numbers and bibliography text. You will, however, have to create a **Bookmark** in Word using the **Insert Ribbon** and manually edit the hyperlink of the citation numbers to link to the bibliography section.

.. note::

	When opening LyXTML in Microsoft Word 2007/2010, do not select **XML document** in the options listed in the **Convert File** window or Word will report an error.
