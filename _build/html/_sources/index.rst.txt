.. doc-chamelon documentation master file, created by
   sphinx-quickstart on Wed Feb 18 12:38:05 2026.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Chamelon's documentation!
========================================

**Chamelon** is an open-source general-purpose delta-debugger for OCaml code. It performs automated testcase reduction: given a program and an error it triggers, Chamelon will output a reduced version of the program triggering the same error.

This documentation explains how to get started with Chamelon. 

Additional resources
--------------------

- The source code of Chamelon is `available on GitHub <https://github.com/Ekdohibs/chamelon.git>`_
- A tool paper on Chamelon is `published at FM24 <https://link.springer.com/chapter/10.1007/978-3-031-71177-0_6>`_. It was awarded the Available, Functional and Reusable badges.
- A docker demonstrating the usage of Chamelon is `available on Zenodo <https://zenodo.org/records/12520654>`_
- A demonstration is also `available on GitHub <https://github.com/Ekdohibs/flambda-backend/tree/chamelon-demo>`_


.. toctree::
   :caption: Getting Started

   pages/installation
   pages/usage


.. toctree::
   :caption: Illustration
   
   pages/illustration


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
