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



4. Return more than one result using nameturple.
=================================================


.. code-block:: python

    from collections import namedtuple

    def fun():
        name = namedtuple("name", ["first", "middle", "last"])
        return name("nick", "sung", "hello")

    test_name = fun()

    print(test_name.first, test_name.middle, test_name.last)