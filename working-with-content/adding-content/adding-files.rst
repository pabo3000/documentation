Adding Files
============

.. include:: ../../_robot.rst

Files of various types can be uploaded to Plone web sites.

Choose file in the *Add new...* menu for a folder to upload a file:

.. replaces ../../_static/copy_of_addnewmenu.png
.. figure:: ../../_robot/adding-files_add-menu.png
   :align: center
   :alt: add-new-menu.png

.. code:: robotframework
   :class: hidden

   *** Test Cases ***

   Show add files menu
       Go to  ${PLONE_URL}

       Click link  css=#plone-contentmenu-factories dt a
       Wait until element is visible
       ...  css=#plone-contentmenu-factories dd.actionMenuContent

       Mouse over  file
       Update element style  portal-footer  display  none

       Capture and crop page screenshot
       ...  ${CURDIR}/../../_robot/adding-files_add-menu.png
       ...  contentActionMenus
       ...  css=#plone-contentmenu-factories dd.actionMenuContent

Select **File** from the drop-down menu, and you'll see the *Add File* panel:

.. figure:: ../../_static/addfile.png
   :align: center
   :alt:

Click the *Browse* button to navigate to the file you want to upload
from your local computer. Provide a title (you can use the same file
name used on your local computer if you want). Provide a *description*
if you want. When you click the save button the file will be uploaded to
the folder.



Example file types include PDF files, Word documents, database files,
zip files... -- well, practically anything. Files on a Plone web site
are treated as just files and will show up in contents lists for
folders, but there won't be any special display of them. They will
appear by name in lists and will be available for download if clicked.

There are specialized add-on tools for Plone web sites that search
the content of files, or can provide a preview of for instance PDF or Office files. If you are interested in this functionality, ask your
Plone web site administrator.

.. robotframework::
   :creates: ../../_robot/adding-files_add-menu.png

