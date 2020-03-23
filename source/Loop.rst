=====
Loop
=====


1. `else` clause of the loop
=============================

if for loop does not interrupted by a `break` or `return`,
the `else` clause of the loop will be executed.


2. Use enumerate instead of len to access each element.
========================================================

.. code-block:: python

    for index, element in enumerate(some_list):
        print(index, element)