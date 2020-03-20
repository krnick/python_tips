======
Lambda
======

1. Don't use lambda with anonymously


* Dont'

.. code-block:: python

    f = lambda x: 2 * x

* Good

.. code-block:: python

    def fun(x): return 2 * x
