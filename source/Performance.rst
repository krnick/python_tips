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

2. Use iteritems() to iterate over large dictionary.
=====================================================

* Don't

.. code-block:: python

    d = {i: i * 2 for i in xrange(10000000)}

    # Slow and memory hungry.
    for key, value in d.items():
        print("{0} = {1}".format(key, value))


* Good

.. code-block:: python

    d = {i: i * 2 for i in xrange(10000000)}

    # Memory efficient.
    for key, value in d.iteritems():
        print("{0} = {1}".format(key, value))