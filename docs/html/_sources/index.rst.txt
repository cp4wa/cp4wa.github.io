.. cp4wa tutorials documentation master file, created by
   sphinx-quickstart on Tue Jun  7 20:14:17 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Cloud Pak for Watson AIOps Tutorials
###############################################


Introduction
************

This project aims to document knowledge that could be useful for beginners into IBM Cloud Pak for Watson AIOps.

The documentation is created using reStructuredText and the html is generated using Sphinx in folder **docs**.

The web documentation is hosted using GitHub Pages.

To generate the static web pages, the following command will generate the html pags in folder **docs**, this target directory is configured in **source/Makefile**.

.. code-block:: bash

   cd source 
   make html


The generated index.html is in folder **docs/html** but github pages expect an *index.html* in **docs** root folder, an *index.html* is created to redirect it to **./html/index.html**

GitHub Pages uses Jekyll by default, to ensure the theme of Sphinx is rendered properly you need to add a ```.nojekyll``` in docs folder.

this project source can be found at `github <https://github.com/cp4wa/cp4wa.github.io>`_ and the generated `site <https://cp4wa.github.io>`_.

Resources
*********
 
- Sphinx

  - `Sphinux Documentation <https://www.sphinx-doc.org/en/master/contents.html>`_
  - `Sphinx lesson <https://coderefinery.github.io/sphinx-lesson/>`_
  - How to host `Sphinix <https://python.plainenglish.io/how-to-host-your-sphinx-documentation-on-github-550254f325ae>`_ documentation on GitHub Pages
- reStructuredTes

  - `Introduction to reStructuredText <https://www.writethedocs.org/guide/writing/reStructuredText/>`_
  - `reStructuredText Primer (Basic) <https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_
  - `A ReStructuredText Primer <https://docutils.sourceforge.io/docs/user/rst/quickstart.html>`_
  - `reStructuredText <https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html>`_
  - `Cheatsheet <https://raw.githubusercontent.com/ralsina/rst-cheatsheet/master/rst-cheatsheet.pdf>`_
- GitHub

  - `GitHub Pages <https://pages.github.com/>`_
  - `GitHub Actions <https://docs.github.com/en/actions>`_
  - `SSH for GitHub <https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh>`_
  - `Git <https://git-scm.com/about>`_
  
.. toctree::
   :maxdepth: 4
   :caption: Table of Contents
   :numbered:

   openshift
   splunk
   cp4wa
   ieam
   references


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
