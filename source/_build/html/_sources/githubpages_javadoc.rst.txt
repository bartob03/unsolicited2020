Using GitHub Pages for Javadoc files
========================================

**GitHub Pages** can be used for hosting **Javadoc** files. No additional steps are required to set up the repository to publish the HTML files.

To set up **GitHub Pages** to display **Javadoc** files:

1. After creating the repository and creating a temporary **.md** file, click **Settings > Options**.

2. On the **GitHub Pages** section, select **master branch** under **Source**. **GitHub** sets up the site and displays the URL of the site.

   .. note::

   	 Do not select a theme to ensure that no changes are made to the **HTML** files.

3. Commit the **Javadoc HTML** files to the repository.

.. note::
   Take note of the following when using **GitHub Pages**:

   - **GitHub Pages** are public by default, so ensure that the **Javadocs** to be published are for public viewing.

   - **GitHub Pages** uses the **index.html** file in the *Master branch* in the output HTML as the main page of the site. To change the path to ``/docs``, click **Settings > GitHub Pages > Source**.

   - The **GitHub Pages** URL for the published **Javadoc** can be found under the repository settings (**Settings > GitHub Pages**).
