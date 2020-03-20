========
Function
========

1. Do not use mutable objects as an argument


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
