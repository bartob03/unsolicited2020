Identifying the PDF producer in Adobe Reader and Okular
===============================================================

There are so many ways to create a PDF today that **Adobe Acrobat** and Adobe products no longer have monopoly over the file format. **XSL-FO, Microsoft Office, Google Chrome**, and most Linux applications are only some of the more popular ways of producing a PDF from a document or project.

If you need to identify what application produced the PDF (for example to check the design or imitate the formatting), you can use the free Adobe Reader to check PDF properties. Adobe Reader has lost some of its gloss over the years due to security problems and lack of features compared to other open source or freeware offerings, but it can still be found installed in most enterprise Windows machines and a dated version is still available for Linux as of this writing (Adobe Reader 9).

To check the PDF producer in **Acrobat Reader**:

1. Open the PDF in Adobe Reader.
2. Click **File > Properties**.
3. On the **Description** tab, the **Application** and **PDF Producer** items indicate which applications/utilities were involved in creating the PDF.

.. image:: images/pdf-properties.png
    :align: center

Unfortunately, complete PDF properties are only available on desktop versions of Adobe Reader and currently can't be viewed from the **iOS** app release.

Linux and **KDE** users can check the PDF producer of a document using the excellent document viewer **Okular**.

To check the PDF producer in **Okular**:

1. Open the PDF in **Okular**.
2. Click **File > Properties**.
3. On the **Properties** tab, the **Creator** and **Producer** items indicate which applications were used to create the PDF.

.. image:: images/pdf-properties2.png
    :align: center

Checking which PDF engine was used to create a PDF is a great way to learn about which industry standard applications are popular with today's software and hardware manufacturers. The *Sony DOStudio* manual documentation, for example, was exported from **MadCap Flare** while AMD's developer guides use an earlier version of **Adobe FrameMaker**. Lenovo, on the other hand, alternately uses **Adobe InDesign CS3** and **XPP XML Publishing** depending on their product line.
