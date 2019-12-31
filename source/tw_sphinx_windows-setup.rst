Setting Up a Sphinx Publishing Environment on Windows 10
===========================================================



Install Sphinx

1. Install Python.

This article uses Python 3.8.1.

Tip:  Add Python 3.8 to PATH to simplify Python setup.

2. pip install -U sphinx

3. sphinx-build --version

.. seealso::

  Sphinx main site
    http://www.sphinx-doc.org

  Writing and publishing documentation using Sphinx, ReStructuredText , and ReadTheDocs
    :doc:`writingpublishingsphinx`

Install Git

https://git-scm.com/downloads

Tip GitHub Desktop for Windows and MacOS simplifies the workflow if your tasks are relatively straightforward, you're working with more than one machine, and little collaboration is required for writing your Sphinx project.

Install Atom text editor (Optional)

Any text editor can be used to create .rst files for Sphinx documentation projects. The free, open-source Atom, however, has community packages for supporting RST previews and snippets.

https://atom.io/

Install RST packages for Atom

Click Settings > Install.

Search and install the following packages.

language-restructuredtext

.. note::

	If RST snippets don't display, restart Atom.

There are other packages available for previewing .rst files. The package rst-preview-pandoc requires a separate installation of Pandoc, an open source software utility for converting text file formats such as Markdown and RST to PDF.

https://pandoc.org/installing.html

rst-preview-pandoc

To display the RST preview, click Packages > reStructuredText Preview Pandoc > Toggle Preview
