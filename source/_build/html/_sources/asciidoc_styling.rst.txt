Styling AsciiDoctor HTML output
================================

By default, HTML generated using Asciidoctor uses a set of predefined stylesheets.

The simplest way to modify the HTML output appearance of the documentation is by creating a **docinfo** file that has formatting content within a style ``<tag>`` or a link to a **.css** stylesheet.

.. note::
    For additional details regarding creating a docinfo file, refer to `Asciidoctor Docinfo Files <https://asciidoctor.org/docs/user-manual/#docinfo-file>`_.

Creating a docinfo file for styling HTML output
-------------------------------------------------

A **docinfo** file adds content header or footer content as needed.

To create and apply a docinfo file to a set of **.adoc** files for HTML output:

1. Create a **docinfo.html** file in the same folder as the **.adoc** files.

2. Add the ``docinfo`` attribute to the **index.adoc** file. For this example, the ``docinfo`` attribute has the value of ``shared``, which indicates that the ``docinfo`` applies to all files in the same folder.

.. code-block:: AsciiDoc

    = Index title
      :toc: left
      :toclevels: 5
      :toc-title: Contents
      :docinfo: Shared

3. To apply formatting using an external **.css** stylesheet, add a link tag pointing to the stylesheet on the **docinfo.html** file.

.. code-block:: html

    <meta name="description" content="External documentation header by CMR">
     <link rel="stylesheet" href="formatting_stylesheet_name.css">

4. To apply formatting using the ``<style>`` tag, add the style element in the **docinfo** file.

.. code-block:: HTML

    <meta name="description" content="External documentation header by CMR">

    <!-- Adjusting max-width expands the content area of the default stylesheet of Asciidoctor. The TomTom brand color #df1b12 is also applied to the Headings in this stle. -->

    <style>
      #header, #content, #footnotes, #footer {
      max-width: 67em;
      }

    h1, h2, h3, h4, h5 {
      color: #df1b12;
      }
    </style>

Adding style-related attributes to an .adoc file
--------------------------------------------------

The following attributes can be added to the .adoc file:

- ``:stylesdir:`` - Specifies the stylesheet directory when applying stylesheets via the command line.
- ``:linkcss:`` - Prevents any styles from being embedded in the HTML output.

Reviewing output using a specific stylesheet
---------------------------------------------

Run the following command to generate HTML output that uses a specific stylesheet.

``$ asciidoctor -a stylesheet=<name_of_stylesheet> <.adoc file>``

The following example applies the **readthedocs.css** stylesheet to **index.adoc**.

``$ asciidoctor -a stylesheet=readthedocs.css index.adoc``

Using prebuilt stylesheets for Asciidoctor
---------------------------------------------

Several stylesheets are available for producing formatted HTML using Asciidoctor. These **.css** files can be modified and referenced as needed.

For additional details, refer to `Stylesheet Factory <https://asciidoctor.org/docs/user-manual/#stylesheet-factory>`_.
