====
List
====

1. unpack the variable in list using explicit unpacking
========================================================

* Don't

.. code-block:: python

    number_list = [1,2,3]

    hello = number_list[0]
    world = number_list[1]
    hey = number_list[2]

* Good

.. code-block:: python

    number_list = [1,2,3]

    hello, world, hey = number_list