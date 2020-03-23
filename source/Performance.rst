===========
Performance
===========

1. Don't check if key in list.
==============================


* Don't

.. code-block:: python


    l = [1, 2, 3, 4]

    # iterates over three elements in the list
    if 3 in l:
        print("The number 3 is in the list.")
    else:
        print("The number 3 is NOT in the list.")

* Good

use a set or dictionary

.. code-block:: python


    s = set([1, 2, 3, 4])

    if 3 in s:
        print("The number 3 is in the list.")
    else:
        print("The number 3 is NOT in the list.")