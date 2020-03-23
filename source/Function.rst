========
Function
========

1. Do not use mutable objects as an argument
=================================================

* Don't
.. code-block:: python

    def some(hello, value=[]):

        value.append(3)


* Good

.. code-block:: python

    def some(hello, value=None):

        if value is None:
            value = []

        value.append(3)

2. Do not return more than one variable type from function call.
================================================================


3. Do not use `global` statement.
=================================

