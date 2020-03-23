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

2. Secure your exception
========================


* Good

.. code-block:: python

    def divide(a, b):

        result = None

        try:
            result = a / b
        except ZeroDivisionError:
            print("Type error: division by 0.")
        except TypeError:
            # E.g., if b is a string
            print("Type error: division by '{0}'.".format(b))
        except Exception as e:
            # handle any other exception
            print("Error '{0}' occured. Arguments {1}.".format(e.message, e.args))
        else:
            # Excecutes if no exception occured
            print("No errors")
        finally:
            # Executes always
            if result is None:
                result = 0

        return result
