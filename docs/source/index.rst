.. sphinx-pyscript-demo documentation master file, created by
   sphinx-quickstart on Fri Dec  1 16:09:44 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Sphinx Site with PyScript
================================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

.. py-config::

    splashscreen:
        autoclose: true

This page demos how PyScript can be used to make online documentation interactive inside of Sphinx. It is one of the demos created for the conference talk 'Making Your Documentation Interactive with PyScript' by Jeff Glass. See [more details on that talk](https://github.com/JeffersGlass/pyscript-docs-demo-S3) or [the code for this site](https://github.com/JeffersGlass/mkdocs-pyscript-demo) on GitHub.

The Datetime Module
###################

The :code:`datetime` module can be used to reference specific times, timespans, epochs, and calendar days.
Let's explore the relationship between the :code:`datetime` and :code:`timedelta` classes. If we create a new datetime:

.. py-repl::
   :output: replOutput1

   from datetime import datetime
   d_1 = datetime(2023, 12, 1, 14, 30, 00)
   print(d_1)

.. raw:: html

    <div id="replOutput1"></div>

.. py-terminal::

We can add a :code:`timedelta` object to it to create another :code:`datetime` object:

.. py-repl::
   :output: replOutput2

   from datetime import datetime, timedelta
   d_1 = datetime(2023, 12, 1, 14, 30, 00)
   delta = timedelta(days=90, hours=16, minutes=35)
   d_2 = d_1 + delta
   print(delta)
   print(d_2)

.. raw:: html

    <div id="replOutput2"></div>

.. py-terminal::

Or we can subtract one :code:`datetime` from another to create a :code:`timedelta`:

.. py-repl::
   :output: replOutput3

   from datetime import datetime
   d_3 = datetime(2023, 12, 14, 16, 30)
   d_4 = datetime(2024, 5, 13, 11, 15)
   print(d_3 - d_4)

.. raw:: html

    <div id="replOutput3"></div>

.. py-terminal::