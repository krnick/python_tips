=====
Class
=====

1. Don't access the private attributes from outside.
====================================================

.. code-block:: python

    class A:
        def __init__(self, name):
            self._name = name

    test = A()

    print(test._name)



2. __init__ do not use return statement.
=========================================

* Don't

.. code-block:: python

    class A():

        def __init__(self, name):

            self.name = name

            return

* Good

.. code-block:: python

    class A():

        def __init__(self, name):

            self.name = name

3. use property instead of setter and getter.


4. Using function instead of method.

When a method is not preceded by the @staticmethod or @classmethod decorators and does not contain any references to the class or instance (via keywords like cls or self)


5. Add the @staticmethod decorator before the static method

6. Add the @classmethod decorator before the class method


3. Do not dynamically creating variable.
=========================================

