Using the `include` directive to combine separate documents in AsciiDoc
========================================================================

The simplest way to organize multiple **.adoc** files into one document is to use the ``include::`` directive. To ensure that the topic hierarchies are retained when the files are aggregated into one document, add the ``[leveloffset=+1]`` attribute.

The following example of an **index.adoc** puts four files under one document.

.. code-block:: ReStructuredText

    = Main Title
    version: {project-version}
    :icons: font
    :toc: left
    :toclevels: 3
    :toc-title: Table of Contents
    :imagesdir: ./images

    include::home.adoc[leveloffset=+1]
    include::endpoints/documentation.adoc[leveloffset=+1]
    include::best_practices.adoc[leveloffset=+1]
    include::tutorials.adoc[leveloffset=+1]
    include::usecases.adoc[leveloffset=+1]

The ``[leveloffset=+1]`` attribute arranges the four separate **.adoc** files in the project folder as one body under the next title level below the main heading, *Main Title*.
