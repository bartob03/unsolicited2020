Writing and publishing documentation using Sphinx, ReStructuredText , and ReadTheDocs
=======================================================================================

Overview
------------

*ReStructuredText* (RST) is a lightweight markup language similar to **Markdown** and is ideal for writing technical documentation. *Sphinx* is a publishing engine that uses RST files for creating static websites for documentation. `ReadTheDocs.org <https://www.readthedocs.org>`_ is an online service that hosts documentation, and can build and publish directly from **GitHub** and **BitBucket**.

Running basic Sphinx commands
-------------------------------

Sphinx uses .rst files for publishing documentation and can be installed on Windows, Linux, and macOS via a software package or pip.

.. note::

  The steps in this article were tested on an `Ubuntu <https://www.ubuntu.com>`_ machine.

The basic operations are described as follows.

::

  $ pip install Sphinx
  # Installs Sphinx.

  $ sphinx-quickstart
  # Run the quickstart script within a docs folder in a project folder. The quickstart option creates default files and folders such as index.rst and conf.py within the docs folder. The options can be later changed by editing the conf.py file.

  $ make html
  # The make html command generates HTML files in the build folder.


For additional details, refer to the official `Sphinx Documentation <https://www.sphinx-doc.org/en/1.7/contents.html>`_

Understanding the ``sphinx-quickstart`` command
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The ``sphinx-quickstart`` command is executed within the ``docs`` folder prior to creating **RST** files.

Although the default options are acceptable, take note of the following options:

- ``Separate source and build directories`` - Separating the source and build directories helps identify which files for uploading for web hosting.
- ``Project name`` - The project name appears in several places in the output document so ensure that this is the correct project name.
- ``Author name(s)`` - The script will not run unless text is entered for this option.
- ``Name of your master document`` - The master document is the main page for the output and is named **index.rst** by default.
- ``githubpages`` - This option creats a **.nojekyll** file used for preventing **Jekyll** options if the final output will be hosted in GitHub pages.
- ``Create makefile`` - This option makes it easy to run the make html script in Windows.

Publishing to PDF
~~~~~~~~~~~~~~~~~~

The output can be published to PDF using the command make **latexpdf**.

.. note::

	Additional **LaTeX** software dependencies are required depending on the operating system. For additional details, refer to `Sphinx LaTeXBuilder <https://www.sphinx-doc.org/en/1.7/builders.html#sphinx.builders.latex.LaTeXBuilder>`_.

Writing using ReStructuredText markup
----------------------------------------

ReStructuredText markup differs from Markdown and includes many directives for organizing and referencing documents. RST uses *docutils*, but additional directives can be used when publishing via Sphinx.

Example of a RST directive: ``contents``
::

  ..contents:: Table of Contents

The contents directive creates a toc based on the headings found on the page and rendered in HTML.

Example of Sphinx directive: ``seealso``

::

  .. seealso::

  Sphinx main site
    http://www.sphinx-doc.org

  Sphinx ReStructuredText Docutils Directives
    http://docutils.sourceforge.net/docs/ref/rst/directives.html

.. note:: - For a list of directives supported by docutils, refer to `reStructuredText Directives <http://docutils.sourceforge.net/docs/ref/rst/directives.html>`_.

   - For a list of directives supported by `Directives <http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html>`_.

Working with tables
~~~~~~~~~~~~~~~~~~~~~

Creating tables manually in ReStructuredText is not always ideal. One solution is to use the ``csv-table`` directive, which renders **.csv** files into tables in the document.

::

  .. csv-table:: Table Title
   :file: <CSV file path and name>
   :widths: 10, 15, 15, 30, 30
   :header-rows: 1

  # The widths option is used to define the width of the column.

An alternative is to use the ``list-table`` directive, which makes writing the contents of the table fairly straightforward.

::

  .. list-table:: Title
   :widths: 25 25 50
   :header-rows: 1

   * - Heading row 1, column 1
     - Heading row 1, column 2
     - Heading row 1, column 3
   * - Row 1, column 1
     -
     - Row 1, column 3
   * - Row 2, column 1
     - Row 2, column 2
     - Row 2, column 3

Note that each cell can contain structured markup, such as markup that indicates literal text.

Editors and Tools for RST
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Users don't need to use a dedicated tool for writing RST. However, the following editors include writing aides for previewing and writing RST:

- **Visual Studio Code**
- **ReText** (Linux) - ReText supports previewing RST using the python-docutils packages.
- **Notepad ++**
- **Atom** (macOS, Windows, Linux) - Atom packages are available for ``ReStructuredText Preview Pandoc``, ``linter-spell-rst``, ``linter-rst``, ``rst-snippets`` and ``language-restructuredtext``.


Publishing the Sphinx project to ReadtheDocs
--------------------------------------------------

`Readthedocs.org <http://www.readthedocs.org>`_ supports Sphinx builds via GitHub.

To publish a Sphinx project hosted on GitHub to Readthedocs.org:

- Log into or sign up for Read the Docs
- Click **My Projects > Import a Project**.
- Enter the GitHub project details (``git@github.com/git-username/project-name.git``), and then click **Create**.
- Click the project name once added, and then click **Build version**.
- Click **View your documentation** or **View Docs** once the build is complete.

Applying the ReadtheDocs default theme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The ``html_theme`` specified in the **conf.py** file determines which theme Sphinx uses when building the documentation. To use the **Readthedocs** theme, change the value of ``html_theme`` to ``default``.

If the output won't be hosted on ReadtheDocs.org, or the user prefers to review the build locally with the Readthedocs theme applied, the theme can be installed via ``pip`` and applied to the HTML build.

To install and apply the **Readthedocs** theme to the HTML build:

- Install the theme using ``pip install sphinx_rtd_theme``
- Change the ``html_theme`` value in the **conf.py** file to ``sphinx_rtd_theme``.

Adding custom CSS to the theme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Custom themes in the ``_static`` folder override applied themes.

To add custom CSS, perform the following steps:

1. Ensure that the ``html_static_path = ['_static']`` line in the **conf.py** file is uncommented.

2. Specify the path of the **.css** file relative to the ``_static`` folder.

::

    ``html_css_files = [
        'bstyle.css',
    ]``

The same process can be applied for adding **Javascript** files (``html_js_files``).

.. note::

	Create a ``_static`` folder under the ``source`` folder if it does not exist.

Editing the Table of Contents tree
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The toctree directive is used to structure the table of contents on the left panel of the page.

The default index.html file, which serves as the landing page, doesn't appear on the TOC tree unless additional sections/headings are present on the index.html file. Files specified in the toctree directive adds items to the output navigation tree in addition to the sections included on the landing page. External links can be added using the label name <``URL``> as shown in the following example.

::

  .. toctree::
     :caption: Site Map
     :maxdepth: 2

     glossary
     reference
     Swagger <https://github.com/bartob03/docs-only>

.. note::

	If the writer prefers to only have a main TOC tree in the landing page and have a different page for the start of the documentation, specify a different filename for the *Name* of your master document when running ``sphinx-quickstart``. For example, specify *main.rst* as the master document then add a separate item for index in the ``toctree`` directive.
