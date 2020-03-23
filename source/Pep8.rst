=====
PEP8
=====



1. Python code indented with 4 spaces.
=======================================


2. None Compare.
=================

* Don't

.. code-block:: python

    if some == None:

* Good

.. code-block:: python

    if some is None:


3. boolean Compare.
===================

* Don't

.. code-block:: python

    if some == True:

* Good

.. code-block:: python

    if some:

4. Type comparison.
===================


* Don't

.. code-block:: python

    if type(c) is type type(a):

* Good

.. code-block:: python

    import types

    if isinstance(c, types.ListType)


5. Only use the `is` operator to check the exact identity of two references.
=============================================================================

.. code-block:: python

    if some_list is None:
        do_somthing_with_the_list()

