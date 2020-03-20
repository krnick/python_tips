=====
Class
=====

Don't access the private attributes from outside.
=================================================

.. code-block:: python

    class A:
        def __init__(self, name):
            self._name = name



    test = A()

    print(test._name)

