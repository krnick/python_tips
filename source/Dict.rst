=====
Dict
=====


1. Use defaultdict() to initialize dict keys
=============================================

* Dont't

.. code-block:: python

    dt = {}

    if "k" not in dt:
        dt["k"] = 6

    dt["k"] += 1

    print(dt["k"])

* Good

.. code-block:: python

    from collections import defaultdict

    dt = defaultdict(lambda : 6)

    dt["k"] += 1

    print(dt["k"])  # 7