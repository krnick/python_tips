===============
Exception
===============


1. subclass of Exception need to place before parent Exception class
=====================================================================


* Don't

.. code-block:: python
    try:
        5/0
    except Exception as e:
        print(e)
    except ZeroDivisionError as e:
        print(e)

* Good

.. code-block:: python
    try:
        5/0
    except ZeroDivisionError as e:
        print(e)
    except Exception as e:
        print(e)
